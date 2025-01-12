# Lecture 8: Choosing an Appropriate Learning Rate (\( \alpha \)) for Gradient Descent

Selecting the correct learning rate is critical for the effective and efficient training of gradient descent. A poorly chosen learning rate can lead to convergence issues or prolonged training times. Here’s how to identify and tune the learning rate effectively:  

---

### **Impact of Learning Rate on Gradient Descent**  

1. **If the Learning Rate is Too Large**:  
   - **Behavior**: Gradient descent may overshoot the minimum, causing the cost \( J \) to oscillate or even increase.  
   - **Visualization**:  
     - Updates might "jump" back and forth, never settling at the global minimum.  
   - **Fix**: Reduce the learning rate \( \alpha \).  

2. **If the Learning Rate is Too Small**:  
   - **Behavior**: Gradient descent progresses very slowly, requiring many iterations to converge.  
   - **Fix**: Increase the learning rate \( \alpha \).  

3. **Cost Consistently Increasing**:  
   - **Possible Reasons**:  
     - \( \alpha \) is too large.  
     - There’s a bug in the code, such as using \( w_1 + \alpha \times \text{derivative term} \) instead of \( w_1 - \alpha \times \text{derivative term} \).  
   - **Debugging Tip**: Use a very small \( \alpha \) to ensure the cost decreases on every iteration. If not, inspect the implementation for errors.  

---

### **Steps to Choose a Good Learning Rate**  

1. **Experiment with Multiple Values**:  
   - Start with a small \( \alpha \), such as \( 0.001 \), and test progressively larger values.  
   - Example values: \( 0.001 \), \( 0.003 \), \( 0.01 \), \( 0.03 \), \( 0.1 \), \( 0.3 \), and so on.  
   - Each \( \alpha \) should be roughly **three times larger** than the previous value.  

2. **Observe the Learning Curve**:  
   - Plot \( J \) as a function of iterations for each \( \alpha \).  
   - Look for the largest \( \alpha \) that consistently decreases \( J \) without causing oscillations or divergence.  

3. **Find the "Too Small" and "Too Large" Boundaries**:  
   - Identify values of \( \alpha \) that are:  
     - **Too Small**: Converges too slowly.  
     - **Too Large**: Causes divergence or instability.  
   - Pick a value slightly smaller than the largest reasonable \( \alpha \).  

4. **Debugging with Small \( \alpha \)**:  
   - Temporarily set \( \alpha \) to a very small value.  
   - If \( J \) still does not decrease, check for bugs in the code.  

---

### **Example Scenarios of Learning Rates**  

1. **Oscillations in Cost**:  
   - Likely due to \( \alpha \) being too large.  

2. **Cost Increases Every Iteration**:  
   - Could be a result of:  
     - Learning rate too large.  
     - Code implementation bug.  

3. **Smooth and Rapid Decrease in Cost**:  
   - Indicates a well-chosen \( \alpha \).  

---

### **Trade-offs**  

- **Small \( \alpha \)**: Safer for debugging but leads to inefficient training.  
- **Large \( \alpha \)**: Faster training but risk of divergence or instability.  

---

### **Using Feature Scaling**  

- Feature scaling can further improve the efficiency of gradient descent, allowing it to converge faster for a wider range of learning rates.  
- Experiment with feature scaling techniques alongside tuning \( \alpha \).  

---

### **Next Steps**  

In upcoming lessons:  
- Explore how to choose **custom features** to make linear regression more powerful.  
- Learn to fit curves to data instead of just straight lines.  

Experiment with these concepts in the optional lab to develop a deeper intuition about \( \alpha \), feature scaling, and their effects on gradient descent performance.