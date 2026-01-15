# Assignment 3 – Data Analytics (BI 2025)

## Overview
This repository contains the implementation and documentation for **Assignment 3: Data Analytics** of the course **188.429 Business Intelligence (WS 2025)** at TU Wien.  
The project follows a subset of the **CRISP-DM** methodology and focuses on predicting house prices using the **King County House Sales** dataset.

The work emphasizes **reproducible data analytics**, **ethical considerations**, and **provenance-aware experimentation**, with all experiments conducted in a Jupyter Notebook environment.

---

## Authors
- **Soroush Naseri** (Student A, Group 26)  
  Matriculation No.: 12448457  
- **Amir Saadati** (Student B, Group 26)  
  Matriculation No.: 12434679  

Location: Vienna, Austria

---

## Dataset
- **Name:** King County House Sales Dataset  
- **Source:** Kaggle  
- **Scope:** Residential property sales in King County, WA, USA (2014–2015)  
- **Size:** 21,613 instances, 21 attributes  
- **Target Variable:** `price` (USD)

The dataset includes structural, locational, and quality-related features such as living area, number of rooms, grade, view, waterfront, and geographic coordinates.

---

## Methodology
The project follows the **CRISP-DM** framework with focus on:

1. **Business Understanding**  
   - Definition of business objectives and success criteria  
   - Identification of AI risks and ethical concerns  

2. **Data Understanding**  
   - Attribute semantics and data quality analysis  
   - Outlier, skewness, and correlation analysis  
   - Ethical sensitivity and bias assessment  

3. **Data Preparation**  
   - Removal of implausible records (e.g., zero bathrooms, extreme bedroom outlier)  
   - Feature engineering (e.g., total square footage, house age, bed–bath ratio)  
   - Log transformation of skewed variables  
   - Group-aware train/test split by zipcode to prevent leakage  

4. **Modeling**  
   - Supervised regression approaches  
   - Models used:
     - Random Forest Regressor
     - Neural Network (MLPRegressor)
   - Extensive hyperparameter tuning using Grid Search  
   - Evaluation using RMSE, MAE, MSE, and R²  

5. **Evaluation & Deployment Considerations**  
   - Model robustness considered acceptable for this project phase  
   - Discussion of ethical risks, monitoring plans, and EU AI Act relevance  

---

## Key Results
- Best-performing model: **Neural Network**
- Achieved performance:
  - R² ≈ 0.34 on validation set
  - Stable convergence and acceptable generalization
- Most influential features:
  - Living area
  - Property grade
  - Location-related features
  - Waterfront presence

---

## Ethical & Risk Considerations
- Potential **proxy bias** through location features (zipcode, latitude, longitude)
- Class imbalance for rare property types (e.g., waterfront homes)
- Limited temporal coverage (2014–2015)
- Reduced interpretability of black-box models

Mitigation strategies and monitoring plans are discussed in the report.

---

## Reproducibility
The project supports reproducibility through:
- Clear documentation of data sources and preprocessing steps
- Explicit modeling and evaluation workflow
- Provenance-aware logging using standard ontologies

Limitations include missing library version pinning and uncontrolled random seeds.

---

## Repository Structure (Expected)
