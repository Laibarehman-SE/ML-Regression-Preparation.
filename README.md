# End-to-End Regression Pipeline: Medical Cost Personal Dataset

## 📌 Overview
This repository contains a complete, end-to-end machine learning regression project developed during my Machine Learning Internship. The objective is to analyze demographic and health attributes to accurately predict and interpret individual medical insurance costs (`charges`).

---

## 📅 Project Workflow & Daily Modules

### **Part 1: Dataset Preparation & Exploratory Data Analysis (EDA)**
- **Dataset Selection:** Loaded and inspected the Medical Cost Personal Dataset (`insurance.csv`).
- **Data Cleaning:** Handled missing values, inspected data types, and removed duplicate rows.
- **Exploratory Data Analysis:** Generated statistical summaries and visual distributions of medical charges, age, BMI, and children.
- **Preprocessing:** Performed One-Hot Encoding (`pd.get_dummies`) on categorical features (`sex`, `smoker`, `region`).
- **Data Split:** Executed an 80/20 train-test split resulting in 1,069 training samples and 268 testing samples.

### **Part 2: Baseline & Linear Regression Models**
- **Baseline Model:** Established reference performance using the training mean.
- **Linear Models:** Implemented Simple Linear Regression (`age`), Multiple Linear Regression (all features), and Polynomial Regression (Degree 2).
- **Evaluation Metrics:** Evaluated models using MAE, RMSE, $R^2$, and Adjusted $R^2$.
- **Residual Diagnostics:** Analyzed residual plots to check error distributions and check for potential heteroscedasticity.

### **Part 3: Regularization & Advanced Models**
- **Regularization:** Applied Ridge, Lasso, and Elastic Net regression to control overfitting on polynomial features.
- **Ensemble Models:** Built and benchmarked Decision Trees, Random Forests, Gradient Boosting, and XGBoost regressor models.

### **Part 4: Cross-Validation & Diagnostics**
- **K-Fold Cross-Validation:** Implemented 5-fold cross-validation on ensemble models to ensure model generalizability and stability.
- **Bias-Variance Analysis:** Compared training vs. testing performance gaps to verify a healthy bias-variance trade-off.
- **Error Identification:** Extracted top prediction errors and examined detailed residual distribution histograms.

### **Part 5: Model Selection & Interpretation**
- **Final Selection:** Selected **Gradient Boosting Regressor** as the final model due to its superior predictive accuracy ($R^2 \approx 0.90$, lowest RMSE).
- **Interpretability:** Generated actual-versus-predicted plots and feature importance charts, confirming that smoking status and BMI are the most dominant predictors of medical charges.

---

## 📊 Final Model Performance Summary
| Model | MAE | RMSE | $R^2$ Score |
| :--- | :--- | :--- | :--- |
| **Baseline** | ~4,177 | ~5,956 | 0.00 |
| **Multiple Linear** | 4,177.05 | 5,956.34 | 0.80 |
| **Polynomial Regression** | 2,867.32 | 4,646.06 | 0.88 |
| **Random Forest** | 2,631.95 | 4,696.32 | 0.88 |
| **Gradient Boosting** | **2,517.47** | **4,268.28** | **0.90** |

---

## 🛠️ Tools & Libraries Used
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Scikit-learn, XGBoost
- **Environment:** VS Code, Jupyter Notebook (`regression_task.ipynb`)
