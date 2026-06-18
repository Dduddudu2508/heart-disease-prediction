# Heart Disease Risk Prediction

Predicting the risk of Coronary Artery Disease (CAD) from clinical data 
using machine learning, based on the UCI Cleveland Heart Disease Dataset 
(Detrano et al., 1989).

## Dataset
UCI Cleveland Heart Disease Dataset — sourced directly from the 
[UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/45/heart+disease).

- 303 patients, 13 clinical features
- Binary target: 0 = No CAD, 1 = CAD (stenosis > 50%)
- Class distribution: 54% No CAD, 46% CAD

## Project Structure
- `notebooks/` — Jupyter notebooks for EDA and modeling
- `data/` — raw dataset (not tracked by Git)

## Notebooks
- `01_eda.ipynb` — Exploratory Data Analysis including missing value 
  treatment, correlation analysis, and visualization of key clinical features
- `02_modeling.ipynb` — Model training, hyperparameter tuning, and 
  evaluation across four machine learning models

## Key EDA Findings
- `thal`, `ca`, `exang`, `oldpeak`, `thalach`, and `cp` are the strongest 
  predictors of CAD
- `chol` and `fbs` show weak correlation with CAD
- Most CAD patients present as asymptomatic (cp=4), consistent with 
  clinical literature
- Dataset is reasonably balanced, requiring no class imbalance correction

## Model Results

| Model | Accuracy | Precision (CAD) | Recall (CAD) | F1 (CAD) |
|---|---|---|---|---|
| KNN (k=8) | 0.84 | 0.94 | 0.65 | 0.77 |
| Logistic Regression | 0.79 | 0.81 | 0.65 | 0.72 |
| XGBoost | 0.77 | 0.77 | 0.65 | 0.71 |
| Random Forest | 0.75 | 0.76 | 0.62 | 0.68 |

## Key Findings
- KNN (k=8) achieved the highest accuracy (84%) and precision (0.94)
- CAD recall remains consistently at 0.65 across all models, suggesting 
  dataset size (303 rows) is the primary bottleneck
- Combining all four UCI hospital datasets (~920 rows) would likely 
  improve recall significantly

## Next Steps
- SHAP values for model interpretability
- Threshold tuning to improve CAD recall
- Cross validation for more robust evaluation
- Combine all four UCI hospital datasets

## Tools & Libraries
Python, pandas, NumPy, scikit-learn, XGBoost, seaborn, matplotlib, SHAP

## Reference
Detrano, R. et al. (1989). *International application of a new probability 
algorithm for the diagnosis of coronary artery disease.* American Journal 
of Cardiology, 64(5), 304–310.
