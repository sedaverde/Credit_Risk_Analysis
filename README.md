# Credit_Risk_Analysis

## Overview :
The purpose of this project was to evaluate six different machine learning models to determine if any of them could be used to predict credit risk. The following models were evaluated:
  - Random Oversampler
  - Smote Model
  - ClusterCentroids (CC) Model
  - SMOTEEN Model
  - BalancedRandomForestClassier (BRFC) Model
  - EasyEnsembleClassifier (EEC) Model

## Results:

### Random Oversampler:

- Balanced Accuracy Score = 0.62
- Precision
  - High Risk = 0.01
  - Low Risk = 1.00
- Recall
  - High Risk = 0.63
  - Low Risk = 0.60
- F1 score 
  - High Risk = 0.02
  - Low Risk = 0.75

![naive oversampling](https://user-images.githubusercontent.com/90329647/161216346-60626727-f301-4a4f-97d3-387c2766df03.PNG)

### SMOTE Model:

- Balanced Accuracy Score = 0.66
- Precision
  - High Risk = 0.01
  - Low Risk = 1.00
- Recall
  - High Risk = 0.63
  - Low Risk = 0.69
- F1 score 
  - High Risk = 0.02
  - Low Risk = 0.83

![SMOTE oversampling](https://user-images.githubusercontent.com/90329647/161216433-07a25576-d5f1-4a8b-b0c6-430003d30bcf.PNG)

### ClusterCentroids Model:

- Balanced Accuracy Score = 0.54
- Precision
  - High Risk = 0.01
  - Low Risk = 1.00
- Recall
  - High Risk = 0.69
  - Low Risk = 0.40
- F1 score 
  - High Risk = 0.01
  - Low Risk = 0.57

![ClusterCentroids undersampling](https://user-images.githubusercontent.com/90329647/161216530-663d95f9-9996-406c-8541-1479980ddf7f.PNG)

### SMOTEEN Model:

- Balanced Accuracy Score = 0.64
- Precision
  - High Risk = 0.01
  - Low Risk = 1.00
- Recall
  - High Risk = 0.70
  - Low Risk = 0.58
- F1 score 
  - High Risk = 0.02
  - Low Risk = 0.73

![SMOTEEN](https://user-images.githubusercontent.com/90329647/161216626-3efc1276-3adf-4eb4-935a-f2206870f10d.PNG)

### BalanceRandomForestClassifier Model:

- Balanced Accuracy Score = 0.79
- Precision
  - High Risk = 0.03
  - Low Risk = 1.00
- Recall
  - High Risk = 0.70
  - Low Risk = 0.87
- F1 score 
  - High Risk = 0.06
  - Low Risk = 0.93

![BRFC](https://user-images.githubusercontent.com/90329647/161216718-6c5cba28-c894-4785-aba0-98f3eb932dee.PNG)

### EasyEnsembleClassifier Model:

- Balanced Accuracy Score = 0.93
- Precision
  - High Risk = 0.09
  - Low Risk = 1.00
- Recall
  - High Risk = 0.92
  - Low Risk = 0.94
- F1 score 
  - High Risk = 0.16
  - Low Risk = 0.97

![EEC](https://user-images.githubusercontent.com/90329647/161216909-4e3bafbb-bc52-4b42-b451-b8e4b3f9b557.PNG)

## Summary:

With the exception of the EEC model, all other model exhibit poor accuracy. All models exhibit an extremely high degree of imprecision in regard to high risk prediction. In all models except the EEC model, recall is low for both high and low risk. F1 scores for the BRFC and EEC for low risk are good, however F1 scores for predicting high risk are poor across the board.

All models except EEC can be eliminated as potentially useful models due to their low accuracy scores. The EEC model while maintaining high values for low risk prediction performs poorly when it comes to predicting high risk. This combination indicates that there are many low risk events that are intepreted as high risk by the model. While not ideal, this model may be useful if the bank wants to focus on only low risk applicants as the number of true high risk applicants classified as low risk is within an acceptable threshold.
