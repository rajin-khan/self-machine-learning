# Lecture 6: Feature Scaling Techniques

### **What is Feature Scaling?**
Feature scaling is a preprocessing technique used to transform data so that features take on comparable ranges of values. This helps gradient descent converge faster and more effectively by addressing disparities in feature ranges.

---

### **Methods of Feature Scaling**
1. **Scaling by Maximum Value**
   - Divide each feature value by the maximum value in its range.
   - Example:
     - \( x_1 \): Original range \( [300, 2000] \)
       - \( \text{Scaled } x_1 = \frac{x_1}{2000} \), resulting in a range of \( [0.15, 1] \).
     - \( x_2 \): Original range \( [0, 5] \)
       - \( \text{Scaled } x_2 = \frac{x_2}{5} \), resulting in a range of \( [0, 1] \).

2. **Mean Normalization**
   - Rescale features to center them around 0, achieving a typical range of \([-1, 1]\).
   - Formula:
     \[
     \text{Normalized } x_i = \frac{x_i - \mu_i}{\text{max}_i - \text{min}_i}
     \]
     - \( \mu_i \): Mean of the feature.
     - \( \text{max}_i, \text{min}_i \): Maximum and minimum values of the feature.
   - Example:
     - \( x_1 \): Original range \( [300, 2000] \), mean \( \mu_1 = 600 \).
       - \( \text{Normalized } x_1 = \frac{x_1 - 600}{2000 - 300} \), resulting in a range of \( [-0.18, 0.82] \).
     - \( x_2 \): Original range \( [0, 5] \), mean \( \mu_2 = 2.3 \).
       - \( \text{Normalized } x_2 = \frac{x_2 - 2.3}{5 - 0} \), resulting in a range of \( [-0.46, 0.54] \).

3. **Z-Score Normalization**
   - Normalize features by subtracting the mean and dividing by the standard deviation (\( \sigma \)).
   - Formula:
     \[
     \text{Z-Score } x_i = \frac{x_i - \mu_i}{\sigma_i}
     \]
     - \( \sigma_i \): Standard deviation of the feature.
   - Example:
     - \( x_1 \): Mean \( \mu_1 = 600 \), standard deviation \( \sigma_1 = 450 \).
       - \( \text{Z-Score } x_1 = \frac{x_1 - 600}{450} \), resulting in a range of \( [-0.67, 3.1] \).
     - \( x_2 \): Mean \( \mu_2 = 2.3 \), standard deviation \( \sigma_2 = 1.4 \).
       - \( \text{Z-Score } x_2 = \frac{x_2 - 2.3}{1.4} \), resulting in a range of \( [-1.6, 1.9] \).

---

### **When to Perform Feature Scaling**
- Features with drastically different ranges should be scaled.
- Examples:
  - A feature ranging from \([-100, 100]\) or \([98.6, 105]\) might require scaling to bring values closer to \([-1, 1]\).
  - Very small ranges (e.g., \([-0.001, 0.001]\)) should also be rescaled for better gradient descent performance.
- If features already have comparable ranges, feature scaling may be optional.

---

### **General Guidelines**
- Aim for feature values to be roughly between \([-1, 1]\), though small deviations (e.g., \([-0.3, 0.3]\) or \([-3, 3]\)) are acceptable.
- If in doubt, scaling the features is recommended, as it rarely causes harm.

---

### **Why Feature Scaling Helps**
- Unscaled features can result in elongated and narrow contour plots of the cost function, leading to slow convergence.
- Rescaling features results in more circular contours, allowing gradient descent to find the global minimum more efficiently.

---

### **Takeaways**
- Feature scaling significantly improves gradient descent performance.
- Choose a scaling method (maximum scaling, mean normalization, or Z-score normalization) based on the dataset and problem context.
- Always consider scaling features that vary widely in range to ensure smoother convergence of gradient descent.