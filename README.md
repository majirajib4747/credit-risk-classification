Credit-risk-classification

Regression Machine learning techniques are used to analyze a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

Overview of the Analysis : 
Factors considered in the analysis included data on:

loan size
interest rate
borrower's income
debt to income ratio
number of accounts 
derogatory marks
the total debt

The dataset (77,535 data points) was split into training and testing sets.Test Size is 20%. The training set was used to build an initial logistic regression model (Logistic Regression Model 1) using the LogisticRegression module from scikit-learn. Logistic Regression Model 1 was then applied to the testing dataset. The purpose of the model was to determine whether a loan to the borrower in the testing set would be low- or high-risk.

This intial model was drawing from a dataset that had 75,036 low-risk loan data points and 2,500 high-risk data points.In Model 2 , I had used RandomOverSampler to sample the data. after resampling high risk and low risk count is same - 60035.  

The resampled data was used to build a new logistic regression model (Logistic Regression Model 2). The purpose of Logistic Regression Model 2 was to determine whether a loan to the borrower in the testing set would be low- or high-risk. The results are summarized below.

Results : 
Logistic Regression Model 1:

This model predict low risk credit with 100% efficiency , and high risk credit with 86% accuracy. The balanced accuracy of the model is 95%.

Logistic Regression Model 2:

This model predit low risk loan with 100% accuracy and high risk loan with 85% accuracy. The balanced accuracy of the model is 99%.

Summary : 

Logistic Regression Model 2 is less likely to predict false negative results(85%). However, based on the confusion matrices for each model, Logistic Regression Model 2 predicted slightly more false positives (low-risk when the actual was high-risk) (99%).

If the goal of the model is to determine the likelihood of high-risk loans, neither model scores above 90% precision. If we compare between 2 Models - Model 2 would be better to use. 
