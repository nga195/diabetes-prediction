# Diabetes Prediction using Decision Tree
Operated Decision Tree Classification to predict diabetes outcomes based on key health metrics, identifying significant features influencing the diagnosis.

## Table of Contents

- [Introduction](#introduction)
- [Data Description](#data-description)
- [Research Questions](#research-questions)
- [Methodology](#methodology)
- [Analysis](#analysis)
- [Result and discussion](#result-and-discussion)
- [References](#references)


## Introduction
This report explores the use of a Decision Tree Classifier to predict diabetes outcomes based on various health metrics. The primary goal is to analyze a dataset containing patient information to determine the factors influencing diabetes prediction and assess the model's performance. Decision Trees are selected for their interpretability and ability to capture non-linear relationships in data.

## Data Description

The dataset consists of medical attributes collected from individuals, with the following key features:

Feature	Description:

- Pregnancies:	Number of times pregnant
- Glucose	Plasma: glucose concentration
- BloodPressure:	Diastolic blood pressure
- SkinThickness:	Triceps skin fold thickness
- Insulin:	2-Hour serum insulin
- BMI:	Body Mass Index
- DiabetesPedigreeFunction:	Diabetes pedigree function
- Age:	Age of the individual (in years)
- Outcome:	Diabetes diagnosis (1 = positive, 0 = negative)
  
The dataset is structured for analysis, allowing for the identification of key features that influence the prediction of diabetes.



## Research Questions

1. What features most significantly impact diabetes prediction?

This question seeks to identify the attributes within the dataset that contribute most to the classification of diabetes outcomes.

2. How well does the Decision Tree model predict diabetes?

This focuses on evaluating the model’s accuracy, precision, and other performance metrics to assess its predictive capability.

## Methodology

**Data Preparation**

The dataset was divided into training and testing sets, with 80% of the data allocated for training and 20% for testing. Key steps in the methodology include:

1. Feature Selection: The model utilizes features such as Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, and Age.
2. Model Creation: A Decision Tree Classifier was initialized with a maximum depth of 3 for initial training.
3. Performance Evaluation: The model's effectiveness was assessed using confusion matrices, classification reports, and cross-validation.

**Hyperparameter Tuning**

To optimize model performance, a grid search was conducted over parameters such as max_depth, min_samples_split, and min_samples_leaf. The best parameters were determined through cross-validation.

## Analysis


**Initial Model Training**

The Decision Tree model was built using the training dataset, determining a split threshold and calculating Gini impurity for each feature. Glucose emerged as the most significant predictor of diabetes, with a Gini impurity of 0.3317, indicating its strong ability to differentiate between diabetic and non-diabetic cases.

**Model Evaluation**

Precision for non-diabetic cases (0) is 0.79, while for diabetic cases (1) it is 0.57. Recall for non-diabetic cases is 0.75, and for diabetic cases, it is 0.62. The model achieves an overall accuracy of 71%, correctly classifying this proportion of instances in the test set. The macro average for precision and recall is around 0.68, indicating balanced performance across classes but lower effectiveness for diabetic predictions. The weighted average maintains a score of 0.71, reflecting the model's overall effectiveness considering class imbalance.

**Cross-Validation**

Cross-validation yielded a mean score of approximately 0.751, confirming consistent predictive performance across different data subsets and reinforcing the model's robustness.




## Result and discussion


The Decision Tree model achieved a reasonable overall accuracy of 71%. The analysis highlighted Glucose as the most critical feature for diabetes prediction, emphasizing its role in distinguishing between diabetic and non-diabetic patients.

However, the precision for positive predictions (diabetic cases) indicates an area for improvement, as the model may benefit from further optimization. Hyperparameter tuning successfully identified optimal parameters, enhancing the model’s performance.

Future work could involve exploring more complex models or additional feature engineering to further improve predictive capabilities, particularly for accurately identifying diabetic patients.


## References





