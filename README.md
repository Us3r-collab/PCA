# Principal Component Analysis (PCA)

**Principal Component Analysis (PCA)** is an unsupervised machine learning technique used for **dimensionality reduction**. It transforms a high-dimensional dataset containing correlated features into a smaller set of linearly uncorrelated variables—called **Principal Components (PCs)**—while retaining as much of the original data's variance (information) as possible.

---

## ⚙️ How PCA Works

1. **Standardization**  
   Scales all features to have a mean of $0$ and a standard deviation of $1$ ($\mu = 0, \sigma = 1$) so features with larger scales do not artificially dominate the analysis.

2. **Covariance Matrix Computation**  
   Constructs a covariance matrix $\Sigma$ to capture the pairwise linear relationships between all features:
   $$\Sigma = \frac{1}{n-1} X^T X$$

3. **Eigen Decomposition**  
   Computes the eigenvectors and eigenvalues of the covariance matrix:
   * **Eigenvectors:** Define the *directions* of the new axes (Principal Components).
   * **Eigenvalues:** Quantify the *magnitude of variance* captured along each direction.

4. **Component Ranking & Selection**  
   Orders the eigenvectors in descending order according to their corresponding eigenvalues:
   * **PC1** captures the highest variance in the dataset.
   * **PC2** captures the second-highest variance and is orthogonal ($\perp$) to PC1.
   * The top $k$ components are selected based on a target cumulative explained variance threshold (e.g., $90\%$).

5. **Projection to Lower-Dimensional Space**  
   Projects the standardized feature matrix $X$ onto the selected $k$ eigenvectors ($W_k$):
   $$X_{\text{reduced}} = X W_k$$

---

## 🎯 Key Use Cases

* **Data Visualization:** Compresses high-dimensional datasets into 2D or 3D representations to visually inspect clusters, patterns, and outliers.
* **Noise Reduction & Preprocessing:** Drops components with negligible eigenvalues (which typically represent noise), reducing computational complexity and mitigating overfitting in downstream models.
* **Multicollinearity Removal:** Replaces correlated features with mutually orthogonal components, stabilizing regression models.

---
