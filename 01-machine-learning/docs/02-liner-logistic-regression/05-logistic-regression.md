[< Back to Machine Learning with Python](../../README.md)

# Introduction to Logistic Regression

## What is Logistic Regression?

- **Statistical modeling technique** used for **binary classification** (target = 0 or 1).
- Predicts the **probability** of an observation belonging to a class.
- Converts probability into a class using a **threshold** (commonly 0.5).
- In ML, logistic regression = **binary classifier + probability predictor**.

---

## When to Use Logistic Regression

1. **Binary target** – e.g., churn (yes/no), disease (present/absent).
2. **Need probability estimates** – not just class labels.
3. **Linearly separable data** – decision boundary = line/plane/hyperplane.
4. **Feature importance** – coefficients show influence of variables.

---

## Examples

- Healthcare: probability of heart attack, diabetes, or cancer.
- Business: customer churn prediction, subscription cancellations.
- Finance: mortgage default prediction, system/process failure.
- Telecom: churn prediction using account info, demographics, service usage.

---

## How It Works

- **Linear regression issue:** predictions extend infinitely, not restricted to [0,1].
- **Thresholding alone (step function):** crude, no probability info.
- **Sigmoid function (logit):**  
  \[
  \sigma(x) = \frac{1}{1 + e^{-x}}
  \]
  - Compresses values into range (0,1).
  - Smoothly maps input to probability.
  - At \(x=0\), \(\sigma(x)=0.5\).
- **Model:**  
  \[
  p(\hat{y}=1|x) = \sigma(\theta_0 + \theta_1 x_1 + \dots + \theta_n x_n)
  \]
- **Decision boundary:** probability > threshold → class 1, else class 0.

---

## Key Concepts

- **Predicted probability (p-hat):** chance observation belongs to class 1.
- **Complement:** probability of class 0 = \(1 - p(\hat{y})\).
- **Coefficients (θ):** indicate influence of features.
- Logistic regression = interpretable, probabilistic, effective for binary outcomes.

---

## Key Takeaways

- Logistic regression predicts **probabilities** and performs **binary classification**.
- Uses the **sigmoid/logit function** to map predictions into [0,1].
- Good for binary targets, probability estimates, and feature impact analysis.
- Commonly applied in healthcare, finance, telecom, and customer analytics.

[< Back to Machine Learning with Python](../../README.md)
