# Student-early-warning-system
# Student Early-Warning & Intervention System

A machine learning-based system designed to identify students who may be at academic risk and support timely, personalized intervention.

## 📌 Project Overview

The Student Early-Warning & Intervention System analyzes academic and engagement indicators such as attendance, midterm performance, assignments, quizzes, and participation to identify students who may require additional support.

Students are assigned a custom risk score and classified into four levels:

- 🟢 Low
- 🟡 Medium
- 🟠 High
- 🔴 Critical

The project goes beyond simply predicting risk by identifying the factors contributing to that risk and suggesting personalized interventions.

## 🎯 Objectives

- Explore and clean student academic data
- Develop a custom early-warning risk scoring framework
- Train and compare multiple machine learning models
- Evaluate models using accuracy, precision, recall, F1-score, and confusion matrices
- Identify the major factors contributing to student risk
- Generate personalized intervention recommendations
- Generate individual student risk reports
- Simulate potential interventions using a What-If Risk Simulator

## 🤖 Machine Learning Models

Three classification models were evaluated:

1. Logistic Regression
2. Decision Tree
3. Random Forest

A class-balanced Random Forest was selected as the final model because the Critical-risk class was highly underrepresented.

The class-balanced model achieved approximately:

- **94% Accuracy**
- **50% Critical-risk Recall**

Although the overall accuracy decreased slightly compared with the initial Random Forest, Critical-risk recall improved from approximately **17% to 50%**, making the model more suitable for an early-warning system where identifying students needing urgent intervention is important.

## 💡 Key Feature — What-If Risk Simulator

The project includes an interactive What-If Risk Simulator.

Users can:

- Enter a Student ID
- View the student's current risk report
- Adjust attendance, midterm, assignment, quiz, and participation values
- See the updated risk score and risk level
- View exactly what intervention changes were applied

For example:

> Attendance: 65% → 85% (+20%)  
> Participation: 6 → 8 (+2)

This allows the system to explore how potential interventions could influence a student's risk level rather than simply predicting their current status.

## 🔍 Explainability & Recommendations

For each student, the system identifies the indicators contributing most to their risk score.

Based on these factors, personalized recommendations are generated, such as:

- Improving attendance
- Strengthening weak academic areas
- Following a consistent assignment schedule
- Practicing through regular quizzes
- Increasing classroom participation

## 📊 Dataset

The cleaned dataset contains **10,000 student records** and includes academic, attendance, engagement, demographic, and assessment-related attributes.

Key features used for risk prediction:

- Attendance
- Midterm Score
- Assignment Average
- Quiz Average
- Participation Score

The target variable, `Risk_Level`, is created using a custom early-warning scoring framework.

## 🧹 Data Preprocessing

The dataset was cleaned by:

- Handling missing values using median imputation
- Correcting inconsistent department names
- Removing invalid numerical values
- Handling unrealistic age and attendance values
- Removing duplicate records

The final cleaned dataset contains:

**10,000 rows × 21 columns**

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- IPyWidgets
- Google Colab

## 📁 Project Files

```text
student-early-warning-system/
│
├── Student_Early_Warning_System.ipynb
├── dcs_student_data.csv
└── README.md
