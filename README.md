# Impact of Socioeconomic and Lifestyle Factors on Resilience Prediction

## 📌 Project Overview

This project explores how socioeconomic, health, and lifestyle factors contribute to **resilience**, defined as maintaining good health outcomes despite high-risk conditions. Using the **BRFSS 2015 diabetes health indicators dataset**, multiple machine learning models are trained and compared to predict whether an individual can be classified as *resilient*.

The notebook performs **end-to-end data analysis**, including preprocessing, feature engineering, handling class imbalance, model training, evaluation, and comparison.

---

## 📂 Dataset

* **Source:** BRFSS 2015 – Diabetes Health Indicators
* **File:** `diabetes_012_health_indicators_BRFSS2015.csv`
* **Type:** Structured, tabular health survey data

### Key Feature Categories

* Socioeconomic: Income, Education
* Lifestyle: Smoking, Physical Activity, Alcohol Consumption
* Health Indicators: BMI, Blood Pressure, Cholesterol
* Demographics: Age, Sex

---

## ⚙️ Workflow

### 1️⃣ Data Loading & Exploration

* Loaded dataset using **pandas**
* Inspected:

  * Data types
  * Statistical summaries
  * Missing values

### 2️⃣ Outlier Detection & Handling

* Boxplots used for univariate analysis
* Outliers capped using **1st and 99th percentile (Winsorization)**

### 3️⃣ Feature Scaling

* Continuous variables standardized using **StandardScaler**

### 4️⃣ Feature Engineering

* **HighBMI:** Binary feature (BMI > 30)
* **RiskFactorScore:** Aggregate score of multiple binary risk factors

### 5️⃣ Target Variable – Resilience

A person is labeled **Resilient (1)** if:

* High risk factor score
* No history of:

  * Heart disease or attack
  * Stroke

Otherwise, labeled as **Non-Resilient (0)**.

---

## 📊 Exploratory Data Analysis (EDA)

* Distribution plots comparing resilient vs non-resilient groups
* Correlation heatmap to identify strongly related features

---

## 🧪 Model Building

### Data Split

* Train/Test split: **80% / 20%**

### Class Imbalance Handling

* Applied **SMOTE** to balance the training dataset

### Models Trained

* Logistic Regression
* Random Forest Classifier
* Support Vector Machine (SVM)
* XGBoost Classifier
* Artificial Neural Network (MLPClassifier)

---

## 📈 Model Evaluation

Each model is evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC

Results are compiled into a comparison table and visualized using bar plots.

---

## 🏆 Model Selection & Optimization

* Best model selected based on **F1 Score**
* Hyperparameter tuning performed using **GridSearchCV**
* Final evaluation done using:

  * Classification report
  * Updated performance metrics

---

## 🛠️ Technologies Used

* **Python**
* **Pandas, NumPy** – Data processing
* **Matplotlib, Seaborn** – Visualization
* **Scikit-learn** – ML models & evaluation
* **Imbalanced-learn (SMOTE)** – Class balancing
* **XGBoost** – Gradient boosting model

---

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost
```

1. Place the dataset CSV file in the project directory
2. Open the notebook:

```bash
jupyter notebook Impact_of_Socioeconomic_and_Lifestyle_Factors_on_Resilience_Prediction.ipynb
```

3. Run all cells sequentially

---

## 📌 Key Takeaways

* Feature engineering significantly improves predictive performance
* Handling class imbalance is crucial in health-related datasets
* Ensemble and boosted models outperform simpler classifiers

---

## 📄 License

This project is for academic and learning purposes.

---

## ✍️ Author

**Jimmy Paul**
Machine Learning & Data Science Enthusiast
