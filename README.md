# Probability of Default (PD) Model — LendingClub

## Overview
A credit risk model built on the LendingClub loan dataset to predict the 
probability that a borrower will default on their loan.

Two notebooks cover the full pipeline:
- `LendingClubProject_DataCleaning.ipynb` — data cleaning, feature engineering and WoE encoding
- `PD_Model.ipynb` — model training, evaluation and comparison

## Results

| Model               | AUC    | KS     |
|---------------------|--------|--------|
| Logistic Regression | 0.7067 | 0.3068 |
| Random Forest       | 0.6963 | 0.2868 |
| Gradient Boosting   | 0.7041 | 0.3009 |

**Selected model: Logistic Regression** — highest AUC and KS, and preferred 
in credit risk for regulatory interpretability.

## How to Run
1. Download the LendingClub dataset and place it in `data/raw/lendingclub.csv`
2. Run `LendingClubProject_DataCleaning.ipynb` to generate processed files
3. Run `PD_Model.ipynb` to train and evaluate the models

## Requirements
```
pip install -r requirements.txt
```

## Tech Stack
Python · scikit-learn · pandas · numpy · matplotlib · seaborn
```

Click **Commit changes**.

---

## Step 4 — Upload your files
1. On your repo homepage click **Add file** → **Upload files**
2. Drag and drop these files:
   - `PD_Model.ipynb`
   - `LendingClubProject_DataCleaning.ipynb`
   - `requirements.txt` (create this as a text file on your desktop first — see below)
3. Click **Commit changes**

**requirements.txt contents:**
```
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

---

## Step 5 — Add a .gitignore
1. Click **Add file** → **Create new file**
2. Name it `.gitignore`
3. Paste this in:
```
data/
*.csv
.ipynb_checkpoints/
__pycache__/
