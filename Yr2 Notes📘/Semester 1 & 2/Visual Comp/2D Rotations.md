# 2D Rotations
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  28-10-2024
> > *Module :* [[Visual Computing]]
> > *Teacher*: KM 
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

#TODO 

## Linear transformations

This covers transformations such as stretches, rotations around the origin and reflections in axis
As shown in point one, every linear transformation maps the Origin to the Origin and is representable by a matrix
![[Summary of transformations1.png]]
![[Summary of transformations2.png]]


> [!abstract] Rotation
> For a rotation **Clockwise** the required matrix for $M$ is as followed : 
> $$\begin{align}  
\begin{bmatrix} \cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{bmatrix} 
\end{align}$$
> For **Anti**, the $-$ is flipped ( follows the clockhand to the first sin)
> 

## Translations
In the form below, a 2D translation can be seen as a matrix to be added
$$\begin{align}  
\begin{bmatrix} p_1' \\
p_2'
\end{bmatrix} = \begin{bmatrix} p_1 \\
p_2
\end{bmatrix} + \begin{bmatrix} t_1 \\
t_2
\end{bmatrix} 
\end{align}$$
However, to create a matrix that can contain a translation alongside an transformation, one can use a matrix that contains Homogeneous coordinates leading to the equation

$$\begin{align} 
\begin{bmatrix} p_1'\\
p_2' \\ 1
\end{bmatrix} =
\begin{bmatrix} a_{11} & a_{21}&$t_1\\
a_{21} & a_{22} & t_2 \\
0 & 0 &1 
\end{bmatrix} \begin{bmatrix} p_1\\
p_2 \\ 1
\end{bmatrix}
\end{align}$$

### Homogeneous coordinates

![[Homogenous Co-ords.png]]


### Rotation around a point

![[Rotation around a point.png]]