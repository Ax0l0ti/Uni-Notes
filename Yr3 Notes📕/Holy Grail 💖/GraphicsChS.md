# Advanced Graphics Cheat Sheet
---
> [!info]+ Module Details
> Includes information about (genus:: Cheat Sheet) from [Year::3]. Links to Module Note and its correspondent attribute tag 
> *Module Tag :* [[Adv Graphics]]
> *Link :* [[Adv Graphics]]
> *Cheat Sheet tag :* [[Grail 🩷]]
> 

> [!abstract]+ Contents
> 
> > [[#🕰️ Speed run]]  
> > [[#Exam breakdown]]
> > [[#🧠 Definitions by Topic]]

---
> [!danger]+ _🕰️ Speed run_
> 
> - **Rasterisation Pipeline**: stages and functions
> - **Ray Tracing**: algorithms and acceleration structures
> - **Lighting Models**: Phong, Blinn-Phong, PBR

---
# Exam breakdown

> [!danger]+ Exam
> Exam details when given
> 
> > [!heart]+ Structure Overview
> > Combination of theory questions and implementation tasks
> 
> > [!omega]+ KEY NOTE
> > Focus on diagrams and pseudo-code clarity

---
# 🧠 Definitions by Topic

> [!note]+ Rasterisation
> - **Definition**: Conversion of 3D primitives to 2D pixels

> [!note]+ Ray Tracing
> - **Definition**: Simulates light paths for realistic rendering


> [!Examples] Meshes
> - **Perlin noise**: [Perlin noise - Wikipedia](https://en.wikipedia.org/wiki/Perlin_noise) (used in minecraft for texture)
> - **Bump Mapping**: like texture mapping but overlays mesh to create illusion of complex geometry
> 	- Most common is height map  
> - **Reflection Maps**: R assume small obj comapred to distance, hence can use refl vector from obj centre, not face
> - **Shadow Map**: We hold a depth map from light source to tell if light is blocked and obj in shadow


> [!leaf]+ Vectors & Intersections
> - For finding if a ray intersects a sphere 
>$$\begin{align}  
\text{ for sphere X Y Z, R, substitute Ray =} P_{XY or Z} + tD_{XY or Z} \\\\
(Px + t * Dx)2 + (Py + t * Dy)2 + (Pz + t * Dz)2 – R2 = 0 \\ 
\text{expand out and then group like below} = 0\\ 
(Dx2+Dy2+Dz2) *t2 + (Dx*Px + Dy*Py+ Dz*Pz)*2t + (Px2 + Py2 + Pz2 – R2) = 0 \\ 
(D.D) * t2 + (D.P) * 2t + (P.P – R2) = 0 \\
\text{anything dotted w itself = its length squared (think pythag } a^2+b^2=c^2\text{) so D.D = 1}
\end{align}$$
> Short form is $b^2 -4ac$ = $(2(D.P))^2 - 4(P.P – R2)$
> - For finding if a ray intersects a plane 
> $$\begin{align}  
  ax+by+cz+d = 0, a^2+b^2 +c^2 = 1, [a, b, c] = Normal N \\
  \text{Ray =} P_{XY or Z} + tD_{XY or Z} \\
  t = -\frac{N.P + d}{N.D} \end{align}$$



---
#TODO
[[Grail 🩷]]


Words to add 
Barycentric Coordinates
OBJ