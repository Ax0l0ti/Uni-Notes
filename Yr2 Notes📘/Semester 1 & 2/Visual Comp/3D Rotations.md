# 3D Rotations
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  18-11-2024
> > *Module :* [[Visual Computing]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Rules]]
> [[#2D vs 3D affine]]
> [[#Euler Angles]]
> [[#Resultant matrix]]
> [[Gimbal Lock]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  
> $b)$ - 
> $c)$ - 

---
## Rules 

when working in 3D, there are  numerous ways to interpret rotations. For our course we will be working around the right hand as seen below.
![[Pasted image 20241118143605.png|100]]

![[Right-Hand Screw rule.png|400]]


Akin to [[2D Rotations]], but only with another dimension, this operates on an additonal layer related to $z$. 


> [!abstract] Rotation
> For a rotation **Clockwise** around the $z$ axis, the required matrix for $M$ is as followed : 
> $$\begin{align}  
\begin{bmatrix} \cos \theta & -\sin \theta & 0 \\
\sin \theta & \cos \theta & 0 \\
0 & 0 & 1
\end{bmatrix} 
\end{align}$$
> For **Anti**, the $-$ is flipped ( follows the clockhand to the first $sin$)
> 

## 2D vs 3D affine 


![[Pasted image 20241118143001.png]]

## Euler Angles
- Generates an arbitrary rotation matrix (rotation about an arbitrary axis passing through the origin) 
- Simple idea: use an ordered combination of rotations about the x-, y- and x-axes

![[Eulers Angles.png|500]]


## Resultant matrix

Obviously, the Resultant rotation $R_{combined}$ is equal to the product of all $R_{z,y,x}$
This can be done with any number of 3 combinations. E.g 2 rotations in $x$ and 1 in $y$ in order $xyx$
An example of this can be seen below
![[Rotation Combination.png]]

----
### Rotation Redundancy

Whilst there is $3^3$ possible combinations for $x, y, z$, it is redundant to do 2 rotations of the same axis multiple times in a row

## Gimbal Lock

[Gimbal lock - Wikipedia](https://en.wikipedia.org/wiki/Gimbal_lock)
this is the rotation strategy used in camera work as it can lock certain directions of movement via euler's law
![[Gimbal_Lock_Plane.gif]]