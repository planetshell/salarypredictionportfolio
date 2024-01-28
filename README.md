# Salary Prediction Project 

## 1. Define Problem
The purpose of this project is to build a predictive model that can make salary predictions based on given job dispcriptions. With a salary dataset of 1 million job roles along with their associated salaries, I will follow the data science 4D framework of Define, Discover, Develop and Deploy to find the best model with lowest RMSE. 

## 2. Data Discovery & Exploration

### 2.1 Discover Data 
As previously mentioned, the dataset is a combination of 1 million job roles along with their associated salaries. The salary dataset is broken up into the following three csv files:
- train_feature.csv
- train_salaries.csv
- test_feature.csv

Combining the feature and target variables we get following dataframe
<img src="images/salary_dataset.png" width = 600, height = 200>

The feature and target variables consist of the following:

Feature - [CompanyID, Degree, Major, milesFromMetroplis,yearsExperience]

Target - [Salary]

### 2.2 Clean Data 
The data cleaning process shows there are no duplicates or missing data.However,statistical analysis on the target column(salary) shows there are 5 rows with 0 salary which indicate invalid data. I removed these rows from the dataset using clean_data().
I will load, clean and perform some explorary data analysis(EDA) on the data before continuing the modeling process

### 2.3 Explore Data EDA 
<img src="images/target_salary.png" width = 600, height =300>
<img src="images/feature_companyId.png" width = 600, height =300>
<img src="images/feature_degree.png" width = 600, height =300>
<img src="images/feature_jobType.png" width = 600, height =300>
<img src="images/feature_industry.png" width = 600, height =300>
<img src="images/feature_major.png" width = 600, height =300>
