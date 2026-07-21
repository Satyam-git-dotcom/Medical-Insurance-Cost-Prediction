# Medical Insurance Cost Prediction using Multiple Linear Regression

**AI-ML Assignment – 1**  
**Topic:** Medical Insurance Cost Prediction using Multiple Linear Regression  
**Submission Deadline:** 21 July 2026, 11:59 PM IST  
Name-Satyam
Reg No.-23BAI10557
ENROLLMENT No.-IN26011304

---

## 📌 Objective
The goal of this assignment is to estimate individual medical insurance charges based on demographic characteristics and personal health-related attributes using a **Multiple Linear Regression** model. The project demonstrates the full machine learning workflow: data exploration, preprocessing, model development, evaluation, and analysis.

---

## 📊 Dataset Information
- **Dataset Name:** Medical Cost Personal Insurance Dataset
- **Kaggle Link:** [Medical Cost Personal Insurance Dataset on Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **Total Samples:** 1,338 records
- **Features:**
  - `age`: Age of primary beneficiary (numerical)
  - `sex`: Insurance contractor gender (`female`, `male`)
  - `bmi`: Body mass index (kg/m²)
  - `children`: Number of children covered by health insurance
  - `smoker`: Smoking status (`yes`, `no`)
  - `region`: Residence region (`southwest`, `southeast`, `northwest`, `northeast`)
  - `charges`: Individual medical costs billed by health insurance (target variable)

---

## 🛠️ Libraries Used
- Python 3.x
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn

---

## ⚙️ Methodology

1. **Data Understanding**
   - Loaded the dataset and inspected its shape and summary statistics.
   - Identified numerical and categorical features, and the target variable.

2. **Data Preprocessing**
   - Checked for missing values and found none.
   - Encoded categorical variables using one-hot encoding with `pd.get_dummies(drop_first=True)`.
   - Split the dataset into training (80%) and testing (20%) sets with `random_state=42`.

3. **Model Development**
   - Trained a `LinearRegression` model on the training set.
   - Made predictions on the test set.

4. **Evaluation**
   - Assessed model performance using MAE, MSE, RMSE, and R².
   - Visualized results with an Actual vs. Predicted scatter plot.

---

## 📈 Results

| Metric | Value |
| :--- | :---: |
| Mean Absolute Error (MAE) | 4,181.19 |
| Mean Squared Error (MSE) | 33,596,915.85 |
| Root Mean Squared Error (RMSE) | 5,796.28 |
| R² Score | 0.7836 |

### Model Insights
- **Intercept:** -11,931.22
- **Smoker:** +23,651.13
- **Number of children:** +425.28 per child
- **BMI:** +337.09 per unit
- **Age:** +256.98 per year
- **Male:** -18.59
- **Region (northwest):** -370.68
- **Region (southeast):** -657.86
- **Region (southwest):** -809.80

---

## 📝 Observations
- The model explains approximately **78.36%** of the variance in insurance charges.
- **Smoking status** is the strongest predictor of medical insurance cost.
- The model may not capture all non-linear interactions, especially between BMI and smoking.

---

## 🎯 Conclusion
This assignment demonstrates a Multiple Linear Regression approach to predicting medical insurance charges. The model shows good predictive performance, but non-linear feature interactions may require more advanced modeling or feature engineering to fully capture cost variance.

---

## 📁 Repository Structure
```
aiml-assignment-1/
├── Assignment-1.ipynb
├── README.md
└── .gitignore
```

---

*Developed for AI-ML Assignment 1.*
