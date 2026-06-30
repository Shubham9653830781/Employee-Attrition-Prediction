# Employee-Attrition-Prediction

Predict employee attrition using Machine Learning and identify the key factors influencing employee turnover. This project combines Exploratory Data Analysis (EDA), data preprocessing, multiple classification models, and business insights to help HR teams make data-driven retention decisions.

---

## Project Overview

Employee attrition is a major challenge for organizations as it increases recruitment costs, training expenses, and productivity loss. The objective of this project is to predict whether an employee is likely to leave the company and identify the factors contributing to attrition.

Using the IBM HR Analytics Employee Attrition dataset, three machine learning models were developed and compared to identify the most suitable model for this business problem.

---

## Dataset

**Dataset:** IBM HR Analytics Employee Attrition

- Source: Kaggle
- Records: **1,470 Employees**
- Features: **35**
- Target Variable: **Attrition (Yes/No)**

---

## Problem Statement

Develop a machine learning model that predicts whether an employee is likely to leave the company based on employee-related information such as:

- Age
- Monthly Income
- Department
- Job Role
- Work-Life Balance
- Business Travel
- Overtime
- Years at Company
- Job Satisfaction
- and other HR-related features.

---

## Project Workflow

```
Data Collection
        │
        ▼
Data Cleaning & Preprocessing
        │
        ▼
Exploratory Data Analysis (EDA)
        │
        ▼
Feature Engineering
        │
        ▼
Train-Test Split
        │
        ▼
Model Training
(Logistic Regression,
Random Forest,
Gradient Boosting)
        │
        ▼
Model Evaluation
        │
        ▼
Business Insights
```

---

## Data Preprocessing

- Removed unnecessary columns
- Checked missing values
- Converted Attrition (Yes/No) into binary values
- One-Hot Encoding for categorical variables
- Standardized numerical features using StandardScaler
- Split dataset into 80% Training and 20% Testing

---

## Exploratory Data Analysis

The following analyses were performed:

- Attrition Rate by Department
- Attrition Rate by Job Role
- Monthly Income vs Attrition
- Work-Life Balance vs Attrition
- Employee Tenure vs Attrition

---

## Machine Learning Models

Three classification models were trained and compared:

- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier

Class imbalance was handled using:

```python
class_weight='balanced'
```

---

## Model Performance

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|--------|---------:|----------:|--------:|---------:|---------:|
| Logistic Regression | 74.8% | 34.1% | **61.7%** | **43.9%** | 0.799 |
| Random Forest | 83.7% | 48.4% | 31.9% | 38.5% | 0.777 |
| Gradient Boosting | **85.0%** | **58.8%** | 21.3% | 31.2% | **0.804** |

Although Gradient Boosting achieved the highest accuracy, Logistic Regression was selected as the final model because it achieved the highest Recall, making it more suitable for identifying employees at risk of leaving.

---

## Key Business Insights

- Sales department recorded the highest attrition rate (20.6%).
- Sales Representatives had the highest attrition among all job roles (39.8%).
- Employees with poor Work-Life Balance showed significantly higher attrition.
- Nearly 30% of employees left within their first two years.
- Overtime, Business Travel, Job Role, and delayed promotions were among the strongest drivers of employee attrition.

---

## Top Features Influencing Attrition

The Logistic Regression model identified the following factors as the most influential:

1. JobRole_Laboratory Technician
2. OverTime_Yes
3. BusinessTravel_Travel_Frequently
4. JobLevel
5. TotalWorkingYears
6. JobRole_Sales Representative
7. BusinessTravel_Travel_Rarely
8. EducationField_Life Sciences
9. YearsSinceLastPromotion
10. Department_Sales

---

## Visualizations

The project includes the following visualizations:

- Attrition Rate by Department
- Attrition Rate by Job Role
- Monthly Income vs Attrition
- Work-Life Balance vs Attrition
- Employee Tenure vs Attrition
- Confusion Matrix
- ROC Curve Comparison
- Top 10 Feature Importance

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Project Structure

```
Employee-Attrition-Prediction/
│
├── analysis.ipynb
├── WA_Fn-UseC_-HR-Employee-Attrition.csv
├── Summary.pdf
│
├── charts/
│   ├── Attrition_by_Department.png
│   ├── Attrition_by_JobRole.png
│   ├── MonthlyIncome_Boxplot.png
│   ├── ConfusionMatrix.png
│   ├── ROC_Curve.png
│   └── FeatureImportance.png
│
├── requirements.txt
└── README.md
```

---

## Future Improvements

- Build an interactive Streamlit web application
- Predict employee attrition probability
- Explain predictions using SHAP values
- Deploy the project on Streamlit Cloud
- Create an HR Analytics Dashboard
- Integrate with SQL database

---

## Author

**Shubham Meena**

B.Tech Chemical Engineering  
Indian Institute of Technology (BHU), Varanasi

---

## License

This project is created for educational and portfolio purposes.
