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
## Maths

> [!NOTE] Bayes' Rule  
> $p(x∣y)=p(y∣x)p(x)p(y)=p(y,x)p(y)p(x|y) = \frac{p(y|x)p(x)}{p(y)} = \frac{p(y, x)}{p(y)}$
### Expectation and Variance

- Expectation $E[f]$ written as $\langle f \rangle$:
    - Continuous: $\bar{x} = \int_{x \in \Omega}p(x)f(x) \, dx$
    - Discrete:  $\bar{x} = \sum_{x \in \Omega} p(x)f(x)$
    - Approximation: $\bar{x} \approx \frac{1}{N} \sum_{i=1}^N f(x) \approx \bar{x}$
- Variance $Var$:
    - $\sigma^2 = \langle (x - \langle x \rangle)^2 \rangle \text{ Also: }= E[x^2] - (E[x])^2$

### Distributions

- Poisson Distribution:  $P(x)=\frac{\lambda^x e^{-\lambda}}{x!}$
- Gaussian/Normal Distribution:  $P(x) = \frac{1}{\sqrt{2\pi \sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$

### Miscellaneous

- Distance in space:  
    $||x|| = \sqrt{x_1^2 + x_2^2 + \ldots + x_n^2}$
- Cosine similarity:  
    $\cos \theta = \frac{u \cdot v}{|u| |v|}$

---

## Vectors

### General Properties
$B B^\top = I$ 
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
    B=X−XˉB = X - \bar{X}
2. Compute covariance matrix:  
    E=1n−1BB⊤E = \frac{1}{n-1} BB^\top
3. Decompose covariance matrix:  
    S=UΛU⊤S = U \Lambda U^\top
    - UU: Eigenvectors
    - Λ\Lambda: Diagonal matrix of eigenvalues
4. Reduce dimensions:
    - Sort eigenvalues in descending order.
    - Choose top kk eigenvectors corresponding to the largest eigenvalues.

### Singular Value Decomposition (SVD)

- Decomposes XX into:  
    X=UΣV⊤X = U \Sigma V^\top
    
    - UU: Orthogonal matrix
    - Σ\Sigma: Diagonal matrix (singular values)
    - V⊤V^\top: Orthogonal matrix
- Applications:
    
    - Compression
    - Feature selection

> [!NOTE] Whitening  
> Transform data to ensure uncorrelated features:  
> P=BV⊤P = B V^\top


---

## Clustering

### K-Means Clustering

> [!NOTE] Steps for K-Means
> 
> 1. Choose kk.
> 2. Initialize kk centroids.
> 3. Assign each point to the closest centroid group.
> 4. Calculate the new center of each cluster.
> 5. Repeat steps 3 and 4 until convergence.

> [!NOTE] Key Notes
> 
> - **Advantages**:
>     - Easy to implement.
>     - Requires predefining kk.
> - **Disadvantages**:
>     - Assumes spherical clusters.
>     - Sensitive to local optima.
>     - O(knd)O(knd), where nn is the number of points and dd is dimensions.
> - **Optimization**: Use elbow method to determine kk:
>     - Select Δy\Delta y (reduction in error) versus Δx\Delta x (number of clusters).

---

### DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

> [!NOTE] Overview
> 
> - **Purpose**: Discovers arbitrary shape clusters.
> - **Based on Density**:
>     - ϵ\epsilon: Maximum distance between neighbors.
>     - MinPts\text{MinPts}: Minimum points required to form a dense region.

> [!NOTE] Classification of Points
> 
> - **Core**: Within the dense cluster.
> - **Border**: Within ϵ\epsilon but fewer than MinPts\text{MinPts}.
> - **Noise**: Not part of any cluster.

---

### Hierarchical Clustering

#### Bottom-Up (Agglomerative)

> [!NOTE] Steps
> 
> 1. Treat each individual point as its own cluster.
> 2. Merge clusters based on similarity.
> 3. Continue until all points belong to a single cluster.
> 4. Consider linkage criteria:
> 
> - Single, average, or complete linkage.

#### Top-Down (Divisive)

> [!NOTE] Steps
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
>     - Prior: P(C∣θ)=πP(C | \theta) = \pi
>     - Mixture: P(X∣C,θ)P(X | C, \theta)
> - **Goal**: Fit data to Gaussian distributions.

---

Let me know if there are additional sections you'd like me to enhance or any diagrams you'd like help recreating digitally!

---
### Topics
1. **Topic 1**
    - **Defintion:** $m+4th5$
    - 
2. **Topic 2**
    - 
    - 
3. **Topic 3**
    - 
    - 
4. **Topic 4**
    - 
    - 
5. **Topic 5**
    - 
    - 

---
#TODO
[[Grail 🩷]]


