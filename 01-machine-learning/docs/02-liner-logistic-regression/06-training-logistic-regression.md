[< Back to Machine Learning with Python](../../README.md)

# Training a Logistic Regression Model

## Objective

- Find parameters (**θ**) that best map inputs → target outcomes.
- Goal: predict classes with **minimal error**.
- Achieved by minimizing a **cost function** (log loss).

---

## Training Steps

1. Initialize parameters (**θ**) – often random.
2. Predict probabilities (p-hat) for each observation.
3. Measure error via **cost function (log loss)**.
4. Update θ to reduce error.
5. Repeat until log loss is sufficiently small or max iterations reached.

---

## Cost Function: Log Loss

- Measures how well predicted probabilities match actual outcomes.
- Formula:  
  \[
  \text{Log Loss} = -\frac{1}{n} \sum\_{i=1}^n \big[ y_i \log(\hat{p}_i) + (1 - y_i) \log(1 - \hat{p}_i) \big]
  \]
- Properties:
  - **Small log loss** when confident & correct (p close to 1 for y=1).
  - **Large log loss** when confident & wrong (p close to 1 for y=0).
- Optimization target: minimize log loss.

---

## Gradient Descent

- Iterative method to find parameter values that minimize cost function.
- Uses gradient (derivative of log loss) → update θ in the **direction of steepest descent**.
- **Learning rate (α):** step size; too small = slow, too large = unstable.
- Converges as slope approaches zero at the optimal θ.

---

## Stochastic Gradient Descent (SGD)

- Variation of gradient descent:
  - Uses **random subset of data** instead of entire dataset per iteration.
  - Much faster, scales better for large data.
- Features:
  - Can escape local minima → more likely to reach global minimum.
  - Convergence can oscillate around the minimum.
  - Improvements:
    - **Decay learning rate** near convergence.
    - **Increase sample size** gradually for stability.

---

## Key Takeaways

- Logistic regression training = iterative optimization to minimize **log loss**.
- **Log loss** penalizes confident wrong predictions.
- **Gradient descent** finds optimal θ but is slow on large data.
- **SGD** is faster and scalable, but noisier → needs tuning.

[< Back to Machine Learning with Python](../../README.md)
