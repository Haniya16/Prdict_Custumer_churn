# Prdict_Custumer_churn
# Summary

**Dataset:** Telco Customer Churn CSV (WA_Fn-UseC_-Telco-Customer-Churn.csv) — loaded from Google Drive.

**Preprocessing**
- Converted `TotalCharges` to numeric and imputed missing values.
- Numeric features: median imputation + standard scaling.
- Categorical features: most-frequent imputation + one-hot encoding.

**Models trained**
- Logistic Regression (class_weight='balanced')
- Random Forest (class_weight='balanced')
- Gradient Boosting (sklearn)

**Imbalance handling**
- Default approach: class weights in LR and RF.
- Optionally: SMOTE oversampling by toggling `use_smote=True`.

**Evaluation**
- Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC.
- Plots: ROC curves for all models, confusion matrices.

**Explainability**
- Feature importance from Random Forest.
- SHAP summary plot for Random Forest to justify decisions.

**Artifacts**
- Best model saved as joblib in: `/content/drive/MyDrive/Colab Notebooks/PredictCustumerChurn/Models/`
