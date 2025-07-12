# Model Evaluation

You can compare the actual values and predicted values to calculate the accuracy of a regression model. Evaluation metrics play a key role in the development of a model, as they provide insight into areas that require improvement.

There are different model evaluation metrics, let's use MSE here to calculate the accuracy of our model based on the test set:

- **Mean Absolute Error:** It is the mean of the absolute value of the errors. This is the easiest of the metrics to understand since it’s just an average error.
- **Mean Squared Error (MSE):** MSE is the mean of the squared error. In fact, it's the metric used by the model to find the best fit line, and for that reason, it is also called the residual sum of squares.
- **Root Mean Squared Error (RMSE):** RMSE simply transforms the MSE into the same units as the variables being compared, which can make it easier to interpret.
- **R-squared** is not an error but rather a popular metric used to estimate the performance of your regression model. It represents how close the data points are to the fitted regression line. The higher the R-squared value, the better the model fits your data. The best possible score is 1.0 and it can be negative (because the model can be arbitrarily worse).

# Polynomial and non-linear regression

- **Nonlinear Regression**:

  - Models the relationship between variables using nonlinear equations (e.g., polynomial, exponential, logarithmic, sinusoidal).
  - Useful when data cannot be represented by a straight line.

- **Polynomial Regression**:

  - A special case of nonlinear regression.
  - Uses transformed input features (e.g., x, x², x³) but remains linear in parameters.
  - Solved using ordinary linear regression techniques.
  - Risk of **overfitting** if the polynomial degree is too high.

- **Examples of Nonlinear Relationships**:

  - **Exponential Growth**: e.g., GDP over time.
  - **Logarithmic Trend**: e.g., diminishing returns in productivity.
  - **Periodicity**: e.g., seasonal temperature or rainfall patterns.

- **Model Selection Techniques**:

  - Visually analyze scatter plots to detect if the relationship is linear or nonlinear.
  - Match data trends to appropriate mathematical functions (linear, exponential, logarithmic, sinusoidal).
  - Focus on modeling the **underlying trend**, not memorizing noise.

- **Fitting and Optimization**:

  - If the model equation is known, use **gradient descent** to find optimal parameters.
  - If not, explore **machine learning models**, such as:
    - Regression Trees
    - Random Forests
    - Neural Networks
    - Support Vector Machines (SVM)
    - Gradient Boosting Machines
    - K-Nearest Neighbors (KNN)

- **Key Takeaway**:
  - Polynomial regression is a linear regression on transformed inputs.
  - Nonlinear regression is broader and includes many real-world patterns that cannot be captured by polynomials.

# Logistic Regression

**What is Logistic Regression?**

- A statistical and machine learning method used for **binary classification**.
- Predicts the **probability** that an observation belongs to class 1 (e.g. churn = 1, no churn = 0).
- Converts probability to a class using a **threshold** (commonly 0.5).

**When to Use It**

- The **target variable is binary** (0 or 1).
- You need **probabilistic predictions**, not just labels.
- You want to **interpret feature importance** (via model coefficients).

**How It Works**

- Starts with a **linear model**:
  $$
  \hat{y} = \theta_0 + \theta_1 x_1 + \theta_2 x_2 + \dots
  $$
- Applies the **sigmoid (logit) function** to squash the output between 0 and 1:
  $$
  \sigma(x) = \frac{1}{1 + e^{-x}}
  $$
- The output is the **predicted probability** $ \hat{p} = P(y=1 | x) $

**Classification Rule (Decision Boundary)**

- If $ \hat{p} > 0.5 $ → predict class 1
- Else → predict class 0
- The value **0.5 is the decision threshold**, which can be adjusted.

**Real-World Use Cases**

- Customer churn prediction
- Disease diagnosis (e.g., diabetes, heart attack)
- Loan default prediction
- Subscription cancellation
- Product or system failure

**Probability Interpretation**

- If $ P(\text{churn}) = 0.8 $, then $ P(\text{no churn}) = 1 - 0.8 = 0.2 $
- Probabilities always sum to 1 for binary classes.

**Key Takeaways**

- Logistic regression is both a **probability predictor** and a **binary classifier**.
- It's suitable when the relationship between inputs and the binary output is **linearly separable** in feature space.
- Offers a balance of **simplicity**, **interpretability**, and **usefulness** for many classification problems.

# Training Logistic Regression

**Goal**

- Find parameters ($\theta$) that **minimize prediction error**.
- Optimize the **log loss** cost function to fit the best model.

**Steps to Train Logistic Regression**

1. **Initialize parameters** $\theta$ (e.g., randomly).
2. **Predict probabilities** $\hat{p}_i$ using sigmoid:  
   $$ \hat{p}\_i = \sigma(\theta^T x_i) $$
3. **Compute cost** using **log loss**:
   $$
   J(\theta) = -\frac{1}{n} \sum_{i=1}^{n} \left[ y_i \log(\hat{p}_i) + (1 - y_i) \log(1 - \hat{p}_i) \right]
   $$
4. **Update $\theta$** to reduce log loss.
5. **Repeat** until loss is small or max iterations reached.

---

**Optimization Methods**

🔹 **Gradient Descent**

- Iteratively adjusts $\theta$ in the direction of **steepest descent**.
- Uses the **full dataset** to compute the gradient.
- Slower for large datasets.

🔹 **Stochastic Gradient Descent (SGD)**

- Uses a **random subset** (mini-batch) of data per iteration.
- **Faster**, more scalable.
- May **overshoot** or wander around the minimum.
- Can improve convergence by:
  - **Reducing learning rate** over time
  - **Increasing batch size** gradually

---

**Key Points**

- **Log loss** rewards confident correct predictions, penalizes confident wrong ones.
- **Gradient descent** moves toward optimal parameters using derivatives.
- **SGD** offers speed and scalability, often better for large datasets.
