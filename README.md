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
  - SVC Model
  - Logistic Regression
  - Logistic Regression with backward features elimination
  - KNN Model
  - DecisionTree Model
- Comparing Results

The code is ordered in the sequence.

## Performance Metric

In our classification model, we are using the the f1 and recall scoring metrics to minimize the misclassification of individuals who should seek treatment as the cost associated with leaving those individuals untreated are high as research has shown.

## Results

![alt text](imgs/Confusion%20Matrix.png)

|                             	| Test Scores 	|      	| CV Scores 	|      	|
|-----------------------------	|-------------	|------	|-----------	|------	|
| Model                       	| Recall      	| f1   	| Recall    	| f1   	|
| DecisionTree                	| 0.79        	| 071  	| 0.81      	| 0.77 	|
| SVC                         	| 0.72        	| 0.73 	| 0.74      	| 0.74 	|
| Logistic                    	| 0.72        	| 0.72 	| 0.74      	| 0.74 	|
| Random Forest               	| 0.71        	| 0.71 	| 0.79      	| 0.77 	|
| Logistic Backward Selection 	| 0.70        	| 0.70 	| 0.73      	| 0.73 	|
| KNN                         	| 0.63        	| 0.64 	| 0.60      	| 0.64 	|

Upon testing the models on our test data set, we were able to reach approximately equivalent results with the different models. However, the SVC model performed slightly better than the other models. Also, notably the KNN have performed a lot worse than all the other models. One explanation to this is that KNN relies on distances between features and the majority of our features are categorical with relatively few categories.

## Conclusion

Using data from the tech mental health survey collected from Kaggle, we built 6 machine learning models and came up with the one that would most efficiently identify individuals who are most likely to seek mental health treatment. We utilized the recall and f1 metrics, to minimize the chance of misclassifiying a potentially sick individuals.

Using the DecisionTreeClassifier, we were able to correctly predict and identify 79% of the people who have seeked treatment.

## Contributors

- Hammad Habib Qazi
- Peiying Li