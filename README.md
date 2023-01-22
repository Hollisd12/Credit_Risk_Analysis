# Credit_Risk_Analysis

## Overview

Use python to evaluate several machine learning models to predict credit risk and determine the accuracy of the models. Models to use and evaluate:

- oversampling with RandomOverSampler and SMOTE
- undersampling with ClusterCentroids
- oversample and undersample using SMOTEENN
- compare two machine learning models that reduce bias BalancedRandomForestClassifier and EasyEnsembleClassifier

## Analysis

### RandomOverSampler

![RandomOversampling](https://user-images.githubusercontent.com/112137694/213941899-3518b108-a453-41ee-be88-beaa19d657e2.png)

- Balanced Accuracy Score: 62.9%
- Precision for high risk: 1%
- Precision for low risk: 100%
- Recall for high risk: 57%
- Recall for low risk: 68%

### Smote

![SMOTEOversampling](https://user-images.githubusercontent.com/112137694/213941908-8d30af61-12e3-468b-ac2c-a6d4171bc339.png)

- Balanced Accuracy Score: 62.8%
- Precision for high risk: 1%
- Precision for low risk: 100%
- Recall for high risk: 62%
- Recall for low risk: 63%

### ClusterCentroids

![ClusterCentroidsUndersampling](https://user-images.githubusercontent.com/112137694/213941918-20e43b52-7c96-4c3b-ad6b-80a9517734b4.png)

- Balanced Accuracy Score: 51.6%
- Precision for high risk: 1%
- Precision for low risk: 100%
- Recall for high risk: 60%
- Recall for low risk: 43%

### SMOTEENN

![SMOTEENN](https://user-images.githubusercontent.com/112137694/213941922-7766acf3-74a1-4929-97ad-5f8043db34ba.png)

- Balanced Accuracy Score: 64.1%
- Precision for high risk: 1%
- Precision for low risk: 100%
- Recall for high risk: 70%
- Recall for low risk: 58%

### BalancedRandomForestClassifier

![BalancedRandomForestClassifier](https://user-images.githubusercontent.com/112137694/213941925-b29c5830-8ca7-489b-b9fd-ae4c249cac5e.png)

- Balanced Accuracy Score: 78.7%
- Precision for high risk: 3%
- Precision for low risk: 100%
- Recall for high risk: 68%
- Recall for low risk: 90%

### EasyEnsembleClassifier

![EasyEnsembleAdaBoostClassifier](https://user-images.githubusercontent.com/112137694/213941929-7b021294-5f5d-4f86-870c-5a3caca1f2de.png)

- Balanced Accuracy Score: 92.5%
- Precision for high risk: 7%
- Precision for low risk: 100%
- Recall for high risk: 91%
- Recall for low risk: 94%

## Summary

Every model returns very low precision in predicting a high credit risk. For the first four models it is evident that the resampling attempted to address the imbalance in classes of high risk and low risk, however could not guarantee better results. The models remain weak in determining high credit risk with low precision, recall, and accuracy. However, the Ensemble models brought significant improvement particularly for the sensitivity for high risk. The EasyEnsembleClassifier model provided a high accuracy of 92.5% as well as high sensitivity for high and low risk credits (91% and 94% respectively). However, the low precision for detecting high risk credit (7%) allows for the false identification of high risk as low risk. Compared to the other models, the EasyEnsembleClassifer model remains the best out of the group. From the group, I would recommend the EasyEnsembleClassifier model. However, more analysis with diverse models might result in a better balance of recall and precision that has not been seen here.
