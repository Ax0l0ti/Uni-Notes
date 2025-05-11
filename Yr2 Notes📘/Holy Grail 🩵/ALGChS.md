# Algorithms and Complexity Cheat Sheet
---
> [!info]+ Module Details
> Includes information about (genus:: Cheat Sheet), link to CS module and it's correspondent attribute tag 
> *Module Tag :* (ModCode :: CM22008) 
> *Link :* [[Algorithms and Complexity]]
> *Cheat Sheet tag :* [[Grail 🩷]]

---

---
> [!danger]+ ⚡ *Speed run*
> - **Automata & Formal Languages**: DFA, NFA, PFA, Pumping Lemma (regular), CFL, CFG, PDA, Pumping Lemma (context-free), Parsing  
> - **Turing Machines & Computability**: Turing Machine, Universal TM, Church-Turing Thesis, Halting Problem, Decidability, Undecidability  
> - **Complexity Classes**: P, NP, NP-Complete, P vs NP, Non-deterministic TM  
> - **Data Structures**: Array, Linked List, Stack, Queue, Tree, BST, AVL, Heap, Graph, Hash Table, Disjoint Set (Union-Find)  
> - **Algorithm Design**: Divide-and-Conquer, Dynamic Programming, Greedy, Recursion, Memoization  
> - **Algorithm Analysis**: Best/Worst/Average Case, Time, Space, Big-O, Big-Θ, Big-Ω, Loop Invariants  
> - **Sorting & Searching**: Selection Sort, Insertion Sort, Merge Sort, Quicksort, HeapSort, TreeSort, BFS, DFS, Dijkstra, Floyd-Warshall, Kruskal  
> - **Special Topics**: Ackermann Function, Inverse Ackermann, Polyalgorithms, Cache Efficiency, Crossover Points
> 

---


Loop invariant is proof statement true before and after loop iteration
Floyd-Warshall
Dijkstra 


$$\begin{aligned}
&\text{Master Theorem} \\
&\text{$a$ is req subproblems per layer, $b$ is rate of dividing (e.g div\&con b = 2)}  \\\\
&T(n) = aT(n/b)+ f(n) \\
&where \ f() \text{ is the recursive function O()} 
\end{aligned}
$$
$$\begin{align}  
&\text{Master Theorem (simplified) Theorem. Given the above recurrence, let $c = log_ba$.}\\ &1. \ \text{If $f(n)$ grows slower than $O(n^c)$ then $T(n) = Θ(n^c)$.}\\ & \ \text{2. If $f(n)$ is equal to $Θ(n^c)$ then $T(n) = Θ(n^clogn)$.}\\ &3. \ \text{If $f(n)$ grows faster than $Ω(n^c)$, then T(n) = Θ(f(n)).}
\end{align}$$


Master theorem basically tells us if a recursive's $O(n)$ is based off its ==**branching**== $(case \ 1)$, ==**function**== calls $(case \ 3)$ or ==**both**== equal $(case \ 2)$

---
### Topics


> [!Flower] $O,\Theta \ and \ \Omega$
> $O$ is considering max time/space , if $f(n) \ is \le O(n), \ then \ f(n) \ is \le O(n^2)$
> $\Theta$ is average, meaning the rate of growth is equal to a specified value 
> $\Omega$ is lower bound, if$f(n) \ is \ge \Omega(n^2), \ then \ f(n) \ is \ge \Omega(n)$


>[!danger]+ Automata	
| **Model**          | **Memory**    | **Power**              | **Problem it can’t solve** |
| ------------------ | ------------- | ---------------------- | -------------------------- |
| Finite automaton   | Finite states | Regular languages      | $w \in \{ a^k b^k\}$       |
| Pushdown automaton | Stack         | Context-free languages | $w \in \{ a^k b^k c^k\}$   |
| Turing machine     | Tape          | Full computation       | $Halting$ $problem$        |

# All trees have $log(n)$ layers
### Binary search trees 
Data structure supporting (somewhat) efficient insert, delete and search. They work best when balanced! Worst case unbalanced operations are $O(n)$. 15 Self-balancing binary search trees do extra work when modified, so that balance is retained. Worst case cost of operations in **AVL trees** is $O(logn)$.
### HEAP 
**Max** heap children are smaller, **min** heap children bigger

| Min for Priority queues<br>Max for  | $left(i) = 2*i$<br>$right(i) = 2*i + 1$<br>$parent(i) — floor (i/2)$ |
| ----------------------------------- | -------------------------------------------------------------------- |



---
#TODO 