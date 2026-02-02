## Week 7 – Principal Component Analysis (PCA)

In this week, I learned Principal Component Analysis (PCA) and the basic linear algebra concepts required to understand how PCA works in machine learning. The goal was to understand why dimensionality reduction is needed, how PCA reduces features, and how it is used in real ML problems.

## Overview

### Why PCA is Needed

- Understood the curse of dimensionality and data sparsity

- Learned why high-dimensional data affects model performance

- Saw how reducing dimensions helps improve efficiency and learning

- Variance and Covariance

- Learned what variance means and why it is important

- Understood covariance and how it shows relationships between features

- Learned how the covariance matrix summarizes feature relationships

---

### Eigenvalues and Eigenvectors

- Understood the intuition behind eigenvalues and eigenvectors

- Learned why eigenvectors represent important directions in data

- Understood why eigenvalues indicate the importance of each direction

---

### How PCA Works (Step by Step)

- Centering and scaling the data

- Computing the covariance matrix

- Finding eigenvalues and eigenvectors

- Sorting components based on variance

- Projecting data onto principal components

--- 

### Explained Variance

- Learned what explained variance means

- Understood how to choose the optimal number of PCA components

- Learned the intuition behind the elbow method

---

### PCA Transformation

- Understood how original data points are transformed into PCA space

- Learned the geometric meaning of projecting data onto new axes

- PCA Variants (Conceptual Understanding)

- Learned SVD-based PCA intuition

- Understood Kernel PCA at a high level

- Learned when standard PCA fails and why variants are needed

--- 

### PCA Comparison

- Understood the difference between PCA and LDA

- Understood how PCA differs from t-SNE

- Learned when to use PCA and when not to use it

### Practical Learning

- Applied PCA on high-dimensional data

- Visualized data using 2D and 3D PCA components

- Studied the effect of number of components on model performance

- Used PCA with KNN to analyze accuracy changes

--- 

### Key Takeaways

- PCA reduces dimensions by maximizing variance

- Principal components are orthogonal and uncorrelated

- PCA is an unsupervised technique

- Feature scaling is important before applying PCA

- PCA works well for linear data and fails on non-linear patterns
