# PROJECT ZANE: Technical Specification & Micro-Architecture
> **Role:** You are the Lead Architect for "Zane," a self-extending Exocortex.
> **Philosophy:** "The File System is the Database."
> **Constraint:** The system must be STATELESS. All state persists to disk (JSON/MD) immediately.

---
## 1. Project Context (The "Why")

We are building a local, voice-enabled AI assistant that runs on a Raspberry Pi/Laptop via Tailscale.* **Core Identity:** Zane is stoic, factual, and transparent. He shows his work ("Thought Process").* **Key Mechanic:** **Dual-Write Memory.** We write `thread.json` for machine context and `thread.md` for human readability. Never parse Markdown to load context.* **Key Mechanic:** **Meta-Capabilities.** Zane can write his own Python skills. This process is safeguarded by Git Snapshots (Auto-rollback on failure).

  

---

## 2. The Directory Scaffold (Strict Constraint)

You must create exactly this structure.```text

/exocortex
├── .env # API Keys (OPENAI_API_KEY, ANTHROPIC_API_KEY)
├── .gitignore # Ignore .system/, __pycache__, .env
├── requirements.txt # fastapi, uvicorn, pydantic, anthropic, chromadb, gitpython
├── main.py # Entry point (FastAPI)
│
├── config/
│ ├── settings.yaml # Static config (paths, model names)
│ └── prompts/
│ ├── system_core.md # The "Stoic" Persona
│ └── architect.md # Instructions for writing code
│
├── core/ # THE BRAIN (Stateless Logic)
│ ├── llm/
│ │ ├── factory.py # BaseLLM class (Provider agnostic)
│ │ └── providers.py # Claude implementation
│ │
│ ├── routing/
│ │ ├── detector.py # Logic: Chat vs. Skill vs. Dev
│ │ └── intent.py # Pydantic models for routing
│ │
│ ├── memory/
│ │ ├── conversation.py # Dual-write logic (JSON + MD)
│ │ ├── indexer.py # ChromaDB / SQLite sync logic
│ │ └── vector_store.py # Wrapper for ChromaDB
│ │
│ └── skills/
│ ├── registry.py # Loads skill.json files
│ └── executor.py # Safe execution of tools
│
├── memory/ # THE DATA (User Facing)
│ ├── inbox/ # Raw notes/transcripts
│ ├── knowledge_base/ # Long-term storage
│ │ ├── projects/ # Active project folders
│ │ └── entities/ # People/Concepts Markdown
│ └── conversations/ # Chat history
│ └── 2024-05/ # Partitioned by month
│ ├── thread_1.json # Source of Truth
│ └── thread_1.md # Read-only mirror
│
├── skills/ # THE TOOLS (User/AI Generated)
│ ├── core_ops/ # Built-in (Time, FileIO, Git)
│ └── [user_skill]/ # e.g., gym_tracker
│ ├── skill.json # Manifest
│ └── [code].py # Implementation
│
└── .system/ # MACHINE INDICES (Disposable)
├── chroma_db/ # Vector embeddings
└── logs/ # System logs

3. Data Contracts (Pydantic Schemas)

The system relies on these exact schemas to function.

3.1 The Router Intent

Used by core/routing/detector.py to decide the next step.

Python

  

from pydantic import BaseModel, Fieldfrom typing import Literal, Optionalclass Intent(BaseModel):

mode: Literal["CHAT", "SKILL", "DEV"] = Field(..., description="The operating mode")

confidence: float = Field(..., description="0.0 to 1.0 confidence score")

skill_name: Optional[str] = Field(None, description="Target skill if mode is SKILL")

project_context: Optional[str] = Field(None, description="Active project name if relevant")

3.2 The Skill Manifest (skill.json)

Used by core/skills/registry.py to load capabilities.

JSON

  

{

"id": "gym_tracker_v1",

"name": "Gym Tracker",

"description": "Logs workout sets and queries PRs.",

"triggers": ["log workout", "check pr", "gym stats"],

"entry_point": "tracker.py",

"class_name": "GymTracker",

"enabled": true

}

3.3 The API Response ("Glass Box" UI)

Used by main.py to return data to the client.

Python

  

class LogEvent(BaseModel):

type: Literal["thought", "tool", "file_io", "error"]

message: str

metadata: Optional[dict] = Noneclass ZaneResponse(BaseModel):

text: str

audio_base64: Optional[str] = None

logs: list[LogEvent] # The "Transparency" layer

4. Implementation Micro-Tasks

Execute these phases in order. Do not skip verification steps.

Phase 1: The Skeleton & Persona

Goal: A running server that accepts text and replies as "Zane" (Stoic).

Setup: Create the file tree. Initialize main.py with FastAPI.

LLM Factory: Implement core/llm/factory.py (Abstract Base Class) and providers.py (Claude 3.5 Sonnet adapter).

Persona: Create config/prompts/system_core.md.
Constraint: Must prioritize facts over empathy.
Endpoint: Create POST /chat.
Logic: Receive text -> Call LLM -> Return ZaneResponse.
Verify: curl the endpoint. Ensure the response is stoic.
Phase 2: Dual-Write Memory
Goal: Persistence. Survives server restart.
JSON Store: Implement core/memory/conversation.py.
Task: save_message(thread_id, role, content) -> Appends to thread.json.
Markdown Mirror: Extend save_message to append formatted text to thread.md.
Constraint: Never read from .md. Only write to it.
Context Loading: Implement load_context(thread_id).
Logic: Read JSON -> Return list of dicts for LLM context window.
Phase 3: The "Glass Box" Router
Goal: Transparency and Tool use.
Router: Implement core/routing/detector.py.
Logic: First LLM pass to classify Intent.
UI Logs: Update ZaneResponse.
Constraint: Every time the Router makes a decision, append a LogEvent (e.g., {"type": "thought", "message": "Detected Intent: SKILL (Gym Tracker)"}).
Tool Execution: Implement core/skills/executor.py.
Logic: Dynamic import of Python modules based on skill.json.
Phase 4: Self-Extension (The Architect)
Goal: Zane writes code.
Git Ops: Implement skills/core_ops/git_tools.py (Wrapper for gitpython).
Functions: snapshot(), rollback(), commit().
Architect Prompt: Create config/prompts/architect.md.
Directive: "You are a Senior Python Engineer. Write robust, error-handled code."
The Meta-Loop:
User: "Build a skill..."
Zane: git snapshot -> Write Code -> pytest -> Success? git commit : git rollback.
5. Critical Rules
No Databases in Phase 1: Use JSON files for everything initially. Add ChromaDB in Phase 5.
Secrets: Never hardcode keys. Use .env.
Error Handling: If a tool fails, Zane must report it in the logs array, not crash the server.