# Magnetocaloric HEA — ΔSref 

Companion to the manuscript:
**Machine-learning-screening-of-magnetocaloric-high-entropy-alloys-using-a-field-normalized-Sref-targ**

## Contents
- `code/dSref_calculation.ipynb` — notebook for ΔSref construction/checks.
- `code/clean_code.ipynb` — performs a grid-searched, stratified K-fold cross-validated regression benchmark (RF/GBR/XGB/LGBM/SVR) to predict ΔSref from composition-only features, reports R²/RMSE/MAE, saves results, and provides feature-importance/SHAP analyses (with optional bootstrap checks) to validate the screening rule.
- `data/COMPO_ONLY_dataset_2.csv` — composition-only dataset.
- `data/COMPO_ONLY_model_ready_with_dSref_n0913.csv` — model-ready dataset with ΔSref (n≈0.913).
  
Reproducibility (scripts used in the revision)
Comment 2.2 (field-scaling exponent n and ΔSref normalization):
n_estimation_dSref_v2.py — estimates the pooled fixed-effects exponent n (cluster bootstrap CI), performs the post-normalization fixed-effects “beta_after ≈ 0” check, and exports the ΔSref-augmented dataset.
Comment 2.5 (model comparison via nested CV):
nested_cv_models_v2.py — runs quantile-stratified nested cross-validation for all regressors (R²/RMSE/MAE), and produces the Table 1 / Table S2 performance summaries (mean±SD and median [Q1, Q3]).
## Quick use
Open the notebook in Jupyter and adjust data paths if needed.

*Operating point (reported in the paper):* coverage≈0.347, recall≈0.720, precision≈0.261.
## License
- Code: MIT (see LICENSE)
- Data (data/): CC BY 4.0 (see LICENSE)
