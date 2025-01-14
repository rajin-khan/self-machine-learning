# Lecture 1: Introduction to Classification and Logistic Regression

This lecture introduces **classification** and discusses why **linear regression** is unsuitable for classification problems, leading to the introduction of **logistic regression**, a powerful algorithm widely used for binary classification tasks.

#### Key Concepts of Classification
- **Classification Problems**:
  - The output variable \( y \) can take on one of a few specific values (e.g., yes/no, true/false, or 0/1).
  - Examples:
    - Determining if an email is spam.
    - Identifying fraudulent financial transactions.
    - Classifying tumors as malignant or benign.
    
- **Binary Classification**:
  - A specific type of classification where \( y \) has only two possible outcomes, often represented as:
    - **0 and 1** (common convention in computer science).
    - **False and True**.
    - **Negative and Positive** classes:
      - Example: For spam classification, non-spam emails are the **negative class** (\( y = 0 \)), and spam emails are the **positive class** (\( y = 1 \)).
    - Note: "Negative" and "Positive" are labels and do not imply good or bad.

#### Issues with Linear Regression for Classification
1. **Linear Regression Model**:
   - Tries to fit a straight line through the data, predicting numerical outputs instead of categories.
   - For binary classification, predictions can fall outside the range [0, 1] (e.g., values less than 0 or greater than 1), which is not meaningful.

2. **Using Thresholds**:
   - A threshold (e.g., 0.5) can be applied to interpret predictions:
     - If \( h(x) < 0.5 \), predict \( y = 0 \) (negative class).
     - If \( h(x) \geq 0.5 \), predict \( y = 1 \) (positive class).
   - However, this approach is problematic:
     - Adding outliers or distant examples can significantly distort the model.
     - The decision boundary (where \( h(x) = 0.5 \)) may shift inappropriately, leading to incorrect classifications.

3. **Example**:
   - A training set for tumor classification (malignant \( y = 1 \), benign \( y = 0 \)):
     - A linear regression model fits a line and uses a threshold to classify examples.
     - Adding a new data point far from the existing examples can shift the line and decision boundary, affecting the classification of other points.

#### Introducing Logistic Regression
- Logistic regression is designed specifically for classification:
  - Output is always between 0 and 1.
  - Provides better handling of binary classification tasks by avoiding issues with linear regression.

- **Why "Logistic Regression"?**
  - Despite the term "regression," logistic regression is used for classification.
  - The name is historical and does not reflect its primary purpose.

#### Practical Learning
- **Optional Lab**:
  - Explore the use of linear regression for classification and observe its limitations.
  - Motivates the need for a model like logistic regression.
  
- **Upcoming Topics**:
  - Learn about **decision boundaries** and their role in classification.
  - Deep dive into **logistic regression** for binary classification problems.

### Summary
- Classification focuses on predicting discrete categories instead of continuous values.
- Linear regression is unsuitable for classification due to its inability to limit predictions within [0, 1].
- Logistic regression is introduced as a solution, offering bounded predictions and effective classification.
- Further exploration of logistic regression and its decision boundaries will follow in subsequent lectures.