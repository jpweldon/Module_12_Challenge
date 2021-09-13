# Credit Risk Analysis Report

## Overview of the Analysis

The purpose of this analysis is to use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers. Credit risk poses a classification problem that is inherently imbalanced due to healthy loans outnumbering risky loans. I am using various techniques to train and evaluate models with imbalanced classes.

I predicted various variables including value_counts, balanced_accuracy_score, precision, recall, and f1-score. I used value counts to determine the number of healthy loans and number of high-risk loans in the data. This showed an imbalance in the original data. The accuracy measures how often the model was correct. The precision, also known as the positive predictive value (PPV), measures how confident we are that the model correctly made the positive predictions. The recall measures the number of actually fraudulent transactions that the model correctly classified as fraudulent. The F1 score, which is also called the harmonic mean, is a single summary statistic for the precision and the recall.

I went through the model, fit, predict, and evaluate stages of the machine learning process. For the model stage, I chose a model appropriate for the data. In this case, I chose logistic regression for classification. For the fit stage, I let the model learn based on existing data. For the predict stage, I have the model make predictions for new data. Finally, for the evaluate stage, I evaluate the model and if I see that the model did not make predictions well, I might select a different machine learning model.

I used logistice regression since logistic regression is designed to predict discrete outcomes. Resampling is used to solve the imbalanced class problem from the original data. Resampling is a way to artificially balance the classes, healthy loaan versus high-risk loan, that the model gets during training. This helps the model avoid hyperfocusing on the larger class, healthy loans, and can improve the predictions for the smaller class, high-risk loans.

## Results

* Machine Learning Model 1:
The logistic regression model predicts both the healthy loan and high-risk loan labels very well. However, the logistic regression model predicts the healthy loans better than it predicts the unhealthy loans. For healthy loans, the majority class, there is a precision of 1.00, recall of 0.99, and f1-score of 1.00. For high-risk loans, the minority class, there was a precision of 0.85, recall of 0.91, and f1-score of 0.88.

* Machine Learning Model 2:
The logistic regression model fit with oversampled data predicts both the healthy loan and high-risk loan labels very well. However, the logistic regression model predicts the healthy loans better than it predicts the unhealthy loans. For healthy loans, the majority class, there is a precision of 1.00, recall of 0.99, and f1-score of 1.00. For high-risk loans, the minority class, there was a precision of 0.84, recall of 0.99, and f1-score of 0.91.

## Summary

For healthy loans, the logistic regression model fit with oversampled data predicted as well as the original logistic regression model based on precision, recall, and f1-score.

For the high-risk loans, the logistic regression model fit with oversampled data versus the original logistic regression model had a slightly lower precision (0.84 versus 0.85), slightly higher recall (0.99 versus 0.91), and slightly higher f1-score (0.91 versus 0.88).

The difference in precision means that the original data was better at detecting whether a loan was actually high-risk.

The difference in recall means that the resampled data correctly clasified a higher percentage of the truly high-risk loans.

The model using resampled data was better at detecting loans that are high-risk than the model generated using the original dataset.

I would use the model using resampled data to predict loans that are high-risk.
