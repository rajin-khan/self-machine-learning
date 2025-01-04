# Lecture 5: Classification in Supervised Learning

## Overview of Supervised Learning
Supervised learning algorithms map input (x) to output (y) by learning from labeled datasets. While regression predicts continuous numerical values, classification algorithms predict discrete categories or classes.

---

## Classification Algorithms
Classification is a type of supervised learning where the algorithm predicts categories instead of continuous values. For example:

- **Regression** predicts from an infinite range of possible numbers (e.g., housing prices).
- **Classification** predicts a small, finite set of possible categories (e.g., spam vs. not spam).

---

## Breast Cancer Detection: A Real-World Example of Classification

### Problem:
Build a machine learning system to help doctors diagnose breast cancer by classifying tumors as benign or malignant.

### Dataset:
- Inputs:
  - **Tumor size**
  - Additional features: patient’s age, thickness of the tumor clump, uniformity of cell size and shape, etc.
- Output classes:
  - Benign (denoted as 0)
  - Malignant (denoted as 1)

### Visualization:
- Tumor size is plotted on the horizontal axis.
- The vertical axis represents the categories:
  - 0 (benign)
  - 1 (malignant)
- Data points are marked:
  - Circles (○): Benign tumors
  - Crosses (✕): Malignant tumors

### Key Points:
- Classification predicts one of a small, finite set of outputs. In this example, the outputs are **0 or 1**.
- New data points are classified based on their features.

---

## Multi-Class Classification
Classification can involve more than two categories. For example:

- If malignant tumors are further categorized into types (e.g., Type 1 and Type 2), the system predicts:
  - 0: Benign
  - 1: Malignant (Type 1)
  - 2: Malignant (Type 2)

In this case, there are three output classes: **0, 1, and 2**.

---

## Input Features in Classification
Most real-world classification problems use multiple input features. For instance:

- **Input features:**
  - Tumor size
  - Patient’s age
  - Tumor clump thickness
  - Uniformity of cell size/shape

### Example:
- Plot tumor size (x-axis) against patient’s age (y-axis).
- Data points:
  - Circles (○): Benign tumors
  - Crosses (✕): Malignant tumors
- A decision boundary separates benign from malignant tumors.

The algorithm’s goal is to find the best boundary that helps classify new data points accurately.

---

## Comparison of Regression and Classification
| **Aspect**                | **Regression**                     | **Classification**                 |
|---------------------------|-------------------------------------|-------------------------------------|
| **Output**               | Continuous numerical values        | Discrete categories or labels      |
| **Example**              | Predicting house prices            | Breast cancer detection            |
| **Possible Outputs**     | Infinite (e.g., 0.5, 1.7, etc.)    | Finite (e.g., 0, 1, 2, etc.)       |
| **Interpretation**       | Predicts values in a continuous range | Predicts a limited set of categories |

---

## Key Takeaways
- Classification algorithms predict discrete categories (e.g., benign vs. malignant).
- Categories can be binary (e.g., 0, 1) or multi-class (e.g., 0, 1, 2).
- Input features can include one or more variables (e.g., tumor size, patient’s age).
- The algorithm learns a decision boundary to separate categories for new predictions.

In the next lecture, we will explore unsupervised learning and its applications.

