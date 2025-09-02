[< Back to Machine Learning with Python](../../README.md)

# Introduction to Multiple Linear Regression

## What is Multiple Linear Regression?

- **Extension of simple linear regression** → uses **2+ independent variables** to predict a dependent variable.
- Model equation:  
  \[
  \hat{y} = \theta_0 + \theta_1 x_1 + \theta_2 x_2 + \dots + \theta_n x_n
  \]
  - **θ₀** = intercept (bias).
  - **θᵢ** = coefficients (weights).
  - **xᵢ** = feature values.
- Geometric interpretation:
  - **1 feature** → line.
  - **2 features** → plane.
  - **>2 features** → hyperplane.

---

## Example

- Predict **CO₂ emissions** from **engine size, cylinders, fuel consumption**, etc.
- Example equation:  
  \[
  CO₂ = 125 + 6.2 \times (engine\ size) + 14 \times (cylinders) + \dots
  \]
- Plugging in values (e.g., 2.4L engine, 4 cylinders) → predicted CO₂ = **214.1**.

---

## Applications

- **Education:** Predict student exam performance using revision time, anxiety, attendance, gender.
- **Healthcare:** Estimate changes in blood pressure based on BMI.
- **What-if scenarios:** Predict outcomes when changing one or more inputs (though risky if unrealistic).
- **General use:** Better modeling than simple regression when multiple factors influence outcomes.

---

## Pitfalls

1. **Overfitting** – too many variables cause the model to memorize training data.
2. **Collinearity** – correlated predictors make variables redundant and unstable.
   - Example: engine size & fuel consumption might overlap.
   - Solution: remove redundant variables.
3. **Invalid What-if Scenarios** – unrealistic or far-from-training data scenarios give misleading results.

---

## Error & Optimization

- **Residual error:** difference between actual vs predicted value.
- **Mean Squared Error (MSE):**
  - Measures average squared residuals.
  - Goal: minimize MSE.
- **Estimation methods:**
  - **Ordinary Least Squares (OLS):** direct calculation with linear algebra.
  - **Gradient Descent:** iterative optimization, useful for large datasets.

---

## Key Takeaways

- **Multiple linear regression** = stronger, more flexible than simple regression.
- Useful for **explaining relationships** and **making predictions** across many domains.
- Requires careful **variable selection** (uncorrelated, controllable, relevant).
- Main risks: **overfitting, collinearity, unrealistic scenarios**.
- Parameters commonly estimated via **OLS** or **gradient descent**.

[< Back to Machine Learning with Python](../../README.md)
