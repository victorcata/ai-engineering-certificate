[< Back to Machine Learning with Python](../../README.md)

# Support Vector Machines (SVM)

## What is SVM?

- **Supervised learning technique** for **classification** (and regression).
- Represents each data point in **multidimensional space**.
- Finds a **hyperplane** that separates classes with the **largest possible margin**.
- **Support vectors** = nearest points to the hyperplane; they define the margin.

---

## Key Concepts

- **Margin:** distance from hyperplane to nearest support vectors.
  - Larger margin → better generalization.
- **Soft Margin (C parameter):**
  - Small C → allows more misclassifications (flexible, generalizes better).
  - Large C → stricter separation (may overfit).
- **Decision Rule:**
  - $f(x) = w^T x + b$
  - If $f(x) > 0$ → Class 1, else Class -1.

---

## Kernel Trick

- Used when data is **not linearly separable**.
- Transforms input into **higher-dimensional space** where separation is possible.
- Common kernels in **Scikit-learn**:
  - **Linear** (default).
  - **Polynomial** (quadratic, cubic, etc.).
  - **RBF (Radial Basis Function):** scores high for nearby points.
  - **Sigmoid:** same as logistic regression activation.

---

## Support Vector Regression (SVR)

- Extension of SVM for **continuous targets**.
- Uses an **epsilon-tube** around prediction curve:
  - Points inside tube → treated as noise-free signal.
  - Points outside tube → treated as noise.
- Parameter **epsilon (ε):** defines tube width.

---

## Advantages

- Works well in **high-dimensional spaces**.
- Robust to overfitting (especially with clear margins).
- Effective with both linearly and weakly separable data.

---

## Limitations

- **Slow training** on large datasets.
- Sensitive to **noise** and overlapping classes.
- Sensitive to **choice of kernel & parameters** (C, gamma, ε).

---

## Applications

- **Image analysis & recognition** (e.g., handwritten digit classification).
- **Spam detection & sentiment analysis.**
- **Speech recognition.**
- **Anomaly detection & noise filtering.**

---

## Key Takeaways

- SVM finds the **optimal hyperplane** that maximizes margin between classes.
- **Soft margin** (C) balances misclassification tolerance and strictness.
- **Kernels** extend SVMs to nonlinear problems.
- SVM can also be used for **regression (SVR)** with epsilon-tube.
- Best suited for **high-dimensional but smaller datasets**.

[< Back to Machine Learning with Python](../../README.md)
