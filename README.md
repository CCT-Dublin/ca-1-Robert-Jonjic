# Predicting EU Housing Prices (Q3 2024) with Machine Learning
**Author · Robert Jonjic – CCT College Dublin**

> Capstone Assessment 3 (CA3) – Strategic Thinking module  
> Date of submission: 14 May 2025  

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Key Results](#key-results)  
3. [Repository Structure](#repository-structure)  
4. [Setup & Reproducibility](#setup--reproducibility)

---

## Project Overview

This project delivers a **supervised machine-learning pipeline** that forecasts **Q3 2024 housing-price indices** for 310 NUTS-level regions across the European Union.  
By blending **macroeconomic indicators**, **demographic factors**, and **recent quarterly price momentum**, the best model achieves near-perfect predictive accuracy (**R² ≈ 0.997**) while remaining interpretable for policy and investment decisions.

### Objectives

| ID | Goal | Success Metric |
|----|------|----------------|
| **O1** | High predictive power | Test-set R² ≥ 0.95 |
| **O2** | Transparent drivers | Rank ≥ 3 key features |
| **O3** | Reproducible code | One-click notebook run |

---

## Key Results

| Model | R² | RMSE | MAE |
|-------|----|------|-----|
| **K-Nearest Neighbours** | **0.9970** | 2.05 | 1.02 |
| Support Vector Regression (RBF) | 0.9932 | 3.11 | 2.36 |
| Random Forest | 0.9880 | 4.12 | 1.67 |
| Gradient Boosting | 0.9811 | 5.18 | 2.34 |
| XGBoost | 0.9759 | 5.85 | 2.32 |
| Linear Regression | 0.9551 | 7.98 | 3.41 |

**Top predictive drivers**

1. Average Income  
2. Housing-price index in **Q2 2024**  
3. Urbanisation Rate  
4. GDP × Urbanisation interaction  

---

## Repository Structure

├── CA3_Final.ipynb # End-to-end Jupyter Notebook
├── EU_Data.csv # Cleaned Eurostat dataset (310 × 29)
├── CA 3 Final Submission.docx # 5 000-word academic report
├── README.md

> *Large raw Eurostat extracts are not included; see “Data Description” for download links.*

---

## Setup & Reproducibility

```bash
# 1 Clone
git clone https://github.com/CCT-Dublin/ca-1-Robert-Jonjic.git
cd ca-1-Robent-Jonjic

# 2 Create and activate environment (Python ≥ 3.9)
python -m venv venv
# macOS / Linux
source venv/bin/activate
# Windows
venv\Scripts\activate

# 3 Install core dependencies
pip install -r requirements.txt

# 4 Launch Jupyter
jupyter notebook    # open CA3_Final.ipynb
# In your browser, open CA3_Final.ipynb and run all cells sequentially.

## Citation
Jonjic, R. (2025) Predicting EU Housing Prices with Machine Learning, CCT College Dublin, Capstone Project.