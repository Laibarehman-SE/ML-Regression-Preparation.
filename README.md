# Regression Fundamentals & Dataset Preparation

## 📌 Overview
This repository contains the dataset preparation, exploratory data analysis (EDA), and feature preprocessing for a regression machine learning task. The objective is to analyze personal demographic and health attributes to predict individual medical insurance costs (`charges`).

---

## 🎯 Task Objectives
- **Dataset Selection:** Selected the Medical Cost Personal Dataset (`insurance.csv`).
- **Problem Statement:** Predict continuous medical expenses (`charges`) billed to individuals based on health characteristics.
- **Variables Identification:**
  - **Target (Dependent Variable):** `charges`
  - **Features (Independent Variables):** `age`, `sex`, `bmi`, `children`, `smoker`, `region`
- **Data Preprocessing & Cleaning:**
  - Inspected dimensions, data types, missing values, and duplicates.
  - Handled duplicate records and validated clean data structure.
- **Exploratory Data Analysis (EDA):**
  - Generated summary statistics.
  - Visualized distributions of the target variable (`charges`).
  - Evaluated feature relationships (e.g., `age` vs `charges`).
  - Analyzed correlation matrices among numerical features.
- **Feature Engineering & Train-Test Split:**
  - Applied One-Hot Encoding (`pd.get_dummies`) to categorical features (`sex`, `smoker`, `region`).
  - Performed an 80/20 train-test split (`train_test_split`) resulting in **1,069 training samples** and **268 testing samples**.

---

## 🛠️ Tools & Libraries Used
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Scikit-learn
- **IDE:** Visual Studio Code / Jupyter Notebook

---

## 📁 Repository Structure
├── insurance.csv            # Medical Cost Personal Dataset
├── regression_task.ipynb    # Jupyter Notebook containing full EDA & preprocessing
└── README.md                # Project documentation
