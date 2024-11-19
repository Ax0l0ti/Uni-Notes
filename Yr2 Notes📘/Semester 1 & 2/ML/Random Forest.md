# Random Forest
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  22-10-2024
> > *Module :* [[Machine Learning]]
> > *Teacher*: 
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
> > $a)$ - random forest = avg of randomly generated trees
> $b)$ - trees overfit, random avg doesn't, but is computationally inefficient
> $c)$ - 

---
### Creating a random tree

When creating a forest, one must first make a tree. This is done by fully dividing up a bootstrapped dataset via a decision tree. After creating many trees, an average of tree opinions can be used to guess the value based on other features.
#### Bootstrapped dataset

![[bootstrapping a dataset.png]]
### Creating a forest
![[Creating Random forest.png]]

> [!example] Pros & Cons of Random Trees
> Below are the advantages of disadvantages of random trees. Whilst simple, the randomness averages out but key details are lost like outliers and how results were gained.
>  
|         Advantages         |         Disadvantages          |
| :------------------------: | :----------------------------: |
| No complex hyperparameters |  Computationally Inefficient   |
|      Does not overfit      | Reliant on the number of trees |
| Not sensitive to outliers  |  Difficult to explain results  |
 