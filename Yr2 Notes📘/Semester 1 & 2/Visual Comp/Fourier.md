# Fourier
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  20-11-2024
> > *Module :* [[]]
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
> 
We change everything in the feature domain to avoid higher computation to do **mults** instead of **powers**

---

#TODO Search up 3blue1brown forier
[Topic: Lecture 7&8 Fourier Transform: Properties and Applications | CM22010 - Visual Computing | Home](https://moodle.bath.ac.uk/course/view.php?id=61733&section=9)

The Fourier transform enables us to observe the characteristics of the image and design the filter that would solve the problem 

This is similar to the way we used histogram equalization to get insights about the intensity domain and design a point filter

We change everything in the feature domain to avoid higher computation to do **mults** instead of **powers**

#### Definition and Formula

> [!heart]  Fourier
> The Fourier Transform of a continuous-time function $f(t)$ is defined as: $F(\omega) = \int_{-\infty}^{\infty} f(t) e^{-i\omega t} dt$ where:
> - $F(\omega)$ is the Fourier transform of $f(t)$
> - $\omega$ is the angular frequency
> - $i$ is the imaginary unit $( i^2 = -1 )$
> - $t$ is time
> 
> The inverse Fourier Transform, which converts the frequency-domain representation back into the time-domain, is given by: $f(t) = \frac{1}{2\pi} \int_{-\infty}^{\infty} F(\omega) e^{i\omega t} , d\omega$


> [!abstract]  Fourier Visualised
> As seen below, when shown in the signal domain, a multiplication of the original and filter creates a convoluted image as opposed to using the box filter on every single pixel
![[fourier km.png|600]]
