# Advanced Textures
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  10-10-2025
> > *Module :* [[Adv Graphics]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]


--- 
> [!danger]+ 🕰️* Speed run*
> Break down of topic 
> - p1
> - p2

---
## Texture Options

We COULD model a brick wall by simulating the bricks, or we could have one polygon and overlay a brick texture

| Option 1                                                                         | Option 2                                                                 |
| -------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Lighting + shading <br>Hundreds of polygons (brick/concrete) Different materials | Texture Mapping <br>Only 1 polygon, then copy the texture from a picture |

---
> [!example]+  ## Texturing a mesh
> > [!note]+ Procedural 
> > This can be done by a procedure e.g mapping. OR it can be done by cutting a mesh ( [https://hhoppe.com/tmpm.pdf](https://hhoppe.com/tmpm.pdf#:~:text=The%20method%20begins%20by%20partitioning%20the%20mesh%20into,simplifies%20the%20mesh%20while%20respecting%20the%20chart%20boundaries.) )
> > ![[Texture mapping.png|300]]
> > We can also use Procedures to create Pretty noise, e.g [Perlin noise](https://en.wikipedia.org/wiki/Perlin_noise)
> > ![[Pasted image 20251010113117.png|200]]
> 
> > [!danger]+ Manual BOOOOOOO
> ![[Manual texture.png|300]]

---


> [!Heart] Bump Mapping
> Very useful for creating illusion but not perfect, It can't distort shadows but it makes the polygon look sexy
> 
| Used to distort polygons to make an illusion of texturing<br>![[Pasted image 20251010114719.png\|200]]                                                                                                                   | ![[Pasted image 20251010114342.png\|200]] |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------- |
| **Height map**<br><br>Given a surface $𝑃(𝑢, 𝑣)$ and height map $𝑏(𝑢, 𝑣)$ So the perturbed surface is $$𝑃′ = 𝑃 + 𝑏 \frac{𝑛}{\|\|𝑛\|\|}$$ • The perturbed normal is $𝑛′$ from $𝑃′$, the surface is still $𝑃$ | ![[Pasted image 20251010114630.png\|200]] |
|                                                                                                                                                                                                                          |                                           |

## Displacement Map
This is commonly used when its close enough to see. BUT, its never bad to scimp when we can to reduce processing
![[Pasted image 20251010115008.png|400]]

---

## Compute buffers and shaders

Texture buffers don't have to just contain textures.
They can contain any data we wish.
We can do general compute on them.
We can also make them the target of the render instead of
the framebuffer.
- This is the basis of GPU compute.
- Newer APIs, e.g. Vulkan, generalise and introduce the idea of a compute shader.
