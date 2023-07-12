# Attrition-Analysis
Analyzing by Logistic regression model, Random Forest Model and Artificial Neural Networks

## Tools used  -  Pandas, Numpy, Sci-learn kit, MatplotLib, Seaborn, Tensorflow, Keras
## Data - 35 features in total, each contains 1470 data points

## Features 

<img width="520" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/f8ae3b6c-8571-448a-baed-090e441759ab">

## Basic stats of Dataset
* Mean age of the employees - 36 years
* Mean age of the employees who are leaving - 33 years
* Mean age of the employees who are staying - 37 years
* Number of employees who left the company = 237
* Percentage of employees who left the company = 16.122448979591837 %
* Number of employees who did not leave the company (stayed) = 1233
* Percentage of employees who did not leave the company (stayed) = 83.87755102040816 %

## Exploring Data

* Mean age of the employees who stayed is higher compared to who left
* 'DailyRate': Rate of employees who stayed is higher
* 'DistanceFromHome': Employees who stayed live closer to home 
* 'EnvironmentSatisfaction' & 'JobSatisfaction': Employees who stayed are generally more satisifed with their jobs
* 'StockOptionLevel': Employees who stayed tend to have higher stock option level

* We don't have any nulls
<img width="264" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/21bdaf0b-0797-4a3c-ae69-5ee302b0dbc8">

* Replacing the 'Attritition' and 'overtime' column with integers before performing any visualizations
<img width="530" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/95a61993-210d-4b40-ad11-7dda9bb626c2">

## Visualizing Dataset 
<img width="858" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/0b47a199-6cf6-4bd5-92e0-eb5a700cf1ed">

<img width="856" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/05c8fdf5-4db0-4308-8093-0ba1a325fb03">

<img width="856" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/f8cf4b25-1f08-4aec-90a0-bda5fddaddbf">

#### Looking at the figures 
* It makes sense to drop 'EmployeeCount' , 'Standardhours', 'EmployeeNumber' and 'Over18' since they do not change from one employee to the other

## Correlations

<img width="385" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/486395c5-4ef3-45f8-acf6-5db645769041">

#### From the above figure we analyze that
* Job level is strongly correlated with total working hours
* Monthly income is strongly correlated with Job level
* Monthly income is strongly correlated with total working hours
* Age is stongly correlated with monthly income

## Age vs Attrition rate

<img width="512" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/e04a55a7-a527-4cf3-a952-9cdcc9c9d37b">

## Some realationships between Y - variable and features
* 'Attrition' vs 'JobRole' , 'MaritalStatus', 'JobInvolvement', 'JobLevel'

<img width="515" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/8a3e85a1-ceac-4066-9f75-b910e64c65c2">
** Sales Representitives tend to leave compared to any other job **
<img width="516" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/2136b5b3-68ab-47a0-906f-b808ff3fee6f">
<img width="512" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/c2b0caa1-aa9d-44fe-b5a6-54bd83541d5d">
** Less involved employees tend to leave the company **
<img width="514" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/132905d9-a25f-4853-ba0f-7e6e340fc95c">
** Less experienced (low job level) tend to leave the company **

## Understanding more with KDE(Kernel Density Estimate)
* Kernel Density Estimate is used for visualizing the Probability Density of a continuous variable.
* We can visualize the relationship for 'DistanceFromHome' column Attrition
<img width="452" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/d4140f27-7e4e-4d0f-ae00-bcb64cb5c211">

* The relationship for 'YearsWithCurrManager' column Attrition
<img width="410" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/76e8bab8-54ac-43ad-a88b-72191108be64">

* The relationship for 'YearsWithCurrManager' column Attrition
<img width="411" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/d3d40e86-9d0d-4341-bcd4-adec9e8b673c">

# Creating Prediction Model
## Doing Random Sampling 
### First converting all the text and categorical columns to numbers 

<img width="308" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/bb4a6c78-c298-46b2-ac2d-3b0bcc17ac93">

## Scaling 
* So that all the integers will be in the range of 0 to 1

## Building a Logistic Regression Model

<img width="313" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/6d3f18ab-73ec-41cc-b1fe-3d4e94dd74f0">

#### Confusion marix

<img width="263" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/be157ada-140a-4015-84e1-110977c308d8">

#### Classification Report 

<img width="329" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/f5a47e98-58cc-4792-834b-02d599544e5f">

## Building the Random Forest model

<img width="323" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/f6ba2b81-2eb7-44bd-9efe-8b617d6a2b18">

#### Testing Performance

<img width="263" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/0d9ca4dc-ded9-4ed0-a01c-b54cbdb10662">

#### Classication Report 

<img width="331" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/f51ad016-92a7-4b1c-a895-84c3227b7ad0">

# Advanced Techinques

## Building a Deep Learing Model

<img width="489" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/a4f66a34-c229-4c34-b21f-82e3466b5eb8">

## Loss and Accuracy progress during training

<img width="289" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/0a52edac-1fff-4be0-94c9-8d026b0debdc">
<img width="298" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/22e08c8b-5725-4bae-aecf-d6bcec971a6b">

## Testing Set Performance

<img width="260" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/481ca126-2466-4c73-9d00-451536a08bc1">

## Classification Report

<img width="323" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/f7e5ca33-cf37-48a8-ac96-516489836ec2">






























  





