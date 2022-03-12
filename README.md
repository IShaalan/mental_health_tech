# Prediction of Individuals in Tech Needing Mental Health Intervention

## Introduction

Technology companies are fast paced that might lead to very stressful working conditions, employees who have mental issues could lead to low productivity for the company and exacerbated mental conditions for themselves. The dataset of 2014 mental health survey in technology companies provide many workplace environment characterstics that help build machine learning algorithms to identify the individuals needing treatment based on their perception of the workplace and their condition. Our goal is to predict the employees in need of mental health treatment.

This document illustrates the process of performing the analysis.

## Data Source

The data is from the Kaggle website.

Source: https://www.kaggle.com/osmi/mental-health-in-tech-survey

**Data collected**
The data was collected in 2014

**Total Observations**

The data set has 1259 observations split betwen 637 seeked treatment and 622 didn't seek treatment from mental health issues.

**Total Features**

The dataset has 27 features with  missing values in the state (location), comments, work_interfere. We didn't use the state (only recorded for the united states) and comments (87% missing) in our analysis. We imputed the rest of the missing data.

## Installation

- Programming Language: Python v 3.9.7
- Data file should be located under 'data' folder within the same folder of the python notebook
- Use a package manager such as conda, miniconda or condaforge to install necessary libraries
- Packages
  - pandas: 1.3.5
  - numpy: 1.21.2
  - scikit-learn: 1.0.2
  - klib: 1.0.1
  - matplotlib: 3.5.0
  - altair: 4.1.0
  - IPython: 7.31.1

## Analysis Process

We applied the following process to achieve our results:

- Data loading
- Exploratory data analysis
- Feature selection
- Feature preprocessing
- Feature transformation
- Modeling
  - Support Vector Classifier
  - Logistic Regression Classifier
  - Logistic Regression with backward features elimination Classifier
  - KNN Classifier
  - DecisionTree Classifier
  - RandomForest Classifier
- Comparing Results

## Performance Metric

In our classification model, we are using the the f1 and recall scoring metrics to minimize the misclassification of individuals who should seek treatment as the cost associated with leaving those individuals untreated are high as research has shown.

## Results

![alt text](imgs/Confusion%20Matrix.png)

## Conclusion

Using data from the tech mental health survey collected from Kaggle, we built 6 machine learning models and came up with the one that would most efficiently identify individuals who are most likely to seek mental health treatment. We utilized the recall and f1 metrics, to minimize the chance of misclassifiying a potentially sick individuals.

## Contributors

- Hammad Habib Qazi
- Peiying Li