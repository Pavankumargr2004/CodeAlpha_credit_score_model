# CodeAlpha_credit_score_model
# 💳 Creditworthiness Prediction

## 📌 Objective
The goal of this project is to **predict an individual's creditworthiness** (good or bad credit risk) using their past financial history.  
This system can help banks and financial institutions make better loan approval decisions.  

---

## 📊 Dataset
We use the **German Credit Dataset (UCI Repository)**:
- **Rows:** 1000 individuals  
- **Features:** 20+ financial and demographic attributes  
- **Target:**
  - `0` → Good credit risk  
  - `1` → Bad credit risk  

🔗 [German Credit Data - UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+data))

---

## ⚙️ Approach
1. **Data Exploration (EDA)** – check distributions, balance of classes  
2. **Feature Engineering** – create useful features like:
   - `credit_per_month = Credit_amount / Duration_in_month`
   - Age group buckets (young, middle-aged, senior)
   - High installment flag  
3. **Preprocessing**  
   - Encode categorical features (OneHotEncoder)  
   - Scale numerical features (StandardScaler)  
   - Handle imbalance using **SMOTE**  
4. **Modeling**  
   - Logistic Regression  
   - Decision Tree  
   - Random Forest  
5. **Evaluation**  
   - Precision, Recall, F1-Score  
   - ROC-AUC  
   - Confusion Matrix & ROC curve  
6. **Model Selection**  
   - Best model chosen based on ROC-AUC  
   - Final pipeline saved for inference  

---

## 🛠️ Tech Stack
- **Language:** Python  
- **Libraries:** pandas, numpy, scikit-learn, imbalanced-learn, seaborn, matplotlib, joblib  

---

## 📈 Results
- **Best Model:** Random Forest Classifier  
- **Metrics (approx):**
  - ROC-AUC: ~0.75–0.80  
  - Precision: ~0.65–0.70  
  - Recall: ~0.55–0.65  
  - F1-score: ~0.60–0.65  

👉 Random Forest outperformed Logistic Regression and Decision Tree.  

---

## 🔑 Key Insights
- Checking account status, credit history, and savings account balance strongly influence creditworthiness.  
- Engineered features like **credit per month** improve model performance.  
- Handling class imbalance (SMOTE) prevents the model from always predicting "good credit".  

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/creditworthiness-prediction.git
   cd creditworthiness-prediction
