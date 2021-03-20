# Module 12 Report

## Overview of the Analysis

In this Credit Risk Classification challenge, we reviewed a set of lending data and used different techniques to train machine learning models to identify high-risk loans from the data.

The variables provided in the lending data file are features such as loan size, interest rate, borrower income, debt to income ratio, etc. There are a total of 75036 entries of healthy loans, and 2500 high-risk loans in the data set.

To analyze the data, we did the following steps:
1. Read csv file and review data frame. 
2. Fit the model
3. Make predictions
4. Evaluate the model with Confusion Matrix
5. Generate classification report

Initially we used Logistic Regression model without over or undersampling the dataset. After reviewing the first set of classification report, we conducted a new around with RandomOverSampler module, repeated all the steps 2-5. Compared both sets of the classification report to determine which module gives better prediction.

## Results

* Machine Learning Model 1: Logistic Regression Model with Original Data ("0": healthy loan, "1": high-risk loan)
  Balanced Accuracy Score = 0.95
  Precision "0" = 0.99
  Precision "1" = 0.91
  Recall "0" = 1.00
  Recall "1" = 0.85
  
* Machine Learning Model 2: Logistic Regression Model with Oversampled Data ("0": healthy loan, "1": high-risk loan)
  Balanced Accuracy Score = 0.99
  Precision "0" = 1.00
  Precision "1" = 0.84
  Recall "0" = 0.99
  Recall "1" = 0.99
  
## Summary

Based on the results stated above, we think both result sets provide pretty good prediction outcome. However, considering the testing data of healthy loans are significantly overstated in our sample, and the main objective for this challenge is to identify the high-risk loans. We would suggest using the Logistic Regression Model with Oversampled Data whcih gives an improved accuracy score at 0.99 from 0.95; and also enhanced Recall value for high-risk loans from 0.85 to 0.99.