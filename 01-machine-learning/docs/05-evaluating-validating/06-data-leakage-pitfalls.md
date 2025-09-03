[< Back to Machine Learning with Python](../../README.md)

# Data Leakage and Other Pitfalls

## 1. What is Data Leakage?

- **Definition:** Data leakage occurs when training data includes information unavailable in real-world predictions (e.g., using future data).
- **Impact:**
  - Artificially inflates model performance during training/validation.
  - Model fails in production due to reliance on leaked info.
- **Example:** Predicting house prices using the **average of all prices in the dataset** → not available in real-world deployment.

---

## 2. Types of Leakage

- **Data Leakage:** Model learns from information it won’t have at deployment.
- **Data Snooping:** Training set contains information from the test set or future values (e.g., using tomorrow’s stock price to predict today).

---

## 3. How to Mitigate Data Leakage

- Avoid **global statistics** (e.g., averages over the whole dataset).
- Ensure **clear separation** between training, validation, and test sets.
- Check that all features exist in **real-world prediction scenarios**.
- Implement cross-validation properly:
  - Run pipelines **independently** for each fold.
  - For time-dependent data, use **time-series splits** instead of random splits.

**Example with Scikit-Learn:**

- Use a pipeline (Scaler → PCA → KNN).
- Pass the **pipeline** into `GridSearchCV` → ensures each fold processes data independently.
- For temporal data: use `TimeSeriesSplit` instead of `train_test_split`.

---

## 4. Feature Importance Pitfalls

- **Redundancy:** Correlated features share importance → underestimate influence.
- **Scaling:** Some models (e.g., linear regression) don’t adjust for scale.
- **Correlation ≠ Causation:** Important features don’t always drive outcomes.
- **Interactions ignored:**
  - Example: Two weak features individually → seem unimportant.
  - Their **interaction** may be critical (detected by nonlinear models like Random Forest).

---

## 5. Other Modeling Pitfalls

- Using raw data without **feature selection/engineering**.
- Choosing **wrong evaluation metrics** or misinterpreting them.
- Ignoring **class imbalance** → bias toward majority class.
- Blind reliance on **AutoML tools** without understanding model + data.
- Running **what-if scenarios** without causal features → misleading predictions.

---

## 6. Key Takeaways

- **Data leakage** misleads training & testing → fix by proper splits, pipelines, and avoiding future info.
- **Cross-validation** must be carefully designed (especially for time-series).
- **Feature importance** needs context: check redundancy, scaling, interactions.
- Avoid pitfalls by using the **right features, metrics, and causal understanding**.

[< Back to Machine Learning with Python](../../README.md)
