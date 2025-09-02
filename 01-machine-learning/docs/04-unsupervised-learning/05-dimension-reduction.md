[< Back to Machine Learning with Python](../../README.md)

# Dimension Reduction Algorithms

## What They Are

- **Dimensionality Reduction Algorithms** reduce the number of dataset features **without losing critical information**.
- High-dimensional data is hard to analyze/visualize → these methods simplify the dataset for ML models.
- They **transform original dimensions** into new features, often improving interpretability and clustering performance.

---

## 1. Principal Component Analysis (PCA)

- **Type:** Linear dimensionality reduction.
- **Assumption:** Dataset features are **linearly correlated**.
- **How it works:**
  - Transforms features into **uncorrelated variables** called **principal components (PCs)**.
  - PCs are **orthogonal** and ordered by the variance they explain.
  - The **first few PCs retain most of the variance** (information), the rest mostly noise.
- **Benefits:** Simplifies data, reduces noise, fast, works well with linearly correlated data.

---

## 2. t-SNE (t-Distributed Stochastic Neighbor Embedding)

- **Type:** Nonlinear dimensionality reduction.
- **Goal:** Visualize **clusters in complex high-dimensional data** (e.g., images, text).
- **How it works:**
  - Preserves **local similarities** → points close in high-d space remain close in low-d space.
  - Focuses less on preserving distances between distant points.
- **Limitations:**
  - Doesn’t scale well to large datasets.
  - Sensitive to hyperparameters (difficult to tune).

---

## 3. UMAP (Uniform Manifold Approximation and Projection)

- **Type:** Nonlinear dimensionality reduction.
- **Goal:** Alternative to t-SNE, with better scalability.
- **How it works:**
  - Builds a **graph-based representation** of high-d data (manifold assumption).
  - Optimizes a low-dimensional graph preserving **local + global structure**.
- **Advantages:**
  - Faster and scales better than t-SNE.
  - Often provides **higher clustering performance** because it balances local & global structure.

---

## Example: MakeBlobs Data in 3D

- Dataset: 4 blobs, some overlap (yellow & purple).
- **PCA** → separated blobs effectively (works well since blobs are linearly correlated).
- **t-SNE** → found 4 distinct clusters, but some mixing between overlapping blobs.
- **UMAP** → also separated well, but slight overlap remained (expected due to input data).

---

## Key Takeaways

- **PCA:** Linear, variance-preserving, noise-reducing.
- **t-SNE:** Nonlinear, excels at visualizing clusters, local structure focused.
- **UMAP:** Nonlinear, scalable, preserves both **local + global** structure.
- All three are essential tools for **simplifying data, improving clustering, and enabling visualization**.

[< Back to Machine Learning with Python](../../README.md)
