# How to use the Pumping Lemma
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  28-10-2024
> > *Module :* [[Yr2 Notes📘/Semester 1 & 2/Algo & Complexity/Algorithms and Complexity]]
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
> > $a)$ -  
> $b)$ - 
> $c)$ - 

---

### About the pumping lemma
[[Yr2 Notes📘/Semester 1 & 2/Algo & Complexity/Pumping Lemma]]

### Summary

In any regular language there is a number $n$, called the pumping length, such that all words in $L$ of $length ≥ n$ can be “pumped”. How to prove that a language $L$ is not regular:
1. Suppose that $L$ is regular. 
2. Then by the pumping lemma, all words that are sufficiently big can be pumped. 
3. Show that for any $n$, there is some word $w ∈ L$ of $length ≥ n$ that cannot be pumped. 
4. Contradiction! 
5. Therefore our original claim was false, and $L$ cannot be regular


### Proof

1. Suppose $L$ is regular. Then by the pumping lemma there exists some $n \gt 0$ such that all words w with $|w| \geq n$ can be pumped 
2. Make a clever choice of $w ∈ L$ with $|w| ≥ n$. Your choice will need to work for any possible value of $n$. 
	Define $w = 0^n1^n \in L$, and note that $|w| = 2n \geq n$.
3. By the pumping lemma there is some division $w = xyz$ with 
> $y=e$  
> $|xy| ≤ n$
> $xy^iz ∈ L$ for $i ≥ 0$ 
4. For any such division, try to use the fact that $y= e$ and $|xy| ≤ n$ to find some $i ≥ 0$ such that $xy^iz / ∈ L$.
5.  You will have then found a CONTRADICTION, therefore L is not regular


### Common mistakes

Let $n = 4$, $w=0^41^4$

what the hell $$\begin{align} \text{Let} w = 0^n1^n\\...\text{Let} x = e, y = 0^m, z=1^n \\\end{align}$$


### Examples

![[pumping lemma ex1.png|500]]




![[pumping lemma ex2.png]]