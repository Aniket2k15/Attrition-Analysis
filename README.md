# Attrition-Analysis
Analyzing by Logistic regression model, Random Forest Model and Artificial Neural Networks

## Tools used  -  Pandas, Numpy, Sci-learn kit, MatplotLib, Seaborn
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

* We can visualize the relationship for 'YearsWithCurrManager' column Attrition
<img width="410" alt="image" src="https://github.com/Aniket2k15/Attrition-Analysis/assets/138878014/76e8bab8-54ac-43ad-a88b-72191108be64">














  





