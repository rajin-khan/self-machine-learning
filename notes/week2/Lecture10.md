# Lecture 10: Polynomial Regression and Feature Engineering

Polynomial regression builds on the ideas of linear regression and feature engineering, allowing models to fit curves or non-linear functions to data. This is particularly useful when data patterns cannot be adequately captured by a straight line.

---

### **Fitting Curves to Data**  

1. **Initial Problem**:  
   - Feature \( x \): Size of a house in square feet.  
   - The data does not align well with a straight-line model.

2. **Quadratic Model**:  
   - Includes \( x \) and \( x^2 \) (size and size squared).  
   - A better fit to the data, but quadratic functions eventually decrease, which may not align with real-world expectations for house prices.

3. **Cubic Model**:  
   - Adds \( x^3 \) (size cubed) to the features.  
   - Produces a better fit, with house prices increasing as size increases without unrealistic downturns.

4. **Alternative Feature Transformations**:  
   - **Square Root** (\( \sqrt{x} \)):  
     - A gentler increase compared to linear or polynomial transformations, suitable for certain data patterns.  

---

### **Key Concepts in Polynomial Regression**

1. **Features in Polynomial Models**:  
   - Transform original features into powers (e.g., \( x^2, x^3, \sqrt{x} \)) or combinations to better capture data trends.  

2. **Feature Scaling**:  
   - Essential when adding polynomial features.  
   - Without scaling:  
     - \( x^2 \) might range from 1 to \( 10^6 \) for \( x = 1 \) to \( 1,000 \).  
     - \( x^3 \) might range from 1 to \( 10^9 \).  
   - Scaled features ensure gradient descent converges efficiently by bringing all feature values into a comparable range.

3. **Choice of Features**:  
   - Polynomial features (e.g., \( x^2, x^3 \)) and alternative transformations (e.g., \( \sqrt{x} \)) provide flexibility.  
   - Selecting features involves testing different combinations and evaluating model performance.

---

### **Implementing Polynomial Regression**

1. **Manual Implementation**:  
   - Understand the core algorithm by coding polynomial regression from scratch.  

2. **Using Libraries**:  
   - **Scikit-learn**:  
     - A popular open-source library for machine learning.  
     - Enables implementation of linear and polynomial regression in just a few lines of code.  
     - Widely used by practitioners in AI and machine learning industries.  

3. **Balancing Theory and Practice**:  
   - Learning to code algorithms manually deepens understanding.  
   - Using tools like Scikit-learn demonstrates how machine learning is applied in real-world scenarios.

---

### **Next Steps**  

1. **Practice Labs**:  
   - Implement linear regression and polynomial regression in the provided lab exercises.  
   - Explore Scikit-learn for hands-on experience with advanced tools.  

2. **Transition to Classification**:  
   - In the next week's lessons, move beyond regression (predicting numbers) to classification (predicting categories).  