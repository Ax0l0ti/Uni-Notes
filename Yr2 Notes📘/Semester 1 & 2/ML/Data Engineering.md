# Data Engineering
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  24-10-2024
> > *Module :* [[]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Feature Selection]]
> [[#Model Considerations]]
> [[#Handling Categorical Features]]
> [[#Data Scaling]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  
> $b)$ - 
> $c)$ - 

---

$$𝑿′ = \frac{𝑿−min(𝑿)}{max 𝑿 −min(𝑿)}$$
### Feature Selection 

> [!warning] GIGO 
> If you put **Garbage In**, expect **Garbage Out** 
> Select what data and features you use carefully
> > [!abstract] Causation vs correlation
> > It's easier to prove correlation but much harder to prove causation

Sometime you might have to Combine features
e.g Features **Area $m^2$** + **House Price** ==create== **price per $m^2$**
on the flip side
Sometimes its better the remove features that are redundant copies

### Model Considerations 

![[Model Considerations.png]]

### Handling Categorical Features 

there are many ways of handling categorical such as ordinal handling, one got encoding and bins
Ordinal handling is taking categoricals and placing them in an ordinal order e.g not good -> okay -> good -> very good. 

> [!tip] One Hot encoding
> One hot encoding is creating a binary feature for the presence of each category
> ![[One hot encoding.png|500]]

>[!example] Bins
> Creating bins is used to collect a range of values into one feature
> E.g collecting **age** into **Child, Young Adult** and **Adult**


### Data Scaling

There are two ways to scale the data: 
• **Normalization** 
• **Standardization**

![[Data Normalisation.png]]

![[Data Standardisation.png]]