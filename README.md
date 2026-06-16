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

## Key EDA Findings
- `thal`, `ca`, `exang`, `oldpeak`, `thalach`, and `cp` are the strongest 
  predictors of CAD
- `chol` and `fbs` show weak correlation with CAD
- Most CAD patients present as asymptomatic (cp=4), consistent with 
  clinical literature
- Dataset is reasonably balanced, requiring no class imbalance correction

## Tools & Libraries
Python, pandas, NumPy, scikit-learn, XGBoost, seaborn, matplotlib, SHAP

## Reference
Detrano, R. et al. (1989). *International application of a new probability 
algorithm for the diagnosis of coronary artery disease.* American Journal 
of Cardiology, 64(5), 304–310.# Heart Disease Risk Prediction
