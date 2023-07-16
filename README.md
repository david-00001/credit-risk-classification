## File Structure

Analysis code resides in /Credit_Risk/credit_risk_classification.ipynb

Data file resides in /Credit_Risk/Resources/lending_data.csv


## Overview of the Analysis

The purpose of this analysis is to predict whether a loan will be healthy or high-risk based on these characteristics (variables): Loan Size, Interest Rate, Borrower Income, Debt to Income, Number of Accounts, Derogatory Marks, and Total Debt. 

From the 75,536 records of data provided, 75,036 or 96.8% of records were healthy loans and 2,500 or 3.2% were high-risk. I first ran a machine learning model of Logistic Regression to classify the data as it was. However, because the data was so imbalanced with the bulk of the data being healthy loans, I ended up using oversampling to make the dataset more even. I then re-ran the machine learning model of Logistic Regression and compared the accuracy of the two scenarios.

Prior to running the models, I split the data between a training set (75%) and a testing set (25%).


## Results

* Machine Learning Model 1 (prior to oversampling):
  * Balanced Accuracy of about 95.2%
  * Precision of Healthy Loans: 1.00
  * Recall of Healthy Loans: 0.99
  * Precision of High-Risk Loans: 0.85
  * Recall of High-Risk Loans: 0.91


* Machine Learning Model 2 (with oversampling):
  * Balanced Accuracy of about 99.4%
  * Precision of Healthy Loans: 1.00
  * Recall of Healthy Loans: 0.99
  * Precision of High-Risk Loans: 0.84
  * Recall of High-Risk Loans: 0.99

## Summary

The first model (prior to oversampling) had perfect precision in that when it predicted a loan as healthy, it was 100% correct. The model correctly identified 99% of the healthy loans. For the high-risk loans, the model was 85% correct in predicting a loan as high-risk. Finally, the model correctly identified 91% of the high-risk loans. The Balanced Accuracy for the model was about 95.2%.

After oversampling the data, we see that the healthy loans remained the same with a precision of 1.00 and a recall of 0.99. However, we do see an increase in the recall of the high-risk loans from 0.91 to 0.99. This came at the small cost of the precision dropping 0.01 from 0.85 to 0.84. This means the oversampling was able to more correctly identify the high-risk loans but it was 1% less correct in predicting a loan as high-risk. The Balanced Accuracy for the model was about 99.4%.

After comparing the two models, I recommend that the loan company uses the second model with oversampling to predict loan health. The oversampling helped ensure better accuracy and precision for the minority data which can be considered the more important data anyway because ultimately the loan company would be more concerned about high-risk loans than they are about healthy loans. By making the model more accurate in predicting the minority data, the model became more accurate overall.
