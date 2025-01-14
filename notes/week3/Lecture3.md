# Lecture 3: Logistic Regression and Decision Boundaries

**Recap of Logistic Regression Model:**
1. Logistic regression predicts probabilities using the sigmoid (logistic) function.
2. The model computes predictions in two steps:
   - Compute \( z = w \cdot x + b \)
   - Apply the sigmoid function \( g(z) = \frac{1}{1 + e^{-z}} \)
3. The output \( f(x) \) can be interpreted as the probability that \( y = 1 \) given \( x \):
   - \( P(y = 1 | x; w, b) = f(x) \)
   - Example: If \( f(x) = 0.7 \), there is a 70% chance that \( y = 1 \).

**Threshold-Based Predictions:**
- To predict whether \( y \) is 0 or 1, a threshold is set:
  - If \( f(x) \geq 0.5 \), predict \( \hat{y} = 1 \).
  - If \( f(x) < 0.5 \), predict \( \hat{y} = 0 \).
- The threshold can be adjusted based on application-specific requirements.

**Understanding Decision Boundaries:**
- A decision boundary is where the model transitions from predicting 0 to predicting 1.
- For logistic regression:
  - \( f(x) \geq 0.5 \) implies \( g(z) \geq 0.5 \).
  - From the sigmoid function graph, \( g(z) \geq 0.5 \) when \( z \geq 0 \).
  - \( z = w \cdot x + b \):
    - If \( z \geq 0 \), predict 1.
    - If \( z < 0 \), predict 0.

**Visualization of Decision Boundaries with Two Features (x₁ and x₂):**
- Example:
  - Dataset: Red crosses (\( y = 1 \)), Blue circles (\( y = 0 \))
  - Model: \( f(x) = g(w_1x_1 + w_2x_2 + b) \)
  - Parameters: \( w_1 = 1 \), \( w_2 = 1 \), \( b = -3 \).
  - Decision boundary equation: \( x_1 + x_2 - 3 = 0 \).
  - Visualization:
    - Points to the right of the line (\( x_1 + x_2 \geq 3 \)) are predicted as \( y = 1 \).
    - Points to the left are predicted as \( y = 0 \).

**Non-Linear Decision Boundaries with Polynomial Features:**
1. Adding polynomial terms allows for more complex decision boundaries.
   - Example: \( z = w_1x_1^2 + w_2x_2^2 + b \).
2. Decision boundary for parameters \( w_1 = 1 \), \( w_2 = 1 \), \( b = -1 \):
   - \( x_1^2 + x_2^2 = 1 \).
   - Visualization:
     - Inside the circle (\( x_1^2 + x_2^2 < 1 \)), predict \( y = 0 \).
     - Outside the circle (\( x_1^2 + x_2^2 \geq 1 \)), predict \( y = 1 \).

**Higher-Order Polynomials for Complex Decision Boundaries:**
- Example: \( z = w_1x_1 + w_2x_2 + w_3x_1^2 + w_4x_1x_2 + w_5x_2^2 \).
- Enables shapes like ellipses, complex curves, or other intricate decision boundaries.
- Logistic regression can handle complex datasets with these additional features.

**Linear vs. Non-Linear Decision Boundaries:**
- If only linear features (\( x_1, x_2, x_3, \dots \)) are used, the decision boundary is always a straight line.
- Including higher-order polynomial features allows logistic regression to fit non-linear patterns.

**Next Steps:**
1. Learn about the cost function for logistic regression.
2. Understand how gradient descent optimizes the model parameters.
3. Explore an optional lab to visualize decision boundaries in code with two features.

By understanding decision boundaries, we gain insight into how logistic regression computes predictions and adapts to data complexity.