# Magnetocaloric HEA — ΔSref 

Companion to the manuscript:
**Machine-learning-screening-of-magnetocaloric-high-entropy-alloys-using-a-field-normalized-Sref-targ**

## Contents
- `code/dSref_calculation.ipynb` — notebook for ΔSref construction/checks.
- `code/clean_code.ipynb` — performs a grid-searched, stratified K-fold cross-validated regression benchmark (RF/GBR/XGB/LGBM/SVR) to predict ΔSref from composition-only features, reports R²/RMSE/MAE, saves results, and provides feature-importance/SHAP analyses (with optional bootstrap checks) to validate the screening rule.
- `data/COMPO_ONLY_dataset_2.csv` — composition-only dataset.
- `data/COMPO_ONLY_model_ready_with_dSref_n0913.csv` — model-ready dataset with ΔSref (n≈0.913).

## Quick use
Open the notebook in Jupyter and adjust data paths if needed.

*Operating point (reported in the paper):* coverage≈0.347, recall≈0.720, precision≈0.261.
## License
- Code: MIT (see LICENSE)
- Data (data/): CC BY 4.0 (see LICENSE)
