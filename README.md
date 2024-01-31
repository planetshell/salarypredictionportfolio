# Salary Prediction Project 

## 1. Define Problem
The purpose of this project is to build a predictive model that can make salary predictions based on given job dispcriptions. With a salary dataset of 1 million job roles along with their associated salaries, I will follow the data science 4D framework of Define, Discover, Develop and Deploy to find the best model with lowest mean square error (MSE). 

## 2. Data Discovery & Exploration

### 2.1 Discover Data 
As previously mentioned, the dataset is a combination of 1 million job roles along with their associated salaries. The salary dataset is broken up into the following three csv files:
- train_feature.csv
- train_salaries.csv
- test_feature.csv

Combining data from train_feature.csv and train_salaries.csv, we get following raw dataframe
<img src="images/salary_dataset.png" width = 600, height = 200>

The feature variables were identified as follows:
- CompanyID
- Degree
- Major
- milesFromMetroplis
- yearsExperience)

The target variable was identified as follows:
- Salary

### 2.2 Clean Data 
The data cleaning process reveal the following results:
- No duplicates data
- No missing data
- Statistical analysis on the target(salary) shows there are 5 rows in dataset with 0 salaries which indicates invalid data

Based on the results above, I only needed to remove the 5 rows with 0 salaries from the dataset.I will now perform some explorary data analysis(EDA) on the cleaned dataset before moving on to the modeling stage. 

### 2.3 Explore Data EDA 
In this section, I summarize each feature variable and the target variable from the cleaned dataframe. I then looked for any relationships between each feature variable and the target variable
<img src="images/target_salary.png" Title = "Salary" width = 600, height =300>
<img src="images/feature_companyId.png" width = 600, height =300>
<img src="images/feature_degree.png" width = 600, height =300>
<img src="images/feature_jobType.png" width = 600, height =300>
<img src="images/feature_industry.png" width = 600, height =300>
<img src="images/feature_major.png" width = 600, height =300>
<img src="images/feature_milesFromMetropolis.png" width = 600, height =300>
<img src="images/feature_yearsExperience.png" width = 600, height =300>

The results above show the following:

- No correlation between compandId and salary
- Positive coorelation between jobType and salary.
- Positive coorelation between degree and salary.
- Positive coorelation between major and salary
- Positive coorelation between industry and salary
- Positive coorelation between yearsExperience and salary
- Negative coorelation between milesFromMetropolis and salary

The results above makes sense. In the real world, salaries are generally higher with more advance job roles or more advance degrees.In addition, salaries are generally higher with more years of experience and lower with distance from the city.

### 2.4 Establish a Baseline
In this section I created a simple model that will serve as the baseline for more advance models. The baseline model was established by taking the mean of the target(salary). I then measured its efficacy using MSE matrics.
### 2.5 Hypothesize a solution
The MSE for the baseline model was calculated to be 1499.07. I will use the following models to improve the current baseline model's results.

- Linear Regression
- Random Forest Regressor
- Gradient Boost Regressor

I choose the 3 models above because the problem we are solving is a regression problem. This can be determined by simply examining the relationship between each feature variable and target in the dataset.The EDA show that there are linear relationships between each feature variable and the target. In addition, there's both positive and negative coorelation between the target variable (salary) and feature variables jobType, degree, major, industry, YearsExperience and milesFromMetropolis.

## 3. Model Development
In this section, I used object oriented programming to build the models. I created the following classes:
- Data class
- Model class
- Feature engineering class 

### 3.1 Create Models
The following model object were created and tested:
- LinearRegression()
- RandomForestRegressor()
- GradientBoostRegressor()
### 3.2 Test Models
#### Model results before feature engineering

<img src="images/Salary Prediction model results before feature engineering.png" width = 500, height =100>
The table above show that the gradient Boost Regressor model perform the best with a MSE=367  

<img src="images/feature importance before feature engineering.png" width = 600, height =300>
The chart above shows the most important feature is "yearsExperience"  

### 3.3 Feature Engineering

### 3.4 Tests Models
#### Model results before feature engineering
<img src="images/Screenshot 2024-01-30 192512.png" width = 500, height =100>
The table above shows that the MSE was significantly lowered with feature engineering applied to the dataset. 
Again,the gradient Boost Regressor model perform the best with a MSE=313.29


<img src="images/feature importance after feature engineering.png" width = 600, height =300>
After applying group statistic to the data, the chart above now shows the most important feature is the "Group_Mean" . 


### 3.4 Select best Model 
After tuning and training all 3 models, we find that the gradient boost regressor was the performing model and can be deployed to production  

## 4. Model Deployment

### 4.1 Automate Pipeline

### 4.2 Deployment Solution



