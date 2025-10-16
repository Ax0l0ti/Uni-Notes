# Markov Decision Processes
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  15-10-2025
> > *Module :* [[Reinforcement Learning]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]


--- 
> [!danger]+ 🕰️* Speed run*
> Break down of topic 
> - episodic means can be split in episodes
> - continuation task mean the task has no clear breaks/ last forever
> - how sequential decision problems can be either **episodic** or **continuing**,
> - introduced notation with which we can describe both episodic and continuing sequential problems,
> - discussed what information needs to be summarised in our state representation, in order to ensure that the **Markov property** holds, and
> - formulated sequential decision problems formally as **Markov decision processes (MDPs)**.

---

#TODO 



1. Components of MDP: states, actions, transition probabilities, rewards, and initial state distribution,
• A set of **states**: $S$
• A set of **actions** available in each state: $A(s), s \in S$
• A **transition** function: $p(s'|s, a), s \in S, s' \in S, a \in A(s)$
• A **reward** function: $r(s, a, s'), s \in S, s' \in S, a \in A(s)$
• An **initial** state distribution: $h(s), s \in S$
We will often combine $p$ and $r$ into $p(s', r | s, a).$

2. Expected values of random variables,
3. Value functions: state value function and action value function,
4. Optimal policies and comparison of policies,
5. Bellman equations: Bellman equation for state value and Bellman optimality equation,

6. Dynamic programming methods for solving MDPs,
![[Dynamic Prog for Bellman.png|400]]
7. Policy evaluation and policy improvement,
8. Iterative policy evaluation algorithm,
![[Pasted image 20251015191745.png|500]]
9. Policy improvement process and general policy iteration,
10. Value iteration algorithm,
11. Summary of dynamic programming methods' limitations,
12. Introduction to Monte Carlo methods (upcoming content next week),
13. Recap of key points from the lecture

