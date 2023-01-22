# Credit_Risk_Analysis

## Overview

Use python to evaluate several machine learning models to predict credit risk and determine the accuracy of the models. Models to use and evaluate:

- oversampling with RandomOverSampler and SMOTE
- undersampling with ClusterCentroids
- oversample and undersample using SMOTEENN
- compare two machine learning models that reduce bias BalancedRandomForestClassifier and EasyEnsembleClassifier

## Analysis

### RandomOverSampler

(image)

- Balanced Accuracy Score: 62.9%
- Precision for high risk: 1%
- Precision for low risk: 100%
- Recall for high risk: 57%
- Recall for low risk: 68%

### Smote

(image)

- Balanced Accuracy Score: 62.8%
- Precision for high risk: 1%
- Precision for low risk: 100%
- Recall for high risk: 62%
- Recall for low risk: 63%

### ClusterCentroids

(image)

- Balanced Accuracy Score: 51.6%
- Precision for high risk: 1%
- Precision for low risk: 100%
- Recall for high risk: 60%
- Recall for low risk: 43%

### SMOTEENN

(image)

- Balanced Accuracy Score: 64.1%
- Precision for high risk: 1%
- Precision for low risk: 100%
- Recall for high risk: 70%
- Recall for low risk: 58%

### BalancedRandomForestClassifier

(image)

- Balanced Accuracy Score: 78.7%
- Precision for high risk: 3%
- Precision for low risk: 100%
- Recall for high risk: 68%
- Recall for low risk: 90%

### EasyEnsembleClassifier

(image)

- Balanced Accuracy Score: 92.5%
- Precision for high risk: 7%
- Precision for low risk: 100%
- Recall for high risk: 91%
- Recall for low risk: 94%

## Summary

Every model returns very low precision in predicting a high credit risk. For the first four models it is evident that the resampling attempted to address the imbalance in classes of high risk and low risk, however could not guarantee better results. The models remain weak in determining high credit risk with low precision, recall, and accuracy. However, the Ensemble models brought significant improvement particularly for the sensitivity for high risk. The EasyEnsembleClassifier model provided a high accuracy of 92.5% as well as high sensitivity for high and low risk credits (91% and 94% respectively). However, the low precision for detecting high risk credit (7%) allows for the false identification of high risk as low risk. Compared to the other models, the EasyEnsembleClassifer model remains the best out of the group. From the group, I would recommend the EasyEnsembleClassifier model. However, more analysis with diverse models might result in a better balance of recall and precision that has not been seen here.