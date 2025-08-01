# Logistic Regression
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  03-10-2024
> > *Module :* [[Yr2 Notes📘/Semester 1 & 2/ML/Machine Learning]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Logistic Regression]]
> [[#Loss Function]]
> [[#Example of Log-less]]
> [[#Multi Class Example]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  Binary = y/n
> $b)$ - Multiclass = either / or 
> $c)$ - Muti-label = either / and

---

![[Classification Types.png]]


>[!info] ### Sigmoid Function
>The sigmoid functions goes between the values of 1 and 0. Hence it is perfect for probability and binary classificiation 
>Sigmoid is defined as the following : $$\frac{1}{𝟏+e^{-x}}$$
>![[Sigmoid Function.png]]


## Loss Function

>[!info] ### Log-loss 
>Log-Loss is a standard classification evaluation metric. 
>$𝐽(𝜃) =−[\log(ℎ_𝜃(𝑥)) + (1 -y)\log(1 -ℎ_𝜃(x))]$
>
![[Log-loss Function.png]]


### Example of Log-less



![[Example of Log-less.png]]



## Multi Class Example

This is solved by creating numerous lines that aim to seperate each class. This can be used by the final classifier to place new points via regioning 

![[Multi Class Example.png]]