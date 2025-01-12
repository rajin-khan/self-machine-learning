# Lecture 7: Gradient Descent Convergence and Learning Curves

Gradient descent is a widely used optimization algorithm to find parameters \( w \) and \( b \) that minimize the cost function \( J \). To ensure it is converging properly, here are key steps and insights:

---

### **Gradient Descent Rule Recap**
- Gradient descent updates parameters using the rule:
  \[
  w := w - \alpha \frac{\partial J}{\partial w}, \quad b := b - \alpha \frac{\partial J}{\partial b}
  \]
  where \( \alpha \) is the learning rate.

---

### **Monitoring Convergence**
- **Key Insight**: Gradient descent minimizes \( J \). Plotting \( J \) over the number of iterations provides insights into convergence.  
- **Learning Curve**: The graph of cost \( J \) versus the number of iterations is a learning curve.  

---

### **Characteristics of a Well-Behaved Learning Curve**
1. **Decreasing Cost**:  
   - \( J \) should decrease after each iteration.  
   - If \( J \) increases, it usually indicates:  
     - Learning rate \( \alpha \) is too large.  
     - A bug in the code.  

2. **Convergence**:  
   - When \( J \) flattens or levels off (e.g., by 300-400 iterations in an example), it indicates that gradient descent has converged.

3. **Iteration Count**:  
   - The number of iterations for convergence varies by application:  
     - Some cases may converge after 30 iterations.  
     - Others may require 1,000 or more.  
   - It's challenging to predict this number in advance, which is why monitoring the learning curve is helpful.  

---

### **Automatic Convergence Test**
- **Threshold \( \epsilon \) (Epsilon)**:  
  - Define \( \epsilon \) (e.g., 0.001 or \( 10^{-3} \)).  
  - If the decrease in \( J \) is smaller than \( \epsilon \) between iterations, declare convergence.  
  - Example:
    \[
    \text{If } J^{(t)} - J^{(t+1)} < \epsilon, \text{ stop training.}
    \]
- **Practical Note**:  
  - While useful, choosing the right \( \epsilon \) can be difficult.  
  - Visual inspection of the learning curve often provides better insights.

---

### **Importance of Monitoring**
- By examining the learning curve:  
  - You ensure \( J \) decreases consistently.  
  - Spot potential issues with \( \alpha \) or implementation bugs early.  
- **Rule of Thumb**: Aim for a smooth, decreasing curve until leveling off.

---

### **Next Step**
- The next focus is on **choosing the learning rate \( \alpha \)**. Selecting an appropriate \( \alpha \) ensures smooth convergence and faster optimization.