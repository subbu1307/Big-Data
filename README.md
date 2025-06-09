# HR Analytics: Predicting Employee Attrition with Spark MLlib

This project analyzes and predicts employee attrition using the IBM HR Analytics dataset. It combines Spark SQL for exploratory data analysis, Spark MLlib for machine learning modeling, and MLflow for experiment tracking. The goal is to help organizations proactively identify high-risk employees and improve retention strategies.

## Problem Statement

Employee attrition can be costly and disruptive. This project aims to understand why employees leave and to build predictive models that can help HR departments take data-driven action to retain talent. 

## Dataset

- Source: Kaggle (IBM HR Analytics Attrition Dataset)
- Size: 1,470 records, 35 features
- Key feature categories:
  - Demographics: Age, Gender, MaritalStatus
  - Job-related: JobRole, Department, YearsAtCompany
  - Compensation: MonthlyIncome, OverTime
  - Target: Attrition (Yes/No)

## Exploratory Data Analysis (Spark SQL)

Key insights from analysis:
- Sales and HR departments have the highest attrition rates
- Overtime is one of the strongest indicators of attrition
- Employees with low income, early in their career, or frequently traveling are more likely to leave
- Single employees and those with poor work-life balance tend to show higher attrition

## Machine Learning Models (Spark MLlib)

We implemented the following classification models:
- Logistic Regression
- Random Forest
- XGBoost
- CatBoost

The best performing model was CatBoost:
- Accuracy: 88.98%
- AUC (ROC): 0.8227
- Precision-Recall AUC: 0.633

Most important features influencing attrition:
- Overtime
- Monthly Income
- Age

## MLOps Integration with MLflow

Model tracking and evaluation were conducted using MLflow:
- Experiment setup and version tracking
- Logged metrics for accuracy, AUC, precision-recall
- Compared multiple model runs and configurations

## Business Impact

- Identified departments and job roles with highest attrition risk
- Provided salary and workload recommendations to improve retention
- Insights can help HR teams design more effective retention policies

## Technology Stack

- Apache Spark (SQL and MLlib)
- Python
- Pandas, Matplotlib
- MLflow
- Databricks Notebooks
