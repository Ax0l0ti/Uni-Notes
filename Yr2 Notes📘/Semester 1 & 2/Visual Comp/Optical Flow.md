# Optical Flow
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  03-02-2025
> > *Module :* [[Visual Computing]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Motion Field and Optical Flow]]
> [[#Optical Flow Constraint Equation]]
> [[#Lucas-Kanade Method]]
> [[#Coarse-to-Fine Flow Estimation]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  WHY? used in mice to tell movement
> $b)$ - Texture is good for calculations,  optical flow = motion flow
> $c)$ - sampling lines is bad, optical flow might not equal motion flow
> $d)$ - blur is used to texture lines.
> Coarse to fine estimation
> - calc optical flow
> - warp image and calculate differrence between next frame, warped and og


---

#TODO 
## Motion Field and Optical Flow 

Motion Field vs optical flow. 
motion field is the movement of an object between frames
Optical flow is the apparent movement of an object between frames

We **WANT** Optical flow = motion Field but sadly this doesn't always happen

> [!leaf]+  Examples where not
> Examples are spinning spheres and illusions e.g leaves or barber shop poles
> ![[Pasted image 20250203114008.png|300]]

> [!help]+  Motion Fields 
> Used to find the difference between 2 frames by using perspective projection to relate seen velocity and actual velocity.
> This is done by taking projected distance along sensor taken from pinhole camera 
>  ![[Motion Field.png|600]]

> [!flower]+  Optical flow
> Optical flow is the apparent change in the view 
![[Optical Flow.png|600]]


## Optical Flow Constraint Equation 


> [!info] ASSUMPTIONS
> 1. Brightness of an image point remains constant over time
> ![[Pasted image 20250203114324.png|400]]
> 1. Displacement $(\delta x,\delta y)$
> ![[Pasted image 20250203114345.png|400]]


> [!example] All blocks
> ![[Pasted image 20250203114239.png|600]]



#### Geometric interpretation


> [!note abstract tip info success failure todo heart flower sigma leaf omega help example quote warning danger bug] All blocks
> The symbol contains everything and defaults to note
> ![[Geometrc interpretation Optic flow.png]]


Normal Flow vs Parallel Flow

![[Normal flow.png]]
## Lucas-Kanade Method 

> [!sigma] Lucas-Kanade Method 
> ![[Lucas-Kanade.png]]



## Coarse-to-Fine Flow Estimation

![[Coarse-to-fine.png]]