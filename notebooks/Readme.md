# notebooks/

Jupyter notebooks for exploration and experimentation — this is where you think out
loud, try things, and make charts. Code that turns out to be reusable should
eventually get moved into `src/` as a proper function/script.

**Naming convention:** prefix with a number so the order of the workflow is obvious
just from the file list:

- `01_data_inspection.ipynb` — first look at the raw data (shape, types, missing values)
- `02_eda.ipynb` — exploratory data analysis, charts, class imbalance check (Week 2)
- `03_feature_engineering.ipynb` — creating new columns, encoding, train/test split (Week 3)
- `04_modeling.ipynb` — training and comparing Logistic Regression, Random Forest, XGBoost (Week 4)
- `05_explainability.ipynb` — feature importance / SHAP analysis (Week 4)

**Rule of thumb:** notebooks are for exploring and explaining your thinking with charts
and markdown notes in between cells — not for production code the dashboard depends on.