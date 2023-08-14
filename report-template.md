# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

Purpose: 
In this challange we are trying to train a supervised ML model in classifying loan status between healthy and high-risk. We do this by evaluating data provided from lending_data.csv

Financial Info:
As stated, data is pulled lending_data.csv which included relevnant financial information from debtors such as debt-to-income ratio, total debt, interest rate and loan status. The goal of the model is to evaluate the financial information and come to the correct conclusion on whether an account has a healthy loan or is high-risk. 

Variables: 
The loan status determines whether an account is either `0` healthy or `1` high-risk, as such it is the answer key needed to be separated from original dataframe. In this case there are far more healthy than high-risk accounts, causing an imbalanced dataset. 

Stages:
- First we import and analyse the data, then separate the answer key from the dataframe. 
- We can then split, the dataframe and if necessary, scale, then fit a model with training data.
- After fitting our model, we can test to see how it does with testing data, then compare it to the answer key.
- We resample our data to reduce overfitting, refit a model and test it a second time. 

Methodology:
As the dataset is imbalanced, we used RandomOverSampler to rebalance the dataset. From what I understand, models with imbalanced dataset has a higher chance of overfitting; resampling the data is an attemp to mitigate that. 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * The first model had great precision and recall regarding class 0, but suffered in precision-recall regarding class 0. 
  * From what I understand model 1 can correct identify healthy accounts and will not misinterpret a high-risk account as healthy. 
  * However, model 1 has difficulty correctly identifying high-risk accounts and can misinterpret a healthy account as high-risk. 


* Machine Learning Model 2:
  * The first model had great precision and recall regarding class 0, and improved in precision-recall regarding class 0 relative to the first model.
  * Model 2 can correct identify healthy accounts and will not misinterpret a high-risk account as healthy. 
  * Model 2 still has difficulty in precision, causing it to interpret some high-risk accounts as healthy. It however will not misinterpret healthy accounts as high-risk.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Model 2, with the resample data, seems to perform better than model 1. It showed better scores overall.
* Performance does depend on the context. In this case, as high-risk accounts are anomolies it would be best if the model could correctly determine an account as high-risk. In other words, it is more important to predict the `1`s.

From the evaluation I would not recommend either model. Model two can maybe serve as a first-line basis to evaluate accounts, but as it cannot (with sufficident degree of accuracy) determine if a loan would be healthy it would be difficult to employ as a reliable tool in determining loan status. 