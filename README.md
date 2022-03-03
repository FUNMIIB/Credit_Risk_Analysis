# Credit_Risk_Analysis

**OVERVIEW**
The purpose of this analysis is to implement Machine Learning statistical algorithms to make predictions based on data patterns. The dataset used is card credit dataset from LendingClub, a peer-to-peer lending services company. This analysis employed Supervised Machinie Learning model to evaluate and predict credit risk. This is referred to as "Supervised Learning" because the data includes a labelled outcome.

In this analysis, different Machine Learning techniques were used to train and evaluate the data with unbalanced classes. The dataset from the LendingClub has an unbalanced classification problem due to the number of good loans outweighing the amount of risky loans. To balance out the classifications to allow for more meaningful predictions and improve the accuracy score, we needed to employ various Machine Learning algorithms to resample the data. These algorithms include RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier, and EasyEnsembleClassifier.

Results

In Q1 of 2019, dataset originally contained 115,675 loan applications. loan status was used to determine whether the application was considered "low" or "high" risk. Applications that had "current" as the "loan status" were classified as "low risk" and the remaining as "high risk". This reduced the dataset to 68,817 total applications with 99% classified as "low risk".

![credit_risk_1](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_1.png)

We used the 75/25% method to split the data for training and testing, 51,366 "low risk" and 246 "high risk" applications were categorized into the training set.


**Deliverable 1**

- Oversampling
RandomOverSampler Model randomly selects from the minority class and adds it to the training set until both classifications are equal. The results classified 51,366 records each as High Risk and Low Risk.

![credit_risk_2](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_2.png)

  Balanced accuracy score: 67%.

![credit_risk_3](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_3.png)

  The "High Risk" precision rate was 1% 
  The recall is 74% with this model F1 score of 2%.
  "Low Risk" had a precision rate of 100% and 
  recall at 61%.

![credit_risk_4](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_4.png)

  SMOTE (Synthetic Minority Oversampling Technique) Model, like RandomOverSampler increases the size of the minority class by creating new values based on the value of the closest neighbors to the minority class instead of random selection.

The balanced accuracy score did not change, it remains 67%.

![credit_risk_5](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_5.png)

Like RandomOverSampler, the "High Risk" precision rate again was only 1% with the recall maintained at 74% giving this model an F1 score of 2%.
"Low Risk" had a precision rate of 100% and an recall maintained at 61%.

![credit_risk_6](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_6.png)

ClusterCentroids Model, an algorithm that identifies clusters of the majority class to generate synthetic data points that are representative of the clusters. The model classified 246 records each as High Risk and Low Risk.

![credit_risk_7](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_7.png)

Balanced accuracy score was did not change at 67%.

![credit_risk_8](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_8.png)

The "High Risk" precision rate again was only at 1% with the recall at 74% giving this model an F1 score of 1%.
"Low Risk" had a precision rate of 100% and with a recall at 61% as the oversampling models.

![credit_risk_9](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_9.png)

**Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk**

Combination Sampling
SMOTEENN (Synthetic Minority Oversampling Technique + Edited NearestNeighbors) Model combines aspects of both oversampling and undersampling. The model classified 68,458 records as High Risk and 62,022 as Low Risk.


![credit_risk_10](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_10.png)

The balanced accuracy score remained at 67% when using a combined sampling model.

![credit_risk_12](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_12.png)

The "High Risk" precision rate did not improve was only 1%
"Low Risk" still showed a precision rate of 100% with the recall remaining at 61%.

![credit_risk_11](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_11.png)

**Deliverable 3**

Use Ensemble Classifiers to Predict Credit Risk
Compare two new Machine Learning models that reduce bias to predict credit risk. The models classified 51,366 as High Risk and 246 as Low Risk.

![credit_risk_13](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_13.png)

BalancedRandomForestClassifier Model, two trees of the same size and equal size to the minority class are constructed to represent one for the majority class and one for the minority class.

The balanced accuracy score increased to 78.9% for this model.

![credit_risk_14](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_14.png)

The "High Risk precision rate increased to 3% with the recall at 70% giving this model an F1 score of 6%.
"Low Risk" still had a precision rate of 100% with the recall at 87%.
The top feature by importance was "total_rec_prncp" at 7.9% of the total.

![credit_risk_15](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_15.png)

EasyEnsembleClassifier Model, a set of classifiers where individual decisions are combined to classify new examples.

The balanced accuracy score increased to 93.2% with this model.

![credit_risk_16](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_16.png)

The "High Risk precision rate increased to 9% with the recall at 92% giving this model an F1 score of 16%.
"Low Risk" still had a precision rate of 100% with the recall now at 94%.

![credit_risk_17](https://github.com/FUNMIIB/Credit_Risk_Analysis/blob/main/credit_risk_17.png)

**Deliverable 4**
**Summary**

The EasyEnsembleClassifer model yielded the best results with an accuracy rate of 93.2% and a 9% precision rate when predicting "High Risk candidates. The sensitivity rate was also the highest at 92% compared to the other models. The result for predicting "Low Risk" was also the highest with the sensitivity rate at 94% and an F1 score of 97%. 


Therefore, to perform this type of analysis, EasyEnsembleClassifier Model is recommended. 

