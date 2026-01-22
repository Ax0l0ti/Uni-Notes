# Computational Complexity Cheat Sheet
---
> [!info]+ Module Details
> Includes information about (genus:: Cheat Sheet) from [Year::3]. Links to Module Note and its correspondent attribute tag 
> *Module Tag :* [[Yr3 Notes📕/Semester 1/Complexity/Complexity|Complexity]]
> *Link :* [[Yr2 Notes📘/Semester 1 & 2/Algo & Complexity/Complexity]]
> *Cheat Sheet tag :* [[Grail 🩷]]
> 

> [!abstract]+ Contents
> 
> > [[#🕰️ Speed run]]  
> > [[#Exam breakdown]]
> > [[#🧠 Definitions by Topic]]

---
> [!danger]+ _🕰️ Speed run_
> 
> - **P vs NP**: Definitions and importance
> - **Complexity Classes**: P, NP, NP-complete, NP-hard
> - **Reductions**: Polynomial-time reductions
> - **Big O**: Time and space analysis basics

---
# Exam breakdown

> [!danger]- Exam
> After Christmas Holiday, Sem 1 worth 5 Creds
Exam details when given
> 
> > [!heart]+ Structure Overview
> > 3 Q of subparts made of bookwork and thinking 
> > contain brief amount of bookwork - innovative parts of calculation will be similar to Problem sheet. 
> > Could imagine do definiitions of deutcha, then non-bookwork part
> > Might get asked to adapt, extend or apply in a different scenario
> > 3007 was last version - pretty good structural similarity
> 
> > [!omega]+ KEY NOTE
> > Focus on clear definitions and correct notation

---
# 🧠 Definitions by Topic

> [!note]- P vs NP
> - **Decision problem**: a computational problem that can be answered either "**Yes**" or "**No**"
> - **P**: Problems solvable in polynomial time with a DTM
> - **NP**: Problems verifiable in polynomial time
> - **Co-NP**:  A problem $X$ is Co-NP $\iff$ (if and only if) its complement $\bar X$ is in the class $NP$ problem. Meaning, we can confirm a given "**No**" answer from the NP in Polynomial time 
> - **NP-Completeness**: 
> - **NP-Hardness**: 

> [!example]+  Examples of Problems
> > **Traveling Salesman** - route of weight $\leq$ K that visits all vertices and returns to the start?
> > [Travelling salesman problem - Wikipedia](https://en.wikipedia.org/wiki/Travelling_salesman_problem)
> > **Satisfiability Problem (SAT)** - Can a given boolean expression evaluate to true
> > [Boolean satisfiability problem - Wikipedia](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem)
> > **Subgraph isomorphism** - Given graphs $H$ and $G$, can you prove one is a subgraph of the other?
> > [Subgraph isomorphism problem - Wikipedia](https://en.wikipedia.org/wiki/Subgraph_isomorphism_problem)
> > **Clique Problem** - clique (all interconnected) is NP-complete. Takes  $O(n^kk^2)$ for $k$-$vertex$
> > [Clique problem - Wikipedia](https://en.wikipedia.org/wiki/Clique_problem)
> > **Independent Set Problem** - (is complement of clique) set of vertices where no 2 adjacent
> > [Independent set (graph theory) - Wikipedia](https://en.wikipedia.org/wiki/Independent_set_\(graph_theory\)) also called Anti-Clique
> 

> [!example]+ Quantum
> > [!omega]- Deutsch and Deutsch-Josza 
> > Balanced or Constant. Deutsch for single cubit ( w check qubit). Deutsch-Josza for multi-cubit  $N+1$ ( w check qubit)
> 
> > [!heart]-  Shor, Grover
> > Grover is a Q Algo for solving unstructured search. Provides Quadratic Speed up ($N$ to $\sqrt{N}$). Starts superposition of all states, (achieved by Hadamard trans for each qubit). Oracle func marks state containing item via flipping amplitudes. Grover Diffusion Operator amplifies marked state & reduces amps of others. Repeat flip and amp roughly $\frac{\pi}{4}O(\sqrt{N})$ times. Measure probability
> > 
> 
> > [!danger]- Quantum Key Distribution
> >  Since we are relying on quantum mechanics, A and B must actually be able to share quanta. So if A and B are using a fibre optic cable to communicate the quanta, that cable must directly connect A and B, with no repeaters etc. in the way. 
> >  All known schemes rely on A and B sharing an authenticated classical communications channel. Hence authenticated channel invalidates need of secrecy. BUT given time this could be cracked, whilst the resultant setup would **NOT**
> >  3. A and B must have good random number generators that can’t be predicted by an eavesdropper, even though the eavesdropper can see some output of the generator.
> 
> > [!NOTE] Quantum Fourier
> > ![[Quantum Fourier.png]]





> [!heart]+ Proofs
> > [!d]- 
> > **infimum**- 
> > **supramum**
> 
> > [!note abstract tip info success failure todo heart flower sigma leaf omega help example quote warning danger bug]-
> 



> [!leaf]+ Additional Topics
> - Cook-Levin theorem
> - SAT problem
> - 4-SAT to 3-SAT $(l_1,1_2,l_3,l_4)\to ((l_1,1_2,\bar{y})\vee(y,l_3,l_4))$
> - Classes beyond NP (PSPACE)


---
#TODO
[[Grail 🩷]]



#Chatted 

---

## 🧠 Complexity Theory Foundations

**Algorithm** — A finite, well-defined sequence of computational steps that transform input into output.

**Computational Problem** — A task mapping valid inputs to desired outputs, often formalised as a function or decision problem.

**Mathematical Model of Computation** — A formal abstraction (e.g. Turing Machine) defining what an algorithm can do and how efficiently.

**Turing Machine (TM)** — A theoretical model with a tape, head, and finite control used to define computation and algorithmic complexity.

**Input Encoding** — Representation of problem instances as finite strings over a finite alphabet.

**Alphabet ($\Sigma$)** — A finite set of symbols used to build input strings.

**Word / String** — A finite sequence of symbols from an alphabet.

**Yes–No Problem (Decision Problem)** — A computational problem whose answer is either _Yes_ or _No_.

**Polynomial-Time Algorithm** — An algorithm whose running time grows no faster than a polynomial in the size of its input.

**Exponential Time** — Algorithms whose running time grows as $O(a^n)$ for some $a>1$; generally infeasible for large $n$.

**Effective Algorithm** — A precisely defined and executable procedure guaranteed to produce correct results for valid inputs.

**Brute Force Algorithm** — Searches all possible cases exhaustively, usually taking exponential time.

---

## ⚙️ Asymptotic Notation

**Big-O ($O$)** — Upper bound: $f(n)=O(g(n))$ means $f(n)$ grows at most as fast as $cg(n)$ for some constant $c$.

**Big-Omega ($\Omega$)** — Lower bound: $f(n)=\Omega(g(n))$ means $f(n)$ grows at least as fast as $cg(n)$ for large $n$.

**Big-Theta ($\Theta$)** — Tight bound: $f(n)=\Theta(g(n))$ means $f(n)$ grows at the same asymptotic rate as $g(n)$.

**Polynomial Growth** — Growth proportional to some $n^k$, where $k$ is constant.

**Exponential Growth** — Growth proportional to $a^n$, where $a>1$.

**Logarithmic Growth** — Growth proportional to $\log n$, increases very slowly.

---

## 🧩 Graph Theory Concepts

**Graph $G=(V,E)$** — A set of vertices $V$ and edges $E$ connecting them.

**Vertex (Node)** — A single point in a graph representing an entity.

**Edge (Arc)** — A connection or relation between two vertices.

**Directed Graph (Digraph)** — Graph where edges have a direction $(v_i,v_j) \neq (v_j,v_i)$.

**Undirected Graph** — Graph where edges are unordered pairs; direction is irrelevant.

**Adjacency Matrix** — A binary matrix where entry $(i,j)=1$ if edge $(v_i,v_j)\in E$.

**Graph Encoding** — Representation of a graph as a binary or symbolic string for Turing Machines.

**Travelling Salesman Problem (TSP)** — Find the shortest route visiting all cities exactly once and returning to the start.

**Triangle Inequality** — For distances $d$, $d(i,j) + d(j,k) \ge d(i,k)$.

**Minimum Spanning Tree (MST)** — A subset of edges connecting all vertices with minimum total weight.

**Kruskal’s Algorithm** — Builds the MST by repeatedly adding the smallest edge that doesn’t form a cycle.

**Prim’s Algorithm** — Grows an MST by starting at one vertex and repeatedly adding the smallest adjacent edge.

**Approximation Algorithm** — Produces near-optimal solutions within a provable ratio $\rho(n)$ of the optimum.

---

## 🧮 Computational Classes

**Class $P$** — Set of decision problems solvable by a deterministic TM in polynomial time.

**Class $NP$** — Set of decision problems whose _solutions_ can be _verified_ in polynomial time by a deterministic TM, or _solved_ by a nondeterministic TM in polynomial time.

**NP-Hard** — Problems at least as hard as any problem in $NP$, not necessarily in $NP$ themselves.

**NP-Complete** — Problems in $NP$ to which every other $NP$ problem can be polynomially transformed.

**Polynomial Transformation (Reduction)** — A function $f$ computable in polynomial time such that $x\in L_1 \iff f(x)\in L_2$.

**Polynomial Equivalence** — Two problems reducible to each other in polynomial time ($L_1 \propto L_2$ and $L_2 \propto L_1$).

**Cook’s Theorem** — Proves that SAT is NP-Complete.

**Satisfiability Problem (SAT)** — Determine whether a Boolean formula has a truth assignment that makes it true.

**3-SAT** — SAT restricted to formulas in CNF where each clause has exactly three literals.

**Decision Problem** — Problem with binary (Yes/No) answers.

**Search Problem** — Problem requiring explicit construction of a solution, not just existence.

**Turing Transformation** — A general reduction allowing multiple calls to a subroutine for another problem.

**Oracle Turing Machine (OTM)** — TM equipped with a special tape and oracle that can instantly decide a particular language.

---

## 🔢 Boolean Logic and Formulas

**Boolean Variable** — A variable that can take values _true_ or _false_.

**Literal** — A Boolean variable $x_i$ or its negation $\bar{x_i}$.

**Clause** — A disjunction ($\lor$) of literals, e.g. $(x_1 \lor \bar{x_2} \lor x_3)$.

**Conjunctive Normal Form (CNF)** — A conjunction ($\land$) of clauses, each a disjunction of literals.

**Disjunctive Normal Form (DNF)** — A disjunction ($\lor$) of conjunctions of literals.

**Tseitin Transformation** — Converts an arbitrary Boolean formula into an _equisatisfiable_ CNF formula, increasing size only linearly.

**Resolution** — Rule of inference combining clauses $(A \lor x)$ and $(B \lor \bar{x})$ into $(A \lor B)$ to simplify SAT.

**DPLL Algorithm** — Recursive SAT-solving method that chooses variable assignments and backtracks when contradictions occur.

**CDCL (Conflict-Driven Clause Learning)** — Advanced SAT solver extending DPLL with learned clauses from conflicts.

**Two-Watched-Literals Scheme** — Efficient SAT implementation tracking two unassigned literals per clause to minimize scanning.

---

## 📈 Algorithmic Problems & Proofs

**Hamiltonian Cycle** — A cycle visiting each vertex exactly once.

**Graph Isomorphism** — Determine whether two graphs are structurally identical via a bijective mapping of vertices.

**Subgraph Isomorphism** — Determine whether one graph contains a subgraph isomorphic to another; NP-complete.

**Linear Programming (LP)** — Determine if a system of linear inequalities has a solution; solvable in polynomial time.

**Distinctness Problem** — Determine whether all elements of a list are distinct.

**Sorting Lower Bound** — Any comparison-based sorting algorithm requires at least $\Omega(n \log n)$ comparisons.

**Algebraic Computation Tree** — Decision model for problems defined by algebraic operations and comparisons.

**Decision Tree** — Tree structure representing comparisons guiding an algorithm’s choices.

**Semialgebraic Set** — Subset of $\mathbb{R}^n$ defined by finitely many polynomial equalities/inequalities.

---

## 💡 Randomized and Probabilistic Classes

**Monte Carlo Algorithm** — Runs in polynomial time and returns the correct result _with high probability_.

**Las Vegas Algorithm** — Always returns a correct result; running time is polynomial _on average_.

**Class $RP$** — Problems solvable by a probabilistic polynomial-time algorithm that may err on _false negatives_.

**Class $co\text{-}RP$** — Complement of $RP$, may err on _false positives_.

**Class $BPP$** — Problems solvable in polynomial time with bounded two-sided error probability ($<\frac{1}{2}$).

**Class $ZPP$** — Zero-error probabilistic polynomial time; expected polynomial runtime and always correct.

**Atlantic City Algorithm** — Informal class: polynomial time with high probability and correct with high probability.

---

## 🧬 Quantum Computing Concepts

**Qubit** — Quantum analogue of a bit; a normalized vector in $\mathbb{C}^2$.

**Basis States** — Orthonormal vectors $|0\rangle$ and $|1\rangle$ spanning $\mathbb{C}^2$.

**Superposition** — A qubit state $|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$ with $|\alpha|^2 + |\beta|^2 = 1$.

**Unitary Matrix** — Matrix $U$ satisfying $U^\dagger U = I$, representing reversible evolution.

**Hermitian Matrix** — Matrix equal to its own conjugate transpose ($A = A^\dagger$).

**Hadamard Matrix / Gate** — Single-qubit gate creating equal superpositions: $H|0\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)$.

**Tensor Product ($\otimes$)** — Combines quantum states or matrices to represent multi-qubit systems.

**Non-Commutativity** — $A \otimes B \ne B \otimes A$ in general.

**Bloch Sphere** — Geometric representation of qubit states as points on a unit sphere.

**Entanglement** — Non-separable multi-qubit state exhibiting correlations stronger than classical ones.

**Quantum Measurement** — Collapses superposed state probabilistically into a basis state.

**Quantum Gate** — Unitary operator acting on qubits to manipulate states.

**Oracle Gate** — Encodes a function $f(x)$ within a quantum circuit, often used for black-box problems.

**Quantum Circuit** — Network of quantum gates performing computation on qubits.

**Quantum Parallelism** — Evaluating $f(x)$ on many superposed inputs simultaneously.

---

## 🔬 Mathematical & Algebraic Tools

**Vector Space** — Set of vectors closed under addition and scalar multiplication.

**Linear Transformation** — Function preserving vector addition and scalar multiplication.

**Adjoint ($A^\dagger$)** — Conjugate transpose of a complex matrix.

**Complex Conjugate ($\bar{z}$)** — Reflection of a complex number across the real axis.

**Semialgebraic Geometry** — Study of sets defined by polynomial constraints, used in lower bound proofs.

**Connected Components** — Maximal subsets of a topological space that are path-connected.

---

## 🧾 Meta Concepts

**Rigorous Definition of Algorithm** — Necessary for proving nonexistence or existence of algorithms within a model.

**Reasonable Encoding Scheme** — Encoding that doesn’t artificially inflate input size beyond polynomial limits.

**Reduction** — Mapping one problem into another, preserving solvability and typically computable in polynomial time.

**Approximation Ratio ($\rho$)** — Quantifies how close an approximate solution is to optimal.

**Lower Bound Proof** — Demonstrates that no algorithm can solve a problem faster than a certain complexity.

**Existence vs. Nonexistence of Algorithm** — Foundational to proving problems are unsolvable or intractable.

---

## Computational Complexity & Theory  
Cook’s Theorem  
Ladner’s Theorem  
P vs NP  
NP  
NP-Complete  
NP-Hard  
NP-Intermediate Problems  
NP-Complete Problems  
BQP  
BPP  
RP  
Co-RP  
Polynomial Time Complexity  
Polynomial Space  
Polynomial Time Transformations  
Polynomial Transformations  
Complexity Classes  
Computational Complexity  
Undecidability  
Halting Problem  
Semi-Decidable Sets  
Computability  
  
## Decision Problems & Reductions  
Decision Problems  
Search Problems  
Boolean Satisfiability Problem (SAT)  
K-SAT  
3-SAT  
Satisfiability  
Satisfiability Threshold Conjecture  
Set Inclusion Problem  
Membership Test  
Feasibility Problem  
  
## Algorithms & Algorithmic Paradigms  
Shor’s Algorithm  
Grover’s Algorithm  
Deutsch–Jozsa Algorithm  
Quantum Phase Estimation  
Quantum Fourier Transform  
Continued Fraction Algorithm  
Approximation Algorithms  
Greedy Algorithms  
Binary Search  
Comparison-Based Sorting  
Master Theorem  
  
## Quantum Computation & Information  
Qubits  
Multiple Qubits  
Quantum Algorithms  
Quantum Circuits  
Quantum Gates  
Controlled Operations  
Unitary Matrices  
Quantum Superposition  
Quantum Entanglement  
Quantum State Vectors  
Measurement Probabilities  
State Collapse  
Independence of Qubits  
Tensor Product for Multiple Qubits  
Quantum Turing Machine  
Quantum Communications  
Quantum Key Distribution  
Quantum Key Establishment  
Eavesdropping Detection  
  
## Linear Algebra & Mathematical Foundations (Advanced Use)  
Inner Product  
Outer Products  
Tensor Product  
Kronecker Product  
Orthonormal Basis  
Gram–Schmidt  
Eigenvalues  
Eigenvectors  
Hermitian Matrices  
Adjoint  
Unitary Operators  
Bra–Ket Notation  
Bloch Sphere  
Orthogonality  
  
## Logic, SAT Solvers & Formal Methods  
DPLL  
CDCL (Conflict-Directed Clause Learning)  
SMT  
Resolution Algorithm  
Conjunctive Normal Form (CNF)  
Disjunctive Normal Form (DNF)  
Clause Representation  
Restart Strategies  
Variable Assignment  
  
## Computation Models  
Turing Machine  
Oracle Turing Machine  
Non-Deterministic Turing Machine  
Single-Tape Turing Machine  
Random Access Machine  
Uniform Sequence of Machines  
  
## Decision Trees & Algebraic Geometry  
Decision Tree  
Computational Tree  
Algebraic Computation Tree  
Algebraic Computation Trees  
Semi-Algebraic Sets  
Cylindrical Algebraic Decomposition  
Quantifier Elimination  
Tarski’s Decision Method  
Collins’ Algorithm  
  
## Graph Theory & NP Problems  
Clique Problem  
Vertex Cover Problem  
Independent Set Problem  
Travelling Salesman Problem  
Hamiltonian Circuit  
Graph Isomorphism  
Bipartite Graphs  
Connected Components  
Minimum Spanning Tree  
  
## Randomised Algorithms  
Monte Carlo Algorithms  
Las Vegas Algorithms  
  
## Cryptography  
RSA  
Discrete Logarithm  
Diffie–Hellman  
Elliptic Curve Cryptography  
Factoring