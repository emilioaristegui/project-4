# Project 4: Final Project

# Hearts disease

## Introduction

For this project, we will be evaluating the heart.csv obtained from Kaggle: https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset. This data set dates from 1988 and consists of four databases: Cleveland, Hungary, Switzerland, and Long Beach V. It contains 76 attributes, including the predicted attribute, but all published experiments refer to using a subset of 14 of them. The "target" field refers to the presence of heart disease in the patient. It is integer valued 0 = no disease and 1 = disease.

We will use deep learning model to predict if a patient is most likely to get a heart disease or not


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

+---+---+---+--------+----+---+-------+-------+-----+-------+-----+---+----+------+
|age|sex| cp|trestbps|chol|fbs|restecg|thalach|exang|oldpeak|slope| ca|thal|target|
+---+---+---+--------+----+---+-------+-------+-----+-------+-----+---+----+------+
| 52|  1|  0|     125| 212|  0|      1|    168|    0|      1|    2|  2|   3|     0|
| 53|  1|  0|     140| 203|  1|      0|    155|    1|    3.1|    0|  0|   3|     0|
| 70|  1|  0|     145| 174|  0|      1|    125|    1|    2.6|    0|  0|   3|     0|
| 61|  1|  0|     148| 203|  0|      1|    161|    0|      0|    2|  1|   3|     0|
| 62|  0|  0|     138| 294|  1|      1|    106|    0|    1.9|    1|  3|   2|     0|
| 58|  0|  0|     100| 248|  0|      0|    122|    0|      1|    1|  0|   2|     1|
| 58|  1|  0|     114| 318|  0|      2|    140|    0|    4.4|    0|  3|   1|     0|
| 55|  1|  0|     160| 289|  0|      0|    145|    1|    0.8|    1|  1|   3|     0|
| 46|  1|  0|     120| 249|  0|      0|    144|    0|    0.8|    2|  0|   3|     0|
| 54|  1|  0|     122| 286|  0|      0|    116|    1|    3.2|    1|  2|   2|     0|
| 71|  0|  0|     112| 149|  0|      1|    125|    0|    1.6|    1|  0|   2|     1|
| 43|  0|  0|     132| 341|  1|      0|    136|    1|      3|    1|  0|   3|     0|
| 34|  0|  1|     118| 210|  0|      1|    192|    0|    0.7|    2|  0|   2|     1|
| 51|  1|  0|     140| 298|  0|      1|    122|    1|    4.2|    1|  3|   3|     0|
| 52|  1|  0|     128| 204|  1|      1|    156|    1|      1|    1|  0|   0|     0|
| 34|  0|  1|     118| 210|  0|      1|    192|    0|    0.7|    2|  0|   2|     1|
| 51|  0|  2|     140| 308|  0|      0|    142|    0|    1.5|    2|  1|   2|     1|
| 54|  1|  0|     124| 266|  0|      0|    109|    1|    2.2|    1|  1|   3|     0|
| 50|  0|  1|     120| 244|  0|      1|    162|    0|    1.1|    2|  0|   2|     1|
| 58|  1|  2|     140| 211|  1|      0|    165|    0|      0|    2|  0|   2|     1|
+---+---+---+--------+----+---+-------+-------+-----+-------+-----+---+----+------+
only showing top 20 rows

## Data Exploration

![Uploading image.png…]()

## Model training

1. We split our data, designating y as the taget (If the person had a disease or not)
2. We used the StandardScaler feaure

# Compile, Train and Evaluate the Model
As mentiones above, we used the deep learning method to train our model and get the best possible outcome.

## First attempt
For the first attempt we used two layers on activation = relu and an output layer on tahn. We decided to use the loss and accuracy to evaluate our model.

Loss: 1.4483760595321655, Accuracy: 0.43968871235847473
activation: softmax because we're not using just binary but we're using also using integers
