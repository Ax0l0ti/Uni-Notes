# CNN
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  28-10-2025
> > *Module :* [[Adv Vision]]
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
>  **History of CNNs**
> - IF $x$ is good, we want $y = f(x)$ to output $x$. 
> - By using $y = f(x) + x$, it is easier for $f(x)$ to tend to $0$ 
> - Stable Diffusion, DALL-E, Midjourney, they all use UNets
> 
> **Metric Learning**
> - positive p attracts anchor a, negative n repels a
> - margin m affects performance 
> 	- small may not learn a good separation
> 	- if too large, the model might not convergence.


---

## History of CNNs

LeNet (1989)
AlexNet (2012)
Inception (2014)
ResNet (2015)
IJNet (2015)

> [!example]+ A few notable CNNs
> > [!flower]- LeNet (1989)
> > CNNs existed, but kernels were hard-coded. Most researchers did not “move” the kernels around the image: kernels were fixed and their parameters were not shared
> > ![[LeNet.png]]
> 
> > [!note abstract tip info success failure todo heart flower sigma leaf omega help example quote warning danger bug]- AlexNet (2012) 
> > The first CNN to beat hand-crafted approaches (e.g. SIFT+SVM) on ImageNet by a large margin. Thanks to ImageNet itself and good techniques to prevent overfitting and speed-up training: dropout, ReLU, image augmentations.
> > ![[AlexNet.png]]
> 
> > [!quote]- Inception (2014)
> > Literally devised from Inception meme of lets go deeper
> > ![[Inception.png]]
> 
> 
> > [!help]- ResNet (2015)
> > In standard CNNs: y = f(x) If x is good, f(x) should output x (learn the identity), which is hard. 
> > In ResNet: y = f(x) + x It’s much easier for f to just output zero when x is good
> >  ![[ResNet.png]]
> 
> > [!success]- UNet (2015)
> > Instead of outputting a compressed vector UNet outputs an image of the same input resolution. Applications in image segmentation and generation: Stable Diffusion, DALL-E, Midjourney, they all use UNets
> > **Left = Contractive path, Right = Expansive path**
> > ![[UNets.png]]

## Metric Learning

> [!heart] Triplet Loss
> Given a triplet of (anchor, positive, negative) images, pull the positive to the anchor while pushing the negative from the anchor.
> $$\begin{align} 
> d(f(a) — d(p)) + m < d(f(a) — d(n)) \\ 
> \text{This transfers into a loss function of }\\
> L = max( d( f(a) – d(p)) - d( f(a) – d(n)) + m, 0) \end{align}$$
> 
> > [!danger]- graphical
> > This maximises the orange margin in the graph below. To increase the speed of learning, sampling hard negatives and semi hard negatives guarantees success on easier negatives
> > ![[Triplet Loss.png|200]]
> 
> We can sample triplets offline or online: 
> - Offline: we form triplets at the beginning of a training epoch. Impractical with large datasets, slow updates. 
> - Online: we form triplets in a given batch during training. More efficient, but needs large batches.
> 
> > [!NOTE] Powerful, but often tricky because it needs: 
> > Margin tuning (L2 normalisation helps) 
> > Careful triplets mining (e.g. online semi-hard) 
> > Large and diverse datasets (data augmentation helps) 
> > A sufficiently complex model 
> > A simple classifier can still outperform a triplet model because classification is an easier optimisation problem


![[triplet loss vs Classification.png]]