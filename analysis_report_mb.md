# Module 20 Report

## Overview of the Analysis

The analysis completed in this challenge was to create a machine learning algorithm to evaluate if candidates were going to be high risk or healthy loan candidates - or, if they were going to default on their loan or not. 

The financial information examined for the analysis were the loan size, interest rate of the loan, the borrower's income and their debt to income ration, the number of revolving accounts the borrower had, any derogatory marks on their revolving accounts or debts, and their amount of total debt. This imformation gives a fairly roubst picture of the type of borrow each candidate is, and offers valuable insight as to whether or not they are likely to default on their loan. 

As part of this analysis, I first loaded the csv file into a dataframe for manipulation. Then, I separated the data into the y variable (loan_status) and the X variables (all other contributing factors listed above). Then, I split the data into the training and testing data for the algorithm to learn and compare itself to. 

I then used the Logistic Regression model so that the y variable was classified as either '0' (Healthy Loan) or '1' (Risky Loan). I fit the model using the training set and predicted using the testing set to evaulate how well the algorithm ran. 

## Results

* Machine Learning Model 1:

**Healthy Loans ('0'):**
- Precision: 
Out of all the loans that the model predicited would be a Healthy Loan candidate, 100% were actually Healthy Loan candidates. This means that there were no false positives for the Healthy Loans, so no High Risk candidates were misidentified as Healthy Loan candidates. 

-  Recall: 
The model correctly predicted 99% of the Healthy Loan Candidates, meaning that there were a few false negatives (1% of actual), where Healthy Loan Candidates were misidentified as High Risk candidates. 

- F1-Score: 
For Healthy Loans ('0'), the F1-Score of 1.00 means that the model does an excellent job of identifying and correctly classifying Healthy Loan candidates. 

**High Risk Loans ('1'):**
-  Precision: 
Out of all of the loans that the model predicted would be a High Risk Loan, only 84% were actually High Risk. This means that there were some False Positives, where Healthy Loan candidates were misidentified as High Risk. 

-  Recall: 
The model correctly predicted 94% of all the High Risk Loans that were actually High Risk. This means that there was a low number of False Negatives in the model, where High Risk Loan candidates were misidentified as Healthy Loan candidates. 

- F1-Score: 
For High Risk Loans ('1'), the F1-Score of .89 lets us know that the model does a decent job of classifying High Risk Loan candidates, but is less accurate and reliable than the F1-Score for Healthy Loans ('0'). The model is not completely accurate and which lets us know that there are some false negatives and false positives: loan candidates being miscategorized as either High Risk when they are Healthy or Healthy when they are High Risk. 


## Summary

Overall, the Accuracy Score of .99 tells us that the model as a whole is strong, with only 1% of the total predictions made being incorrect or misclassified. 

It is more important to the financial institution to predict the '1's (High Risk Loans) because it is costly to misclassify someone who is likely to default on their loan. 

If the financial institution using thie model allows a 99% accuracy and deems 1% appropriate for their margin of error when classifying candidates as either healthy or high risk, I would recommend this model to them. 

