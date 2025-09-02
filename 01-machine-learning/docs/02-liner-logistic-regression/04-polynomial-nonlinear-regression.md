[< Back to Machine Learning with Python](../../README.md)

# Introduction to Polynomial and Nonlinear Regression

## What is Nonlinear Regression?

- A statistical method modeling relationships **not represented by a straight line**.
- Uses equations such as **polynomial, exponential, logarithmic, sinusoidal**, etc.
- Suitable for complex patterns that linear regression cannot capture.
- Examples: exponential growth (GDP), logarithmic diminishing returns, seasonal periodicity.

---

## Polynomial Regression

- **Special case of nonlinear regression.**
- Transforms features into polynomial terms, but coefficients remain linear → solved with linear regression methods.
- Example:  
  \[
  y = \theta_0 + \theta_1 x + \theta_2 x^2 + \theta_3 x^3
  \]
- Implemented by introducing new variables:
  - \(x_1 = x\), \(x_2 = x^2\), \(x_3 = x^3\).
- **Strength:** Can approximate curved relationships.
- **Risk:** High-degree polynomials → **overfitting** (memorizing noise instead of patterns).

---

## Non-Polynomial Nonlinear Regression

- Captures relationships polynomial regression cannot:
  - **Exponential growth** → investments, GDP.
  - **Logarithmic** → diminishing returns in productivity.
  - **Periodic (sinusoidal)** → seasonal rainfall, temperature cycles.

---

## Model Selection

- **Visual analysis:** Scatter plots help decide if the relation is linear, exponential, logarithmic, sinusoidal.
- **Optimization techniques:**
  - Gradient Descent to fit parameters for a chosen equation.
- **Alternative ML models for nonlinear relationships:**
  - Regression trees, Random Forests, Gradient Boosting Machines.
  - Support Vector Machines.
  - Neural Networks.
  - k-Nearest Neighbors.

---

## Key Takeaways

- **Polynomial regression**: nonlinear in features, linear in coefficients. Useful but prone to overfitting.
- **Nonlinear regression**: broader, includes exponential, logarithmic, periodic functions.
- Used when data cannot be represented by a straight line.
- Optimal model depends on data patterns → analyze visually and test different models.

[< Back to Machine Learning with Python](../../README.md)
