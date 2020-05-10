# Credit Risk Prediction 

## Background
The objective is to evaluate different sampling models to determine which model is recommended for credit risk prediction. 

The important criteria for a lending facility should be a model that optimzes prediction of high risk, ie, more emphasis should be paid to sensitivity (recall) score for high risk prediction in order for the lending facility not to lend at a loss. 

## 1) Random Oversampling
The accuracy score is 0.65, with a high risk precision score of 0.01, high risk recall score of 0.62, and F1 score of 0.02.

With only 0.62 recall score, the model isn't very accurate in helping to classify the potential high-risk borrowers.  With a very low precision score it also causes potential loss to the bank as it turns away a lot of low-risk borrowers. 

## 2) SMOTE Oversampling 
The accuracy score is 0.64, with a high risk precision score of 0.01 and a high risk recall score of 0.63 and F1 score of 0.02.

As sensitivity is more important for the bank in preventing default, this SMOTE recall score is marginally higher than Random Oversampling model, and yet still low. 

## 3) Under Sampling
The accuracy score is only 0.51, with a high risk precision score of 0.01 and a high risk recall score of 0.61 and F1 score of 0.01.

This model performance is very poor with only half of the time being accurate.  The recall rate is also lower than the other two models, mostly due to not sufficient observances in the dataset (only 246 in the training set) 

## 4) SMOTE ENN Sampling 
The accuracy score is 0.62, with a high risk precision score of 0.01 and a high risk recall score of 0.68 and F1 score of 0.02.

Even though the accuracy score is lower than random and SMOTE oversampling, the high risk recall score is the highest at 0.68, so out of the four models, the best one in classifying the high-risk borrowers. 

## Recommendation 
Out of the four models, none should be recommended for use in classifying and predicting borrowers. A sub-optimal model will cause a lot of loss to the lending facility if the model fails to classify high risk borrowers.  Out of the four evaluated models, the highese performing model is SMOTE-ENN sampling model with a high risk recall score of 0.68.  With 100,000 borrowers, 32,000 high risk borrowers would not be correctly classified and that could potentially cause the bank a huge loss.  

Therefore none of the models is robust enough to be used by a lending facility as its risk prediction model.  
