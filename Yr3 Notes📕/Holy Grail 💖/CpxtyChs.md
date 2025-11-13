# Computational Complexity Cheat Sheet
---
> [!info]+ Module Details
> Includes information about (genus:: Cheat Sheet) from [Year::3]. Links to Module Note and its correspondent attribute tag 
> *Module Tag :* [[Yr2 Notes📘/Semester 1 & 2/Algo & Complexity/Complexity]]
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
> > Likely essay questions and problem-solving proofs
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
