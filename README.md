# Credit_Risk_Analysis

## Project Overview
The purpose of this project was to determine the best machine learning methods to implement for 

## Results
* **Naive Random Oversampling**
This maching learning model trained the logistic regression model with data resampled by the RandomOverSampler. This resulted in a balanced accuracy scores of 67.38% However, it is more enlightening to analyse the precision and recall scores:

As shown in the table above, the precision score for high credit risk is 0.1 and the recall score is 0.71. In this case, a higher recall score is more important than a higher precision score.

* **SMOTE Oversampling**
This model also trained the logistic regression model, but with data resampled by SMOTE. The balanced accuracy score was 64.16%, the high risk precision score was 0.01, and the high risk recall score was 0.61. Compared to RandomOverSampler, SMOTE had lower accuracy and recall scores. Therefore, it was the lower performing oversampler method.

* **Cluster Centroids Undersampling**
This model trained the logistic regression model with data resampled by ClusterCentroids. The balanced accuracy score was 54.33%, the high risk precision score was 0.01, and the high risk recall score was 0.68.

* **SMOTEENN Combination Sampling**
SMOTEENN combines oversampling and undersampling to resample the data. The logistic regrssion model was then fit with the resampled SMOTEENN data. The balanced accuracy score was 64.19%, the high risk precision score was 0.01, and the high risk recall score was 0.7. 

* **Balanced Random Forest Classifier**
The Balanced Random Forest Classifier resampled the test data using 100 estimators. The resulting balanced accuracy score was 99.97%, the high risk precision score was 0.9, and the high risk recall score was 1. 

* **Easy Ensemble AdaBoost Classifier**
The Easy Ensemble Classifier resampled the test data using 100 estimators. The resulting balanced accuracy score was 100%, and the high risk precision and recall scores were both 1.

## Summary
The Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier had the best performance out of the above machine learning models. The Easy Ensemble Adaboost Classifier was able to accurately predict all the credit risks, while the Balanced Random Forest Classifier was a close second. Therefore I would recommend trying both the Easy Ensemble AdaBoost Classifier and the Balanced Random Forest Classifier, and comparing their accuracy, precision, and recall scores. The other models had much lower accuracy, precision, and recall scores so I would not recommend using those models for predicting credit risk.
