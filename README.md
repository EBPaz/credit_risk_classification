# credit_risk_classification
  supervised Machine Learning, Module 20

## Overview of the Analysis
This challenge utilized data related to lending to determine the creditworthiness of borrowers. A logistic regression model was applied to determine if it was a good model for predicting borrowers ending with a healthy loan or risky loan. 

The dataset included information such as: loan size, interest rate, borrower's income, debt to income raio, number of bank accounts, derogatory marks and total debt. The loan status was the information attempting to be predicted.

When looking further at the loan status data, it was broken down by healthy loans and risky loans. There were 75,036 health loans reported and 2,500 risky loans reported. This data is clearly imbalanced.

The dataset was broken down to the X values (all of the above listed information) and the Y value (the loan status). Then split with the 'train-test-split' module from sklearn into Training(75% of total data) and Testing(25% of total data) sets. 

A logistic regression model was then applied to the data using sklearn's 'LogisticRegression' module. That model was fit with the training data and then predictions were made with the test data. 

The performance of the logistic regression model was checked using the sklearn metric 'accuracy_score'. Finally a confusion matrix and classification report of the test data was printed for analyizing the final results.

## Results
Machine Learning Model 1 (Logistic Regression):
  * The model accuracy was 99%
  * The precision score for healthy loan prediction was 99%
  * The precision score for risky loan prediction was 91%
  * The recall score for healthy loan prediction was 100%
  * The recall score for risky loan prediction was 88%

## Summary
Overall, we have an accuracy rating of 99%, however, our data is imbalanced. We have way more healthy loan data points than risky loan data points.

The healthy loan predictions shows 99% of the loans we predicted to be healthy, ended up actually being healthy. This is a great outcome for this model. Comparing this to the f1-score of 1.0(a better predictor when the data is imbalanced), it also shows this model is a good predictor of healthy loan outcomes. 

The risky loan predictions shows 91% of the loans we predicted to be risky, actually ended up being risky. This is also a pretty good outcome for this model, however, because the data is imbalanced, we should look at the f1-score for risky loans, the number drops to .88. Still this is close to 1.0 but much less accurate for using this model to predict risky loans. 

In conclusion, this model should be used for predicting potential healthy loans but not risky loans. 