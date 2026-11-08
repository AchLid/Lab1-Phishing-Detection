# Lab 1: Phishing URL Detection

Lab for Module M115 (AI & Intelligent Systems), Master in Intelligent Systems and Cyberdefense, ENSIASD Taroudant, 2026–2027.

The lab detects phishing URLs with Logistic Regression and explains the model's alerts with SHAP for a Security Operations Center (SOC).

All the work is in `Lab1.ipynb`, including the code, plots, answers and SOC synthesis.

## What it covers

1. Exploratory analysis of 235,795 URLs
2. Leakage-free train/test split and standardization
3. Five Logistic Regression configurations and L1 feature selection
4. SHAP explanations and decision thresholds for SOC use

## Results

The Standard L2 model (M3) reached Precision 0.9996, Recall 0.9989 and F1 0.9992 on the test set. The sparse L1 model (M4) reached F1 0.9982 using 25 of the 49 features.

The recommended policy blocks URLs automatically at P(Phishing) ≥ 0.85, which gave 0 false alarms on the test set, and sends 0.20 to 0.85 to analysts.

These scores come from a very cleanly separated dataset, so they shouldn't be expected on live traffic.

## How to run

Download the [PhiUSIIL Phishing URL Dataset](https://www.kaggle.com/datasets/kaggleprollc/phishing-url-websites-dataset-phiusiil/data), which is not included here, and place `PhiUSIIL_Phishing_URL_Dataset.csv` next to the notebook.

```bash
pip install numpy pandas matplotlib seaborn scikit-learn shap jupyter
```

A full run takes about 25 minutes, mostly in Exercise 6.

## AI use

Claude (Anthropic) assisted with the code and written answers.

## Author

Achraf Lidrissi, under the instruction of Prof. Sara EL-ATEIF.
