# Visual Computing Sexy Key Terms

---

> [!info]+ File Details
> 
> > **Date:** 26-04-2025  
> > **Module:** [[Yr2 Notes📘/Semester 1 & 2/Visual Comp/Visual Computing]]  
> > **Teacher:** #Chatted  
> > **Resources:** Lecture notes, coursework

---

> [!abstract]+ Contents
> 
> > [[#🕰️ Speed run]]  
> > [[#🔢 Definitions by Topic]]

---

> [!danger]+ _🕰️ Speed run_
> 
> - **Basics**: Colour spaces, Imaging systems, Displays, Videos
>     
> - **Image Formation**: Pinhole cameras, Lenses, Calibration, Projection
>     
> - **Image Processing**: Filtering, Convolution, Fourier Transforms, Warping
>     
> - **Modelling**: 2D/3D Transformations, Surfaces, Meshes, Textures
>     
> - **Low-Level Vision**: Edges, Corners, Harris Detector, SIFT
>     
> - **Mid-Level Vision**: Optical Flow, Tracking, Stereo Matching
>     
> - **Rendering**: Ray Tracing, Lighting Models, Shading, Rasterization
>     
> - **Animation**: Motion Capture, Keyframes, Rigging
>     
> - **Deep Learning**: CNNs, Feature Extraction, Backpropagation
>     
> - **Panorama Stitching**: Features, Matching, Alignment, Blending
>     

---

# 🔢 Definitions by Topic

> [!tip]+ Basics
> 
> - **Image**: A 2D array of intensity or color values.
>     
> - **Colour Space**: Models like RGB (additive) or CMYK (subtractive) that represent color numerically.
>     
> - **Display Devices**: Technologies like LCD, OLED for rendering images.
>     
> - **Video**: Sequence of frames over time, typically 24-60 fps.
>     

> [!tip]+ Image Formation
> 
> - **Pinhole Camera Model**: Light passes through a small hole projecting an inverted image onto a surface.
>     
> - **Lens**: Focuses light onto a sensor, affecting field of view and focus.
>     
> - **Projection**: Transformation from 3D world coordinates to 2D image plane.
>     
> - **Calibration**: Process of estimating camera parameters.
>     

> [!info]+ Image Processing
> 
> - **Filtering**: Enhancing or suppressing parts of an image.
>     
> - **Convolution**: Sliding a kernel over an image and computing weighted sums.
>     
> - **Fourier Transform**: Converts spatial domain information into frequency domain.
>     
> 
> $$\mathcal{F}(u,v) = \sum_x \sum_y f(x,y) e^{-j2\pi (ux/M + vy/N)}$$
> - **Warping**: Spatially transforming an image.
>     

> [!success]+ Modelling
> 
> - **2D Transformations**: Scaling, rotation, translation in 2D plane.
>     
> - **3D Transformations**: Use of homogeneous coordinates to handle translation and rotation.
>     
> - **Meshes**: Collections of vertices, edges, and faces representing 3D shapes.
>     
> - **Textures**: 2D images wrapped onto 3D surfaces.


![[Graphics Pipeline.png]]

> [!example]+ Low-Level Computer Vision
> 
> - **Edge Detection**: Finding areas of strong intensity change.
>     
> - **Harris Corner Detector**: Measures change of intensity in all directions.
>     
> - **SIFT**: Scale-Invariant Feature Transform for detecting and describing local features.
> - Scale, Rotation and Illumination Resistance 
> - Robust to Noise 
> - varying levels of $\sigma$ gaussian blur, uses local neighbourhood gradients to assign object vectors
>     

> [!example]+ Mid-Level Computer Vision
> 
> - **Optical Flow**: Apparent motion of brightness patterns in an image sequence.
>     
> - **Lucas-Kanade Method**: Assumes constant motion within a small window.
>     
> - **Stereo Matching**: Finding correspondences between two views to infer depth.
>     
> - **Sum of Absolute Differences (SAD)**: Metric for block matching.
>     

> [!bug]+ Rendering
> 
> - **Ray Tracing**: Simulates light transport by tracing paths of rays.
>     
> - **Visibility**: Determining which surfaces are visible to the camera.
>     
> - **Shading**: Calculating surface color based on lighting models.
>     
> - **Rasterization**: Converting 3D primitives into 2D pixel representations.
>     

> [!warning]+ Animation and Interaction
> 
> - **Keyframes**: Essential poses in an animation.
>     
> - **Rigging**: Skeleton structure allowing deformation and animation.
>     
> - **Motion Capture**: Capturing real-world motion data.
>     

> [!leaf]+ Panorama Stitching
> 
> - **Feature Matching**: Finding correspondences (e.g., SIFT, SURF).
>     
> - **Alignment**: Transforming images to match overlapping regions.
>     
> - **Blending**: Smoothing transitions between stitched images.
>     

> [!heart]+ Deep Learning
> 
> - **CNNs**: Convolutional Neural Networks for feature extraction and classification.
>     
> - **Forward Propagation**: Computing outputs from inputs.
>     
> - **Backpropagation**: Updating weights using gradient descent.
>     
> 
> Weight Update: $w \leftarrow w - \eta \frac{\partial L}{\partial w}$
> 
> - **ReLU Activation**: $f(x) = \max(0,x)$
>     

---

# 🔍 Quick Links to Complex Topics

- [Convolutional Neural Networks (CNNs)](https://en.wikipedia.org/wiki/Convolutional_neural_network)
    
- [SIFT (Scale-Invariant Feature Transform)](https://en.wikipedia.org/wiki/Scale-invariant_feature_transform)
    
- [RANSAC (Random Sample Consensus)](https://en.wikipedia.org/wiki/Random_sample_consensus)
    
- [Fourier Transform in Images](https://en.wikipedia.org/wiki/Fourier_transform)
    
- [Ray Tracing]([Ray tracing (graphics) - Wikipedia](https://en.wikipedia.org/wiki/Ray_tracing_\(graphics\)))
    
- [Optical Flow](https://en.wikipedia.org/wiki/Optical_flow)
    
- [Panorama Stitching](https://en.wikipedia.org/wiki/Image_stitching)
    

---

# 🦜 Index of Key Terms

Basics, Colour Space, Display Devices, Video, Pinhole Camera, Lens, Projection, Calibration, Filtering, Convolution, Fourier Transform, Warping, Transformations, Mesh, Texture, Edge Detection, Harris Detector, SIFT, Gradient, Optical Flow, Lucas-Kanade, Stereo Matching, Ray Tracing, Visibility, Shading, Rasterization, Keyframes, Rigging, Motion Capture, Panorama Stitching, CNN, Forward Propagation, Backpropagation, ReLU

---

