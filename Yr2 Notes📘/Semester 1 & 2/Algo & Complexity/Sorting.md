# Sorting
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  11-02-2025
> > *Module :* [[Yr2 Notes📘/Semester 1 & 2/Algo & Complexity/Algorithms and Complexity]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Master theorem]]


--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  Selection
> > - Insertion
> > - 
> $b)$ - Loop Invariance
> $c)$ - Master Theorem

---

## Sorting Algorithms

![[Big O Cheatsheet.png]]

#### Selection
for every element $i$, get the next smallest element $s$ and swap $i$ and $s$ 

![[Selection Sort.png]]

#### Insertion
sort from one side. get next small element, compare to each element till inserted into correct place of sorted list section
Loop invariant - after each iteration the array $a$ is a permutation of the og array, and the first $i$ elements are in sorted order
![[Single Insertion Sort Loop.png|200]]

#### Merge Sort
Divide and Conquer
break list in half. Repeatedly break till single item lists, combine small ordered lists into bigger ordered lists


## Loop Invariant
A loop invariant is a property that holds before and after every iteration of a loop.

Generic loop code checks predicate $p$ is always true where property of $p$ being a loop invariant
```python
setup_code(); #the code we execute before entering the loop 
while (guard) { # the guard decides whether we enter the loop 
	loop_body(); # whatever the loop is doing 
} # end of loop
```


Uses:
- Helps prove correctness of an algorithm.
- Used in sorting algorithms to show that a certain property (e.g., sorted portion of an array) holds after each iteration.
Example: Insertion Sort
Invariant: At the start of each iteration, the first $𝑖$ elements are sorted.
Proof:
- Base case: set $p$ Before first iteration, one element is trivially sorted.
- Inductive step: If first $i$ elements are sorted, inserting the $(i+1)^{th}$
correctly maintains the sorted order. 

Loop invariants are crucial in proving the correctness of algorithms like selection sort, insertion sort, and mergesort.

--- 
## Master theorem



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