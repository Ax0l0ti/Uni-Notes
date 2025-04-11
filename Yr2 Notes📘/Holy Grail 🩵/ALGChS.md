# Algorithms and Complexity Cheat Sheet
---
> [!info]+ Module Details
> Includes information about (genus:: Cheat Sheet), link to CS module and it's correspondent attribute tag 
> *Module Tag :* (ModCode :: CM22008) 
> *Link :* [[Algorithms and Complexity]]
> *Cheat Sheet tag :* [[Grail 🩷]]

---
### Equations and phrases
**Structure :** (Topic) Phrase
#### Phrases

#### Equations
Master theorem for recursion
e.g 
$$\begin{aligned}
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
>[!danger]+ Automata	
| **Model**          | **Memory**    | **Power**              | **Problem it can’t solve** |
| ------------------ | ------------- | ---------------------- | -------------------------- |
| Finite automaton   | Finite states | Regular languages      | $w \in \{ a^k b^k\}$       |
| Pushdown automaton | Stack         | Context-free languages | $w \in \{ a^k b^k c^k\}$   |
| Turing machine     | Tape          | Full computation       | $Halting$ $problem$        |


Binary search trees are a data structure supporting (somewhat) efficient insert, delete and search. They work best when balanced! Worst case unbalanced operations are $O(n)$. 15 Self-balancing binary search trees do extra work when modified, so that balance is retained. Worst case cost of operations in **AVL trees** is $O(logn)$.

1. Turing Machine
    - 
    -

2. **Topic 3**
    - 
    - 
3. **Topic 4**
    - 
    - 
4. **Topic 5**
    - 
    - 

---
#TODO 