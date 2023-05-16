# Credit Risk Analysis Report



Table of Contents
=================

  * [Overview of the Analysis](#overview-of-the-analysis)
  * [Model Results](#model-results)
  * [Summary](#summary)



## Overview of the Analysis


<u><b>Purpose of the analysis:</b></u> 

The purpose of the analysis is to identify the creditworthiness of borrowers. It will help identify the risk associated with a borrower not paying back a loan causing a loss of money. In this analysis, supervised machine learning was implemented to train and evaluate models based on loan risk. The dataset that was used was historical lending activity from a peer-to-peer lending services company. 



**Explanation of the financial information and what was needed to predict:** 

The financial information that the data was on encompassed loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks and total debt. The prediction is to determine whether a loan status is considered healthy (value of `0`) or whether the loan has a high-risk of defaulting (value of `1`). 



**Provide information about the variables you were trying to predict (i.e., `value_counts`):** 

When analyzing the `value_counts` after splitting the data into training and testing sets, we are able to identify that the data is highly imbalanced. The majority class is healthy loans `0`, with a total of 75,036 loans, where the minority class is the high-risk loans `1`, with a total of 2,500 loans.



**Stages of the machine learning process as part of this analysis:** 

The stages of the machine learning process encompassed the following, data collection, preparing the datasample, splitting the data into training and testing sets, fitting a logistic regression model with the original data and resampled training data and evaluating each model's performance.  



**Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method):**

The most appropriate tool for the machine learning model is the Logistic Regression Algorithm as it is able to predict the probability of a target variable in classification problems. Accuracy scores, balanced and imbalanced, were generated to assess for the number of correct predictions made by a model in relation to the total number of predictions made. A confusion matrix was then generated to compare the actual target values with those predicted by the machine learning models. As the data was imbalanced, a resampling method was completed on the Logistic Regression Model in order to better train and predict loan statuses. 



## Model Results


**Machine Learning Model 1 - Logistic Regression Model Fitted with Original Data:**
  * Confusion Matrix:
      * 56 False Positives: Actual value is healthy and predicted value is high-risk
      * 102 False Negatives: Actual value is high-risk and predicted value is healthy
  * Balanced accuracy score of 95%.
  * Healthy loan status:
      * Precision: 100%
      * Recall: 99%
  * High-risk loan status:
      * Precision: 85%
      * Recall: 91%


**Machine Learning Model 2 - Logistic Regression Model Fitted with Resampled Training Data:**
  * Confusion Matrix:
      * 4 False Positives: Actual value is healthy and predicted value is high-risk
      * 116 False Negatives: Actual value is high-risk and predicted value is healthy
  * Balanced accuracy score of 99%.
  * Healthy loan status:
      * Precision: 100%
      * Recall: 99%
  * High-risk loan status:
      * Precision: 84%
      * Recall: 99%



## Summary


Overall, in analyzing the results of the machine learning models, the oversampled model would be the model of choice. The oversampled model generated a balanced accuracy score of 99%, which is an improvement than the prior logistic regression model of 95%. It continues to perform the same when being able to correctly identify health loans, as the precision is 100%, and the recall remains high at 99%. Most importantly, where the oversampled model performs better is with the recall rates for high-risk loans. Although still obtaining a similar precision as the logistic regression model at 84% in comparison to 85%, of these 84% that are correctly identified at high-risk, there is a recall of 99%. This is an improvement from the 91% on the prior logistic regression model. According to the confusion matrices, the number of False Positives significantly decreases, which indicates the model will classify healthy and high-risk loans correctly. 

The oversample model helps to better predict the true positives meaning that it is more effective at distinguishing high-risk loans with high recall accuracy. The oversample model will make fewer mistakes when classifying high-risk loans. This is important to a lending company as this may be more costly for the lending company due to the loss of funds being provided by the lender. Further to this, if healthy loans are being identified as high-risk, this may cause potential for loss of customers. Lastly, having fewer False Positives, will decrease the possibility of the lending company losing funds when classifying high-risk loans as healthy. 

Therefore, the recommended model would be Model 2, Logistic Regression Model fitted with Resampled Data. 
