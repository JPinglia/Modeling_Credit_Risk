# Modeling Credit Risk

## Overview of the Analysis
### Purpose of the analysis:

The purpose of this analysis is to help determine credit risk and identify risk loans within a data set. We are tasked to create a machine learning model to help classify the loans and help lenders determine the credit worthiness of clients. 


The financial data provided is a csv file with historical leading activity of borrowers for a peer-to-peer leading services company. As an example information contained includes, loan size, loan interest rates, burrowers income, debt to income ratios, total debt etc. etc.


The goal of the machine leaning model is to detect loan status (our target values), a loan status marked (0) is heathy and a loan status marked (1) is considered high risk.

### Stage of modeling and analysis: 
Original Model:
- CSV data is read into jupyter labs file
- Data is separated into X (features) and y (target) variables
- Data is split into training and testing model data sets
- Logistic Regression model is chosen to fit the data and determine an optimal model 
- Model outputs are tested against testing data to determine model metrics for model performance

Resampled Model:
In addition to above, the data is resampled to fix data imbalances.
- Data is randomly resampled with an oversampling method. 
- Logistic Regression Model is applied 
- Metrics determined

Logistic Regression: is a statistical model that uses a log function to model binary decision making. Example: 1 and 0. 

Resampling Method: method of resampling data for imbalanced data sets, methods include oversampling, under-sampling, or mixed sampling data. Resampling can help to improve the training or a model. An example: A student is learning Math and English but spends 95% of his time on English and is then tested on Math. The student can’t be expected to perform well. Resampling helps to train the student in equal amount of Math and English and then tests the student for improvement. 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

### Machine Learning Model 1:

![original_confusion_matrix](https://user-images.githubusercontent.com/95830866/159170533-29365900-e0ab-4324-a0b6-6f3de703198c.PNG)

![original_classification_report](https://user-images.githubusercontent.com/95830866/159170523-a47fb219-96b1-40a0-aba7-86a4d28158c8.PNG)

Description of Model 1 Accuracy, Precision, and Recall scores.

- Precision was 100% for class 0 and 85% for class 1. 
- Recall was 99% for class 0 and 91 % for class 1. 
- Model Accuracy was 95.2% 

Although we have a high precision and recall scores, we have a highly imbalanced data set. The results of this model are meaningless. The goal was to have our model capture high risk loans. The model has a precision of 85% and recall of 91% of or class 1 with 619 high risk loans. We can however conclude our model is good at determining the 0 class, or healthy loans.

### Machine Learning Model 2:

![resampled_confusion_matrix](https://user-images.githubusercontent.com/95830866/159170544-e87b9d54-c2ad-48cf-96df-2cfb4e3131b0.PNG)

![resampled_classification_report](https://user-images.githubusercontent.com/95830866/159170553-6b1a8756-111a-4e19-a453-043a885e35e7.PNG)

Description of Model 2 Accuracy, Precision, and Recall scores.

- Precision was 100% for class 0 and 84% for class 1. 
- Recall was 99% for class 0 and 99 % for class 1. 
- Model Accuracy was 99.3% 

Oversampling the data helped to improve the model's recall, F1-score at the expense of 0.01 or 1 % of precision. This is a better model than ordinal we we capture 99% of the high-risk loans, with recall. With a precision of 84% we can refer all the high-risk loans for further analysis. Our model still performs well at capturing all the healthy loans with 99% recall at a rate of 100% precision.

## Summary

Based on the results as summarized above. The best machine learning model to use for accurately predicting high risk loans is the oversampled model. The model more efficient at capturing 99% of high-risk loans and this will allow the leaders to further assess loan related risk. It is important to ensure we capture all high-risk loans thus the importance for a high recall rate, having good precision of 85% for class 1 is a bonus. Both models are good at capturing healthy loans within class 0. 
The oversampled model is the clear winner, with a model accuracy of 99.3%.



