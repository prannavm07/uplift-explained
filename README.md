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

## 📖 Usage

Run the Jupyter Notebook to reproduce results:
```bash
jupyter notebook "Final Code.ipynb"
```
Example: Training and evaluating a Two-Model Classifier:
```python
from sklift.models import TwoModels
from sklearn.ensemble import RandomForestClassifier

tm = TwoModels(
    estimator_trmnt=RandomForestClassifier(n_estimators=100, random_state=42),
    estimator_ctrl=RandomForestClassifier(n_estimators=100, random_state=42)
)
tm.fit(X_train, y_train, treatment=train_treatment)
uplift_scores = tm.predict(X_test)
```
---

## 📊 Results

The models were evaluated on uplift prediction accuracy.
| Model                     | Men’s Uplift | Women’s Uplift |
| ------------------------- | ------------ | -------------- |
| Single-Learner (XGBoost)  | 0.0580       | 0.0377         |
| SKLift TwoModel RF        | 0.0624       | 0.0162         |
| Custom Two-Model (RF)     | **0.0647**   | 0.0187         |
| T-Learner (GradientBoost) | 0.0639       | 0.0306         |

📈 Visuals & Insights
* Uplift curves show Custom Two-Model achieved the strongest uplift, particularly in the men’s campaign.
* SHAP analysis revealed recency, history, and newbie as the most influential features driving uplift.

---

## 🔎 Key Insights

* Uplift modeling provides better targeting than traditional methods.
* Custom Two-Model performed best overall.
* Explainability (via SHAP) adds transparency, crucial for business decision-making.

---

## 📚 Reference
This project was submitted as part of the MSc Data Science program at the University of Exeter.
For the full dissertation, see [Final_Report.pdf](https://github.com/prannavm07/uplift-explained/blob/main/Final_Report.pdf)

If you use this work, please cite:
```bibtex
@thesis{more2025uplift,
  title={Comparative Analysis and Explainability of Uplift Modeling Techniques for Targeted Marketing Campaigns},
  author={Pranav More},
  year={2025},
  school={University of Exeter}
}
```

---

## 🙌 Acknowledgements

* Supervisor: Dr. Aishwaryaprajna
* Hillstrom dataset provider
* Libraries: scikit-learn, scikit-uplift, XGBoost, SHAP
