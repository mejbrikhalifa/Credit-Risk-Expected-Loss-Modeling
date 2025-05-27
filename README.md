# Credit-Risk-Expected-Loss-Modeling
**This project implements the second phase of a comprehensive Credit Risk Modeling pipeline. It covers Probability of Default (PD), Loss Given Default (LGD), and Exposure at Default (EAD) estimation using statistical and machine learning models. It includes model development, feature selection, performance evaluation, credit scoring, and Expected Loss (EL) calculation. Advanced techniques like two-stage LGD modeling and cross-validated EL prediction pipelines are applied. Visualizations and risk tier segmentation are also included.**

## **Overview**
**The project covers the following key components:**

### **1. Data Preparation**
* **Loading and exploring the Lending Club loan dataset**
* **Handling missing values and selecting reference categories**
* **Feature engineering and preprocessing**

### **2. Probability of Default (PD) Modeling**
* **Logistic Regression and Random Forest comparison**
* **Feature selection using p-values: 148 features retained, 102 dropped**
* **Model interpretation and feature importance analysis**
* **Model evaluation using Gini coefficient and Kolmogorov-Smirnov (KS) statistic**

### **3. Applying the PD Model**
* **Credit Score calculation and mapping to PD**
* **Setting score-based cutoffs for risk stratification**
* **Population Stability Index (PSI) analysis for 2019 & 2020**

### **4. Loss Given Default (LGD) Modeling**
#### **Stage 1: Classification**
* **Models evaluated: Logistic Regression, Random Forest, XGBoost, LightGBM**
* **Final model: LightGBM Classifier**

#### **Stage 2: Regression**
* **Models evaluated: Linear Regression, Random Forest Regressor, Gradient Boosting, XGBoost Regressor**
* **Final model: Tuned LightGBM Regressor**
* **Performance: RMSE = 0.0767, MAE = 0.0463, R² = 0.3438**

### **5. Exposure at Default (EAD) Modeling**
* **Linear Regression model on defaulted loans**
* **Performance: RMSE = 0.0714, MAE = 0.0582, R² = 0.8937**

### **6. Expected Loss (EL) Calculation**
* **Implementation of an ExpectedLossPipeline class**
* **Integration of PD, LGD, and EAD predictions**
* **Cross-validation support**
* **Risk tier assignment based on EL thresholds**
* **Visualization of EL distribution and high-risk segments**

## **Tools & Technologies**
* **Python (Pandas, NumPy, Scikit-learn, LightGBM, XGBoost)**
* **Matplotlib & Seaborn for visualization**
* **Jupyter Notebooks**

## **Results Summary**
* **PD Model: Logistic Regression retained for interpretability**
* **LGD Model: Two-stage LightGBM pipeline**
* **EAD Model: Linear regression with strong fit (R² ≈ 0.89)**
* **Expected Loss estimates used to segment accounts into risk tiers for strategic decision-making**

## **Future Work**
* **Incorporation of macroeconomic indicators**
* **Survival analysis for time-to-default modeling**
* **Model deployment for production scoring**

## **Contact**
**For questions or collaboration, feel free to reach out via GitHub Issues or email.**
