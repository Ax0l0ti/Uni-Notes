# Noise
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  17-10-2024
> > *Module :* [[Visual Computing]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Types of Noise]]
> [[Image Dehazing]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  4 types of noise, Thermal, Shot, Replacement and Speckle

---
## Types of Noise

| Types of noise | definition                                                                                                                                                                                      | Example                   |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| Thermal        | Also called ”Additive Gaussian Noise”<br>Often due to random fluctuations of electrons when photo sensor is amplified.<br>Highly related to ISO level<br>Apply Gaussian Noise to simulate       | ![[Thermal Noise Ex.png]] |
| Shot           | Also called ”Poisson Noise”<br>highly related to photodiode of which the signal strength is proportional to the number of photons that hits the sensor.<br>The photons hits the sensor randomly | ![[Shot Noise Ex.png]]    |
| Replacement    | Also called ”Salt&Pepper Noise”<br> ’Dead pixels’- dark<br>‘Hot pixels’- over bright                                                                                                            | ![[S&P Noise Ex.png]]     |
| Speckle        | Subjective speckles <br>Objective speckles <br>Commonly happen in medical image, Radar, etc                                                                                                     |                           |

## Image Dehazing

### 1. **Image Denoising**

**Purpose:**  
Image denoising aims to remove unwanted noise from an image, which can be caused by low light, high ISO settings on cameras, or transmission errors. Noise manifests as random variations in brightness or color.

**How it is done:**  
Several methods are used to denoise an image, depending on the type of noise (e.g., Gaussian noise, salt-and-pepper noise):

- **Gaussian Filter**: Smoothens the image by averaging nearby pixel values, but it can blur fine details.
- **Median Filter**: Effective for removing salt-and-pepper noise by replacing a pixel’s value with the median of neighboring values.
- **Non-Local Means (NLM)**: More advanced, NLM uses the similarity of patches within the image to reduce noise, preserving edges and textures.
- **Deep Learning-Based Denoising (Denoising Autoencoders)**: Neural networks are trained on noisy and clean images to learn how to remove noise while preserving details.

---

### 2. **Image Deblurring**

**Purpose:**  
Deblurring aims to reverse the blurring effect caused by motion, defocus, or camera shake, restoring sharpness and clarity.

**How it is done:**  
Deblurring is typically more challenging because it involves inverting the blurring process:

- **Wiener Filter**: Based on linear filtering techniques, it works well when the blur function (Point Spread Function, PSF) is known.
- **Blind Deconvolution**: In cases where the blur function is unknown, blind deconvolution algorithms estimate the blur and then try to recover the image. This often involves iterative methods and optimization techniques.
- **Deep Learning**: Convolutional neural networks (CNNs) are trained to recognize and undo specific types of blur in images by learning from large datasets.

---

### 3. **Super-Resolution (SR)**

**Purpose:**  
Super-resolution enhances the resolution of an image, reconstructing a higher-resolution image from one or multiple low-resolution inputs.

**How it is done:**  
There are two primary methods:

- **Single-Image Super-Resolution (SISR)**: Algorithms upscale a single image using:
    - **Interpolation (Bicubic, Bilinear)**: These are simple techniques that estimate the missing pixel values when enlarging an image, but they often lead to a blurry result.
    - **SRGAN (Super-Resolution Generative Adversarial Network)**: A deep learning-based approach where the model learns how to generate high-resolution images from low-resolution inputs by leveraging adversarial training.
    - **SRCNN (Super-Resolution Convolutional Neural Network)**: An end-to-end deep learning model that learns the mapping between low-resolution and high-resolution images.
- **Multi-Image Super-Resolution (MISR)**: Uses multiple images (slightly different versions of the same scene) to reconstruct a higher-resolution image. This approach uses information from multiple viewpoints or frames to improve resolution.

---

### 4. **Dehazing**

**Purpose:**  
Dehazing is the process of removing the effects of haze, fog, or other atmospheric conditions that reduce visibility in images. Hazy images tend to have reduced contrast and a washed-out appearance.

**How it is done:**  
The challenge is estimating how much haze is present and removing it:

- **Dark Channel Prior**: This is one of the most well-known methods. It assumes that in non-hazy areas, some pixels have very low intensity in at least one color channel. Using this prior, the algorithm estimates the haze transmission map and removes the haze.
- **Retinex Theory**: Based on the idea that the perceived color of an object is not affected by the surrounding light, Retinex-based methods enhance contrast and remove haze.
- **Deep Learning (DehazeNet)**: Trained on pairs of hazy and clear images, a CNN can learn to estimate the haze density and remove it from images.

---

### 5. **Deraining**

**Purpose:**  
Deraining is designed to remove rain streaks from images or videos to make them clearer. Rain can obscure important details and negatively affect image quality.

**How it is done:**

- **Dictionary Learning**: Rain streaks have specific directional and shape characteristics, so traditional methods use sparse representation to separate rain streaks from background details.
- **Guided Filtering**: This technique relies on identifying and preserving edges while removing directional noise like rain streaks.
- **Deep Learning (ResNet for Deraining)**: Neural networks, particularly residual networks (ResNet), can learn the pattern of rain streaks and remove them, leaving the background intact.

---

### Summary of Techniques:

- **Image Denoising**: Gaussian Filter, Median Filter, Non-Local Means, Denoising Autoencoders.
- **Image Deblurring**: Wiener Filter, Blind Deconvolution, Deep Learning (CNNs).
- **Super-Resolution**: Interpolation (Bicubic), SRGAN, SRCNN, Multi-Image Super-Resolution.
- **Dehazing**: Dark Channel Prior, Retinex, DehazeNet (deep learning).
- **Deraining**: Dictionary Learning, Guided Filtering, ResNet for Deraining.