# Big O & Complexity Basics
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  30-09-2025
> > *Module :* [[Yr3 Notes📕/Semester 1/Complexity/Complexity|Complexity]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]


--- 
> [!tip]+ 🕰️* Speed run*
> Break down of topic 
> - Big O Notation is also known as Landau's Notation
> - the removal of smaller factors from $O(n^22^n)$ is known as "Soft O" $Õ(2^n)$ 
> - Church Turing Thesis - Any algorithm can be ran with a Deterministic TM, any D TM can be ran with an algorithm  [[Finite Automata & Regular Languages]] 

---
## Soft O

> [!cite] Soft O and basic notation
> People normally write $f(x) = O(n)$ but correct notation is $f(x) \in O(n)$  
> 
> $\exists c$ means up to a constant multiple, $\exists X$ form some point on eventually, $\forall x\gt X, f(c) \leq cg(x)$
> We say the function f(x) is in the class 
> **Soft O** is the simplified complexity via the removal of smaller factors from $O(n^22^n)$ is known as "Soft O" $Õ(2^n)$ 

## Time complexity graph and Cheat Sheet 

> [!note]+ Time Complexity
> In the graph, below $O(n)$ there exists things like $O(\log x \log \log x),O(\log^2 x)$ and $O(\sqrt{x})$
> ![[Big O Cheatsheet.png|]]

## Master theorem

> [!leaf]+ MAster Theorem
> $$\begin{aligned}
&\text{Master Theorem} \\
&\text{$a$ is req subproblems per layer, $b$ is rate of dividing (e.g div\&con b = 2)}  \\\\
&T(n) = aT(n/b)+ f(n) \\
&where \ f() \text{ is the recursive function O()} 
\end{aligned}$$
> $$\begin{align}  
&\text{Master Theorem (simplified) Theorem. Given the above recurrence, let $c = log_ba$.}\\ &1. \ \text{If $f(n)$ grows slower than $O(n^c)$ then $T(n) = Θ(n^c)$.}\\ & \ \text{2. If $f(n)$ is equal to $Θ(n^c)$ then $T(n) = Θ(n^clogn)$.}\\ &3. \ \text{If $f(n)$ grows faster than $Ω(n^c)$, then T(n) = Θ(f(n)).}
\end{align}$$
> Master theorem basically tells us if a recursive's $O(n)$ is based off its ==**branching**== $(case \ 1)$, ==**function**== calls $(case \ 3)$ or ==**both**== equal $(case \ 2)$

---

## Complexity Examples

### Adding 2 numbers


### Multiplying  2 numbers

Simple multiplication is $O(n^2)$ for square multiplying for each digit in each number

### Karatsuba Algorithm

This is a **Divide and Conquer** Algorithm that reduces the multiplication of two $n$-digit numbers to three multiplications of $n/2$-digit numbers and, by repeating this reduction, to at most $n^{log_2⁡3}≈n"{1.58}$ single-digit multiplications. It is therefore [asymptotically faster](https://en.wikipedia.org/wiki/Asymptotic_complexity "Asymptotic complexity") than the [traditional](https://en.wikipedia.org/wiki/Long_multiplication "Long multiplication") algorithm, which performs $n^2$ single-digit products.

![[Karatsuba Algo.png|600]]

This leaves a recursive $T(N) \leq 100N + 3T(\frac{N}{2})$ as 3 multiplications are needed per break and 
