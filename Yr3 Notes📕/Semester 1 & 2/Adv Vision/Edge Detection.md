# Edge Detection
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  07-10-2025
> > *Module :* [[Adv Vision]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Edges]]


--- 
> [!danger]+ 🕰️* Speed run*
> Break down of topic 
> - Edges caused by Discontinuity in Surface normal, Depth, Colour, Illumination
> - Smoothing filters
>  Gaussian removes "high freq" - "low pass" filter

---

## Edges

Edges can be caused by numerous factors,
- Surface normal Discontinuity ()
- Depth Discontinuity (Shape w varying depth)
- Surface Colour Discontinuity (Different colours)
- Illumination Discontinuity (Shadow edge)

Edges give value and info 
This is great for **Recognising Objects** and calculating **3D Shape & Geometry**


> [!NOTE]+ How are they characterised? 
> Edges can be defined as a rapid change in image intensity.
> 
> ![[Edge Characterisation.png|600]]


> [!error]+ PROBLEM, Noise
> Noise massively impacts this gradient when looking at the intensity change across an image
> We can define these Intensities as seen below $$\Delta I(x, y)= \frac{\delta I(x,y)}{\delta x} \frac{\delta I(x,y)}{\delta y}$$
> AN example of how the noise affects can be seen below
> ![[noise on Intensity gradient.png|300]]
> > [!Success]- Solution
> > By using a Gaussian Smoothing Filter can be used to map a Signal of the original image via a convolution to make $f \times g$ 
> > ![[Gaussian Smoothing Filter.png|400]]
> > BUT this is very expensive. To compensate, we can use the derivative of gaussian to do the removal of noise and use derivative to find the edge **together**


--- 
# Canny Edge Detection 
[Canny edge detector - Wikipedia](https://en.wikipedia.org/wiki/Canny_edge_detector)


> [!heartt] Canny's Proposal
> Canny proposed a set of properties that an edge detector must satisfy 
> • Good detection - The filter must have a stronger response at the edge location than to noise 
> • Good localisation – The filter response must be maximum very close to true edge location 
> • Low false positives - There should be only one maximum in a reasonable neighbourhood of the edge location


## Process

The process of Canny edge detection algorithm can be broken down to five different steps:

1. Apply [Gaussian filter](https://en.wikipedia.org/wiki/Gaussian_filter "Gaussian filter") to smooth the image in order to remove the noise
2.  Compute “robust” gradient of the image
3. Apply gradient magnitude thresholding or lower bound cut-off suppression to get rid of spurious response to edge detection
4. Apply **Non-Maximum Suppression** for “edge-thinning” Keep largest edge (i.e. local maxima in a neighborhood) across gradient direction, suppress the rest 
![[Non-Maximum Suppression.png|300]]
5. **“[hysteresis](https://en.wikipedia.org/wiki/Hysteresis "Hysteresis") thresholding”** to discard non-connected components • Define two thresholds: T-high and T-low • ‘Track’ a strong ed

