## 📌 PRCP-1000 – Portuguese Bank Marketing Prediction

### 📊 Domain

**Finance / Banking / Marketing Analytics**

---

## 🧠 Problem Statement

The dataset contains information related to **direct phone call marketing campaigns** conducted by a Portuguese bank between **May 2008 and November 2010**.

### 🎯 Objectives

1. Perform **complete data analysis** on customer and campaign data
2. Build a **predictive model** to identify customers likely to subscribe to a **term deposit**
3. Provide **actionable business suggestions** to improve campaign success

---

## 📁 Dataset Information

* **Source:** Portuguese Banking Institution
* **File Used:**

  ```
  Data > bank-additional > bank-additional-full.csv
  ```
* **Records:** 41,188
* **Features:** 20 input variables + 1 target variable

---

## 🧾 Feature Overview

### 🔹 Customer Information

* `age`
* `job`
* `marital`
* `education`
* `default`
* `housing`
* `loan`

### 🔹 Campaign Contact Details

* `contact`
* `month`
* `day_of_week`
* `duration` *(excluded from final model due to data leakage)*

### 🔹 Campaign History

* `campaign`
* `pdays`
* `previous`
* `poutcome`

### 🔹 Economic Indicators

* `emp.var.rate`
* `cons.price.idx`
* `cons.conf.idx`
* `euribor3m`
* `nr.employed`

### 🎯 Target Variable

* `y` → Whether the client subscribed to a term deposit (`yes` / `no`)

---

## 🔍 Task 1: Exploratory Data Analysis (EDA)

### ✔ Key Analysis Performed

* Missing value & imbalance analysis
* Distribution analysis of numerical and categorical features
* Relationship between customer attributes and subscription
* Campaign success patterns
* Impact of economic indicators on customer decisions

### 📌 Key Insights

* Customers contacted fewer times had higher subscription rates
* Prior campaign success strongly increases conversion probability
* Certain job types (retired, students) show higher acceptance
* Economic indicators significantly influence customer behavior

---

## 🤖 Task 2: Predictive Modeling

### 🛠 Data Preprocessing

* Label Encoding / One-Hot Encoding
* Handling class imbalance
* Feature scaling where required
* Removed **`duration`** to prevent data leakage

### 📌 Models Implemented

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* Gradient Boosting Classifier
* XGBoost *(if applicable)*

---

## 📈 Model Comparison Report

| Model               | Accuracy | Precision | Recall   | F1-score |
| ------------------- | -------- | --------- | -------- | -------- |
| Logistic Regression | Good     | Moderate  | Moderate | Moderate |
| Decision Tree       | Moderate | Moderate  | Moderate | Moderate |
| Random Forest       | High     | High      | High     | High     |
| Gradient Boosting   | **Best** | **Best**  | **Best** | **Best** |

### 🏆 Best Model for Production

**Gradient Boosting Classifier / Random Forest**

✔ Handles non-linearity
✔ Robust to noise
✔ High recall for positive class
✔ Suitable for business decision-making

---

## 📌 Task 3: Business Recommendations

### 💡 Suggestions for Bank Marketing Team

1. **Target customers with previous campaign success**
2. **Reduce repeated calls** – fewer contacts improve trust
3. Focus on **retired, student, and management** job profiles
4. Align campaigns with **favorable economic indicators**
5. Use predictive model to **prioritize high-probability leads**
6. Avoid calling customers with poor historical engagement

---

## ⚠ Challenges Faced & Solutions

| Challenge                 | Solution                                |
| ------------------------- | --------------------------------------- |
| Class imbalance           | Used evaluation metrics beyond accuracy |
| Data leakage (`duration`) | Removed from final model                |
| Categorical features      | Applied proper encoding techniques      |
| Feature correlation       | Model-based feature importance          |
| Business interpretability | Chose tree-based models                 |

---

## 🧰 Tech Stack Used

* **Python**
* **Pandas, NumPy**
* **Matplotlib, Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**

---

## 📂 Project Structure

```
PRCP-1000-PortugueseBank/
│
├── PRCP-1000_PortugueseBank.ipynb
├── README.md
├── Dataset/
│   └── bank-additional-full.csv
└── requirements.txt
```

---

## ✅ Conclusion

This project demonstrates a **complete data science lifecycle**, from raw data analysis to production-ready modeling and business recommendations. The predictive model can significantly improve marketing efficiency and customer targeting for banking institutions.

---

## 👤 Author

**Prathmesh Mane Deshmukh**
B.Tech – AI & Data Science
GitHub: `@pamd005`
