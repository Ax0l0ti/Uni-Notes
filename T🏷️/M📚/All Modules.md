# All Modules
---

> [!info]+ Tag Details
> Includes information about this (genus:: Tag)
> > *Tag Purpose:*  Contains List of all Module links
> > *Content below*: Modules for year 1 & 2

---
## Year 1 Modules
```dataview
list 
WHERE genus = "Module" & file.name !="Module 📚" & Year = 1
```


Yr3 Notes 
	Holy Grail
	Semester 1
		Complexity
	Semester 1 & 2
		Adv Graphics
		Adv Vision
		Proj
		Reinforcement Learning
	Semester 2
		Business 

---
## Year 2 Modules
```dataview
list 
FROM ""
WHERE genus = "Module" & file.name !="Module 📚" & Year = 2

```


> [!example]+ Yr 2 Module Content
> ```dataview 
table
file.outlinks AS "Module Content" 
FROM ""
WHERE genus = "Module" & file.name !="Module 📚" & Year = 2  ```

---

# Year 3 Modules
```dataview
list 
WHERE genus = "Module" & file.name !="Module 📚" & Year = 3
```
