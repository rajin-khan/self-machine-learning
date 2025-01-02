# Lecture 9: Introduction to the Cost Function for Linear Regression

### Overview
This lecture introduces the concept of a cost function, a fundamental tool used to evaluate how well a machine learning model performs. Specifically, we examine its role in linear regression, focusing on how it helps adjust parameters to improve model accuracy.

---

### Defining the Cost Function

1. **Key Objective**:
   - The first step in implementing linear regression is defining a cost function to evaluate the model's performance. The cost function quantifies how well or poorly the model predicts the target values.

2. **Training Set**:
   - The dataset consists of input features \(x\) and output targets \(y\).

3. **Linear Model**:
   - The model is represented as:
     \[
     f_{w,b}(x) = w \cdot x + b
     \]
   - Here, \(w\) and \(b\) are the parameters (or coefficients/weights) of the model.

4. **Role of Parameters**:
   - Adjusting \(w\) and \(b\) during training alters the function \(f\), generating different lines on a graph.
   - The parameter \(b\) (intercept) determines where the line crosses the y-axis, while \(w\) (slope) dictates the steepness of the line.

---

### Visualizing Parameters

- **Examples of \(w\) and \(b\)**:
  - \(w = 0, b = 1.5\): Horizontal line at \(y = 1.5\).
  - \(w = 0.5, b = 0\): Line passes through the origin with a slope of 0.5.
  - \(w = 0.5, b = 1\): Line intersects the y-axis at \(b = 1\) and has a slope of 0.5.

- **Fitting the Data**:
  - The objective is to adjust \(w\) and \(b\) such that the line fits the training data points well.

- **Notation**:
  - Training examples are denoted as \((x^i, y^i)\).
  - Predictions are denoted as \(\hat{y}^i\), computed as:
    \[
    \hat{y}^i = f_{w,b}(x^i) = w \cdot x^i + b
    \]

---

### Constructing the Cost Function

1. **Error Term**:
   - The error is the difference between the predicted value \(\hat{y}\) and the true target \(y\):
     \[
     \text{Error} = \hat{y} - y
     \]

2. **Squared Error**:
   - To avoid negative errors canceling out positive errors, square the error:
     \[
     (\hat{y} - y)^2
     \]

3. **Summing Over All Examples**:
   - Compute the total squared error across all training examples:
     \[
     \sum_{i=1}^{m} (\hat{y}^i - y^i)^2
     \]
     - \(m\) is the number of training examples.

4. **Averaging the Error**:
   - To normalize for the number of examples, take the average:
     \[
     \frac{1}{m} \sum_{i=1}^{m} (\hat{y}^i - y^i)^2
     \]

5. **Final Cost Function**:
   - By convention, include a factor of \(\frac{1}{2}\) to simplify future calculations:
     \[
     J(w,b) = \frac{1}{2m} \sum_{i=1}^{m} \left( f_{w,b}(x^i) - y^i \right)^2
     \]
   - This is called the **squared error cost function** and is widely used in linear regression.

---

### Understanding \(J(w,b)\)

1. **Large \(J(w,b)\):**
   - Indicates a poor fit; the predictions \(\hat{y}\) are far from the actual targets \(y\).

2. **Small \(J(w,b)\):**
   - Indicates a good fit; the predictions are close to the targets.

3. **Objective**:
   - The goal is to find values for \(w\) and \(b\) that minimize \(J(w,b)\).

---

### Summary

The cost function provides a quantitative measure of how well the model fits the data. By minimizing \(J(w,b)\), we adjust \(w\) and \(b\) to improve the model's accuracy. In the next lecture, we will explore the intuition behind \(J(w,b)\) further and discuss how to compute the optimal parameters.