# Image Dehazing Method
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  28-10-2024
> > *Module :* [[]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Dark Channel]]
> [[#Transmission Maps]]
> [[#Resultant method for Dehaze]]

---
### Definition

> [!NOTE] Definition
> Dehazing is the process of improving image quality by removing haze to crystalise an image 

> [!Info] Dehazing Summary
> a brief summary is as followed
> ![[Dehazing Summary.png|600]]


#TODO 

### Dark Channel 

Dark Channel Computation– basically brighter misty areas will have higher avg for $I^c$, this leads to $I_{dark}$ to be higher around haze

![[Pasted image 20241120132642.png]]

### Transmission Maps

> [!quote] Trasmission Maps
> Dark Channel Computation– high $I_{dark}$ around haze leads to darkness around haze in the transmission
> ![[Transmission Maps.png]]

### Resultant method for Dehaze

> [!NOTE] Dehaze Image Equation
> This works by dividing the difference between the avg brightness and the original hazy image to scale the change from the avg. This leads to the hazed areas having much larger changes due to low $t(x)$ and near to no change around areas that have a a distinguished colour aka non hazed areas
> ![[Dehaze Image Equation.png]]
