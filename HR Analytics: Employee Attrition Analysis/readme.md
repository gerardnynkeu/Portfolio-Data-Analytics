# HR Analytics: Employee Attrition Analysis

## 📊 Overview

This project explores the key factors that drive employee attrition within a company, using data analytics and machine learning techniques. The goal is to help businesses identify high-risk attrition profiles, gain actionable insights, and proactively retain valuable employees.

## 🎯 Project Objective

Employee attrition significantly impacts a company's operational efficiency, financial health, and morale. Through data-driven analysis, this project aims to:

- Understand the patterns and trends behind employee turnover.
- Identify key features contributing to attrition.
- Build predictive models to forecast attrition.
- Recommend actionable HR strategies based on insights.

## 🧠 Business Context

Employee retention is critical for long-term success. High turnover leads to increased recruitment costs, productivity loss, and decreased team morale. Predictive HR analytics allows businesses to anticipate attrition risks and respond effectively.

## 🗂 Dataset

- **Source**: Public dataset from Kaggle: `HR_comma_sep.csv`
- **Target variable**: `left` (binary: 1 = employee left, 0 = stayed)
- **Key Features**:
  - `satisfaction_level`
  - `last_evaluation`
  - `average_monthly_hours`
  - `time_spend_company`
  - `Work_accident`
  - `promotion_last_5years`
  - `salary` (categorical: low, medium, high)
  - `department`

## 🔍 Workflow Summary

### 1. Exploratory Data Analysis (EDA)
- Assessed dataset shape and structure.
- Analyzed distributions of features.
- Identified outliers and potential data quality issues.
- Visualized relationships between features and attrition.

### 2. Data Cleaning
- Checked for and handled missing values.
- Removed duplicate records.
- Detected and treated outliers.

### 3. Feature Engineering
- Encoded categorical variables.
- Standardized column names.
- Created new variables for modeling.

### 4. Model Building
Several classification models were trained and evaluated:
- **Logistic Regression**
- **Decision Tree**
- **Random Forest**
- **XGBoost**

### 5. Model Evaluation
- Evaluated using accuracy, precision, recall, F1-score, and confusion matrix.
- Tuned hyperparameters via Grid Search and Randomized Search.
- Analyzed feature importances to interpret model decisions.

## 🏆 Key Insights

- **Satisfaction Level** and **Average Monthly Hours** are strong predictors of attrition.
- Employees with no recent promotion and low salary are more likely to leave.
- High performers with excessive workload may also have increased attrition risk.

## 💡 Recommendations

- Monitor employee satisfaction regularly.
- Address overwork among high-performing staff.
- Improve internal mobility and promotion opportunities.
- Design targeted retention strategies for high-risk profiles.

## 📌 Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost

## 📁 Project Structure

├── hr-analytics-employee-attrition-analysis.ipynb
├── README.md
└── dataset/
└── HR_comma_sep.csv

## 🔗 Project Links

- [Full Kaggle Project Notebook](https://github.com/gerardnynkeu/Portfolio-Data-Analytics/blob/main/HR%20Analytics%3A%20Employee%20Attrition%20Analysis/hr-analytics-employee-attrition-analysis.ipynb)


## ✍️ Author

> **Gerard Nynkeu**  
Aspiring Data Analyst | Passionate about solving business problems with data  
[LinkedIn](https://www.linkedin.com/in/gerard-nynkeu-njike-63282a327/)



