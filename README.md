# Integrated Retail Analytics for Store Optimization and Demand Forecasting

## 📌 Project Overview
This project delivers an end-to-end data-driven machine learning framework designed to solve retail supply chain and inventory challenges. By unifying multi-source retail datasets—historical weekly sales, store structural metadata, and macroeconomic indicators (CPI, Unemployment, Fuel Price, MarkDowns)—the pipeline delivers actionable demand forecasts to optimize inventory stock levels and prevent stockouts during peak holiday periods.

---

## 📂 Repository Structure
* `data/`: Raw historical sales, store metadata, and environmental feature datasets.
* `models/`: Serialized trained machine learning models (`.pkl`) and feature scaling transformers.
* `notebooks/`: Complete Jupyter Notebook containing end-to-end Data Cleaning, EDA, Model Building, Hyperparameter Tuning, and Evaluation.
* `requirements.txt`: Necessary Python libraries and packages required to run the project.

---

## 🛠️ Technical Stack & Workflow
* **Data Wrangling & Imputation:** Handled structural nulls across promotional MarkDowns (`MarkDown1`–`5`) using zero-imputation and forward/backward filling for macroeconomic metrics (`CPI`, `Unemployment`).
* **Feature Engineering:** Log-transformed sales data (`np.log1p`) to mitigate severe right-skewness, extracted temporal drivers (`Year`, `Month`, `Week`), and built promotional intensity features (`Total_MarkDown`).
* **Machine Learning Algorithms:** Implemented and evaluated **Linear Regression**, **Random Forest Regressor**, and **XGBoost Regressor**.
* **Hyperparameter Optimization:** Used `RandomizedSearchCV` across 3-fold cross-validation to fine-tune non-linear decision tree parameters.
* **Model Explainability:** Analyzed Gini/Gain feature importance to isolate key demand drivers (`Dept`, `Size`, `Week`, `IsHoliday`).

---

## 📊 Key Results
* **Best Model:** Tuned XGBoost / Random Forest Regressor.
* **Evaluation Metrics:** Achieved the lowest out-of-sample RMSE/MAE and highest variance explanation ($R^2$) on holdout test data.
* **Business Impact:** Precise store-department demand forecasting allows operations teams to optimize safety stock during high-velocity Q4 holiday surges while reducing holding costs during standard weeks.

---

## 🚀 Quickstart Guide
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/AliHamzaHabib/Integrated-Retail-Analytics-Store-Optimization.git](https://github.com/AliHamzaHabib/Integrated-Retail-Analytics-Store-Optimization.git)
   cd Integrated-Retail-Analytics-Store-Optimization
