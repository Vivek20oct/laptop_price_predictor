# 🔮 Laptop Price Predictor

A machine learning project to predict laptop prices based on technical specifications such as CPU, RAM, GPU, storage type, display resolution, and more. The goal is to explore how hardware features influence price and build an accurate predictive model.

---

## 📦 Dataset

* The dataset contains **1303 rows** and **12 columns** originally.
* Columns include:

  * `Company`, `TypeName`, `Inches`, `ScreenResolution`, `Cpu`, `Ram`, `Memory`, `Gpu`, `OpSys`, `Weight`, `Price`
* Target variable: `Price` (in INR)

---

## 🔧 Features Engineered

During preprocessing, multiple new features were derived:

* `Touchscreen` and `IPS Panel` from screen resolution
* `ppi (Pixels Per Inch)` based on resolution and screen size
* `CPU Brand` and `GPU Brand`
* Split `Memory` into: `HDD`, `SSD`, `Hybrid`, `Flash Storage`
* Cleaned units (e.g., GB, kg) and converted to numeric
* Simplified operating system into: Windows, Mac, Others

---

## 📈 Exploratory Data Analysis

Visualizations and analysis include:

* Price distribution
* Company-wise and type-wise price comparisons
* Impact of RAM, CPU brand, GPU brand, and storage types
* Correlation heatmaps and scatter plots

---

## 🧪 Machine Learning Models

Several regression models were trained and evaluated using `log(Price)` as the target:

| Algorithm              | R² Score | MAE      |
| ---------------------- | -------- | -------- |
| Linear Regression      | 0.81     | 0.21     |
| Ridge Regression       | 0.81     | 0.21     |
| Lasso Regression       | 0.81     | 0.21     |
| K-Nearest Neighbors    | 0.80     | 0.19     |
| Decision Tree          | 0.84     | 0.18     |
| Support Vector Machine | 0.81     | 0.20     |
| Random Forest          | 0.89     | 0.15     |
| Extra Trees            | 0.87     | 0.16     |
| Gradient Boosting      | 0.88     | 0.16     |
| XGBoost                | 0.88     | 0.16     |
| **Voting Regressor**   | **0.89** | **0.15** |

---

## 💡 Best Performing Model

**Voting Regressor** combining:

* Random Forest
* Gradient Boosting
* XGBoost
* Extra Trees

Gave the best results with:

* **R² Score**: 0.89
* **MAE**: 0.158

---

## 🚀 How to Use

1. Clone the repository
2. Install dependencies:

   ```bash
   pip install pandas numpy seaborn matplotlib scikit-learn xgboost
   ```
3. Run the notebook or script to train and evaluate the model.

---

## 📌 Project Highlights

* Full pipeline from raw data to deployment-ready model
* Real-world ML use case
* Strong feature engineering and EDA
* Tested multiple regressors and ensemble models

