# 📊 Bank Marketing Prediction - Data Science Project

## 📌 Project Overview
This project aims to predict the success of bank telemarketing campaigns using machine learning techniques. The study is based on the dataset from a Portuguese bank, containing customer information and past marketing campaign interactions.

## 📂 Files in this Repository
- **`bank_marketing.ipynb`** – Main notebook with data preprocessing, model training, and evaluation.
- **`bank.csv` & `bank-additional-full.csv`** – Dataset files used in the project.
- **`Similar_dataset.ipynb`** – Testing the methodology of the paper on similar datasets.
- **`bank_marketing.png` & `bank_marketing_SMOTE.png`** – Decision tree visualizations before and after applying SMOTE.

---

## 📌 Steps Reproduced from the Paper
The following machine learning models were implemented as described in the original research paper:
- **Logistic Regression**
- **Decision Tree**
- **Support Vector Machine (SVM)**

🔹 The paper did not specify the hyperparameters used, so we followed a standard approach.

---

## 🚀 Contributions
In addition to reproducing the original methodology, we made several improvements:
- **Testing the methodology on similar datasets** to assess the generalizability of the models.
- Implemented **K-Nearest Neighbors (KNN)** and **Random Forest** models to compare performance.
- Applied **XGBoost**, which demonstrated better predictive power.
- Conducted **feature importance analysis** to identify the most relevant variables affecting customer response.

---

## 📈 Significant Improvements
To handle the class imbalance problem, **SMOTE (Synthetic Minority Over-sampling Technique)** was applied, leading to significant improvements:
- **Logistic Regression:** Accuracy slightly dropped to 89%, but recall for "yes" improved from 40% to 90%.
- **Decision Tree:** Accuracy increased to 93%, and recall for "yes" improved to 94%.
- **SVM:** Accuracy remained at 92%, but recall for "yes" improved to 94%.
- **Random Forest:** Accuracy reached 95%, with recall for "yes" improving to 97%.
- **XGBoost:** Accuracy was 94%, and recall for "yes" increased to 96%.
- **KNN:** Performance improved after SMOTE, reducing misclassification of the minority class.

📌 **AUC-ROC curves confirmed that models performed significantly better after applying SMOTE.**

---

## 🔍 Insights from Decision Tree Analysis
The **Decision Tree** visualization revealed key insights:
- **"nr.employed" (employment rate) and "duration" (call duration)** were the strongest predictors.
- **Economic indicators ("consumer confidence index" and "euribor3m")** influenced customer decisions.
- Customers were more likely to accept an offer when the economy was stable and the call duration was longer.

---

## ⚙️ How to Run This Project
1. Clone this repository:
   ```bash
   git clone https://github.com/Elvis-Jekir/bank_marketing.git 
   cd bank_marketing
