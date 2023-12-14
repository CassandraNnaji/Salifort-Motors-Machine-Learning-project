# Predicting Salifort Motors Employee Turnover

# Overview
Salifort Motors is experiencing high employee turnover. Which has become a financial burden on the company. The goal of the project is to build a model that will predict is an employee leave or not. A predictive model will help the company understand which factors contribute to employee resignation and hopefully help them develop a solution. The Human Resources department collect a survey sample from 15,000 employees. With this data we built Both a Random Forest and XGBoost Model, and a Logistic Regression Model. We did this to see which model predicted employee turnover the best.

The Random Forest Model had a precision score of ~95%, a recall score of ~91%, a f1 score of ~93% and an accuracy score of ~98%.
The XGBoost Model had a precision score of ~96%, a recall score of ~91%, a f1 score of ~93% and an accuracy score of ~98%. 
The Logistic Regression Model had a precision score of ~82%, a recall score of ~84%, a f1 score of ~82% and an accuracy score of ~84% (These are all weighted averages).
The Random Forest and XGBoost model performed pretty much the same, but when it came down to the decimal, the XGBoost Model was the best predictive model overall. 

# Business Understanding 
The main stakeholders for this project are the Human Resources Department and the Salifort leadership team. The main problem they are trying to solve/understand is why employees decide to leave the company. They want to know the contributing factors that make an employee to leave. The model should help answer the question:

What’s likely to make the employee leave the company?

# Data Understanding 
The data used was provided by the Human Resources Department, that surveyed 15,000 employees. The original dataset has 14,999 rows and 10 columns. Some features include (satisfaction level, last evaluation, number of projects, average monthly hours, if an employee left or not, how many years they worked, last promotion in the last five years, if they had a work accident, salary and department). An engineered feature added to the dataset was 'overworked', which is if an employee worked >167 hr/month.

# Modeling and Evaluation 
A XGBoost Model comprising of 100 decision trees was used to determine if an employee would leave or not. The plot below shows the diffrent features that contribute to an employee wanting to leave. The top five features that help predict if an employee will leave are last evaluation, satisfaction level, number project, tenure, and overworked. The model overall performed with a f1 score of 93%, a recall score of 91%, a precision score of 96% and an accuracy score of 98%.

![image](https://github.com/CassandraNnaji/Salifort-Motors-Machine-Learning-project/assets/120784310/08f63181-a1bc-4e01-b338-549a47558990)


The Confusion Matrix below shows the machines perdictions:
- Upper Left quadrant (True Neg) Number of correctly predicted employees that 'stayed' (1993)
- Upper Right quadrant (False Pos) Number of incorrectly predicted employees that 'left' but actually 'stayed' (8)
- Lower Left quadrant (False Neg) Number of incorrectly predicted employees that 'stayed' but actually 'left' (30)
- Lower Right quadrant (True Pos) Number of correctly predicted employees that 'left' (368)
- The model correctly identified ~94% of employees that 'left'. 
- The model identified 3x as many False Negatives than it did False Positives

![image](https://github.com/CassandraNnaji/Salifort-Motors-Machine-Learning-project/assets/120784310/75cce529-bdae-4424-8b49-c72f303229c4)


## Conclusion, Recommendations & Next Steps
### Summary of Model Results:
1. Both models performed pretty much the same. So we chose the XGBoost Model as the best model predictor out of the two. The recall score was ~92%.

2. The model correctly identified ~94% of employees that 'left' the company.

3. The top five features that help predict if an employee will leave are (last evaluation, satisfaction level,   number project, tenure, and overworked).

4. By the models it is confirmed that many of the employees are overworked.

### Employee Retention Recommendations:
1. As employee tenure goes up, so should their salary. From the 'Salary histogram by tenure' plot in the Jyputer Notebook, we saw that even at a 10 year tenure many of the employees were getting paid a medium to low salary.

2. There needs to be a better scale for evaluation. Most of the employees that left were overworked and had high evaluations, as we saw in the 'Monthly hours by last evaluation score' plot in the Notebook. This tells us that the company by default gave high evaluation score to those who were being overworked. 

3. From the 'Monthly hours by last evaluation score' plot, many of the employees that were overworked also were involved in multiply projects. There should be better management on dividing projects up between employees. If an employee is going to take on more projects and more hours there should be an incentive of higher pay or higher overtime pay.

### Next Steps:
1. It was stated that some of the data was also taken from employees that were fired. Maybe having a sample that did not include those employees, could return a different outcome. So a next step could be to acquire a sample from employees that are not in line to possibly being fired.

2. I believe it may be wise to conduct a survey/building a predictive model on each individual department. So we can see how each department stacks up. From the plot we saw that the departments Sales, Technical and Support had the most employees that left the company. Maybe looking more into those departments individually can help learn about the treatment of employees.

3. I think having a discussion or taking a survey on company culture would be beneficial. Maybe having questions about employee benefits, work life balance or even work culture would be beneficial. 

