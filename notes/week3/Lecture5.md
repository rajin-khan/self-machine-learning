
# Lecture 5: Simplifying the Loss and Cost Functions in Logistic Regression

**1. Recap of the Loss Function for Logistic Regression**  
   - Logistic regression is applied to binary classification problems where the target label \( y \) is either 0 or 1.
   - The original loss function was defined as two separate cases:
     - When \( y = 1 \): \( -\log(f(x)) \)
     - When \( y = 0 \): \( -\log(1 - f(x)) \)

**2. Simplified Loss Function**  
   - The loss function can be rewritten into a single equation:  
     \[
     \text{Loss} = -y \cdot \log(f(x)) - (1 - y) \cdot \log(1 - f(x))
     \]
   - This expression works for both cases:
     - **Case 1**: If \( y = 1 \), \( 1 - y = 0 \), and the loss reduces to \( -\log(f(x)) \).
     - **Case 2**: If \( y = 0 \), \( y = 0 \) and the loss reduces to \( -\log(1 - f(x)) \).

**3. Cost Function for Logistic Regression**  
   - The cost function \( J \) is defined as the average loss across all \( m \) training examples:  
     \[
     J(\theta) = \frac{1}{m} \sum_{i=1}^{m} \text{Loss}_i
     \]
   - Substituting the simplified loss function:  
     \[
     J(\theta) = -\frac{1}{m} \sum_{i=1}^{m} \left[ y^{(i)} \cdot \log(f(x^{(i)})) + (1 - y^{(i)}) \cdot \log(1 - f(x^{(i)})) \right]
     \]

**4. Why Use This Cost Function?**  
   - The cost function is derived from **maximum likelihood estimation (MLE)**, a statistical principle for efficiently finding model parameters.
   - It has the property of being **convex**, which ensures a single global minimum, making gradient descent optimization more straightforward.

**5. Practical Insights from the Cost Function**  
   - In the optional lab, you'll:
     - Implement the logistic cost function in code.
     - Explore how different parameter choices affect the cost function.
   - A plot comparing two decision boundaries (blue and magenta) demonstrates:
     - A better-fitting decision boundary (blue) has a **lower cost**.
     - This highlights the importance of minimizing the cost for better model fitting.

**6. Next Steps**  
   - With the simplified loss and cost functions, the next topic will cover **applying gradient descent** to logistic regression.