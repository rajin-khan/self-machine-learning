# Lecture 6: Logistic Regression - Gradient Descent Implementation

To train a **logistic regression** model, we need to determine the optimal values for the parameters \( w \) and \( b \) that minimize the cost function \( J(w, b) \). This ensures that the model makes accurate predictions when given new input data.

---

### **Understanding Logistic Regression Predictions**
- Given a new input \( x \) (e.g., a patient's tumor size and age), the model estimates the probability that the label \( y = 1 \).
- The function \( f(x) \) used in logistic regression is the **sigmoid function**:
  \[
  f(x) = \frac{1}{1 + e^{-(wx + b)}}
  \]
- This function ensures that the predicted output lies in the range \( [0, 1] \), making it ideal for **binary classification**.

---

### **Gradient Descent for Logistic Regression**
To minimize the **cost function**, we use **gradient descent**, an iterative optimization algorithm that updates the parameters in the direction of the negative gradient.

#### **Cost Function Recap**
The logistic regression cost function is:
\[
J(w, b) = -\frac{1}{m} \sum_{i=1}^{m} \left[ y^{(i)} \log f(x^{(i)}) + (1 - y^{(i)}) \log (1 - f(x^{(i)})) \right]
\]

Where:
- \( m \) is the number of training examples.
- \( f(x^{(i)}) \) is the model's predicted probability for the \( i \)-th example.
- \( y^{(i)} \) is the actual label (0 or 1).

---

### **Gradient Descent Update Equations**
For each iteration of gradient descent, we update \( w \) and \( b \) using:

\[
w_j := w_j - \alpha \frac{\partial J}{\partial w_j}
\]
\[
b := b - \alpha \frac{\partial J}{\partial b}
\]

Where \( \alpha \) is the **learning rate** (controls the step size).

#### **Gradient Calculation**
Using calculus, we derive:

\[
\frac{\partial J}{\partial w_j} = \frac{1}{m} \sum_{i=1}^{m} \left( f(x^{(i)}) - y^{(i)} \right) x_j^{(i)}
\]

\[
\frac{\partial J}{\partial b} = \frac{1}{m} \sum_{i=1}^{m} \left( f(x^{(i)}) - y^{(i)} \right)
\]

These gradients represent the average error across all training examples.

---

### **Simultaneous Updates**
- Compute the right-hand side for all updates.
- Then, **simultaneously update** all parameters to prevent dependency issues.
- This ensures **efficient learning**.

---

### **Why Do the Equations Look Like Linear Regression?**
- The gradient descent equations for logistic regression **appear similar** to those in linear regression.
- **Key difference:**  
  - In **linear regression**, \( f(x) = wx + b \).
  - In **logistic regression**, \( f(x) = \sigma(wx + b) \), where \( \sigma \) is the sigmoid function.
- Despite the similar equations, they are **different algorithms** due to the non-linearity introduced by the sigmoid function.

---

### **Ensuring Convergence**
- Similar to linear regression, we monitor **gradient descent convergence** by:
  - Checking if the cost function decreases with each iteration.
  - Using techniques like **feature scaling** to speed up convergence.

---

### **Vectorization for Efficiency**
- Instead of computing updates for each parameter separately, we use **vectorized implementations** to optimize computations.
- This significantly speeds up training, especially for large datasets.

---

### **Feature Scaling for Faster Convergence**
- Scaling features (e.g., normalizing them between \(-1\) and \(+1\)) ensures that gradient descent **converges faster**.
- Prevents features with large values from dominating the updates.

---

### **Implementation in Scikit-Learn**
- A **popular Python library**, `scikit-learn`, provides built-in functions for logistic regression.
- Learning how to use it is essential for real-world applications.

---

### **Summary**
- **Logistic regression** models probabilities using the **sigmoid function**.
- **Gradient descent** is used to minimize the cost function by updating \( w \) and \( b \).
- The **update equations** for gradient descent look similar to those of linear regression but differ due to the sigmoid function.
- **Vectorization** and **feature scaling** improve efficiency.
- **Scikit-learn** provides a practical way to implement logistic regression.

After understanding these concepts, the next step is to implement gradient descent for logistic regression in **code** and visualize the learning process using **contour plots, cost function evolution, and learning curves**.