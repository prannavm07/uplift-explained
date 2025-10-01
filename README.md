# 📈 Comparative Analysis and Explainability of Uplift Modeling Techniques

This repository contains the implementation and analysis for my **Master’s dissertation**:  
**"Comparative Analysis and Explainability of Uplift Modeling Techniques for Targeted Marketing Campaigns"**  

The project explores how **uplift modeling** can improve targeted marketing decisions compared to traditional predictive models. It implements and compares multiple approaches (Single-Learner, Two-Model, T-Learner) on the **Hillstrom dataset**, with an added focus on **explainability using SHAP**.

---

## 🚀 Project Overview

- **Goal:** To evaluate uplift modeling techniques that optimize marketing resource allocation by identifying customer segments most likely to respond positively.  
- **Dataset:** [Hillstrom’s Email Marketing Dataset](https://www.uplift-modeling.com/en/latest/api/datasets/fetch_hillstrom.html).  
- **Techniques Compared:**  
  - Single-Learner (XGBoost)  
  - Two-Model Classifier (Custom RF & SKLift RF)  
  - T-Learner (Gradient Boosting)  
- **Explainability:** SHAP (SHapley Additive exPlanations) to interpret feature impact.  

> 📊 This project demonstrates how uplift modeling can maximize ROI and improve marketing efficiency.

---

## 🗂 Repository Structure

```bash
├── Final Code.ipynb       # Jupyter notebook with full implementation
├── Final_Report.pdf       # Full dissertation report
├── data/                  # Dataset (not included for licensing)
├── images/                # Plots and visualizations (uplift curves, SHAP, etc.)
└── README.md              # Project overview
```

---

## ⚙️ Installation & Setup

Clone the repository:
```bash
git clone https://github.com/yourusername/uplift-modeling-dissertation.git
cd uplift-modeling-dissertation
```
Create a virtual environment & install dependencies:
```bash
pip install -r requirements.txt
```

Dependencies include:
* Python 3.8+
* pandas, numpy
* scikit-learn
* xgboost
* matplotlib, seaborn
* shap
* scikit-uplift
