
# Project Overview
In this project we are going to build a machine learning model to predict whether or not an applicant will default on their loan for the [Home Credit Default Risk](https://www.kaggle.com/c/home-credit-default-risk/data) competition  on Kaggle.  As part of the competition, Home Credit have providing historical data on actual clients and loans.
This is a standard Binary Classification problem.

# Data
The data is provided by Home Credit, a service dedicated to provide lines of credit (loans) to the unbanked population. There are 7 different sources of data:
- application_train: the main data with information about each loan application at Home Credit. Every loan has its own row and is identified by the feature SK_ID_CURR. The application data comes with the TARGET indicating 0: the loan was repaid or 1: the loan was not repaid. We will only be using application_train data and not the test data for our project.
- bureau: data concerning client's previous credits from other financial institutions. Each previous credit has its own row in bureau, but one loan in the application data can have multiple previous credits.
- bureau_balance: monthly data about the previous credits in bureau. Each row is one month of a previous credit, and a single previous credit can have multiple rows, one for each month of the credit length.
- previous_application: previous applications for loans at Home Credit of clients who have loans in the application data. Each current loan in the application data can have multiple previous loans. Each previous application has one row and is identified by the feature SK_ID_PREV.
- POS_CASH_BALANCE: monthly data about previous point of sale or cash loans clients have had with Home Credit. Each row is one month of a previous point of sale or cash loan, and a single previous loan can have many rows.
- credit_card_balance: monthly data about previous credit cards clients have had with Home Credit. Each row is one month of a credit card balance, and a single credit card can have many rows.
- installments_payment: payment history for previous loans at Home Credit. There is one row for every made payment and one row for every missed payment.

Some datasets are related to each other. We are also provided with the definitions of all the columns (in HomeCredit_columns_description.csv). The datasets can be found [here](https://www.kaggle.com/competitions/home-credit-default-risk/data) and they are free to download and use.

# Goal
An important fraction of the population finds it difficult to get their home loans approved due to insufficient or absent credit history. This prevents them to buy their own dream homes and at times even forces them to rely on other sources of money which may be unreliable and have exorbitant interest rates. Conversely, it is a major challenge for banks and other finance lending agencies to decide for which candidates to approve housing loans. The credit history is not always a sufficient tool for decisions, since it is possible that those borrowers with a long credit history can still default on the loan and some people with a good chance of loan repayment may simply not have a sufficiently long credit history.
The goal of this project is to a build a model which can ensure that applicants capable of repayment are not rejected, thereby empowering their applicants/clients to be successful.

# Code 
Please refer the ipynb notebooks for a detailed walkthrough of the entire project. If you are not able to view any notebook please copy the url of the notebook and paste it in [nbviewer.org](https://nbviewer.org/) and you will be able to view it there.

# Workflow
1.  Exploratory Data Analysis   
    - Basic Checks
    - Missing Values
    - Target Variable
    - Numerical Features
    - Discrete Features
    - Continuous Features
    - Categorical Features
    - Outliers
    - Correlation
    - Multicollinearity
2.  Feature Engineering
    - Discarding Missing values above threshold
    - Removing Multicollinear features above threshold value
    - Handling Outliers
    - Imputing Missing Values
    - Encoding
    - Aggregations and groupby
    - Checking for duplicates
    - Checking for constant values
    - Final Preprocessing after merging all dataframes
3.  Feature Selection, Model Building and Evalation  
    - Train Test Split
    - Scaling
    - Feature Selection
    - Models
    - Performance Table
    - Hyper tune few Models
    - Hyper tuned model Performance table
    - Feature Importance
    - Threshold Impact

# Evalation Metric
We will be using the Receiver Operating Characteristic Area under the curve (ROC AUC score) Metric. The ROC curve is useful for predicting the probability of a binary outcome such as our case (loan default versus non-default). The ROC curve plots the false positive rate (x-axis) versus the true positive rate (y-axis) for a number of different candidate threshold values between 0.0 and 1.0. One benefit of the ROC curves is that different models can be compared directly in general or for different thresholds using the area under the curve (AUC) measurement. A higher AUC score means a better model.

# Contributers
Akshay Shettigar

# Acknowledgments
Inspirations are drawn from various Kaggle notebooks but majorly motivation is from the following :
- [Start Here: A Gentle Introduction - WILL KOEHRSEN](https://www.kaggle.com/code/willkoehrsen/start-here-a-gentle-introduction) and rest of his notebooks.
- [LightGBM with Simple Features - AGUIAR](https://www.kaggle.com/code/jsaguiar/lightgbm-with-simple-features)
- [Simple Bayesian Optimization for LightGBM - OSKIRD](https://www.kaggle.com/code/sz8416/simple-bayesian-optimization-for-lightgbm)

