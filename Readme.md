# Near-Earth Asteroid Risk Analysis & Prediction System

A machine learning system that studies Near-Earth Asteroids (NEAs) using real NASA/JPL data,
and classifies whether an asteroid is potentially hazardous based on its size, speed, and
distance from Earth. Results are explained through feature importance and shown on an
interactive Streamlit dashboard.

## Team

- Adrika Anand
- Shivangi Maurya
- Shreya Sonal
- Harsh Choudhary
- Sukrat Srivastava
- Jimmy Khanpara

## Problem Statement

Thousands of asteroids pass near Earth, but only a small fraction are genuinely risky.
Manually checking each one isn't practical. This project builds a model that classifies
an asteroid as **Hazardous** or **Not Hazardous** based on its physical and orbital
properties, and presents the result through an easy-to-use tool.

## Objectives

- Clean and understand real NASA asteroid data
- Explore the data to find useful patterns
- Engineer features from size, speed, and distance
- Train an XGBoost model to predict hazard risk
- Compare against simpler baseline models
- Build a Streamlit dashboard for live predictions
- Explain results in simple, real-world terms (feature importance / SHAP)

## Tech Stack

| Purpose             | Tools                                   |
|---------------------|------------------------------------------|
| Language            | Python                                   |
| Data Handling       | Pandas, NumPy                            |
| Astronomy Data      | Astropy, NASA/JPL Data (NeoWs API)       |
| Machine Learning    | Scikit-learn, XGBoost                    |
| Visualization       | Matplotlib, Seaborn, Plotly              |
| Dashboard           | Streamlit                                |
| Development         | Jupyter Notebook                         |
| Version Control     | Git + GitHub                             |

## Project Structure

```
nea-project/
├── data/              # raw and cleaned datasets (not committed if large — see .gitignore)
├── notebooks/         # Jupyter notebooks for EDA, feature engineering, modeling
├── src/                # reusable Python scripts (data loading, cleaning, model training)
├── dashboard/         # Streamlit app
├── reports/           # final report, presentation, figures
├── requirements.txt
├── .gitignore
└── README.md
```

## Setup

1. Clone the repo:
   ```
   git clone https://github.com/<your-org-or-username>/nea-project.git
   cd nea-project
   ```

2. Create and activate a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate        # Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Get a free NASA API key at https://api.nasa.gov and add it to a `.env` file:
   ```
   NASA_API_KEY=your_key_here
   ```

## Timeline

| Week | Focus | Deliverable |
|------|-------|-------------|
| 1 | Getting Started | Tools set up, NASA data collected & cleaned |
| 2 | Exploring the Data | EDA charts on size, speed, distance |
| 3 | Preparing for Modeling | Engineered features, baseline models |
| 4 | Building the Main Model | Tuned XGBoost model |
| 5 | Building the Dashboard | Streamlit app for live predictions |
| 6 | Wrapping Up | Testing, report, presentation |

## Notes

This model is a project-level educational analysis. Where relevant, results are compared
against NASA/JPL CNEOS data, but this project is not a substitute for CNEOS's official
risk assessments.