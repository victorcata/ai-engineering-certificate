[< Back to Machine Learning with Python](../../README.md)

# DBSCAN & HDBSCAN

## DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

- **Density-based clustering** → forms clusters by finding dense regions of points.
- Handles **clusters of arbitrary shape**, unlike K-Means (convex clusters).
- Can identify **noise/outliers** (points not belonging to any cluster).
- Useful when **number of clusters is unknown**.

### Parameters

- **ε (epsilon):** neighborhood radius.
- **minPts:** minimum number of points required to form a dense region.

### Point Types

- **Core point** → ≥ minPts inside ε.
- **Border point** → in neighborhood of a core, but not enough points to be a core.
- **Noise point** → not a core or border.

### Algorithm

1. For each point, check ε-neighborhood.
2. If ≥ minPts → mark as **core** and form cluster.
3. Add reachable points (border/core) to the cluster.
4. Continue until no new points can be added.
5. Remaining points → **noise**.

- **Not iterative**: clusters are grown in a single pass.

---

## HDBSCAN (Hierarchical DBSCAN)

- **Extension of DBSCAN** → no need to set ε manually.
- Uses **cluster stability** → measures persistence of clusters across density levels.
- Builds a **hierarchical tree** of clusters (bottom-up agglomerative + density-based).
- Produces a **condensed tree** with the most stable clusters.
- More **robust to noise/outliers** and adapts to **varying local densities**.

---

## Comparison

| Feature         | DBSCAN             | HDBSCAN                                      |
| --------------- | ------------------ | -------------------------------------------- |
| Parameters      | Needs ε and minPts | Fewer params (min cluster size, min samples) |
| Shapes          | Arbitrary          | Arbitrary                                    |
| Noise handling  | Good               | Better                                       |
| Varying density | Poor               | Strong                                       |
| Output          | Flat clusters      | Hierarchical + stable clusters               |

---

## Applications

- **DBSCAN:** detecting anomalies, spatial clustering (e.g., GPS coordinates), shapes with noise.
- **HDBSCAN:** datasets with **varying densities**, e.g., geographic clustering, genetic data, or complex shapes.

---

## Key Takeaways

- **DBSCAN**: density-based, non-iterative, requires ε + minPts, good for unknown k.
- **HDBSCAN**: adapts density threshold automatically, uses stability for robust results, better with varying densities and noise.

[< Back to Machine Learning with Python](../../README.md)
