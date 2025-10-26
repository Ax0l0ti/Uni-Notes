# Global Lighting
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  15-10-2025
> > *Module :* [[Adv Graphics]]
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
> 1. Global lighting effects,
> 2. Shadows
> 3. Ambient light contribution,
> 4. Diffuse and specular light terms,
> 5. Lambertian reflection model,
> 6. Dot product calculations for lighting,
> 7. Reflection and glossy surfaces,
> 8. Reflection direction and ray tracing,
> 9. Fresnel equations for refraction,
> 10. Snell's law and angle calculations,
> 11. Total internal reflection considerations,
> 12. Shadow handling in ray tracing,
> 13. Recursive definitions and stopping conditions,
> 14. Visual effects in ray tracing,
> 15. Practical ray tracing examples and rendering,

---

#TODO 

1. Global lighting effects,
2. Local lighting recap,
Surface model
Ambient
general light in a scene. The reason shadows and under table has light & colour
Directional lights
from a source
Diffuse / Lambertian 
https://youtu.be/HPNW0we-ft0?si=a-ERiKG2tx9FqYL5
![[Pasted image 20251020144702.png|300]]
Specular
[Reflection from Rough Surfaces | Radiometry and Reflectance](https://www.youtube.com/watch?v=oa3Yo7Ro02A)

![[Pasted image 20251017113928.png]]

3. Shadow calculations in ray tracing,
4. Shadow rays and intersection tests,
5. Ambient light contribution,
Reason why under the table has light

6. Diffuse and specular light terms,
Specular is mirror, inifintely far light source
Diffuse is light diffuses OBVIOUSLLY
7. Lambertian reflection model
$𝐼 =𝐼_𝑖𝑘_𝑑 (𝑁.𝐿)$ $𝐼_𝑖$ is the diffuse intensity of the light $i$. 
$𝑘_𝑑$ is the diffuse co-efficient of the object surface. 
𝑁 is the normal of the object surface. 
𝐿 is the direction towards the light.

8. Dot product calculations for lighting,
9. Reflection and glossy surfaces,
10. Specular reflection calculations,
11. Reflection direction and ray tracing,
12. Recursive ray tracing for reflections,
13. Fresnel equations for refraction,
14. Snell's law and angle calculations,
15. Total internal reflection considerations,
16. Shadow handling in ray tracing,
17. Recursive definitions and stopping conditions,
18. Visual effects in ray tracing,
19. Practical ray tracing examples and rendering,
20. CM5 coursework preparation details


![[graphics lab struct.png]]



## Radiosity

• It relies on the principle that light as energy is conserved. 
• That light leaving one surface must arrive at another.

$𝐵_𝑖=𝐸_𝑖+𝑅_𝑖\sum{𝐵_𝑗𝐹_{𝑗𝑖}}$
$𝐸_𝑖$ is the energy emitted by the surface. 
$𝑅_𝑖$ is the reflection coefficient of the surface ($k_d$) 
$𝐹_{𝑗𝑖}$ is the fraction of the energy from patch 𝑗 that falls on patch 𝑖.

Hemi Cube
