# Project 4: Final Project

# Hearts disease

## Introduction

For this project, we will be evaluating the heart.csv obtained from Kaggle: https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset in order to traing a deep learning model to predict when a patient has a heart disease or not. This data set dates from 1988 and consists of four databases: Cleveland, Hungary, Switzerland, and Long Beach V. It contains 76 attributes, including the predicted attribute, but all published experiments refer to using a subset of 14 of them. The "target" field refers to the presence of heart disease in the patient. It is integer valued 0 = no disease and 1 = disease.


## Database & Variables 
- age - age in years 
- sex - (1 = male; 0 = female) 
- cp - chest pain type 
- trestbps - resting blood pressure (in mm Hg on admission to the hospital) 
- chol - serum cholestoral in mg/dl 
- fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false) 
- restecg - resting electrocardiographic results 
- thalach - maximum heart rate achieved 
- exang - exercise induced angina (1 = yes; 0 = no) 
- oldpeak - ST depression induced by exercise relative to rest 
- slope - the slope of the peak exercise ST segment 
- ca - number of major vessels (0-3) colored by flourosopy 
- thal - 3 = normal; 6 = fixed defect; 7 = reversable defect 
- target - have disease or not (1=yes, 0=no)

<img width="724" alt="Captura de pantalla 2023-09-04 a la(s) 19 56 31" src="https://github.com/emilioaristegui/project-4/assets/128106993/10d6767b-095a-4bb3-921a-817b9bd060bd">


## Data Exploration

Our dataset contains over 1,000 rows, for which we dive into the information that we had to have a better understanding of our results.

In this grafic, we can see the amount of people on the dataset that has a heart disease vs the ones that doesn't
<img width="579" alt="Captura de pantalla 2023-09-04 a la(s) 19 56 43" src="https://github.com/emilioaristegui/project-4/assets/128106993/810cd2c4-e9a6-411f-9bc7-8975dee5f959">

We discovered that our study covers mainly men with almost 700 people. 
Note: 0 is for woman, 1 is for man
<img width="586" alt="Captura de pantalla 2023-09-04 a la(s) 19 56 53" src="https://github.com/emilioaristegui/project-4/assets/128106993/eda650a6-80c2-4205-af28-f221cc4354f3">

A graph with resting blood pressure (in mm Hg on admission to the hospital) vs age
<img width="1161" alt="Captura de pantalla 2023-09-04 a la(s) 19 57 07" src="https://github.com/emilioaristegui/project-4/assets/128106993/09901df6-527f-4baf-9e53-4521c2aec961">

thalach - maximum heart rate achieved in the hospital per age
<img width="1162" alt="Captura de pantalla 2023-09-04 a la(s) 19 57 16" src="https://github.com/emilioaristegui/project-4/assets/128106993/85ba47cd-4523-4a2a-924a-83002d52d56b">

Confusion matrix
<img width="1328" alt="Captura de pantalla 2023-09-04 a la(s) 19 57 29" src="https://github.com/emilioaristegui/project-4/assets/128106993/fc022d8b-3fc2-4b94-abcc-eb653d6ec6ee">

## Model training

1. We split our data, designating y as the taget (If the person had a disease or not)
2. We used the StandardScaler feaure

# Compile, Train and Evaluate the Model
As mentiones above, we used the deep learning method to train our model and get the best possible outcome.

## First attempt
For the first attempt we used two layers on activation = relu and an output layer on tahn. We decided to use the loss and accuracy to evaluate our model.

Loss: 1.4483760595321655, Accuracy: 0.43968871235847473
activation: softmax because we're not using just binary but we're using also using integers
