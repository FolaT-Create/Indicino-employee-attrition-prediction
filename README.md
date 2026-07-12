## Indicino Employee Attrition Prediction

### Project Overview

Employee attrition is one of the biggest challenges faced by organizations, leading to increased recruitment costs, loss of institutional knowledge, and reduced productivity. This project analyzes employee data to identify the key drivers of attrition and builds predictive machine learning models capable of identifying employees who are likely to resign.

The project follows an end-to-end Data Science workflow, including data cleaning, exploratory data analysis (EDA), feature engineering, predictive modeling, model optimization, and business recommendations.

### Business Problem

Indicino's HR department wants to answer the following business questions:

1. What are the root causes of employee attrition?
2. Which employees are most likely to resign?
3. Which age groups are more likely to be retained?
4. Does the relationship with the current manager influence employee attrition?
5. What insights can be drawn from the company's performance and reward culture?
6. What actionable recommendations can HR implement to improve employee retention?

### Project Objectives

- Understand factors influencing attrition
- Perform exploratory data analysis (EDA)
- Perform feature engineering
- Build machine learning models to predict employee attrition
- Evaluate and improve models performance
- Provide business recommendations based on analytical findings

### Dataset

The dataset contains 1,470 employee records and includes demographic, compensation, job satisfaction, performance, and career progression information.

### Target Variable

- Attrition
    - Yes (Employee Left)
    - No (Employee Stayed)

### Key Features

- Age
- Department
- Job Role
- Monthly Income
- Job Satisfaction
- Environment Satisfaction
- Work-Life Balance
- Years at Company
- Years with Current Manager
- Overtime
- Performance Rating
- Training Times Last Year
- Stock Option Level
- Total Working Years

### Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- imbalanced-learn (SMOTE)
- Jupyter Notebook
- Git
- GitHub
- VS Code

### Project Workflow

#### 1. Data Cleaning

- Removed unnecessary columns
- Checked for duplicate records
- Verified missing values
- Corrected data types
- Encoded categorical variables

#### 2. Exploratory Data Analysis (EDA)

Performed analysis on:

- Attrition distribution
- Department-wise attrition
- Job role attrition
- Monthly income
- Age distribution
- Work-life balance
- Job satisfaction
- Years at company
- Years with current manager

#### 3. Feature Engineering

- Encoding using `pd.get_dummies()`
- Feature selection
- Correlation analysis
- Train/Test split
- Addressed class imbalance using SMOTE


#### 4. Machine Learning Models

The following Random Forest models were developed and compared:

- Baseline Random Forest
- Random Forest with Class Weighting
- Random Forest with SMOTE
- Random Forest with SMOTE + Class Weighting
- Hyperparameter-Tuned Random Forest


#### Model Performance

| Model | Accuracy | Precision | Recall | F1-Score |
|--------|---------:|----------:|-------:|---------:|
| Original RF | 87.07% | 57.14% | 10.26% | 17.39% |
| Balanced RF | 87.76% | 100.00% | 7.69% | 14.29% |
| SMOTE RF | 89.12% | 68.42%| 33.33% | 44.83% |
| Tuned RF | 77.89% | 30.88% | 53.85% | 39.25% |


### Key Findings

The exploratory analysis identified several factors associated with higher employee attrition:

- Employees with lower job satisfaction showed higher attrition rates.
- Lower environment satisfaction correlated with increased turnover.
- Employees earning lower monthly incomes were more likely to leave.
- Employees with fewer years at the company exhibited higher attrition.
- Younger employees demonstrated higher turnover compared to older employees.
- Employees with fewer years under their current manager were more likely to resign.


### Model Optimization

To improve the model's ability to identify employees at risk of leaving:

- SMOTE was applied to address class imbalance.
- Hyperparameter tuning was performed using GridSearchCV.
- Models were evaluated using Accuracy, Precision, Recall, F1-Score, and Confusion Matrix.
- Recall was prioritized because the business objective is to identify employees likely to resign.

Although the tuned model produced lower overall accuracy, it achieved the highest Recall by correctly identifying over half of the employees who eventually left the company, making it the most suitable model for proactive employee retention.


### Business Recommendations

Based on the analysis, Indicino's HR department should consider the following:

- Reduce excessive overtime to improve work-life balance.
- Improve employee engagement and job satisfaction through regular feedback and recognition.
- Strengthen manager-employee relationships through leadership development.
- Review compensation strategies for lower-income employees.
- Provide clear career progression opportunities and timely promotions.
- Identify high-risk employees early using predictive analytics and targeted retention programs.


### Repository Structure

Indicino-Employee-Attrition-Prediction/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── Indicino_project_notebook.ipynb
│   └── Model_eveluation_&_improvement.ipynb
│
├── models/
│   └── employee_attrition_prediction_model
│
├── reports
├── requirements.txt
├── README.md
└── LICENSE


### Future Improvements

- Evaluate additional machine learning algorithms such as XGBoost, LightGBM, and CatBoost.
- Optimize the classification threshold to further improve Recall.
- Perform feature selection to reduce overfitting.
- Deploy the final model using Flask, FastAPI, or Streamlit.
- Build an interactive HR dashboard for real-time attrition monitoring.


### Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Data Visualization
- Machine Learning
- Class Imbalance Handling (SMOTE)
- Hyperparameter Tuning
- Model Evaluation
- Business Insight Generation
- Predictive Analytics
- Git & GitHub
- Python Programming


### Author

Folashade Adekunle

Aspiring Data Scientist | Machine Learning Enthusiast | Operations Excellence Professional


### Acknowledgements

This project was completed as part of my Data Science learning journey to demonstrate the application of machine learning techniques in solving real-world HR analytics and employee attrition prediction problems.