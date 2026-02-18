# Stroke Risk ML Replication

This repository contains a **replication study** of a machine learning–based stroke risk prediction paper.  
The goal is to reproduce the original analysis pipeline, validate reported results, and provide a clean,
reproducible baseline for further improvements.

---

## Project Overview

Stroke is a major cause of mortality and long-term disability.  
This project replicates a published study that applies **machine learning models** to predict stroke risk
using demographic, lifestyle, and clinical features.

The replication includes:
- Exploratory Data Analysis (EDA)
- Multiple ML classifiers
- Dimensionality reduction and clustering
- Survival analysis using an age-based proxy

---

## Dataset

- **Source:** Kaggle – Stroke Prediction Dataset  
- **Type:** Tabular (demographic, lifestyle, clinical features)
- **Target variable:** `stroke` (binary)

⚠️ The dataset is **not stored in this repository**.  
It is downloaded automatically inside the Google Colab notebook using the Kaggle API.

---

## Methodology

The notebook implements the following steps:

1. **Data Preprocessing**
   - Missing value handling
   - Encoding categorical variables
   - Feature scaling

2. **Exploratory Data Analysis**
   - Age, BMI, glucose distributions
   - Class imbalance inspection

3. **Machine Learning Models**
   - Decision Tree
   - K-Nearest Neighbors
   - Naïve Bayes
   - Gradient Boosting
   - AdaBoost  
   *(Optional: XGBoost, CatBoost if available)*

4. **Evaluation Metrics**
   - Accuracy
   - Precision
   - Recall
   - F1-score
   - ROC–AUC
   - Confusion matrices

5. **Clustering & Visualization**
   - PCA
   - t-SNE
   - K-means clustering

6. **Survival Analysis**
   - Kaplan–Meier curves
   - Cox proportional hazards model  
   *(Age used as a proxy timeline due to lack of follow-up data)*

---

## How to Run the Project

### Option 1: Google Colab (Recommended)

1. Open the notebook:  
   **`Stroke_Risk_Replication.ipynb`**
2. Run all cells top to bottom
3. Upload your `kaggle.json` when prompted
4. Outputs (plots, metrics) are saved in the `outputs/` directory

---

### Option 2: Local Execution

```bash
pip install -r requirements.txt
python replicate_stroke_paper.py
