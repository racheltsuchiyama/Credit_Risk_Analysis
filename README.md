# Credit_Risk_Analysis

## Project Overview
The purpose of this project was to determine the best machine learning methods to use for predicting credit risk. The models look at various features of the loan applicants and predict if the applicant is a low or high credit risk. However, the classes are unbalanced because the number of low credit risks largely outnumbers the high credit risks. Therefore, I will try oversampling, undersampling, and combined sampling the training data and compare the performance of these algorithms. I will also compare these machine learning models to classifiers that reduce bias.

## Results
* **Naive Random Oversampling**
This maching learning model trained the logistic regression model with data resampled by the RandomOverSampler. This resulted in a balanced accuracy scores of 67.38% However, it is more enlightening to analyse the precision and recall scores:

<img width="821" alt="Screen Shot 2021-08-28 at 5 29 39 PM" src="https://user-images.githubusercontent.com/83552696/131234295-696e9a20-7834-4782-a43e-bc322fe8e9a9.png">

As shown in the table above, the precision score for high credit risk is 0.1 and the recall score is 0.71. In this case, a higher recall score is more important than a higher precision score.

* **SMOTE Oversampling**
This model also trained the logistic regression model, but with data resampled by SMOTE. The balanced accuracy score was 64.16%, the high risk precision score was 0.01, and the high risk recall score was 0.61. Compared to RandomOverSampler, SMOTE had lower accuracy and recall scores. Therefore, it was the lower performing oversampler method.

<img width="749" alt="Screen Shot 2021-08-28 at 5 29 46 PM" src="https://user-images.githubusercontent.com/83552696/131234297-2a915128-d67b-43df-bfab-fe9ebf7e0b50.png">

* **Cluster Centroids Undersampling**
This model trained the logistic regression model with data resampled by ClusterCentroids. The balanced accuracy score was 54.33%, the high risk precision score was 0.01, and the high risk recall score was 0.68.

<img width="738" alt="Screen Shot 2021-08-28 at 5 29 53 PM" src="https://user-images.githubusercontent.com/83552696/131234301-aec9e036-841e-46b7-bb40-c18573211498.png">

* **SMOTEENN Combination Sampling**
SMOTEENN combines oversampling and undersampling to resample the data. The logistic regrssion model was then fit with the resampled SMOTEENN data. The balanced accuracy score was 64.19%, the high risk precision score was 0.01, and the high risk recall score was 0.7. 

<img width="740" alt="Screen Shot 2021-08-28 at 5 29 58 PM" src="https://user-images.githubusercontent.com/83552696/131234302-e096e5e1-7679-4a5c-a388-f5b17929d7f4.png">

* **Balanced Random Forest Classifier**
The Balanced Random Forest Classifier resampled the test data using 100 estimators. The resulting balanced accuracy score was 99.97%, the high risk precision score was 0.9, and the high risk recall score was 1. 

<img width="766" alt="Screen Shot 2021-08-28 at 5 31 12 PM" src="https://user-images.githubusercontent.com/83552696/131234314-eebc735a-8716-4efc-8fc9-9cb7295ccef9.png">

* **Easy Ensemble AdaBoost Classifier**
The Easy Ensemble Classifier resampled the test data using 100 estimators. The resulting balanced accuracy score was 100%, and the high risk precision and recall scores were both 1.

<img width="763" alt="Screen Shot 2021-08-28 at 5 31 18 PM" src="https://user-images.githubusercontent.com/83552696/131234316-2a732e81-644e-4843-a192-4f51a9f66172.png">

## Summary
The Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier had the best performance out of the above machine learning models. The Easy Ensemble Adaboost Classifier was able to accurately predict all the credit risks, while the Balanced Random Forest Classifier was a close second. Therefore I would recommend trying both the Easy Ensemble AdaBoost Classifier and the Balanced Random Forest Classifier, and comparing their accuracy, precision, and recall scores on a larger dataset. The other models had much lower accuracy, precision, and recall scores so I would not recommend using those models for predicting credit risk. Therefore, under, over, or combined sampling training data results in less accurate predictions than machine learning models that reduce bias.
