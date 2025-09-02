[< Back to Machine Learning with Python](../../README.md)

# K-Means Clustering

## What is K-Means?

- **Centroid-based, iterative clustering algorithm**.
- Partitions dataset into **k non-overlapping clusters**.
- Each cluster is defined by a **centroid** (mean of points in cluster).
- Goal: minimize **within-cluster variance** and maximize **between-cluster dissimilarity**.

---

## How K-Means Works

1. **Initialize**: choose number of clusters, k, and randomly select initial centroids.
2. **Assign points**: compute distances from points → nearest centroid.
3. **Update centroids**: recalculate as mean of assigned points.
4. **Repeat**: reassign points and update centroids until convergence (centroids stop moving or max iterations reached).

---

## Behavior & Assumptions

- Works well for **convex, balanced clusters**.
- Assumes clusters contain approximately the **same number of points**.
- Struggles with:
  - **Imbalanced clusters** (smaller clusters drift into larger ones).
  - **Non-convex shapes**.
  - **Outliers / noise** (variance is sensitive to them).
- Efficient and scales well → good for **big data**.

---

## Objective Function

Minimize total **within-cluster variance**:

$$
\sum_{i=1}^{k} \sum_{x \in C_i} \|x - \mu_i\|^2
$$

- $C_i$: set of points in cluster $i$.
- $\mu_i$: centroid of cluster $i$.

---

## Example Experiments

- **make_blobs dataset**:
  - With low std (1 or 4) → clusters identified correctly.
  - With high std (15) → overlap increases, results become inaccurate.
- **Incorrect k**:
  - If k < actual classes → merges clusters.
  - If k > actual classes → produces meaningless splits.

---

## Choosing the Best K

Since true k is often unknown, heuristics are used:

- **Silhouette analysis**: cohesion (similarity within cluster) vs separation (difference from other clusters).
- **Elbow method**: plot objective function (SSE) vs k → “elbow point” indicates good k.
- **Davies-Bouldin index**: measures average similarity ratio between clusters (lower is better).

---

## Key Takeaways

- **K-Means** is simple, efficient, and widely used.
- Best for **balanced, convex, well-separated clusters**.
- Sensitive to **imbalances, noise, and choice of k**.
- Use heuristics like **silhouette, elbow, and Davies-Bouldin index** to determine k.

[< Back to Machine Learning with Python](../../README.md)
