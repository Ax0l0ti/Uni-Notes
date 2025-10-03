# Big O
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
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
> [!danger]+ 🕰️* Speed run*
> Break down of topic 
> - Big O Notation is also known as Landau's Notation
> - the removal of smaller factors from $O(n^22^n)$ is known as "Soft O" $Õ(2^n)$ 

---

#TODO 

People normally write $f(x) = O(n)$ but correct notation is $f(x) \in O(n)$  

$\exists c$ means up to a constant multiple, $\exists X$ form some point on eventually, $\forall x\gt X, f(c) \leq cg(x)$
We say the function f(x) is in the class 


### Time complexity graph and Cheat Sheet 

![[Big O Cheatsheet.png|]]


> [!note abstract tip info success failure todo heart flower sigma leaf omega help example quote warning danger bug] All blocks
> In the graph, below $O(n)$ there exists things like $O(\log x \log \log x),O(\log^2 x)$ and $O(\sqrt{x})$
> 


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

---

## Sorting


