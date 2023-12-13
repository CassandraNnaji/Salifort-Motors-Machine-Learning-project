# Predicting Salifort Motors Employee Turnover

# Overview
Salifort Motors is experiencing high employee turnover. Which has become a financial burden on the company. The goal of the project is to build a model that will predict is an employee leave or not. A predictive model will help the company understand which factors contribute to employee resignation and hopefully help them develop a solution. The Human Resources department collect a survey sample from 15,000 employees. With this data we built Both a Random Forest and XGBoost Model, and a Logistic Regression Model. We did this to see whihc model predicted employee turnover the best.

The Random Forest Model had a percesion score of ~95%, a recall score of ~91%, a f1 score of ~93% and an accuracy score of ~98%.
The XGBoost Model had a precision score of ~96%, a recall score of ~91%, a f1 score of ~93% and an accuracy score of ~98%. 
The Logistic Regression Model had a precision score of ~82%, a recall score of ~84%, a f1 score of ~82% and an accuracy score of ~84% (These are all weighted averages).
The Random Forest and XGBoost model performed pretty much the same, but when it came down to the decimal, the XGBoost Model was the best predictive model overall. 

# Business Understanding 
The main stakeholders for this project are the Human Resources Department and the Salifort leadership team. The main problem they are trying to solve/understand is why employees decide to leave the company. They want to know the contributing factors that make an employee to leave. The model should help answer the question:

What’s likely to make the employee leave the company?

# Data Understanding 
The data used was provided by the Human Resources Department, that surveyed 15,000 employees. The original dataset has 14,999 rows and 10 columns. Some features include (saticifaction level, last evaluation, number of projects, avergae monthly hours, if an employee left or not, how many years they worked, last promotion in the last five years, if they had a work accident, salary and department). An engineered feature added to the dataset was 'overworked', which is if an employee worked >167 hr/month.
