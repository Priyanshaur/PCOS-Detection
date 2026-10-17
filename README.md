# PCOS Detection

A machine-learning project that predicts Polycystic Ovarian Syndrome (PCOS/PCOD) from clinical and survey features, with a Flask web app so the model can be used without touching any code.

This is a team project and the basis of our paper, **"PCOD Prediction Using Predictive Modeling"**, accepted at RCAAI 2025, the 4th International Conference on Robotics, Control, Automation and AI, at Manipal Institute of Technology, MAHE (December 2025). This repository is my fork of the team's original repo: [PrathmeshVishwakarma/PCOS-Detection](https://github.com/PrathmeshVishwakarma/PCOS-Detection).

## My contribution

I'm Priyansh Gaur, and my part of this project covered three areas:

- **Backend:** I worked on the backend that connects the trained model to the web app, so that users can enter their details and get a prediction.
- **Machine learning:** I contributed to the modelling work: building and comparing the gradient-boosting models (CatBoost, XGBoost, LightGBM) and the ensemble.
- **Research paper:** I'm a co-author of the paper, which was accepted at RCAAI 2025.

The rest of the team's contributions are listed in the Team section below.

## What it does

- Trains and compares gradient-boosting models (CatBoost, XGBoost, LightGBM) and combines them into an ensemble
- Selects features with SHAP, balances classes with SMOTE and tunes hyperparameters with Optuna
- Serves predictions through a Flask web app (`PCOS_webapp/`)
- Reports 99.56% accuracy on a dataset of 1,500+ records; the evaluation protocol is described in the paper

## Repository contents

| Path | What it is |
|---|---|
| `LGBM_K_fold.ipynb` | LightGBM with k-fold cross-validation |
| `shap + catboost.ipynb` | CatBoost modelling and SHAP feature analysis |
| `PCOS_webapp/` | Flask web app that serves the model |
| `best_model`, `scaler.pkl`, `selected_features.json` | Saved model, scaler and the selected feature list |
| `PCOS_data.csv`, `pcos_dataset.csv`, `CLEAN- PCOS SURVEY SPREADSHEET.csv` | Datasets used |
| `requirements.txt` | Python dependencies |

## Team

| Member | Contribution |
|---|---|
| Prathamesh | Machine learning, backend, research paper |
| Pratik | Data preprocessing, machine learning |
| Priyanka | Frontend, machine learning, research paper |
| **Priyansh Gaur (me)** | **Backend, machine learning, research paper** |
| Vidya | Machine learning, research paper |

## Limitations

- The results come from one dataset of about 1,500 records, so they are not evidence of how the model would perform in a clinical setting.
- This is a research and learning project. It is not a medical device and should not be used to diagnose anyone.
