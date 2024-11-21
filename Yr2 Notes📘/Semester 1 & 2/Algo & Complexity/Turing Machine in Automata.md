# Turing Machine in Automata
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  20-11-2024
> > *Module :* [[Algorithms and Complexity]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Formal and Informal Definition]]
> [[#Transition Composition]]
> [[#State Diagram]]
> [[#]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  Made of **Head** and **Tape**. 
> > - **Head** points and contains instructions
> > - **Tape** contains memory
> 
> $b)$ - Transition function looks like $δ(state_0, read) → (state_1, write, move)$

---

## Formal and Informal Definition 

> [!Example]+ Definitions  of a Turing Machine 
> > [!info]+ Formal Definition 
> > Formally a Turing machine is described by the following: 
> > ![[Turing Machine Formal Defi.png|500]]
> > 
>  ---
> > [!flower]+ Informal Definition 
> > A Turing machine consists of two main components:
> > - **Head** ≈ ==Pointer== + the ”brain”, or control unit
> > - **Tape** ≈ an infinite memory for storing calculations, made up of individual cells
> > 

### Transition Composition

> [!sigma] Transition
> A Turing Machine's transitions are called a **Transition Relation**
> Each Transition is comprised of 5 elements. This can be seen to have the following structure: 
> $δ : (Q/H) × Σ → Q × (Σ ∪ \{L, R\})$ is the transition function
> this is structured as $δ(state_0, read) → (state_1, write, move)$
> where $move \in \{L,S,R\}$
> 

### State Diagram 
An example state diagram of a Turing machine can be seen below. 
![[Turing State Trans Diag Ex.png|400]]

