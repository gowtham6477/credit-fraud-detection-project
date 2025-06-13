# Credit-Card-Fraud-Detection

![Python](https://img.shields.io/badge/Python-3.8.10-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-LightGBM-orange)
![Tuning](https://img.shields.io/badge/Tuning-Optuna-red)
![Deployment](https://img.shields.io/badge/Dashboard-Plotly-purple)


## Introduction
It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase...

## Problem Statement
With the provided information, build a model to predict whether this customer will commit fraud when using a credit card or not.

## Description
This data set is [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) from Kaggle. The dataset contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

### Exploratory Data Analysis
* Due to security issues, the original features V1, V2, ... V28 have been modified by PCA. However, we can guess that these features could be credit card number, expiration date, CVV, cardholder name, transaction location, transaction datetime, etc.
The only two features that have not been converted with PCA are ```Time``` and ```Amount```. Therefore, we only need to focus on processing these two features

### Data Preprocessing
* Log transform ```amount``` feature
* Handling Data Imbalance: I used **SMOTE** method for balancing the dataset. 
* **Robust scaling** all data

### Features Selection:
* On using **Pearsonr Correlation** method, I don't need to drop any features.

### Model Training

#### Training lists
* Widely used ML models: Logistic Regression, Decision Tree, Random Forest, LightGBM, Catboost, XGBoost, AdaBoost
#### Amount and Time

<p align='center'>
    <img src="download (5).png"/>
</p>

#### Training score and cross validation score

<p align='center'>
    <img src="download (3).png"/>
</p>

#### Training set and validation set

<p align='center'>
    <img src="9101820.jpg"/>
</p>

#### precision-recall curve
<p align='center'>
    <img src="download (6).png"/>
</p>
