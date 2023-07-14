## Credit-Card-Approval-Prediction
![image](https://github.com/ndungek/Credit-Card-Approval-Prediction/assets/124627374/5244e353-a1ce-4476-b220-ecdea5a081a7)


# Business Understanding
# 1.1 Introduction

In the financial industry, credit score cards are extensively utilized to evaluate the risk associated with issuing credit cards to applicants. These cards utilize historical data to anticipate potential defaults and credit card borrowing patterns, enabling banks to make well-informed decisions regarding card approval. Nevertheless, the reliability of traditional approaches, such as assessing financial metrics like debt-to-income ratios and utilization ratios can be impacted by economic fluctuations. To enhance credit scoring, alternative methods like machine learning algorithms have been introduced. Although these methods enhance prediction accuracy, they often lack transparency, creating challenges in providing clear explanations for acceptance or rejection decisions to both customers and regulatory bodies.

# 1.2 Problem Statement

The existing credit scoring methods rely on historical data and traditional financial metrics like debt-to-income ratios, face limitations in accurately predicting creditworthiness due to economic fluctuations. The introduction of machine learning algorithms has shown promise in enhancing credit scoring accuracy but lacks transparency in explaining acceptance or rejection decisions. As a result, there is a need to develop a credit scoring model that leverages both historical data and advanced machine learning techniques to improve prediction capabilities while providing transparent and interpretable results for customers and regulators. The objective is to create a reliable and transparent credit scoring system that effectively assesses the risk of issuing credit cards based on applicants' personal information, contributing to informed decision-making by financial institutions and ensuring fair treatment of applicants.

The end user is the bank that will use this deployment in conjunction with their own to complement the credit scoring system

# 1.3 Project Objectives

Develop a credit scoring model that incorporates personal and social factors and machine learning algorithms to enhance the accuracy of creditworthiness predictions.
Improve transparency in credit scoring by utilizing interpretable machine learning techniques, allowing for clear explanations of acceptance or rejection decisions to customers and regulatory bodies.
Mitigate the impact of economic fluctuations on credit scoring models by incorporating dynamic factors and adapting the model to changing economic conditions.
Optimize the balance between prediction accuracy and interpretability to ensure a fair and reliable credit scoring system for both applicants and financial institutions.

# 1.4 Success Metrics.

We set a specific target for our credit card approval prediction model, aiming to achieve a recall score of 80%. This means our focus is on maximizing the identification of approved credit card applications, minimizing the chances of false negatives and ensuring a high level of accuracy in predicting positive outcomes.

# 2. Data Understanding

This phase is broken down into four tasks together with its projected outcome or output in detail:

Collect Initial Data
Describe Data
Explore Data
Verify Data Quality

The data for this project was sourced from Kaggle . This data consists of information of past application and credits

# 2.1 Applications Dataset

Feature name 	Explanation
ID 	Client number
CODE_GENDER 	Gender
FLAG_OWN_CAR 	Is there a car
FLAG_OWN_REALTY 	Is there a property
CNT_CHILDREN 	Number of children
AMT_INCOME_TOTAL 	Annual income
NAME_INCOME_TYPE 	Income category
NAME_EDUCATION_TYPE 	Education level
NAME_FAMILY_STATUS 	Marital status
NAME_HOUSING_TYPE 	Way of living
DAYS_BIRTH 	Birthday
DAYS_EMPLOYED 	Start date of employment
FLAG_MOBIL 	Is there a mobile phone
FLAG_WORK_PHONE 	Is there a work phone
FLAG_PHONE 	Is there a phone
FLAG_EMAIL 	Is there an email
OCCUPATION_TYPE 	Occupation
CNT_FAM_MEMBERS 	Family size

Note -
DAYS_BIRTH ---> Count backwards from current day (0), -1 means yesterday
DAYS_EMPLOYED ---> Count backwards from current day(0). If positive, it means the person currently unemployed.

# 2.2 Credits Dataset
Feature name 	Explanation
ID 	Client number
MONTHS_BALANCE 	Record month
STATUS 	Status

Note -
MONTHS_BALANCE ---> The month of the extracted data is the starting point, backwards, 0 is the current month, -1 is the previous month, and so on.
STATUS ---> 0: 1-29 days past due 1: 30-59 days past due 2: 60-89 days overdue 3: 90-119 days overdue 4: 120-149 days overdue 5: Overdue or bad debts, write-offs for more than 150 days C: paid off that month X: No loan for the month

# 2.3 Merged Dataset

# 3. Data Preparation

This phase, which is often referred to as “data munging”, prepares the final data set(s) for modeling. It has the following tasks:

Clean Data
EDA
Data Preprocessing

3.1 Clean Data

In this section, we will be looking at the missing values, duplicate records in the dataset as well as the outliers in the dataset.

3.1.1 Completeness

We will be considering the completeness of the dataset in this section. In this section, we will be looking at the missing values in the dataset.

3.1.2 Uniformity

In this section, we will be looking at the uniformity of the data. Uniformity refers to the consistency of the data with respect to the formatting, labelling. We will be looking at the following:

Labelling
Formatting

3.1.2.1 Labelling

Labelling refers to the consistency of the data with respect to the labelling of the data. We will be looking at the following:

Are the columns small case?
Are there any spaces?
Are they interpretable?

3.1.2.2 Formatting

The formatting of the data refers to the consistency of the data with respect to the datatypes of the columns.

3.1.3 Validity

In this section, we will be looking at the validity of the data. We will be looking at the following:

Duplicated Data
Outliers

3.1.3.1 Dealing with duplicates

3.1.3.2 Dealing with Outliers

Outliers are data points that significantly deviate from the majority of the data in a dataset. They are observations that lie at an abnormal distance from other observations, and they can have a substantial impact on statistical analyses and modeling.

Outliers can occur due to various reasons, such as measurement errors, data entry mistakes, natural variations, or genuine extreme values in the data.

# 3.2 Exploratory Data Analysis

In this section, we shall be exploring the columns in the dataset. We shall be performing the following

Univariate Analysis

Bivariate Analysis

Multi-variate Analysis

# 3.3. Data Preprocessing
3.3.1 Feature Engineering

3.3.2 Feature selection

# 4. Modeling

In the modeling phase, we will address the issue of class imbalance before training our models. We will start with a decision tree as our baseline model, which provides a good understanding of feature-target relationships. Then, we will explore ensemble models such as Random Forest, AdaBoost, Gradient Boosting, and XGBoost. 

4.1 Splitting the Dataset

4.2 Handling Class Imbalance

4.3 Decision Tree Classifier (Baseline Model)

4.4 Random Forest Classifier
- Random Forest Classifier with best parameters

4.5 AdaBoostClassifier

- AdaBoostClassifier with best parameters

4.6 Gradient Boosting

- 4.6.1 Gradient Boosting Classifier with best parameters

4.7 XGB Classifier

- 4.7.1 XGB Classifier with the best parameters

# 5. Model Evaluation.

The evaluation metric for this project is the recall score of the classes of the credit approval status in this project we are using the following algorithms to predict the credit approval status of each credit card applicant and these were the results.

# Decision Tree Classifier:
Rationale.

Results.

Limitations.

# Random Forest Classifier:
Rationale.

Results.

Limitations.

# Adaboost Rationale:
Rationale.

Results.

Limitations.

# Gradient Boost:
Rationale.

Results.

Limitations.

# XGBoost:
Rationale.

Results.

Limitations.

# Finding the best model, and incorporation shap values for recommendation purposes.

# Conclusion.

# Reccomendation.
