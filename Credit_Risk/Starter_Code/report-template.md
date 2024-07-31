
# Credit Risk Analysis Report

## Overview of the Analysis

In this analysis, we aimed to build a machine learning model to predict the risk of loan default using financial data from a lending institution. The primary purpose of this analysis is to identify high-risk loans to better manage credit risk.

The data provided includes various financial attributes and the loan status, where a value of `0` in the `loan_status` column indicates a healthy loan, and a value of `1` indicates a high-risk loan. Our goal was to predict the `loan_status` using the other financial attributes as features.

### Data Information
- The data was read from `lending_data.csv`.
- The label (`y`) was derived from the `loan_status` column.
- The features (`X`) included the remaining columns.

### Machine Learning Process
1. **Data Splitting**: The data was split into training and testing sets using `train_test_split`.
2. **Modeling**: A logistic regression model (`LogisticRegression`) was trained using the training data.
3. **Evaluation**: The model was evaluated on the testing data using a confusion matrix and a classification report.

### Methods Used
- **Logistic Regression**: This algorithm was used due to its suitability for binary classification problems like predicting loan status.

## Results

### Machine Learning Model 1: Logistic Regression
- **Accuracy Score**: 0.99
- **Precision Score**:
  - Healthy Loan (0): 1.00
  - High-Risk Loan (1): 0.85
- **Recall Score**:
  - Healthy Loan (0): 1.00
  - High-Risk Loan (1): 0.91

## Summary

The logistic regression model demonstrates a high overall accuracy of 99%, with perfect precision and recall for predicting healthy loans (0). For high-risk loans (1), the precision is 0.85 and the recall is 0.91, which are still relatively high but indicate some room for improvement.

### Recommendation
Based on the results, the logistic regression model is recommended for use in predicting loan defaults. The model performs exceptionally well in predicting healthy loans, which are the majority class, and reasonably well in predicting high-risk loans. This model is beneficial for managing credit risk effectively, as it can accurately identify most high-risk loans while maintaining high accuracy for healthy loans.

### Considerations
- While the model performs well overall, further improvements could be made to enhance the precision and recall for high-risk loans.
- Depending on the business requirement, if predicting high-risk loans is more critical, additional techniques like handling class imbalance or using more complex algorithms could be explored.

This comprehensive analysis and the resulting logistic regression model provide a robust tool for predicting loan defaults, aiding in better credit risk management for the lending institution.
