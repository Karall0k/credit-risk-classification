# Credit Risk Report

## Overview of the Analysis

The purpose of this analysis is to create a model to evaluate loan applicant's risk of default using a linear regression model.

The model was trained using financial data that included the following standard loan applicant variables:
 * loan size
 * income
 * interest rate
 * debt-to-income ratio
 * number of accounts
 * derogatory marks
 * total debt
 * loan status
 
 
The "loan status" variable was used a the prediction target to discern between two outcomes: "healthy loan" (0) and "high-risk loan" (1). The data was then split into a training set and a testing set using sklearn train_test_split. The linear regression model was then fit to the training data set. Next the model was applied to the test data to predict the loan status outcome. The classification report that analyze the prediction outcomes is discussed in the Results section.


## Results

Below are the accuracy, precision and recall scores of the Linear Regression Model:

    * Overall Accuracy: 0.99
    * Healthly Loan (0): Precision 1.00 Recall 0.99
    * High-Risk Loan (1): Precision 0.84 Recall 0.91

## Summary

The Linear Regression model has a high level of accuracy at 99%, but its ability to predict the healthy loan is more precise than its ability to predict the high-risk loans. All of the loans it predicted as healthy were healthy, and it captured 99% of the healthy loans in its prediction, as indicated by the precision and recall scores, respectively. The only 85% of the loans it predicted as high-risk, were in fact high-risk, but it captured 91% of the high risk loans in the prediction. 

In spite of the weaker performance of the model when predicting the high-risk loan, I would still recommend the use of linear regression model for loan status prediction, with the added caveat that the model should be optimized using a more balanced dataset with greater number of high-risk loan outcomes in the testing data set. This model has a high accuracy and will be successful in positively identifying healthy loan candidates. If the main purpose of this model is to reduce lender risk, as oppopsed to improving lending rates, then model optimization for high risk loans will make a good model great.
