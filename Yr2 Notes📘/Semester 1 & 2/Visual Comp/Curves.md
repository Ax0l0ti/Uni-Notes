# Curves
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  20-11-2024
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
> > $a)$ -  Hermite Curves $p(t) = CQ(t) = SMQ(t)$
> $b)$ - Bezier Curves
> 	
> $c)$ - Catmull-Rom curve 
> 	based on control points, gradient not specified

---

#TODO 
[Topic: Lecture 15- Curves | CM22010 - Visual Computing | Home](https://moodle.bath.ac.uk/course/view.php?id=61733&section=15)


> [!lead]+ 2D Curve Recap
> ![[2D curve Recap.png|600]]


## Hermite


 We can model complex curves by piecewise functions 
 We typically want to have continuity of:
	 – value – e.g. $𝑓(1) =𝑔(0) (C^0 continuity)$ and
	 – derivative – e.g. $𝑓′(1) =𝑔′(0) (C^1 continuity)$ 
 The simplest curve that can do this is the cubic polynomial
	 – $C1$ continuity specifies value and derivative at 2 endpoints 
 We can derive the cubic equation for a given pair of endpoint values and endpoint derivatives
	 – A curve specified in this way is called a **Hermite curve**

![[Pasted image 20241125150511.png|600]]

![[Hermite Explanation.png|500]]


## Bezier

![[Pasted image 20241127112813.png|500]]
## Catmull-Rom curve

![[Catmull-Rom.png|600]]