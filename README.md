# Credit Risk Prediction 

## Background
The objective is to evaluate different sampling models to determine which model is recommended for credit risk prediction. 

The important criteria for a lending facility should be a model that optimzes prediction of high risk, ie, more emphasis should be paid to sensitivity (recall) score for high risk prediction in order for the lending facility not to lend at a loss. 

## 1) Random Oversampling
The accuracy score is 0.65, with a high risk precision score of 0.01, high risk recall score of 0.62, and average F1 score of 0.80.

With only 0.62 recall score, the model isn't very accurate in helping to classify the potential high-risk borrowers.  With a very low precision score it also causes potential loss to the bank as it turns away a lot of low-risk borrowers. 
<img src = "https://github.com/pegkhiev/ML_credit_risk_prediction/blob/master/Module-17-Challenge/Images/Random_oversampling.png">

## 2) SMOTE Oversampling 
The accuracy score is 0.64, with a high risk precision score of 0.01 and a high risk recall score of 0.63 and average F1 score of 0.79.

As sensitivity is more important for the bank in preventing default, this SMOTE recall score is marginally higher than Random Oversampling model, and yet still low. 
<img src = "https://github.com/pegkhiev/ML_credit_risk_prediction/blob/master/Module-17-Challenge/Images/SMOTE_oversampling.png">

## 3) Under Sampling
The accuracy score is only 0.51, with a high risk precision score of 0.01 and a high risk recall score of 0.61 and average F1 score of 0.57.

This model performance is very poor with only half of the time being accurate.  The recall rate is also lower than the other two models, mostly due to not sufficient observances in the dataset (only 246 in the training set).
<img src = "https://github.com/pegkhiev/ML_credit_risk_prediction/blob/master/Module-17-Challenge/Images/Under_sampling.png">

## 4) SMOTE ENN Sampling 
The accuracy score is 0.62, with a high risk precision score of 0.01 and a high risk recall score of 0.68 and average F1 score of 0.72.

Even though the accuracy score is lower than random and SMOTE oversampling, the high risk recall score is the highest at 0.68, so out of the four models, the best one in classifying the high-risk borrowers. 
<img src = "https://github.com/pegkhiev/ML_credit_risk_prediction/blob/master/Module-17-Challenge/Images/SMOTEENN_sampling.png">

## 5) Balanced Random Forest Classifier 
The accuracy score is 0.78, with a high risk precision score of 0.04 and a high risk recall score of 0.67 and average F1 score of 0.94.

The F1 score has improved to 0.07 but the high risk recall score is just 0.67, still not accurate enough to be used by a pank to prevent most false negatives of high-risk borrowers. 
<img src = "https://github.com/pegkhiev/ML_credit_risk_prediction/blob/master/Module-17-Challenge/Images/Balanced_forest.png">

## 6) Easy Ensemble AdaBoost Classifier 
The accuracy score is 0.93, with a high risk precision score of 0.09 and a high risk recall score of 0.92 and average F1 score of 0.97.

Though the high risk precision score is low due to the imbalanced sample size, the high risk recall score is very high and hence effective in predicting and preventing false negatives of high risk borrowers. 
<img src = "https://github.com/pegkhiev/ML_credit_risk_prediction/blob/master/Module-17-Challenge/Images/Easy_ensemble.png">

## Recommendation 
Out of the all models, I would recommend the Easy Ensemble AdaBoost Classifier as it clearly demonstrates that it is the most accurate in predicting high-risk borrowers to prevent default loans.  The high recall score of 0.92 is robust for a lending facility in preventing loss by predicting high-risk borrowers. 
