# Meshes
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  06-10-2025
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
> - **Perlin noise**: [Perlin noise - Wikipedia](https://en.wikipedia.org/wiki/Perlin_noise) (used in minecraft for texture)
> - **Bump Mapping**: like texture mapping but overlays mesh to create illusion of complex geometry
> 	- Most common is height map  
> - **Reflection Maps**: R assume small obj comapred to distance, hence can use refl vector from obj centre, not face
> - **Shadow Map**: We hold a depth map from light source to tell if light is blocked and obj in shadow

---

#oldTODO
Meshes 
• Structure 
• Sourcing Meshes 
• Construction 
•Scanning 
• Subdivision 
• CSG 
• File example 
• OBJ Files 
• Rendering 
• Triangles 
• Barycentric Coordinates
## Meshes 

𝑀 = (𝑉, 𝐸, 𝐹) 𝑉: 𝑚𝑒𝑠ℎ 𝑣𝑒𝑟𝑡𝑒𝑥 𝑠𝑒𝑡 E: 𝑚𝑒𝑠ℎ 𝑒𝑑𝑔𝑒 𝑠𝑒𝑡 𝐹: 𝑚𝑒𝑠ℎ 𝑓𝑎𝑐𝑒 𝑠𝑒𝑡 We may not store the edges unless we have a specific need for them.

## Subdivision




> [!important] Subdivision
> recursively smoothing a mesh means we need to store less and can smooth a surface till required level 
> > [!example]- Chaikin’s Subdivision Method in 2D
>  > ![[Chaikins 2D subdivision.png|500]]
> 
>  > [!omega]- Doo Sabin
>  > [Doo–Sabin subdivision surface - Wikipedia](https://en.wikipedia.org/wiki/Doo%E2%80%93Sabin_subdivision_surface)
>  > Doo Sabin works by 
>  > ![[Pasted image 20251006175011.png|300]]
>  > 
>  
>  Alongside others e.g [Catmull–Clark subdivision surface - Wikipedia](https://en.wikipedia.org/wiki/Catmull%E2%80%93Clark_subdivision_surface) which i have coded



> [!note abstract tip info success failure todo heart flower sigma leaf omega help example quote warning danger bug] Constructive Solid Geometry
> Use Boolean operations to combine simple building block shapes. 
>
| • Union • $𝐹𝑐∪𝑆 . =min{𝐹𝑐(.),𝐹𝑆(.)}$<br><br><br>• Intersection • $𝐹𝑐∪𝑆 . =m𝑎𝑥{𝐹𝑐(.),𝐹𝑆(.)}$<br><br><br>• Difference • $𝐹𝑐∪𝑆 . =max{−𝐹𝑐(.),𝐹𝑆(.)}$ | <br>![[Pasted image 20251006174111.png\|200]] |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- | 
> 
> > [!heart]- Examples of CSG Heirachies
> > This can be combined with trees to produce the following examples
>  > ![[Pasted image 20251006174412.png]]



[**Barycentric coordinates** are a system of coordinates used in geometry to specify the location of a point relative to the vertices of a triangle](https://www.bing.com/ck/a?!&&p=4fc09e03fb57f1a039957d368be162dc2f6975c0b71e5a74a79ec522b0121813JmltdHM9MTc1OTcwODgwMA&ptn=3&ver=2&hsh=4&fclid=14cee7c4-78da-6654-06f2-f44979ad6754&psq=Barycentric+Coordinate&u=a1aHR0cHM6Ly9tYXRod29ybGQud29sZnJhbS5jb20vQmFyeWNlbnRyaWNDb29yZGluYXRlcy5odG1s&ntb=1)