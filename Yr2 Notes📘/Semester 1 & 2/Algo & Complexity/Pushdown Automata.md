# Pushdown Automata
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  20-11-2024
> > *Module :* [[]]
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
> > $a)$ -  Basically DFA but with memory
> $b)$ -  Stack acts as memory
> $c)$ - Transition $\delta : ((state_0,input,pop), (state_1,stack))$

---

## Formal and Informal Definition 

> [!Example]+ Definitions  of a Pushdown Automata 
> > [!info]+ Formal Definition 
> > Formally a Pushdown automata is described by the following: 
> > ![[PDA formal definition.png]]
> > 
>  ---
> > [!flower]+ Informal Definition 
> > Literally just a DFA but with a stack as memory
> > 

### Transition Composition

> [!sigma]+ Transition
> A Pushdown Automata's transitions are called a **Transition Relation**
> Each Transition is comprised of 5 elements. This can be seen to have the following structure: 
> ![[Transition Relation PDA.png| 600]]
> 

### State Diagram 
An example state diagram and the formal definition can be seen below in the image. This is a non-regular expression that cant be accomplished by a DFA. 
![[PDA example.png| 600]]

| **Model**          | **Memory**    | **Power**              | **Problem it can’t solve** |
| ------------------ | ------------- | ---------------------- | -------------------------- |
| Finite automaton   | Finite states | Regular languages      | $w \in \{ a^k b^k\}$       |
| Pushdown automaton | Stack         | Context-free languages | $w \in \{ a^k b^k c^k\}$   |
| Turing machine     | Tape          | Full computation       | $Halting$ $problem$        |
