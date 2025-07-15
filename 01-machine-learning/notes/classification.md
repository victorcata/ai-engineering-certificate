# Classification

## What is Classification?

- A **supervised machine learning** method.
- Predicts **categorical (discrete)** labels using trained models.
- Common in tasks like spam detection, churn prediction, and image recognition.

## Applications and Use Cases

- **Email filtering**
- **Speech-to-text**
- **Handwriting recognition**
- **Biometric identification**
- **Document classification**
- **Churn prediction**
- **Customer segmentation**
- **Loan default prediction**
- **Drug prescription (multi-class)**

## Classification Algorithms

- Logistic Regression
- Naive Bayes
- Decision Trees
- K-Nearest Neighbors (KNN)
- Support Vector Machines (SVM)
- Neural Networks

## Binary vs Multi-class Classification

### Binary Classification Example

Predict if a customer will default on a loan (yes/no) using features like:

- Age
- Income
- Credit debt

### Multi-class Classification Example

Predict which of three drugs best treats a patient based on:

- Patient history
- Treatment outcomes

## Multi-class Strategies

### One-vs-All (OvA)

- Train one binary classifier per class.
- Each predicts if a sample belongs to its class or not.
- Total of _k_ classifiers for _k_ classes.

### One-vs-One (OvO)

- Train classifiers for **every pair** of classes.
- Each predicts which of the two classes the sample belongs to.
- Final decision by **voting** or **confidence weighting**.

## Summary

- Classification assigns labels using supervised learning.
- Useful for many real-world tasks with labeled data.
- Binary classifiers can be extended for multi-class problems using OvA or OvO.
