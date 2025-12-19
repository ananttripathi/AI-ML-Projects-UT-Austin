# Wind Turbine Predictive Maintenance

## 📌 Business Context
Renewable energy plays a critical role in reducing environmental impact, and wind energy is one of the most mature and widely adopted renewable technologies worldwide. However, maintaining wind turbines is costly, especially when failures occur unexpectedly, leading to expensive replacements and downtime.

Predictive maintenance leverages sensor data and machine learning to anticipate equipment failures before they occur. By accurately predicting failures, organizations can:
- Reduce replacement costs
- Optimize repair and inspection schedules
- Improve operational efficiency
- Minimize unplanned downtime

**ReneWind** aims to use machine learning–based predictive maintenance strategies to identify potential generator failures in wind turbines using sensor data.

---

## 🎯 Objective
The objective of this project is to **build and evaluate classification models** that can predict whether a wind turbine generator is likely to fail, enabling **cost-effective maintenance decisions**.

The business interpretation of predictions is **cost-sensitive**:

| Prediction Type | Business Impact |
|-----------------|-----------------|
| True Positive (Failure detected) | Repair cost |
| False Negative (Failure missed) | Replacement cost (highest) |
| False Positive (False alarm) | Inspection cost (lowest) |

Since **replacement costs >> repair costs > inspection costs**, the model must prioritize minimizing **false negatives**, even at the expense of slightly higher false positives.

---

## 🧠 Problem Type
- **Supervised Classification**
- **Cost-Sensitive Machine Learning**
- **Industrial / IoT Analytics**

---

## 📊 Dataset Description
The dataset is a **ciphered sensor dataset** collected from wind turbines.

- **Training set:** 20,000 observations  
- **Test set:** 5,000 observations  
- **Features:** 40 sensor-based predictors  
- **Target Variable:**  
  - `1` → Generator failure  
  - `0` → No failure  

The ciphered nature of the data ensures confidentiality while preserving predictive patterns.

---

## 🛠️ Approach & Methodology

### 1️⃣ Exploratory Data Analysis (EDA)
- Data distribution analysis
- Missing value checks
- Feature behavior understanding
- Target imbalance analysis

### 2️⃣ Data Preprocessing
- Feature scaling
- Handling class imbalance
- Train-validation split

### 3️⃣ Model Building
Multiple classification models were trained and compared, including:
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- Neural Networks

### 4️⃣ Model Evaluation
Models were evaluated using:
- Recall (Failure detection priority)
- Precision
- F1-score
- Confusion Matrix
- Cost-based interpretation of errors

### 5️⃣ Model Tuning
- Hyperparameter tuning
- Threshold optimization
- Focus on minimizing **false negatives**

---

## 🏆 Final Model
After evaluating multiple approaches, the **best-performing model** was selected based on:
- High recall for failure cases
- Balanced trade-off between false positives and false negatives
- Alignment with business cost priorities

The final model demonstrates strong potential for **real-world predictive maintenance deployment**.

---

## 📈 Key Insights
- Sensor data contains strong signals for early failure detection
- Cost-sensitive evaluation is crucial for industrial ML use cases
- Slightly higher inspection costs are acceptable to avoid expensive replacements
- Predictive maintenance can significantly reduce operational risk

---


## 🧰 Tools & Technologies
- **Programming:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn  
- **Visualization:** Matplotlib, Seaborn  
- **Environment:** Jupyter Notebook / Google Colab  

---

## 🎯 Business Impact
This solution helps:
- Prevent unexpected turbine breakdowns
- Reduce maintenance and replacement costs
- Improve reliability of wind energy generation
- Enable data-driven maintenance strategies

---

## ⚠️ Disclaimer
This project was developed for **educational purposes** as part of an academic program. The dataset is anonymized and ciphered to protect proprietary sensor information.

---

⭐ *This project demonstrates the application of machine learning in industrial predictive maintenance with a strong focus on cost-sensitive decision-making.*
