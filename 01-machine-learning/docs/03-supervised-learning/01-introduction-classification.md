[< Back to Machine Learning with Python](../../README.md)

# Introduction to Classification

## What is Classification?

- A **supervised machine learning method**.
- Predicts **categorical labels** (discrete values) for new data.
- Models are trained on labeled data to learn input → output mappings.
- Outputs can be **binary (2 classes)** or **multi-class (>2 classes)**.

---

## Applications & Use Cases

- **Email filtering** – spam vs not spam.
- **Speech-to-text** & **handwriting recognition**.
- **Biometric identification** – e.g., face or fingerprint recognition.
- **Document classification** – topic or category labeling.
- **Customer analytics:**
  - **Churn prediction** – whether a customer leaves.
  - **Segmentation** – assign customers to categories.
  - **Campaign response prediction** – likelihood of response.
- **Finance** – loan default prediction.
- **Healthcare** – drug prescription based on patient response (multi-class).

---

## Algorithms

Common classification algorithms include:

- **Naive Bayes**
- **Logistic Regression**
- **Decision Trees**
- **K-Nearest Neighbors (KNN)**
- **Support Vector Machines (SVMs)**
- **Neural Networks**

Some support **multi-class classification** directly (e.g., Logistic Regression, KNN, Decision Trees).  
Others require strategies to extend binary classifiers.

---

## Multi-Class Classification Strategies

### 1. One-vs-All (OvA)

- Train **k binary classifiers**, one per class.
- Each classifier distinguishes “class i” vs “all others.”
- A data point may:
  - Be assigned to one class.
  - Not fit any class (helpful for **outliers/noise**).

### 2. One-vs-One (OvO)

- Train a classifier for **each pair of classes**.
- Each decides: _“Is it class A or class B?”_
- Final prediction = **voting scheme**:
  - **Majority vote** → most votes wins.
  - **Weighted voting** → use confidence/probability scores (handles ties better).

---

## Key Takeaways

- Classification = supervised ML for **categorical outcomes**.
- Used in industries like **finance, telecom, healthcare, marketing**.
- Many algorithms available: from simple (Naive Bayes) to complex (Neural Nets).
- Multi-class handled via **One-vs-All** or **One-vs-One** strategies.

[< Back to Machine Learning with Python](../../README.md)
