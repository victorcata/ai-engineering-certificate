[< Back to Machine Learning with Python](../../README.md)

# Regression Trees

## What is a Regression Tree?

- A **decision tree adapted for regression tasks**.
- **Target variable**: continuous (e.g., salary, temperature).
- **Key difference**:
  - Classification Tree → categorical target, prediction = majority vote.
  - Regression Tree → continuous target, prediction = average (or median) of values in node.

---

## Applications

- **Regression Trees:** predict revenue, temperature, wildfire risk.
- **Classification Trees:** spam detection, medical diagnosis, image classification.

---

## How Regression Trees Work

1. **Recursive Splitting** – dataset is split into subsets to minimize prediction error.
2. **Prediction Rule** – at leaf nodes, prediction = average (or median if skewed) of target values.
3. **Splitting Criterion** – minimize **Mean Squared Error (MSE)**, not entropy or information gain.

---

## Split Quality: MSE

- For a node with prediction $\hat{y}$:  
  $$ MSE = \frac{1}{n} \sum\_{i=1}^n (y_i - \hat{y})^2 $$
- **Weighted MSE of split**:  
  $$ MSE\_{split} = \frac{n_L}{n} MSE_L + \frac{n_R}{n} MSE_R $$
  - $n_L$, $n_R$ = samples in left/right nodes.
  - Lower $MSE_{split}$ = better feature split.
- Tree chooses feature + threshold with **lowest weighted MSE**.

---

## Handling Feature Types

- **Continuous features:**
  - Sort feature values.
  - Remove duplicates.
  - Candidate thresholds = midpoints between consecutive values:  
    $$ \alpha*i = \frac{X_i + X*{i+1}}{2} $$
  - Choose threshold that minimizes weighted MSE.
- **Binary features:**
  - Split into two groups directly.
- **Multi-class features:**
  - Use **One-vs-One** or **One-vs-All** strategies to generate binary splits.
  - Pick split with lowest weighted MSE.

---

## Efficiency Considerations

- Exhaustive search = accurate but expensive (doesn’t scale well).
- For very large datasets:
  - Use a **subset of thresholds** for faster training (tradeoff: less accuracy).
  - Consider **distribution of values** when sampling thresholds.

---

## Key Takeaways

- Regression Trees = **Decision Trees for continuous targets**.
- Built by **recursive partitioning** using MSE to evaluate splits.
- Predictions = average (or median) at leaf nodes.
- Must balance **accuracy vs efficiency** when selecting thresholds.
- Practical for many real-world regression problems (finance, environment, etc.).

[< Back to Machine Learning with Python](../../README.md)
