[< Back to Machine Learning with Python](../../README.md)

# Bias, Variance, and Ensemble Models

## Bias & Variance

- **Bias:** measures how far predictions are from actual values (accuracy).
  - High bias → underfitting (oversimplified model).
  - Low bias → better accuracy.
- **Variance:** measures sensitivity to training data fluctuations (precision).
  - High variance → overfitting (model tracks noise).
  - Low variance → stable predictions.

🎯 Analogy: Dartboard

- Top left: low bias, low variance (ideal).
- Bottom: high bias.
- Right: high variance.

---

## Bias-Variance Tradeoff

- As **model complexity increases**:
  - Bias ↓ (better fit to training data).
  - Variance ↑ (more sensitivity to noise).
- **Underfitting:** high bias, low variance.
- **Overfitting:** low bias, high variance.
- Best point: balance between bias & variance.
- Some **generalization error is inevitable** due to noise in data.

---

## Weak vs Strong Learners

- **Weak learner:** only slightly better than random guessing.
  - High bias, low variance.
- **Strong learner:** low bias, high variance.

---

## Ensemble Methods

### Bagging (Bootstrap Aggregating)

- Trains multiple models on **bootstrapped subsets** of data.
- Predictions are **averaged** → reduces variance, lowers overfitting risk.
- Example: **Random Forests** (many shallow trees).
  - Shallow trees = high variance.
  - Aggregation reduces variance.

### Boosting

- Builds models **sequentially**, each correcting previous errors.
- Focuses on **reducing bias**.
- Final model = weighted sum of weak learners.
- Popular algorithms: **AdaBoost, Gradient Boosting, XGBoost**.

---

## Ensemble Outcomes

- **Bagging:**

  - Parallel training on bootstrapped data.
  - Base learners = high variance, low bias.
  - Goal → reduce **variance**.

- **Boosting:**
  - Sequential training, reweights misclassified examples.
  - Base learners = high bias, low variance.
  - Goal → reduce **bias**.

---

## Key Takeaways

- **Bias:** accuracy; **Variance:** precision.
- Tradeoff: model complexity ↓ bias but ↑ variance.
- **Bagging → reduces variance** (mitigates overfitting).
- **Boosting → reduces bias** (mitigates underfitting).
- Ensemble methods improve generalization and predictive power.

[< Back to Machine Learning with Python](../../README.md)
