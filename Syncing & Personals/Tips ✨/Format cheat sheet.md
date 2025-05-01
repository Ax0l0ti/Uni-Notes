# Obsidian Tips 
---
--- creates a spacer like above
### Hash creates title, more hash = smaller title
[[Stips ✨]]
# Index : 
> [[#Tables]]
> [[#Bullets]]
> [[#Links]]
> [[#Maths]]
> [[#Graphs]]
> [[#Callouts]]
> [[#Data view]]
---

#### Tables

The text below creates the following table   
L-al text | C-al text | R-al text 
:-- | :--: | --: 
I'm **bold** because of \*\*text\*\* | I'm *Italian* because of \*text\* | I'm ==high== because of text \=\=text\=\=

L-al text | C-al text | R-al text 
:-- | :--: | --: 
I'm **bold** because of \*\*text\*\* | I'm *Italian* because of \*text\* | I'm ==high== because of text \=\=text\=\

--- 
#### Bullets 
\- , \1. and - \[  \] used to make : 
- Bullet
1. Numbered
- [ ] Checkbox 

#### Links
links to other files can be made by \[\[ link ]] and links within the files to titles can be done by \[\[# title ]]
[Some text](README)
[[#Index]]

---
#### Maths

in text equations use $ on both sides  $= e^{i\theta\pi}$ 
Block use \$\$ $$ \text{Bonjour, je ne pas da baguette. } \\ f(x) =  \frac{\sum i( 9.81m)}{a} \text{ where } m \text{ is mass }$$

---
# Memaid

### Deployable Themes 
The following are a list of **Deployable themes**, sample `%%init%%` directives and `initialize` calls.
base, forest, dark, default/light, neutral
> [!note]+ Base Gantt
> **base**- Designed to be modified, as the name implies it is supposed to be used as the base for making custom themes.
> ```mermaid
%%{init: {'theme': 'base'}}%%
gantt 
title A Gantt Diagram 
dateFormat YYYY-MM-DD 
section Section 
A task :a1, 2014-01-01, 30d 
Another task :after a1, 20d 
section Another 
Task in Another :2014-01-12, 12d 
another task :24d ```

> [!leaf]+ Forest Gantt
>  **forest**- A theme full of light greens that is easy on the eyes.
> ```mermaid
%%{init: {'theme': 'forest'}}%%
gantt 
title A Gantt Diagram 
dateFormat YYYY-MM-DD 
section Section 
A task :a1, 2014-01-01, 30d 
Another task :after a1, 20d 
section Another 
Task in Another :2014-01-12, 12d 
another task :24d

> [!omega]+ Dark Gantt
> **dark**- A theme that would go well with other dark-colored elements.
> ```mermaid
%%{init: {'theme': 'dark'}}%%
gantt 
title A Gantt Diagram 
dateFormat YYYY-MM-DD 
section Section 
A task :a1, 2014-01-01, 30d 
Another task :after a1, 20d 
section Another 
Task in Another :2014-01-12, 12d 
another task :24d

> [!example]+ Default Gantt
 > **default**- The default theme for all diagrams.
> ```mermaid
%%{init: {'theme': 'default'}}%%
gantt 
title A Gantt Diagram 
dateFormat YYYY-MM-DD 
section Section 
A task :a1, 2014-01-01, 30d 
Another task :after a1, 20d 
section Another 
Task in Another :2014-01-12, 12d 
another task :24d

> [!heart]+ Neutral Gantt
> **neutral**- The theme to be used for black and white printing.
> ```mermaid
%%{init: {'theme': 'neutral'}}%%
gantt 
title A Gantt Diagram 
dateFormat YYYY-MM-DD 
section Section 
A task :a1, 2014-01-01, 30d 
Another task :after a1, 20d 
section Another 
Task in Another :2014-01-12, 12d 
another task :24d



> [!omega]+ All blocks
> The symbol contains everything and defaults to note

```mermaid 
%%{init: {'theme': 'dark'}}%%
mindmap
root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid 
```

> [!leaf] Sequential
> 
> 

```mermaid
%%{init: {'theme': 'forest'}}%%
sequenceDiagram
    Uni ->>+Me: How's it going?
    Uni->>+Me: Hello? Are you there? 
    Me-->>-Uni: I want to die...
    Me-->>-Uni: At least I stole all these cool notes tho...
```

```mermaid
%%{init: {'theme': 'dark'}}%%
graph TD

Shortcuts --> README

class Shortcuts,README internal-link;
```

> [!abstract]+ Logic
> ```mermaid
stateDiagram-v2
[*] --> Still
Still --> [*]
Still --> Moving
Moving --> Still
Moving --> Crash
Crash --> [*]


--- 

## Callouts

> [!note]+
> > [!abstract]-  Abstract, Summary, Tldr
> > Womp womp

> [!info]+ Info, Todo
> > [!success]+ Success, Check, Done
> > susssy $\alpha + \lambda$ $$\begin{aligned} \text{womp womp???} \\ = \sum_{i = 0} ^{i \leq 69} x^2 \\ = 0 + c\end{aligned}$$
> > BOOM and thats how u do it
> 
> > [!failure] Failure, Fail, Missing
> > 

> [!tip] Tip, Hint, Important


> [!question] Question, Help, FAQ

> [!warning]+ Warning, Caution, Attention
> > [!danger] Danger, Error
> 
> > [!bug]

> [!example]+

> [!quote] Quote, Cite

# Data view


| Field Name         | Data Type      | Description                                                                                                                                                                     |
| :----------------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `file.name`        | Text           | The file name as seen in Obsidians sidebar.                                                                                                                                     |
| `file.folder`      | Text           | The path of the folder this file belongs to.                                                                                                                                    |
| `file.path`        | Text           | The full file path, including the files name.                                                                                                                                   |
| `file.ext`         | Text           | The extension of the file type; generally `md`.                                                                                                                                 |
| `file.link`        | Link           | A link to the file.                                                                                                                                                             |
| `file.size`        | Number         | The size (in bytes) of the file.                                                                                                                                                |
| `file.ctime`       | Date with Time | The date that the file was created.                                                                                                                                             |
| `file.cday`        | Date           | The date that the file was created.                                                                                                                                             |
| `file.mtime`       | Date with Time | The date that the file was last modified.                                                                                                                                       |
| `file.mday`        | Date           | The date that the file was last modified.                                                                                                                                       |
| `file.tags`        | List           | A list of all unique tags in the note. Subtags are broken down by each level, so `#Tag/1/A` will be stored in the list as `[#Tag, #Tag/1, #Tag/1/A]`.                           |
| `file.etags`       | List           | A list of all explicit tags in the note; unlike `file.tags`, does not break subtags down, i.e. `[#Tag/1/A]`                                                                     |
| `file.inlinks`     | List           | A list of all incoming links to this file, meaning all files that contain a link to this file.                                                                                  |
| `file.outlinks`    | List           | A list of all outgoing links from this file, meaning all links the file contains.                                                                                               |
| `file.aliases`     | List           | A list of all aliases for the note as defined via the [YAML frontmatter](https://help.obsidian.md/How+to/Add+aliases+to+note).                                                  |
| `file.tasks`       | List           | A list of all tasks (I.e., `\|[ ] some task`) in this file.                                                                                                                     |
| `file.lists`       | List           | A list of all list elements in the file (including tasks); these elements are effectively tasks and can be rendered in task views.                                              |
| `file.frontmatter` | List           | Contains the raw values of all frontmatter in form of `key \|value` text values; mainly useful for checking raw frontmatter values or for dynamically listing frontmatter keys. |
| `file.day`         | Date           | Only available if the file has a date inside its file name (of form `yyyy-mm-dd` or `yyyymmdd`), or has a `Date` field/inline field.                                            |
| `file.starred`     | Boolean        | if this file has been starred via the Obsidian Core Plugin "Starred Files".                                                                                                     |
