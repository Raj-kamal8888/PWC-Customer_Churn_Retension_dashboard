# PWC-Customer_Churn_Retension_dashboard

**Table of Contents:**

Problem Statement

Datasource

Data Preparation

Data Modeling

Data Analysis (DAX)

Insights

Recommendation

**Problem Statement :**

The purpose of this task is to:

Define proper KPI's

Create a dashboard for the retention manager reflecting the KPI's

Write a short email to him (the engagement partner) explaining your findings, and include suggestions as to what needs to be changed

Customers who left within the last month

Services each customer has signed up for: phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies

Customer account information: how long as a customer, contract, payment method, paperless billing, monthly charges, total charges and number of tickets opened in the categories administrative and technical

Demographic info about customers – gender, age range, and if they have partners and dependents

**Datasource :**

Dataset used for this task was presented by Pwc and customer churn Retention dataset:


**Data Preparation:**

Completed the Data transformation in Power Query and the dataset loaded into Microsoft Power BI Desktop for modeling.

Customer Churn dataset is give table named:

Customer churn dataset which has 23 columns and 7043 rows of observation

Data Cleaning for the dataset was done in the power query editor as follows:

Replaced the value is SeniorCitizen N coverted No and Y converted Yes

Removed Unnecessary columns

Removed Unnecessary rows

Each of the columns in the table were validated to have the correct data type

**Data Modeling:**

And then dataset was cleaned and transformed, it was ready to the data modeled.



**Data Analysis (DAX):**

Measures used in all visualization are:


Average MonthlyCharges = AVERAGE('01 Churn-Dataset'[MonthlyCharges])


Average TotalCharges = AVERAGE('01 Churn-Dataset'[TotalCharges])


churn count = CALCULATE(COUNT('01 Churn-Dataset'[Churn]), ALLSELECTED('01 Churn-Dataset'[Churn]),'01 Churn-Dataset'[Churn] = "Yes")


churn rate % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Churn]), '01 Churn-Dataset'[Churn] = "yes" ), COUNT('01 Churn-Dataset'[Churn]), 0)


Dependent in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Dependents]), '01 Churn-Dataset'[Dependents]="Yes",'01 Churn-Dataset'[Churn]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Churn]="Yes"), 0)


Device protection in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]), '01 Churn-Dataset'[DeviceProtection] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]),'01 Churn-Dataset'[Churn]="Yes"),0)

Online backup in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]), '01 Churn-Dataset'[OnlineBackup] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[Churn]="Yes"),0)

Online security in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]), '01 Churn-Dataset'[OnlineSecurity] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[Churn]="Yes"),0)

Partner in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Partner]="Yes",'01 Churn-Dataset'[Churn]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[Partner]), '01 Churn-Dataset'[Churn]="Yes"), 0)

Phone service in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]), '01 Churn-Dataset'[PhoneService] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[Churn]="Yes"),0)

SenioCitizen in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[SeniorCitizen]=1,'01 Churn-Dataset'[Churn]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[Churn]="Yes"), 0)

Streaming Movies in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]), '01 Churn-Dataset'[StreamingMovies] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[Churn]="Yes"),0)

Streaming TV in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]), '01 Churn-Dataset'[StreamingTV] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[Churn]="Yes"),0)

Tech Support in % =

Explain
DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]), '01 Churn-Dataset'[TechSupport] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]),'01 Churn-Dataset'[Churn]="Yes"),0)

**Data Visualization (Dashboard):**

Data visualization for the data analysis (DAX) was done in Microsoft Power BI Desktop:



Insights:

**Customer Overview :**

There are total 7,043 customers subscribed to the client, out of which 3,555 are Males & 3,488 are Females, & the revenue earned is $16.1M

84% of our customers are Young i.e. 5901.

By tenure, 31% customers are subscribed to below 12 months, as a result there are more customers with month-to-month contract

Most customers have Fiber optic internet for which they are paying high charges.

73.5% of customers have been retained i.e. 5,174

**Churn Customers**

1,869 customers have churned i.e. 26.5% , out of which 380 customers churned last month itself.

Revenue lost due to churn is $2.9M.

Gender is not the major factor of churning as ratio of Males and Females is same.

1037 customers with less than 12 months tenure have churned, whereas customers with 61-72 months of tenure are just 93.

89% customers churned had month-to-month contract.

Customers paying high charges have churned the most i.e.1274, along with customers with fiber optic internet have also churned the most


**Churning factors are:**

Young Customers

Customers with tenure of last than 12 months

Customers with month-to-month contract

Customers subscribed to fiber optic

Customers paying high charges


2955 tech tickets were opened and 3632 admin tickets were opened.

Most of the churned customers did not sign up for Online Security and tech support and also did not sign up for Phone Services.

It a lot of customers had an issue with Fiber Optic . Up to 42% of the customers churned were using Fiber Optic as their Internet Services.

**Recommendation:**

The Company could try convincing customers to subscribe to One-Year and Two-Year contract. The contract are not favorable to customers as they tend to pay more monthly.

Giving the discount to customers based on the some specific tasks is also good wat retaining them, specially those month-to-month contract.

From analysis majority customers who churned did not sigh up for Online Security and Tech Support. These are the important services that customers should customers signup for. The company should educate customers on the benefits of signing up for these services.

Increase sale of 1 and 2 year contract by 5% each and Yearly increase of automatic payments by 5%.
