
# Customer Survival Analysis and Churn Prediction  


---

## Table of Contents  
1. [Project Overview](#project-overview)  
2. [Tech Stack](#tech-stack)  
3. [Project Organization](#project-organization)  
4. [Customer Survival Analysis](#customer-survival-analysis)  
5. [Customer Churn Prediction](#customer-churn-prediction)  
6. [Flask App](#flask-app)  
7. [Prerequisites](#prerequisites)  
8. [Configuration](#configuration)  
9. [How to Run](#how-to-run)  
10. [Dashboard Sample](#dashboard-sample)  
11. [Clean-Up](#clean-up)  
12. [Acknowledgments](#acknowledgments)  
13. [Conclusion](#conclusion)  

---

## Project Overview  

This project aims to analyze customer churn using **Survival Analysis** and build a machine learning model for churn prediction.  
I also deployed a **Flask Web App** where users can check customer lifetime value, survival probability, and churn risk.  

---

## Tech Stack  

- **Python** — Data analysis, modeling, and backend  
- **Lifelines** — Survival analysis modeling  
- **Scikit-learn** — Machine Learning (Random Forest)  
- **SHAP & ELI5** — Model explainability  
- **Flask** — Web framework  
- **Heroku** — Deployment  
- **Bootstrap & HTML** — Web UI  

---

## Project Organization  

```
├── Images/                             : Analysis plots  
├── static/images/                      : Images used in Flask app  
├── templates/index.html                : HTML Template for Flask  
├── Customer Survival Analysis.ipynb    : Survival analysis with CoxPH  
├── Exploratory Data Analysis.ipynb     : EDA on customer dataset  
├── Churn Prediction Model.ipynb        : Random Forest Model  
├── app.py                              : Flask Web App  
├── app-pic.png                         : Final app layout  
├── explainer.bz2                       : SHAP Explainer  
├── model.pkl                           : Random Forest Model  
├── survivemodel.pkl                    : CoxPH Model  
├── requirements.txt                    : Python dependencies  
├── Procfile                            : Deployment Procfile  
├── LICENSE.md                          : License  
└── README.md                           : Project Report  
```

---

## Customer Survival Analysis  

- **Kaplan-Meier Curves** and **Log-Rank Test** for churn patterns  
- **Cox Proportional Hazards Model** for hazard ratios  
- Calculated **Survival Curve**, **Hazard Curve**, and **Customer Lifetime Value**  

---

## Customer Churn Prediction  

- Built Random Forest classifier with class imbalance handling  
- Achieved **0.62 F1 Score** and **0.85 ROC-AUC**  
- Explained predictions with **Permutation Importance**, **PDP**, and **SHAP**  

---

## Flask App  

Deployed using **Flask**, the app shows:  
- Churn probability  
- Survival & Hazard curves  
- SHAP plots for explainability  
- Lifetime value estimate  

---

## Prerequisites  

- Python 3.x  
- Pip (for installing dependencies)  
- A Heroku account (if deploying)  
- SQL dataset and trained models  

---

## Configuration  

- Install Python dependencies:  
```bash
pip install -r requirements.txt
```  

- Update model paths if needed in `app.py`  

- Place trained models and explainer in project root:  
  - `model.pkl`  
  - `survivemodel.pkl`  
  - `explainer.bz2`  

---

## How to Run  

1. **Clone the repository**  
2. **Install requirements**  
```bash
pip install -r requirements.txt
```  
3. **Run Flask App locally**  
```bash
python app.py
```  
4. **Open in browser**  
```
http://localhost:5000
```  

---

## Dashboard Sample  

![Final App Layout]()  

---

## Clean-Up  

- Stop Flask app by pressing `Ctrl+C` in the terminal  
- If deployed on Heroku, stop or scale down dynos  
- Remove any temporary output or logs  

---

## Acknowledgments  

Big thanks to:  
- **Lifelines** for survival analysis  
- **Scikit-learn** for machine learning  
- **SHAP & ELI5** for explainability tools  
- **Flask** for the web framework  
- **Heroku** for hosting  

---

## Conclusion  

This project taught me how to combine **statistical survival analysis**, **machine learning modeling**, and **web deployment** into a production-ready solution.  
It demonstrates a real-world approach to customer churn prediction and business impact analysis.  

---
