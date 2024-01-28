# Salary Prediction Project 

## Define Problem
The purpose of this project is to build a predictive model that can make salary predictions based on given job dispcriptions. With a salary dataset of 1 million job roles along with their associated salaries, I will follow the data science 4D framework of Define, Discover, Develop and Deploy to find the best model with lowest RMSE. 

## Data Discovery & Exploration
As previously mentioned, the dataset is a combination of 1 million job roles along with their associated salaries. The salary dataset is broken up into the following three csv files:
- train_feature.csv
- train_salaries.csv
- test_feature.csv

Combining the train feature and train target we get following dataframe
<img src="images/salary_dataset.png" width = 600, height = 200>

The feature and target variables consist of the following:

Feature - [CompanyID, Degree, Major, milesFromMetroplis,yearsExperience]

Target - [Salary]


I will load, clean and perform some explorary data analysis(EDA) on the data before continuing the modeling process
<img src="images/target_salary.png" width = 600, height =300>
