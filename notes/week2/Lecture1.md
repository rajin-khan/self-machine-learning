# Lecture 1: Linear Regression with Multiple Features (Multiple Linear Regression)

- In **linear regression**, we initially dealt with a single feature \(x\) (e.g., size of a house) to predict \(y\) (e.g., house price). The model was defined as:  
  \[
  f_{w,b}(x) = wx + b
  \]

- **Multiple Features:**  
  When more information is available (e.g., number of bedrooms, floors, age of the house), the model can be extended to use multiple features:
  \[
  f_{w,b}(\mathbf{x}) = w_1x_1 + w_2x_2 + \dots + w_nx_n + b
  \]

  **Key Terms:**
  - \(x_1, x_2, x_3, ..., x_n\): Features (e.g., size, bedrooms, etc.)
  - \(w_1, w_2, w_3, ..., w_n\): Parameters (weights) corresponding to each feature
  - \(b\): Bias term
  - \(n\): Total number of features

#### **Example**
For housing price prediction:
\[
f_{w,b}(\mathbf{x}) = 0.1x_1 + 4x_2 + 10x_3 - 2x_4 + 80
\]
  - \(x_1\): Size of the house (sq. ft)
  - \(x_2\): Number of bedrooms
  - \(x_3\): Number of floors
  - \(x_4\): Age of the house (years)

  **Interpretation of Parameters:**
  - \(b = 80\): Base price (\$80,000) if all features are zero.
  - \(w_1 = 0.1\): House price increases by \$100 for each additional square foot.
  - \(w_2 = 4\): Price increases by \$4,000 for each additional bedroom.
  - \(w_3 = 10\): Price increases by \$10,000 for each additional floor.
  - \(w_4 = -2\): Price decreases by \$2,000 for each additional year of age.

---

### **Vector Representation and Notation**

To simplify notation and implementation:
- Define \( \mathbf{w} \): A **vector** (list) of parameters \([w_1, w_2, ..., w_n]\)
- Define \( \mathbf{x} \): A **vector** (list) of features \([x_1, x_2, ..., x_n]\)
- Use the **dot product** (\( \mathbf{w} \cdot \mathbf{x} \)) to represent the weighted sum of features:
\[
f_{w,b}(\mathbf{x}) = \mathbf{w} \cdot \mathbf{x} + b
\]
  - The dot product \( \mathbf{w} \cdot \mathbf{x} \) is computed as:
    \[
    \mathbf{w} \cdot \mathbf{x} = w_1x_1 + w_2x_2 + \dots + w_nx_n
    \]

This **compact notation** makes the mathematical representation concise and paves the way for efficient computation.

---

### **Key Differences**
- **Univariate Regression:** Linear regression with one feature (e.g., size of a house).
- **Multiple Linear Regression:** Linear regression with multiple features (e.g., size, bedrooms, floors, age).

---

### **Next Steps: Vectorization**
- **Vectorization** is a technique to efficiently implement algorithms like multiple linear regression.  
- It leverages matrix and vector operations to reduce computational time and simplify implementation.  