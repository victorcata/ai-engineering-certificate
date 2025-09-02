[< Back to Machine Learning with Python](../../README.md)

# Clustering Strategies

## What is Clustering?

- **Unsupervised ML technique** → groups data points into clusters based on similarity.
- Unlike classification (supervised), clustering finds **patterns without labels**.
- Applications:
  - Customer segmentation (marketing).
  - Image segmentation (e.g., medical abnormality detection).
  - Anomaly detection (fraud, equipment faults).
  - Feature engineering (create new features, dimensionality reduction).
  - Data summarization (compression, simplification).

---

## Partition-Based Clustering

- Divides data into **non-overlapping groups**.
- Most common: **K-Means**.
  - Finds **k clusters** that minimize variance within each cluster.
  - Efficient and scalable for large datasets.
- Limitation: struggles with irregular cluster shapes.

---

## Density-Based Clustering

- Forms clusters of **any shape**, robust to noise.
- Example: **DBSCAN**.
  - Groups high-density areas into clusters.
  - Can identify outliers as points not belonging to any cluster.
- Limitation: can create unnecessary extra clusters in noisy regions.

---

## Hierarchical Clustering

- Organizes data into a **tree of nested clusters** (dendrogram).
- **Agglomerative (bottom-up):**
  - Start with each point as a cluster.
  - Iteratively **merge closest clusters** based on distance metrics (e.g., centroid distance).
- **Divisive (top-down):**
  - Start with all points in one cluster.
  - Iteratively **split into smaller clusters** until stopping criterion met.
- Useful for small/mid-sized datasets and visualizing relationships.

---

## Example Applications

- **K-Means:** customer segmentation into behavioral groups.
- **DBSCAN:** separating irregular shapes (e.g., "moons" dataset).
- **Hierarchical clustering:** analyzing genetic similarities (e.g., dog breeds and wolves).

---

## Key Takeaways

- **Partition-based (K-Means):** efficient, works best on spherical clusters.
- **Density-based (DBSCAN):** good for irregular shapes and noise handling.
- **Hierarchical:** builds dendrograms; supports both top-down (divisive) and bottom-up (agglomerative).
- Choice of method depends on dataset size, shape, and noise level.

[< Back to Machine Learning with Python](../../README.md)
