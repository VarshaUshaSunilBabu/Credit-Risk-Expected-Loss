# Credit Risk Analysis Using Lending Club Data

**What happens when you combine Machine Learning with financial risk assessment?**  
You get a predictive model that tells banks who’s likely to default and how much they might lose!  

After crunching millions of loan records, running hyperparameter tuning, and wrestling with imbalanced data, I finally built a model that estimates **Expected Loss (EL)** in lending. 😎  

---

## **Project Overview**

### 🎯 **Project Goal**  
Can We Predict How Much Banks Will Lose on Loans?  
Banks love lending money, but hate losing it (who doesn’t?). This project predicts the **Expected Loss (EL)** for loans using machine learning.

---

## **Challenges**  

### 🤯 **The Struggles Were Real**  
- **Massive dataset (~2.1M records)** – My laptop nearly overheated! 🔥  
- **Class imbalance** – Most borrowers don’t default, so the model kept predicting “safe” loans only! 😭  
- **Trade-off between recall & precision** – Too many false positives or missed defaults? Decisions, decisions...  

---

## **Solution**  

### 💡 **Approach**  
- **SMOTE** to balance the dataset.  
- **Threshold tuning** to optimize recall (catch defaults better).  
- **Feature engineering** (DTI, Income-to-Installment, Credit Utilization).  
- **XGBoost + RandomizedSearchCV** – Best combo for speed & accuracy.  

---

## **Key Results**  

### ⚡ **Model Performance**  
- **Best Parameters**:  
  - `subsample: 0.6`  
  - `n_estimators: 100`  
  - `max_depth: 10`  
  - `learning_rate: 0.2`  
  - `colsample_bytree: 1.0`  
- **Optimized Model Accuracy**: 49.62% (not great, but expected in imbalanced data).  
- **ROC AUC Score**: 0.6455 (model can differentiate risky vs. non-risky loans).  
- **Recall**: 84.07% (✅ catches most actual defaults!).  

---

### 📊 **Expected Loss Calculation**  
- **Total Expected Loss**: $1.55 BILLION 💸 (No, this isn’t Monopoly money!).  
- **Mean Expected Loss**: $3,681 per loan.  
- **Max Expected Loss**: $19,650 – Some loans are ticking time bombs!  

---

### 🔍 **Visualizing Risk**  
- Most loans fall under $5,000 EL, but a small percentage have extreme losses ($15K+).  

---

## **Final Takeaways**  
- **High Recall = Better Risk Management** → Catching more defaulters is key!  

---

## **Tools & Technologies Used**  
- Python  
- Pandas, NumPy, Scikit-learn, XGBoost  
- SMOTE, RandomizedSearchCV  
- Matplotlib, Seaborn (for visualizations)  

---

