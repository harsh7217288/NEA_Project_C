# dashboard/

The Streamlit app — the final user-facing product (Week 5).

**Suggested files:**

- `app.py` — the main Streamlit entry point. Run it with:
  ```
  streamlit run dashboard/app.py
  ```
- `pages/` (optional, if using Streamlit's multi-page app structure) — one file per
  page: overview, model comparison, live prediction

**What the app should do, at minimum:**

1. Show a dataset overview + key EDA charts
2. Show a model comparison table (metrics from Week 4)
3. Let a user input an asteroid's size/speed/distance and get a hazard prediction,
   with a short explanation of which features drove that result

**Rule of thumb:** the dashboard should import trained models and cleaning functions
from `src/` rather than duplicating that logic — it's a thin presentation layer on
top of the work already done in notebooks and src.
