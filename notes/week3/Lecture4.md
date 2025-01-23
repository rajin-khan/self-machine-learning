# **Lecture Notes: Cost Function for Logistic Regression**

- The **cost function** measures how well a set of parameters (weights \(w\) and bias \(b\)) fits the training data. It guides the model to choose better parameters.

- **Squared Error Cost Function** is commonly used in linear regression but not suitable for logistic regression:
  - Logistic regression uses the sigmoid function \(f(x) = \frac{1}{1 + e^{-(wx + b)}}\), which leads to a non-convex cost function if squared error is used.
  - A **non-convex cost function** has multiple local minima, making gradient descent unreliable.

### Logistic Regression Loss Function
- A new loss function ensures a **convex cost function**, making gradient descent converge to the **global minimum**.

1. **Loss for a Single Training Example**:
   - The loss function is defined as \(L(f(x), y)\), where:
     - \(f(x)\) is the model's prediction.
     - \(y\) is the true label (0 or 1).
   - The loss function depends on \(y\):
     - If \(y = 1\): Loss = \(-\log(f(x))\)
     - If \(y = 0\): Loss = \(-\log(1 - f(x))\)

2. **Intuition for the Loss Function**:
   - **Case 1: \(y = 1\)**:
     - If \(f(x)\) (prediction) is close to 1, the loss is small (model is accurate).
     - If \(f(x)\) is far from 1, the loss increases significantly.
   - **Case 2: \(y = 0\)**:
     - If \(f(x)\) is close to 0, the loss is small.
     - If \(f(x)\) is far from 0 (close to 1), the loss increases steeply.

3. **Cost Function for the Entire Training Set**:
   - The cost function \(J(w, b)\) is the average loss across all training examples:
     \[
     J(w, b) = \frac{1}{m} \sum_{i=1}^{m} L(f(x_i), y_i)
     \]
   - Convexity of the logistic regression cost function ensures that gradient descent converges reliably to the global minimum.

### Summary
- **Key Issues with Squared Error in Logistic Regression**:
  - Non-convex cost function.
  - Inefficient convergence using gradient descent.
- **Advantages of the New Logistic Loss Function**:
  - Convex cost function ensures stable and reliable optimization.
  - Penalizes incorrect predictions effectively, encouraging accurate probability estimates.

In the next steps, we will:
- Derive the full cost function for logistic regression.
- Simplify its expression for efficient computation.
- Use it with gradient descent to optimize parameters.