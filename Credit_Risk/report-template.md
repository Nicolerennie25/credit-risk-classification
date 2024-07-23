# Module 12 Report Template

## Overview of the Analysis

In this analysis, the goal was to develop a machine learning model to predict the creditworthiness of borrowers using historical lending data from a peer-to-peer lending service. The primary objective was to identify loans that are at high risk of default (labeled as `1`) versus those that are likely to be repaid (labeled as `0`).

The dataset provided contained various financial features, including the loan amount, interest rate, and borrower credit score. The target variable, `loan_status`, indicated whether a loan was healthy (`0`) or high-risk (`1`).

Key steps in the machine learning process included:

1. **Data Preparation:**
   - Reading the CSV file into a Pandas DataFrame.
   - Reviewing the structure of the DataFrame and the distribution of the target variable using `value_counts`.

2. **Data Splitting:**
   - Splitting the data into training and testing sets using `train_test_split` with a `random_state` of 1.

3. **Model Training:**
   - Using the `LogisticRegression` algorithm to train the model on the training data.

4. **Model Evaluation:**
   - Making predictions on the testing data.
   - Evaluating the model's performance using a confusion matrix and classification report to calculate precision, recall, and F1-score.

## Results

Using the logistic regression model, the following accuracy, precision, and recall scores were obtained:

* **Logistic Regression Model:**
    * **Accuracy:** 0.95
    * **Precision for Class 0 (Healthy Loan):** 0.95
    * **Recall for Class 0 (Healthy Loan):** 0.97
    * **F1-Score for Class 0 (Healthy Loan):** 0.96
    * **Precision for Class 1 (High-Risk Loan):** 0.93
    * **Recall for Class 1 (High-Risk Loan):** 0.90
    * **F1-Score for Class 1 (High-Risk Loan):** 0.91

## Summary

The logistic regression model demonstrates strong performance in predicting both healthy loans and high-risk loans. The model's high precision and recall values for both classes indicate that it is effective at correctly identifying both healthy and high-risk loans. The overall accuracy of 95% supports the model's reliability for this classification task.

Given the balanced performance across both classes, the logistic regression model is recommended for deployment in identifying loan risks. This recommendation is based on the following observations:

* The model achieves high accuracy, precision, and recall, which means it correctly predicts the majority of both healthy and high-risk loans.
* The performance is balanced, indicating that the model does not favor one class over the other, which is important for maintaining fairness and reliability in loan approvals.

In conclusion, the logistic regression model performs best in this context and is suitable for predicting the creditworthiness of borrowers. Regular monitoring and retraining with new data will ensure the model maintains its performance over time.

