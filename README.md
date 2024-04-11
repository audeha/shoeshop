# Shoeshop Return Prediction Model

This repository contains the machine learning model for predicting whether an item sold by a shoeshop will be returned.  <br />
The model is built using a dataset of transactions stored in `transactions.parquet` (not uploaded in repo). 

## Dataset

The dataset `transactions.parquet` includes various features extracted from the transaction records of a shoeshop.  <br />It is structured in a way that each row represents a unique transaction, and each column represents a feature that could be related to the likelihood of an item being returned.

## Model

2 models are compared, you can see the results in file pycaret_comp.pdf <br />
If you open the file and scroll at the end of it, you can see the blue bars for model1 and orange bars for model2. <br />
Preprocessing steps (such as scaling, encoding, missing value imputation) have been applied to both dataset. <br />
The difference is that for model 1 missing values have been imputed using a simple strategy; filling missing numeric values with the mean and categorical values with the mode. <br />
In model 2 the Yeo-Johnson method was used to transform the data and data normalization was applied.  <br />
We can see that the Revenue has a significant impact on the prediction of the model, so if an item will be returned or not. <br />
We can also see that CustomerID, Shop and ProductCode have an impact, while BrandName, ModelGroup and ProductGroup seem to have no impact on the prediction. <br />

In the next file we focus our analysis for model2 since it has higher difference in feature importance.

## Analysis

In file pycarettest.pdf there are the results of the analysis of model2.  <br />
We can see the transformation pipelinefor both models.  <br />
In table 'best = compare_models()' we see metrics for model2 and that we can choose from 3 models: Random Forest Classifier with high accuracy but low AUC, Logistic Regression with high AUC and Decision Tree Classifier with low AUC.  <br />
We choose the Random Forest Classifier but we could change some parameters to get better results.  <br />

When creating the model 10-fold we get a new table with highlighted mean scores. <br />
It shows that our model is consistently high in accuracy but struggles with AUC and Recall.  <br />
This could indicate the model is performing well on the majority class but not as well on the minority class, which is common in imbalanced datasets. 

## To improve given more time

Compare models playing with different parameters to get better results for AUC and Recall. <br />
We could also try to balance the dataset to improve the model's performance.

