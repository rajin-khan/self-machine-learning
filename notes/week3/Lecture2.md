# Lecture 2: Logistic Regression Overview

Logistic regression is one of the most widely used classification algorithms, frequently applied in various domains. For instance, it can classify whether a tumor is malignant or benign. Here, the positive class (malignant) is represented as 1, and the negative class (benign) is represented as 0. Unlike linear regression, which is not suitable for such binary classification problems, logistic regression fits an S-shaped curve (sigmoid curve) to the dataset.

### Example: Tumor Classification

The dataset is visualized with the tumor size on the x-axis and the binary label (0 or 1) on the y-axis. If a tumor size corresponds to an algorithm output of 0.7, it indicates a 70% probability that the tumor is malignant. However, the output label (y) is always 0 or 1.

### The Sigmoid Function

The sigmoid function, also known as the logistic function, is key to logistic regression. It maps any real-valued number to a value between 0 and 1.

#### Formula:
\[ g(z) = \frac{1}{1 + e^{-z}} \]

- **e** is the mathematical constant (approximately 2.718).
- When \(z\) is large (e.g., 100), \(e^{-z}\) approaches 0, making \(g(z)\) close to 1.
- When \(z\) is a large negative number, \(g(z)\) approaches 0.
- When \(z = 0\), \(g(z) = 0.5\), which explains why the sigmoid curve crosses the vertical axis at 0.5.

### Logistic Regression Model

Logistic regression involves two steps:
1. Compute \(z\) as a linear function:
   \[ z = w \cdot x + b \]
   - Here, \(w\) represents the weights, \(x\) represents the input features, and \(b\) is the bias.
2. Pass \(z\) through the sigmoid function:
   \[ g(z) = \frac{1}{1 + e^{-z}} \]

Combining these steps gives the logistic regression model:
\[ f(x) = g(w \cdot x + b) \]

This model outputs a value between 0 and 1, representing the probability that the label \(y\) equals 1 for the given input \(x\).

### Interpreting the Output

The output of logistic regression can be interpreted as the probability that \(y = 1\) given the input \(x\):
\[ P(y=1 \mid x; w, b) \]

For example, if the model predicts 0.7 for a tumor size \(x\), it implies a 70% chance that the tumor is malignant. The probability of \(y = 0\) is then 1 - 0.7 = 0.3.

### Notation

In some contexts, the logistic regression model is represented as:
\[ f(x) = P(y = 1 \mid x; w, b) \]

Here:
- \(w\) and \(b\) are the model parameters.
- The vertical bar \(|\) denotes conditional probability.

### Applications

Logistic regression has been pivotal in fields such as Internet advertising, where it predicts the likelihood of user actions like clicking on ads. While more advanced algorithms are now in use, logistic regression remains a foundational tool for binary classification tasks.

### Next Steps

In the following lessons, we will explore:
- Visualizations of logistic regression.
- Decision boundaries, which map the continuous output (e.g., 0.3, 0.7) to discrete predictions (0 or 1).
- Implementation details and code examples for the sigmoid function and logistic regression.