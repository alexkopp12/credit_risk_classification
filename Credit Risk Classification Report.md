# Module 12 Report Template

## Overview of the Analysis
The Credit Risk Classification analysis is an analysis of data relevant to credit risk as classified by two clusters of loans - "High-Risk" and "Healthy" loans looking to determine if a logistic fit model can accurately predict what cluster a loan will reside in based on the provided data.
* Explain the purpose of the analysis.
* Data:
The provided features the model was trained on include loan size, interest rate, borrower income, debt to income,number of accounts, derogatory marks, and total debt for each of the loans and relevant borrower. The model attempted to utilize a weighting of these relevant factors to predict whether the loan belonged in one of two groups, high-risk or healthy loans. Healthy loans are defined as loans with a normal risk of default where as a high-risk loan is a loan with an abnormally high risk of default and are typically associated with higher interest rates. The data provided for this analysis was covering a set of 77,536 loans with provided information. Of those loans just over 3% were marked High-Risk.

* Method:
For this analysis we utilized the Scikit-learn logistic regression method which models the probability of the target variable belonging to a particular class which is commonly used for binary classification such as this. Based on background from ChatGPT, "Scikit-learn's logistic regression method learns the optimal coefficients (weights) for the features by minimizing a cost function, often the negative log-likelihood, using optimization techniques like gradient descent. The goal is to find the weights that maximize the likelihood of the observed data given the model."
To conduct this analysis we input our data into a data frame. We then isolated our X feature set and our y variable. We the subset both the x and y data into a test and train data set. We created the model and fit it to the training data. We then utilized the model to predict a set of y values from our test x data set and compare those values to the actual y values of the test set to determine the models accuracy.


* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced Accuracy: The balanced accuracy score for this model 99.19% which indicates a high level of precision from the model in predicting whether a loan is healthy or high risk. The balanced accurary score is the average of a models ability to reflect the true positive rate and true negative rate which provides a balanced view of a models fit for both the 0 and 1 class. This high score indicates that our model is likely highly accurate for both classes.

  * Precision Score: The precision score for this model is 100% for 0 or Healthy Loans whereas it is only 85% for 1 or High-Risk loans. This indicates that the model is noticeably more precise at predicting a healthy loan then a high-risk loan. In other words the model is not likely at all to predict a false positive when it comes to Healthy loans but has a 15% chance of predicting a false positive for High Risk loans.

  * Recall Score: The recall score for this model is 99% for Healthy Loans and 91% for High-Risk Loans. This demonstrates a marginal higher likelihood of the model predicting false negatives when compared to false positive for Healthy loans but is on the whole very precise and sensitive regarding Healthy outcomes. For High Risk Loans the model performs with a marginally higher level of sensitivity when compared to precision and is less likely to predict a false negative compared to a false positive when it comes to High-Risk loans.




## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any.
The logistic regression model performs well at classifying loans as either high risk or healthy. This is confirmed by a 99% balanced accuracy rating display over a test sample size of close to twenty thousand. It is worth noting that model is less accurate at predicting High-Risk loans then Healthy loans but in both instances performs with enough accuracy to be significantly confident in the results. If the data model were to be trained on an equivalent number of High Risk loans to Healthy loans it is likely that the model could be further improved for this task.
