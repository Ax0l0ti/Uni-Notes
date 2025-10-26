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
> #todo at the end of the term

### **Words to add** 
Barycentric Coordinates
OBJ


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

> [!example]+ Light & Shadow
> > [!d]- Light
> > **Ambient Light**: Why under the table is not pitch black. Light Diffuses $𝐼 =𝐼_𝑎𝑘_𝑎 +\sum{𝐼_𝑥(𝑘_𝑑 𝑁.𝐿 +𝑘_𝑠(𝑅.𝑉)^𝑛)}$
> > - $k_a$ ambient reflection co-efficient, $I_a$ intensity
> >
> > **Specular**: perfect reflective [Global Lighting], Reflection $R = I - 2.0 * (I.N) * N$ 
> > **Diffusion Mode**l: Dull matte 
> > **Glossy**: balance between Spec and Diff
> > **Translucence**: By firing Transmission rays though an object, we can create translucents via Super Sampling
> > **Pre-baked Lighting**: 
> > **Radiosity**: 
> > • Primary rays – from the eye into the scene. 
> > • Shadow rays – from an object to a light.
> > 
> > 
> 
> > [!omega]- Shadow & Shade
> > Shadows are vital to a realistic scene, but is costly to do realistically. To find, work out if light intersection hits other obj
> > **Z buffer** 
> > **Depth Buffer**
> > **Shadow Mapping**
> > **Phong**: Approximation of Micro Facets
> > **Cook-Torrance/BRDF**

> [!Examples] Meshes
> - **Mesh**
> **- Tesselation**
> - **Perlin noise**: [Perlin noise - Wikipedia](https://en.wikipedia.org/wiki/Perlin_noise) (used in minecraft for texture)
> - **Bump Mapping**: like texture mapping but overlays mesh to create illusion of complex geometry
> 	- Most common is height map  
> - **Reflection Maps**: R assume small obj comapred to distance, hence can use refl vector from obj centre, not face
> - **Shadow Map**: We hold a depth map from light source to tell if light is blocked and obj in shadow

> [!quote] Modelling
> **Implicit Surfaces**
> **Parametric Surfaces**
> **Procedural Geometry**
> **Constructive Solid Geometry**
> **Mesh Decimation**

> [!example] Rendering
> **Rendering Equation**
> **BRDFs**
> **Global Illumination**
> **Advanced Textures**
> **Non-Photorealistic Rendering**
> **Photon-mapping**
> **Volume Rendering**
> **Tone Mapping**
> 
> > [!NOTE]- Quality
> > Ray tracing
> > Ray Casting
> > Super Sampling Anti-Aliasing 
> > Anti-Aliasing 

---

> [!bug] Animation
> **Blendshape Models**
> **Kinematics**
> **Skeletons & Bones**
> **Skinning**
> **Motion Capture**
> **Retargeting**
> **Simulation**

> [!NOTE]+ Pipeline
> **GPUs**
> **Graphics Pipeline**
> **Rasterisation**
> **Deferred Shading**
> **Clipping**
> **Vertex Processing**
> **Frame Buffer**
> **Post-Processing**

> [!Heart] Machine Learning for Graphics
> **Generative Models**
> **Differentiable Rendering**
> **Inverse Rendering**
> **Adaptive Tools**
> **Just-in-Time Rendering**
> **Denoising**

> [!leaf]- Vectors & Intersections
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
[[Grail 🩷]]
