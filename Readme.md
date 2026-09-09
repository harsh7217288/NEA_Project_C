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

| Purpose          | Tools                              |
| ---------------- | ---------------------------------- |
| Language         | Python                             |
| Data Handling    | Pandas, NumPy                      |
| Astronomy Data   | Astropy, NASA/JPL Data (NeoWs API) |
| Machine Learning | Scikit-learn, XGBoost              |
| Visualization    | Matplotlib, Seaborn, Plotly        |
| Dashboard        | Streamlit                          |
| Development      | Jupyter Notebook                   |
| Version Control  | Git + GitHub                       |

## Project Structure

```
nea-project/
├── data/              # raw/ and processed/ datasets (not committed — see .gitignore)
├── notebooks/         # Jupyter notebooks for EDA, feature engineering, modeling
├── src/               # reusable Python scripts (data loading, cleaning, model training)
├── dashboard/         # Streamlit app
├── reports/           # final report, presentation, figures
├── requirements.txt
├── .gitignore
└── README.md
```

## ⚠️ Important: The dataset is NOT in this repo

The `data/raw/` and `data/processed/` folders are excluded via `.gitignore` to keep
the repo small and fast to clone. **Every teammate must download the dataset
themselves** after cloning — see Step 4 below. If you `git status` and don't see
your CSV listed as a change, that's expected and correct — it means it's being
ignored properly, not that something is broken.

## Setup & Installation

### Prerequisites

- **Python 3.14** — everyone on the team should use this exact version to avoid
  version-conflict bugs (see "Python Version & VS Code Interpreter" below)
- Git installed
- A free Kaggle account (to download the dataset) and/or a free NASA API key

### 0. Python Version & VS Code Interpreter (do this first)

To avoid "it works on my machine but not yours" bugs, **everyone must use Python 3.14**.

**Check your version:**

```bash
py --version
```

If it doesn't say `Python 3.14.x`, download and install Python 3.14 from
[python.org/downloads](https://www.python.org/downloads/) before continuing.

**Set it as your interpreter in VS Code:**

1. Open the Command Palette: `Ctrl+Shift+P` (Windows) or `Cmd+Shift+P` (Mac)
2. Type and select **"Python: Select Interpreter"**
3. Choose the entry showing **Python 3.14.x** (if you've already created `venv/`, pick the
   one inside `venv/Scripts/python.exe` — Windows — or `venv/bin/python` — Mac/Linux — instead,
   since that's your project's isolated environment)
4. Confirm the bottom-left status bar in VS Code now shows `3.14.x` (or `('venv': venv)`)

### 1. Clone the repo

```bash
git clone https://github.com/harsh7217288/NEA_Project_C.git
cd NEA_Project_C
```

### 2. Create a virtual environment

**Important:** create the venv using Python 3.14 specifically, so it matches everyone
else's setup:

**Windows (Command Prompt or PowerShell):**

```bash
py -3.14 -m venv venv
venv\Scripts\activate
```

**macOS / Linux:**

```bash
python3.14 -m venv venv
source venv/bin/activate
```

You'll know it worked when your terminal prompt shows `(venv)` at the start of the line.

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Get the dataset

Download `neo_v2.csv` from the "NASA - Nearest Earth Objects" Kaggle dataset and place it at:

```
data/raw/neo_data.csv
```

### 5. (Optional) Set up the NASA API key

Only needed if using the live NeoWs API instead of the Kaggle CSV. Get a free key at
api.nasa.gov, then create a `.env` file in the project root:

```
NASA_API_KEY=your_key_here
```

### 6. Verify the setup

```bash
python -c "import pandas, sklearn, xgboost, streamlit; print('All good')"
```

If this prints `All good` with no errors, you're ready to start.

### 7. Run the dashboard (once built)

```bash
streamlit run dashboard/app.py
```

## Timeline

| Week | Focus                   | Deliverable                                 |
| ---- | ----------------------- | ------------------------------------------- |
| 1    | Getting Started         | Tools set up, NASA data collected & cleaned |
| 2    | Exploring the Data      | EDA charts on size, speed, distance         |
| 3    | Preparing for Modeling  | Engineered features, baseline models        |
| 4    | Building the Main Model | Tuned XGBoost model                         |
| 5    | Building the Dashboard  | Streamlit app for live predictions          |
| 6    | Wrapping Up             | Testing, report, presentation               |

## Notes

This model is a project-level educational analysis. Where relevant, results are compared
against NASA/JPL CNEOS data, but this project is not a substitute for CNEOS's official
risk assessments.
