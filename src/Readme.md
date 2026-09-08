# src/

Reusable Python scripts — the "real" code, as opposed to exploratory notebook code.
Anything imported by more than one notebook, or used by the dashboard, belongs here.

**Suggested files:**

- `fetch_data.py` — functions to pull data from the NASA NeoWs API (optional/bonus,
  since Week 1 uses the Kaggle CSV as the primary source)
- `clean_data.py` — functions that take raw data and return a cleaned DataFrame
  (drop duplicates, handle missing values, fix units, drop useless columns)
- `features.py` — feature engineering functions (velocity/distance ratio, log
  transforms, encoding the target column)
- `train_model.py` — functions to train and save a model (Logistic Regression,
  Random Forest, XGBoost)
- `evaluate.py` — functions to compute precision/recall/F1/ROC-AUC and produce a
  confusion matrix

**Rule of thumb:** if you find yourself copy-pasting the same code cell into a second
notebook, that's the signal to turn it into a function here instead, and `import` it.