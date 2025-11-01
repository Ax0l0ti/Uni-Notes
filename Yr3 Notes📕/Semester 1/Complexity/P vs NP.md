# P vs NP
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  10-10-2025
> > *Module :* [[Yr3 Notes📕/Semester 1/Comple$x_i$ty/Comple$x_i$ty|Comple$x_i$ty]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]

---
> [!tip]+ Speed run
> - **P**: Problems solvable in polynomial time.
> - **NP**: Problems verifiable in polynomial time.
> - **NP-Complete**: Hardest problems in NP; all NP problems reduce to them.
> - **P vs NP**: Major open problem asking if every problem whose solution can be verified quickly can also be solved quickly.
> - **Non-deterministic Turing Machine**: TM that can explore many possibilities simultaneously.
> - **Clique**: a Clique is a grouping of nodes all adjacent to each other

---

> [!example]+  Examples of Problems
> > [!flower]- Traveling salesman
> > Given N locations, can a salesman work out a route of weight $\leq$ K that visits all vertices and returns to the start?
> > This ends up resulting in $N!$ possible routes, as after the first there are $N-1$ left, hence $f(N)=N(N-1)(N-2)... = N!$
> > [Travelling salesman problem - Wikipedia](https://en.wikipedia.org/wiki/Travelling_salesman_problem)
> 
> > [!bug]- Satisfiability Problem (SAT)
> > Can a given boolean expression evaluate to true given you replace variables with true or false?
> > [Boolean satisfiability problem - Wikipedia](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem)
> > 
> 
> > [!leaf]- Subgraph isomorphism
> > Given two graphs, $H$ and  $G$, can you prove one is a subgraph of the other?
> > [Subgraph isomorphism problem - Wikipedia](https://en.wikipedia.org/wiki/Subgraph_isomorphism_problem)
> > 
> 



## Exploring SAT 
---
> [!tip]+ Speed run
> - **SAT is NP-Complete**
> - **Monte Carlo** (Different from ML MC) A polynomial-time algorithm that returns the right result with high probability (but not necessarily 1). 
> - **Example** Rabin’s primality: if N is prime returns “prime”, if not, returns “prime” with probability ≤ 1/4 (so if run 10 times on N, ≤ 1/410 < 10−6). [Dav92, random!] 
> - **One-sided error**, there are also algorithms with two-sided errors. 
> - Comple$x_i$ty $RP$ (one-sided: randomized polynomial time) $⊆ BPP$ (two-sided: Bounded-error probabilistic polynomial). 
> - **Las Vegas** Always the right result, and polynomial time with high probability (expected polynomial time). Comple$x_i$ty class ZPP (zero-error probabilistic polynomial time). 
> - **Theorem**: $ZPP=RP∩co-RP$. 
> - **Proof**: run both until they agree! 
> - **Atlantic City** Polynomial time with high probability and right result with high probability

### DPLL 
while $S \neq ∅$
1 If Some clause is just $x_i$, set $x_i$ to true, remove all clauses containing $x_i$ from S, and delete all $x_i$ from clauses in S. 
2 If Some clause is just $x_i$, set $x_i$ to false, remove all clauses containing $x_i$ from S, and delete all $x_i$ from clauses in S. 
3 If There are no $x_i$ in clauses in S, set $x_i$ to true, remove all clauses containing $x_i$ from S 
4 If There are no $x_i$ in clauses in S, set $x_i$ to true, remove all clauses containing $x_i$ from S 
5 Pick some $x_i$, compute DPLL(S ∪{$x_i$}). If this works, return DPLL(S ∪{$x_i$}) with $x_i$ = T 
6 Otherwise return DPLL(S ∪{$x_i$}) with $x_i$ = F NB Can do $x_i$ and $x_i$ in either order 

Essentially Resolution meets lazy brute force

### Conflict Directed Clause Learning 

> [!Success]+ Solutions
> > [!d]- Conflict Directed Clause Learning
> > Basically back jumping. If contradiction, find contradicting elements and make new rule
> > ![[Pasted image 20251017144705.png|450]]
> 
> > [!Danger]- Restarts
> > ![[Pasted image 20251017144900.png|450]]

