# Credit Risk Report

## Overview of Analysis
The purpose of this analysis is to train and evaluate a model based on loan risk by using a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers. This is accomplished by using a data set with loan size, interest rate, borrower income, debt-to-oncome, number of accounts, derogartory marks, total debt and loan status. Our goal is to be able to predict loan status based on the other data provided. The data was split into a training set and a testing set, where the training set was fed into a logistic regression model, then a scaled data set was fed into a random forest model, K-Neighbor model, and a logistic regression model, and evaluated against the testing set. The logistic regression model performed the best, with more accurate results from being performed on a scaled data set.

## Results
Data has 19384 entries: 18759 Healthy Loans, 625 High-Risk Loans
### Logisitic Regression Model on Scaled Data:
* Dominant Feature: Debt-to-Income
* Accuracy: 0.99
* Healthy Loans:
    * Precision:    1.00
    * Accuracy:     1.00
* High-Risk Loans:
    * Precision:    0.87 (90)
    * Accuracy:     0.98 (14)
### Logisitic Regression Model:
* Dominant Feature: Derogatory Marks
* Accuracy: 0.99
* Healthy Loans:
    * Precision:    1.00
    * Accuracy:     1.00
* High-Risk Loans:
    * Precision:    0.87 (86)
    * Accuracy:     0.95 (32)
### K-Neighbor Model:
* Accuracy: 0.99
* Healthy Loans:
    * Precision:    1.00
    * Accuracy:     1.00
* High-Risk Loans:
    * Precision:    0.88 (82)
    * Accuracy:     0.92 (47)
### Random Forest Model:
* Dominant Feature: Interest Rate
* Accuracy: 0.99
* Healthy Loans:
    * Precision:    1.00
    * Accuracy:     1.00
* High-Risk Loans:
    * Precision:    0.88 (79)
    * Accuracy:     0.88 (72)

## Summary
 All models have an overall accuracy of 99% and are able to predict healthy loans with close to 100% accuracy, but have varying performance with high-risk loans. Out of the various models explored, the best model to use is the linear regression model on scaled data. While it marginally has the lowest precision for high-risk loans (with 90 healthy loans misclassified as high-risk), it performs significantly better at correctly identifying high-risk loans (with only 14 high-risk loans misclassified as healthy). Thus it is the most suitable model as it is the most conservative in identifying more high-risk loans, even if it results in more healthy loans being flagged incorrectly.