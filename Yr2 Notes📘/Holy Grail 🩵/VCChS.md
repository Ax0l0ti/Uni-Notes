# Visual Computing Cheat Sheet
---
> [!info]+ Module Details
> Includes information about (genus:: Cheat Sheet), link to CS module and it's correspondent attribute tag 
> *Module Tag :* (ModCode :: CM22010) 
> *Link :* [[Visual Computing]]
> *Cheat Sheet tag :* [[Grail 🩷]]

> [!abstract]+ Contents
> 
> > [[#🕰️ Speed run]]  
> > [[#Exam breakdown]]
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
# Exam breakdown

> [!danger]+ Exam
> 30/70 Sl/S2
> **14** Convolution and Filtering
> 2D Transformations and Image Warping
> **4**   Fourier Transforms
> **12** SIFT, 3D transformations, and curves
> **10** Optical Flow and Tracking
> **15** Graphics
> **30** Matching
> **15** Deep learning
**This course is assessed 60% by coursework (in three phases) and 40% by examination.**#

**10** Optical Flow and Tracking:
- Optical Flow, (Equations related to Motion Field, Computing Partial Derivatives are NOT required to be remembered)
- Tracking, (Equations related to Epanechnikov Kernel, Similarity metrics for Minimum Normalised Cross-Correlation are Not required to be remembered) 
**15** Graphics:
- Mesh, Lighting, Reflection, Ray-tracing,- Graphics pipeline, Vertex processing, Clipping, Rasterisation, Painter’s algorithm, The z-buffer algorithm,- Keyframe Animation, Motion Capture, Rigging
**30** Matching:
- template matching, (Equations related to Normalized Cross Correlation Function are Not required to be remembered)
- least square matching, (Equations related to least square line fitting are Not required to be remembered)
- Harris corner detector, descriptor,
- feature matching, RANSAC
- window-based matching, scanline stereo (Contents related to SGM are Not required to be remembered) 
**15** •Deep learning:
- forward propagation,
- back propagation, (Equations related to loss and loss minimisation are Not required to be remembered)
- fully connected network, 
- Convolutional neural network (Equations related to local contrast normalisation are Not required to be remembered)
- Recurrent neural network (Only concepts, no equations)


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
>     

> [!example]+ Low-Level Computer Vision
> 
> - **Edge Detection**: Finding areas of strong intensity change.
>     
> - **Harris Corner Detector**: Measures change of intensity in all directions.
>     
> - **SIFT**: Scale-Invariant Feature Transform for detecting and describing local features.
>     
> - **Gradient**: Rate of change of intensity.
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
    
- [Ray Tracing](https://en.wikipedia.org/wiki/Ray_tracing_\(graphics\))
    
- [Optical Flow](https://en.wikipedia.org/wiki/Optical_flow)
    
- [Panorama Stitching](https://en.wikipedia.org/wiki/Image_stitching)
    

---

# 🦜 Index of Key Terms

Basics, Colour Space, Display Devices, Video, Pinhole Camera, Lens, Projection, Calibration, Filtering, Convolution, Fourier Transform, Warping, Transformations, Mesh, Texture, Edge Detection, Harris Detector, SIFT, Gradient, Optical Flow, Lucas-Kanade, Stereo Matching, Ray Tracing, Visibility, Shading, Rasterization, Keyframes, Rigging, Motion Capture, Panorama Stitching, CNN, Forward Propagation, Backpropagation, ReLU

---

