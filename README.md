# Probability of Default (PD) Model — LendingClub

## Overview
A credit risk model built on the LendingClub loan dataset to predict the 
probability that a borrower will default on their loan.

Two notebooks cover the full pipeline:
- `LC_DataCleaning.ipynb` — data cleaning, feature engineering and WoE encoding
- `PD_Model.ipynb` — model training, evaluation and comparison

## Results

| Model               | AUC    | KS     |
|---------------------|--------|--------|
| Logistic Regression | 0.7067 | 0.3068 |
| Random Forest       | 0.6963 | 0.2868 |
| Gradient Boosting   | 0.7041 | 0.3009 |

**Selected model: Logistic Regression** — highest AUC and KS, and preferred 
in credit risk for regulatory interpretability.

## Data
The raw dataset is the LendingClub loan data, publicly available on Kaggle:
[Download here](https://www.kaggle.com/datasets/wordsforthewise/lending-club)

Once downloaded, place the file in `data/raw/lendingclub.csv` and run the cleaning notebook first.

## How to Run
1. Download the dataset from the link above and place it in `data/raw/lendingclub.csv`
2. Run `LC_DataCleaning.ipynb` to clean the data and generate processed files
3. Run `PD_Model.ipynb` to train and evaluate the models

## Requirements
```
pip install -r requirements.txt
```

## Tech Stack
Python · scikit-learn · pandas · numpy · matplotlib · seaborn
