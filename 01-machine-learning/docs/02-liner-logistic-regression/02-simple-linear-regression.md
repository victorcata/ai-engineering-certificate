[< Back to Machine Learning with Python](../../README.md)

# Introduction to Simple Linear Regression

## What is Simple Linear Regression?

- A **supervised learning technique** modeling a **linear relationship** between:
  - **Independent variable (x)** → predictor (e.g., engine size).
  - **Dependent variable (y)** → response/target (e.g., CO2 emissions).
- Uses a **single predictor variable** to estimate a continuous outcome.

---

## How It Works

- **Scatter plot** shows correlation between x and y.
- **Best-fit line** is calculated → captures approximate linear trend.
- Model equation:  
  \[
  \hat{y} = \theta_0 + \theta_1 x_1
  \]
  - **θ₀ (intercept)**: bias coefficient.
  - **θ₁ (slope)**: coefficient showing how x impacts y.
- Example:
  - Engine size = 2.4 → Predicted CO₂ emission = 214.

---

## Error & Optimization

- **Residual error**: vertical distance between actual and predicted values.
- **Mean Squared Error (MSE):**
  - Average of squared residuals.
  - Measures model fit.
- **Ordinary Least Squares (OLS) Regression**:
  - Minimizes MSE to find best-fit line.
  - Parameters θ₀ and θ₁ derived from means (x̄, ȳ).
  - Fast, no hyperparameter tuning required.

---

## Strengths

- Easy to understand & interpret.
- Computationally efficient (quick for small datasets).
- Transparent mathematical foundation (Gauss & Legendre, 1800s).

---

## Limitations

- Too simplistic for **nonlinear relationships**.
- **Outliers** can heavily distort results.

---

## Key Takeaways

- **Simple linear regression** = one variable predicting one outcome.
- Produces a best-fit line using OLS to minimize errors.
- Useful for continuous predictions (e.g., car emissions).
- Strengths: simplicity & speed. Weakness: sensitivity to outliers and limited to linear patterns.

[< Back to Machine Learning with Python](../../README.md)
