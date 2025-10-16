# Complexity
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  10-02-2025
> > *Module :* [[]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]
> [[#]]
> [[#]]
> [[#]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  Big $O$ is **Upper Bound** Complexity on rate of growth "no worse than"
> $b)$ - Big $\Omega$ is  **Lower Bound** "no better than"
> $c)$ - Big $\Theta$ is complexity has some of both O and $\Omega$

---
> [!heart] Big $O$
>  Big $O$ is the *Upper Bound* Complexity of a function. we say $f(n)$ is $O(g)$ if g always smaller than $f(n)$ as n lim infinite
>  **Definition**. Given a function $g(n)$, we say that “$f(n)$ is $O(g(n))$” if there exists $c > 0$ and $n_0 ≥ 0$ such that for all $n ≥ n_0 0 ≤f(n) ≤ cg(n)$ People sometimes write “$f(n) = O(g(n))$” or “$f = O(g)$”


> [!omega] Big $\Omega$
>  Big $\Omega$ is the *Lower Bound* Complexity of a function. we say $f(n)$ is $\Omega(g)$ if g always smaller than $f(n)$ as n lim infinite
>  **Definition**. Given a function $g(n)$, we say that “$f(n)$ is $\Omega(g(n))$” if there exists $c > 0$ and $n_0 ≥ 0$ such that for all $n ≥ n_0 0 ≤ cg(n) ≤f(n)$ People sometimes write “$f(n) = \Omega(g(n))$” or “$f = \Omega(g)$”


> [!flower] Big $\Theta$
>  Big $\Theta$ is the middle ground. some constants are above and below this complexity
>  **Definition**. Given a function $g(n)$, we say that “$f is Θ(g(n))$” if it is both $O(g(n))$ and $Ω(g(n))$.
>  **More explicitly:** $f$ is $Θ(g(n))$ if there are positive constants $c1 > 0, c2 > 0$ and $n_0 ≥ 0$ such that for all $n ≥ n_0 0 ≤c_1g(n) ≤ f(n) ≤ c_2g(n)$. Big-$Θ$ combines Big-$O$ and Big-$Ω$ to capture an exact (asymptotic) complexity
