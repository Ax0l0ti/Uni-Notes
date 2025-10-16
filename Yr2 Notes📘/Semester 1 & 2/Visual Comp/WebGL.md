# WebGL
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  13-02-2025
> > *Module :* [[Yr2 Notes📘/Semester 1 & 2/Visual Comp/Visual Computing]]
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
> > $a)$ -  Web graphic library
> $b)$ - 
> $c)$ - 

---

#TODO 



> [!sigma] WebGL code looks like the below
>  WebGL code looks like the following below![[WebGL code.png|600]]


> [!leaf] Simple application
> below is a Basic three.js application for WebGL
> ``` js
var scene = new THREE.Scene();
var camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
var renderer = new THREE.WebGLRenderer(); renderer.setSize(window.innerWidth, window.innerHeight);
document.body.appendChild(renderer.domElement);
var geometry = new THREE.BoxGeometry(1, 1, 1);
var material = new THREE.MeshBasicMaterial({ color: 0x00ff00 });
var cube = new THREE.Mesh(geometry, material); scene.add(cube)
> ```
> ![[WebGL simple setup.png|300]]



### PLY mesh file format
this includes a file header that contains and sets the stucture

![[PLY FIle.png|400]]

### OBJ mesh file format


![[OBJ mesh file format.png|400]]