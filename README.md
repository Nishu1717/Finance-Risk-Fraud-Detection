# Credit Card Fraud Detection: A Cost-Benefit Optimization Approach

**Author**: Nisarg Patel  
**Date**: 3rd January 2026

## 📌 Executive Summary
This project tackles the critical financial challenge of credit card fraud detection using advanced machine learning techniques (XGBoost) and Explainable AI (SHAP). Moving beyond simple accuracy metrics, this solution implements a business-centric **Cost-Benefit Analysis** to optimize decision thresholds, minimizing financial loss from both fraud and false positives.

## 🏢 The Business Problem
Credit card fraud results in billions of dollars in losses annually. Financial institutions face two competing risks:
1.  **Fraud Loss**: Direct financial loss from unauthorized transactions.
2.  **Customer Friction (False Positives)**: Blocking legitimate transactions leads to lost revenue (interchange fees) and customer churn.

A model optimized solely for technical accuracy may fail to maximize profitability. The business requires a solution that continuously balances these costs to find the optimal operating point.

## 🚀 The Solution
We developed a comprehensive data pipeline and predictive model:
- **Data Preprocessing**: Handling class imbalance (0.5% fraud rate) and extensive feature engineering (velocity checks, time-based patterns, behavioral profiling).
- **Modeling**: Training an **XGBoost Classifier** optimized for Area Under the Precision-Recall Curve (AUPRC).
- **Explainability**: Utilizing **SHAP (SHapley Additive exPlanations)** to provide transparency for every fraud prediction, enabling compliance and trust.
- **Optimization**: Implementing a custom **Threshold Optimization Strategy** based on the financial weight of False Negatives vs. False Positives.

## 📊 Key Results
- **Fraud Detection**: Achieved high precision and recall in the top deciles.
- **Financial Impact**: The cost-sensitive threshold significantly reduced projected losses compared to default classifications.
- **Key Determinants**: Identified high-value transaction velocity and specific merchant categories as primary fraud indicators.

## 🛠️ Tech Stack
- **Python**: Core logic and analysis.
- **Pandas & NumPy**: Data manipulation and vectorization.
- **XGBoost**: Gradient boosted decision trees for high-performance classification.
- **SHAP**: Model interpretability.
- **Matplotlib & Seaborn**: Professional visualization.

## 📂 Repository Structure
```
/data             # For dataset
/notebooks        # Jupyter notebooks with full analysis and outputs
/visualizations   # High-resolution charts and model metric plots
/docs             # Project documentation including BRD
```

# Dataset Information

The datasets used in this project (`fraudTrain.csv` and `fraudTest.csv`) are sourced from the **Sparkov Data Generation** project on Kaggle.

Due to their large size, they are not hosted directly in this repository's main view but are required for the analysis.

## Source
- **Name**: Credit Card Fraud Detection Dataset (Simulated)
- **Source**: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/kartik2112/fraud-detection)

## File Structure
- `fraudTrain.csv`: Training data
- `fraudTest.csv`: Testing data

Please download these files and place them in this `data/` directory to run the notebook locally.

## 🚀 Getting Started
1.  Clone this repository.
2.  Install dependencies: `pip install -r requirements.txt`
3.  Download data (see `Source` section above)
4.  Run the notebook in `/notebooks`.
