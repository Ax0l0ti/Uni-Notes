# Machine Learning Cheat Sheet
---
> [!info]+ Module Details
> Includes information about (genus:: Cheat Sheet), link to CS module and it's correspondent attribute tag 
> *Module Tag :* (ModCode :: CM22009) 
> *Link :* [[ML]]
> *Cheat Sheet tag :* [[Grail 🩷]]
> 

---

![[ML Semester 1 Speed Run.png]]
### Equations and phrases
**Structure :** (Topic) Phrase

Gen Model built of **Prior** $p(c|\theta) = \pi$ and **Noise Model** 
#### Phrases

#### Equations

---


---

## Vectors

### General Properties
Orthogonal = $B B^\top = I$ 
- $\text{Rank} = \text{number of independent columns/rows}$
- $Rank \leq \text{min}(\text{rows}, \text{cols})$

### Covariance Matrix

- **Symmetric**:
    - Variance = Diagonal elements
    - Covariance = Off-diagonal elements
- Used in **Principal Component Analysis (PCA)**:
    - Analyse data in axes of maximal variance.
    - Dimension reducing:
        - Rotate data to align with eigenvectors.

---

## Dimension Reducing

### Principal Component Analysis (PCA)

1. Center data:  
    $B = X - \bar{X}$
2. Compute covariance matrix:  
    $E = \frac{1}{n-1} BB^\top$
3. Decompose covariance matrix:  
    $S = U \Lambda U^\top$
    - $UU$: Eigenvectors
    - $\Lambda$: Diagonal matrix of eigenvalues
4. Reduce dimensions:
    - Sort eigenvalues in descending order.
    - Choose top kk eigenvectors corresponding to the largest eigenvalues.

### Singular Value Decomposition (SVD)

- Decomposes XX into:  
    $X = U \Sigma V^\top$
    
    - $UU$: Orthogonal matrix
    - $\Sigma$: Diagonal matrix (singular values)
    - $V^\top$: Orthogonal matrix
- Applications:
    
    - Compression
    - Feature selection

> [!NOTE] Whitening  
> Transform data to ensure uncorrelated features:  
> $P = B V^\top$
> [[]]


---

## Clustering

### K-Means Clustering

> [!NOTE] Steps for K-Means
> 
> 1. Choose $k$.
> 2. Initialize kk centroids.
> 3. Assign each point to the closest centroid group.
> 4. Calculate the new center of each cluster.
> 5. Repeat $steps$ $3$ and $4$ until convergence.

> [!NOTE] Key Notes
> 
> - **Advantages**:
>     - Easy to implement.
>     - Requires predefining $k$.
> - **Disadvantages**:
>     - Assumes spherical clusters.
>     - Sensitive to local optima.
>     - $O(knd)$, where $n$ is the number of points and dd is dimensions.
> - **Optimization**: Use elbow method to determine kk:
>     - Select $\Delta y$ (reduction in error) versus $\Delta x$ (number of clusters).

---

### DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

> [!NOTE] Overview
> 
> - **Purpose**: Discovers arbitrary shape clusters.
> - **Based on Density**:
>     - $\epsilon$: Maximum distance between neighbours.
>     - $\text{MinPts}$: Minimum points required to form a dense region.

> [!NOTE] Classification of Points
> 
> - **Core**: Within the dense cluster.
> - **Border**: Within $\epsilon$ but fewer than $\text{MinPts}$.
> - **Noise**: Not part of any cluster.

---

### Hierarchical Clustering


> [!leaf] Bottom-Up (Agglomerative)
> 
> 1. Treat each individual point as its own cluster.
> 2. Merge clusters based on similarity.
> 3. Continue until all points belong to a single cluster.
> 4. Consider linkage criteria:
> 
> - Single, average, or complete linkage.

> [!omega] Top-Down (Divisive)
> 
> 1. Start with all points in a single cluster.
> 2. Split clusters based on dissimilarity or apply kk-means.
> 3. Terminate at appropriate depth.

> [!NOTE] Visualization
> 
> - **Dendrogram**:
>     - Represents hierarchical relationships between clusters.
>     - Useful for visualizing large datasets.

---

### Gaussian Mixture Models (GMM)

> [!NOTE] Overview
> 
> - **Probabilistic Approach**:
>     - Prior: $P(C | \theta) = \pi$
>     - Mixture: $P(X∣C,θ)P(X | C, \theta)$
> - **Goal**: Fit data to Gaussian distributions.

---

---
#TODO
[[Grail 🩷]]


