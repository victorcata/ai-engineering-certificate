[< Back to Machine Learning with Python](../../README.md)

# K-Nearest Neighbors (KNN)

## What is KNN?

- **Supervised ML algorithm** used for **classification** and **regression**.
- Idea: **similar points are close in feature space** → neighbors have similar labels.
- Predicts based on the labels of the **K nearest neighbors** to a query point.
- Known as a **lazy learner** → does not build a model, just stores training data.

---

## How KNN Works

1. Pick a value for **K** (number of neighbors).
2. Compute distance from query point to all labeled training points.
3. Select the **K nearest neighbors**.
4. Make prediction:
   - **Classification:** majority vote among neighbors.
   - **Regression:** average or median of neighbors’ target values.

---

## Example: Iris Dataset

- Features: sepal length, sepal width, petal length, petal width.
- KNN (with $k=3$):
  - Point classified by majority of 3 nearest neighbors.
  - Achieved ~93% accuracy in classification.

---

## Choosing K

- **Small K** → sensitive to noise, may **overfit**.
- **Large K** → smoother boundaries, may **underfit**.
- **Optimal K** → found via testing with validation dataset.
- Example: accuracy best at $k=4$.

---

## Impact of Data & Features

- **Skewed class distribution:** majority voting may be biased toward frequent classes.
  - Fix: **distance-weighted voting**.
- **Feature scaling needed:** large-valued features dominate distance calculations.
  - Fix: **standardization** or normalization.
- **Irrelevant features = noise:**
  - Require larger K to avoid overfitting.
  - Increase computation cost, lower accuracy.
- **Relevant features:**
  - Lower optimal K.
  - Better accuracy and efficiency.
  - Selection requires **domain knowledge**.

---

## Key Takeaways

- KNN is a **simple, supervised algorithm** for classification & regression.
- Predictions depend on **distance to nearest labeled neighbors**.
- Performance depends heavily on:
  - Choice of **K**.
  - **Feature scaling**.
  - Removing **irrelevant features**.
- Optimal K is found by **testing and validation**.

[< Back to Machine Learning with Python](../../README.md)
