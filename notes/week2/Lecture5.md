# Lecture 5: Feature Scaling for Faster Gradient Descent

**Introduction to Feature Scaling:**  
Feature scaling is a technique used to enable gradient descent to converge faster by adjusting the range of feature values. When features have different ranges, gradient descent may become inefficient.

---

**Impact of Feature Size on Parameters:**  
- Features with larger ranges often have smaller associated parameter values, while features with smaller ranges have larger parameter values.  
- Example: Predicting house prices with two features:  
  - **x₁ (size of house in square feet)**: Ranges from 300 to 2000.  
  - **x₂ (number of bedrooms)**: Ranges from 0 to 5.  
  - When **x₁** has large values, a smaller parameter (e.g., 0.1) is suitable.  
  - When **x₂** has smaller values, a larger parameter (e.g., 50) is more reasonable.

---

**Challenges with Unscaled Features in Gradient Descent:**  
1. **Elliptical Contours of the Cost Function:**  
   - If features have different ranges, the cost function contours can become tall and skinny ellipses.  
   - This occurs because large ranges in features (e.g., square footage) cause large parameter updates, while smaller ranges (e.g., bedroom count) result in smaller updates.

2. **Inefficient Gradient Descent:**  
   - Gradient descent may oscillate back and forth for a long time along one axis before converging, slowing down the process.

---

**Benefits of Feature Scaling:**  
- Rescaling features so they take on comparable ranges (e.g., both between 0 and 1) results in circular contours for the cost function.  
- Gradient descent converges much faster because it takes a more direct path to the global minimum.

---

**How to Implement Feature Scaling:**  
1. **Normalize Features:**  
   - Adjust each feature to range between 0 and 1 or between -1 and 1.
   - Example formula:  
     \[
     x' = \frac{x - \text{min}(x)}{\text{max}(x) - \text{min}(x)}
     \]
2. **Standardize Features:**  
   - Transform features to have a mean of 0 and a standard deviation of 1.
   - Example formula:  
     \[
     x' = \frac{x - \mu}{\sigma}
     \]
   Where \(\mu\) is the mean, and \(\sigma\) is the standard deviation.

---

**Conclusion:**  
- Feature scaling can significantly speed up gradient descent by eliminating the disparity in feature ranges.  
- In the next lecture, you'll learn practical ways to implement feature scaling in your code and see its impact on the efficiency of gradient descent.