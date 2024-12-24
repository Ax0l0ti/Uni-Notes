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

### Unclear or partially readable sections:

- A few handwritten notes near the "SVD" section related to matrices and eigenvalues are partially illegible.
- Diagrams included in the notes cannot be transcribed exactly into text.

Let me know if you need additional clarification!

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