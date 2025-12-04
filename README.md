Explainable AI for Amputation Risk Prediction in Diabetic Foot Ulcers

This repository contains the code and materials for predicting amputation risk in diabetic foot ulcer (DFU) patients using explainable machine learning (ML) techniques. The models leverage routine clinical data and provide interpretable insights for clinical decision support.

Background
Diabetic foot ulcers affect 6–34% of diabetic patients and are associated with high morbidity, with 15–20% requiring amputation within 12 months. Traditional risk stratification relies on the Wagner grading system, which suffers from inter-clinician variability and limited integration of systemic biomarkers. Explainable ML models offer improved predictive accuracy and transparency, even in resource-limited settings.

Methods
- Retrospective cohort of 734 DFU patients (2017–2023) from Ardabil University of Medical Sciences.
- Feature selection retained 12 routine clinical variables.
- Ten ML algorithms evaluated: XGBoost, CatBoost, LightGBM, SVM, logistic regression, Random Forest, and a stacking ensemble.
- Evaluation metrics: AUC-ROC, calibration (Brier score, Hosmer-Lemeshow test), sensitivity/specificity, and SHAP for interpretability.
- Data split: 80:20 train-test, SMOTE for class imbalance, 10-fold cross-validation with hyperparameter tuning.

Key Findings
- CatBoost achieved highest mean AUC (0.978±0.021) in cross-validation.
- On independent testing, SVM performed best (AUC=0.982, F1=0.930).
- Wagner Grade was the dominant predictor (~85% SHAP importance).
- Secondary predictors: WBC, monocyte count.
- LightGBM showed superior calibration (Brier=0.053, HL p=0.45).
- Optimal thresholds yielded sensitivity 0.90–0.95 and specificity 0.95–0.99.

Features
- Explainable AI using SHAP for feature importance
- Ensemble and single ML models for risk prediction
- Compatible with routine clinical data, suitable for resource-limited settings

Installation
Clone the repository:
bash
git clone https://github.com/AmirArshiaBeheshti/Explainable-Artificial-Intelligence-XAI-for-Amputation-Risk-Prediction-in-Diabetic-Foot-Ulcers.git

Install required Python packages: pip install -r requirements.txt

Usage

Open the Jupyter notebooks to explore data, train models, and generate SHAP explanations.

Review feature importance and interpret model predictions.

Modify or extend the notebooks for additional analysis.

Keywords

Diabetic foot ulcer, amputation prediction, machine learning, explainable AI, SHAP, Wagner Grade, ensemble learning


