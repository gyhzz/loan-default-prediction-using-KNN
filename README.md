# Loan Default Prediction Using KNN with Data Cleaning, Exploratory Data Analysis, and Hyperparameter Tuning



## Problem Definition
This project is an attempt of Exploratory Data Analysis, as well as to build a machine learning model using a credit risk data set in order to predict the likelihood of a loan default. A lot of information is collected upon application of a loan in order to underwrite the risk a bank faces if they were to approve the loan. Some of these factors, such as default history, or credit history, generally gives the underwriter a clue on what the loan's risk might be however, there are many more factors that could impact this risk and are not as intuitive. Furthermore, in order for banks to maximize their profit margins by discovering lower risk applicants who might have had a default history or a high risk applicant without any credit history, it is imperative that each attribute of an applicant (that positively or negatively correlate to risk) be well scrutinized.

The data set used in this study was taken from https://www.kaggle.com/datasets/laotse/credit-risk-dataset

## Project Summary
#### Data Preparation
- Data was first prepared for analysis by standardizing column names, filling in missing values, and converting categorical data to 1s and 0s

#### Exploratory Data Analysis
- EDA was performed on the dataset to identify positive/negative/non-correlated features, as well as to get an overall understanding of the data using heatmaps, pie chart, bar charts, and scatter plots

#### Machine Learning Modelling
- Dataset was split 80% as training data and 20% as test data
- KNeighborsClassifer, LogisticRegression, DecisionTreeClassifier machine learning models were used
- KNeighborsClassifer gave the most accurate result of 89.04% with n = 8
- DecisionTreeClassifier was the second most accurate at 84.59%
- LogisticRegression was the least accurate at 84.24%

#### Hyper-parameter Tuning Using GridSearchCV
- Using GridSearchCV, the KNeighborsClassifer model was further improved from 89.04% accuracy to 89.49% accuracy
- Comparing the businesses cases of the 2 KNeighborsClassifier models, the first model returned an overall revenue of (5,219,600), while the second model returned an overall revenue of (4,298,300), a difference of 921,300

#### Limitations
- Dataset could include more negatively correlated features, as this data set seems to be overweight on positively correlation
- More time could be spend on adjusting each model's hyperparameter to find the highest accuracy of each model, since GridSearchCV's run time is qutie significant
