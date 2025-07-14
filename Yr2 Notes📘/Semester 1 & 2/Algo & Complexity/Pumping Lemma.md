# Pumping Lemma
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  24-10-2024
> > *Module :* [[Yr2 Notes📘/Semester 1 & 2/Algo & Complexity/Algorithms and Complexity]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Why use it?]]
> [[#What is it?]]
> [[#When can it be used?]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  Pumping Lemma aka **Looping theory**
> $b)$ - Sufficiently long means $|w|$ $\geq$ number of states
> $c)$ - Pumping Lemma can prove **NOT** regular, cannot be used to prove regular

---
### Why use it? 
Concept - Regular languages can't define everything. If we need to prove a language $L$ is not regular, if we can prove it cant be pumped, this proves it isn't a regular language.

### What is it? 
Pumping is the statement we can repeat 0 or infinite numbers of $y$
$[w = x(y)^*z] \in L$

>[!abstract] Proof
Let $y$ denote the word represented by the first loop, so that $w = xyz$ with $y\not =e$ and $|xy| ≤ n$. Then we can either remove this loop or repeat it as many times as we like i.e. $xz,xyz,xyyz,xyyyz,...$ all result in paths to an accepting states. Therefore they are all words in the language $L$

### When can it be used?
If you language regular and sufficiently long, it can be pumped
> [!example] Sufficiently long definition
> Sufficiently long means $|w|$ $\geq$ number of states

### How to use it 

[[Yr2 Notes📘/Semester 1 & 2/Algo & Complexity/How to use the Pumping Lemma]]
