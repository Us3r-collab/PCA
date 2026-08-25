# PCA
Principal Component Analysis (PCA) is an unsupervised machine learning technique used for dimensionality reduction. It transforms a high-dimensional dataset with many correlated features into a smaller set of uncorrelated variables—called Principal Components (PCs)—while retaining as much of the original data's variance (information) as possible.
How PCA Works:
  1.Standardization: Scales all features to have a mean of $0$ and a standard deviation of $1$ so variables with larger numeric ranges do not dominate the analysis.
  2.Standardization: Scales all features to have a mean of $0$ and a standard deviation of $1$ so variables with larger numeric ranges do not dominate the analysis.
  3.Eigen Decomposition: Computes the eigenvectors and eigenvalues of the covariance matrix:
    -Eigenvectors define the directions of the new feature axes (Principal Components).
    -Eigenvalues quantify the amount of variance captured along each direction.
  4.Ranking & Selection: Orders the components by eigenvalue in descending order. PC1 captures the highest variance, PC2 captures the second-highest (orthogonal to PC1),
  and so on. You select the top $k$ components that explain a target proportion of total variance (e.g., $90\%$).
  5.Projection: Multiplies the original standardized data matrix by the top $k$ eigenvectors to project the data into the new lower-dimensional space.
