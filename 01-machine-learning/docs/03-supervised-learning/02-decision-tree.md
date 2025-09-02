[< Back to Machine Learning with Python](../../README.md)

# Decision Trees for Machine Learning

## What is a Decision Tree?

- **Algorithm for classification** represented as a **flowchart**.
- **Internal node** = test on a feature.
- **Branch** = result of the test.
- **Leaf node** = assigned class (prediction).
- Highly interpretable → shows _how_ decisions are made.

---

## Example: Drug Prescription

- Features: **age, gender, blood pressure, cholesterol**.
- Target: drug (A or B) prescribed.
- Decision Tree rules:
  - Middle-aged → Drug B.
  - Young + male → Drug B.
  - Senior + normal cholesterol → Drug B.
  - Young + female → Drug A.
  - Senior + high cholesterol → Drug A.

---

## How Decision Trees Learn

1. **Start with root node** and labeled data.
2. **Select best feature** (splitting criterion) → split data into branches.
3. Continue splitting **recursively** (recursive partitioning).
4. Stop when:
   - All nodes contain a single class.
   - No features left.
   - **Stopping criteria** met (max depth, min samples per node/leaf, max leaves).

---

## Stopping & Pruning

- **Stopping criteria:**
  - Max tree depth reached.
  - Minimum number of samples per node/leaf exceeded.
  - Max number of leaf nodes reached.
- **Pruning:**
  - Cut branches that don’t improve performance.
  - Prevents **overfitting**.
  - Produces simpler, more generalizable, and more accurate trees.

---

## Splitting Criteria

- **Entropy (measure of randomness):**

  - $Entropy = -\sum p_i \log_2(p_i)$
  - 0 = pure node (homogeneous).
  - 1 = maximum disorder (equal split).

- **Information Gain (IG):**

  - $IG = Entropy(before) - Weighted\ Entropy(after)$
  - Higher IG = better feature for splitting.

- **Gini Impurity:**
  - Another common metric (not detailed in transcript).

---

## Advantages

- Easy to **visualize and interpret**.
- Provides **feature importance** (features chosen near root are most predictive).
- Works with categorical and numerical data.
- Handles multi-class problems.

---

## Key Takeaways

- Decision Tree = **flowchart-based classifier**.
- Built via **recursive partitioning** with **splitting criteria** (IG, entropy, Gini).
- **Pruning** avoids overfitting and simplifies the model.
- Advantage = interpretability, visualization, and feature importance insights.

[< Back to Machine Learning with Python](../../README.md)
