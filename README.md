# Credit-Risk-Analysis

## Introduction
In this project, I analyzed credit risk data to predict loan defaults. Credit risk is crucial for financial institutions to assess the likelihood that a borrower will default on their loan. Mismanagement of credit risk can lead to substantial financial losses.

The dataset contains information about individuals such as age, income, home ownership, employment length, and loan characteristics. By performing thorough data preprocessing, statistical analysis, and model training, I developed a classifier capable of predicting whether a loan will default, with a focus on precision, recall, and interpretability.

## Data Preprocessing:
- Missing Values: First, I explored the dataset for missing values, addressing the person_emp_length column by filling missing values with the median, as it's a numerical column. Rows with missing loan_int_rate values were dropped due to their potential significance in model training.
- Outlier detection and removal: To ensure the dataset's integrity, I used boxplots to visually identify and remove outliers from columns like person_income and person_age. I also replaced extreme values in person_emp_length with the mean to ensure consistency.
- Feature Transformation: I utilized one-hot encoding for categorical columns, such as loan intent and home ownership, to convert them into binary variables.

## Exploratory Data Analysis (EDA):
Utilized: 
- Visualizations like histograms, scatter plots, and count plots helped to gain insights into relationships between loan_status, loan_amount, loan_interest_rate, and loan_intent.
- Statistical tests (T-tests and Chi-Square) to explore significant relationships between variables like income, interest rate, and loan intent in relation to loan status.
  
I started by visualizing distributions, such as loan status, to understand the class imbalance and how variables like 'income' and 'age' correlate with loan default. The scatter plot of income vs. loan amount revealed that individuals with lower income are more likely to default on loans.
One key insight was that older individuals with higher incomes are less likely to default. Additionally, loan interest rate was found to be significantly higher for defaulters, which aligns with our hypothesis that riskier loans are associated with higher rates.

## Modeling:
I used several machine learning models to predict loan default, including Logistic Regression and Random Forest. The Random Forest model performed best, with an accuracy of 92%, which shows it was able to effectively capture the patterns in the data.

## Intrepretations:
The high accuracy of the Random Forest model suggests that it can reliably predict the risk of loan default. Financial institutions can use this model to make better lending decisions, ensuring they provide loans to individuals with a lower likelihood of default.
