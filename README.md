# Non-Invasive Machine Learning Biomarker Discovery Pipeline for Renal Fibrosis

> *“See inside the kidney — without ever touching it.”*  
> A data-driven pipeline integrating machine learning, bioinformatics, and clinical insights to predict renal fibrosis severity non-invasively.

---

## Project Overview

Kidney fibrosis — the scarring process that drives chronic kidney disease — is typically diagnosed via **biopsy**, which is invasive and risky.  
Our project builds a **non-invasive biomarker discovery pipeline** that predicts fibrosis severity using *clinical data* and *plasma biomarkers*, benchmarked against pathology-derived ground truth.

** Key Discovery:**  
> Blood-based biomarkers predicted fibrosis **almost as accurately as biopsy reports** — demonstrating the potential of replacing invasive procedures with simple blood tests.

**Goal:** Develop an explainable ML model that approximates biopsy-level insights using only blood and clinical data.

---

## Workflow Summary

| Step | Description |
|------|--------------|
| **1️. Data Integration** | Merged clinical, plasma, and pathology data from the [Kidney Precision Medicine Project (KPMP)](https://atlas.kpmp.org/). |
| **2️. Data Cleaning** | KNN & regression imputation for missing values, feature normalization, and variance reduction. |
| **3️. Feature Engineering** | Converted fibrosis % into binary classes — *Mild/Moderate (≤15%)* vs *Advanced/Severe (>15%)*. |
| **4️. Model Training** | Built interpretable models using **Random Forest** and **XGBoost**. |
| **5️. Explainability (SHAP)** | Identified top predictive biomarkers and their influence on model predictions. |
| **6️. Pathway Enrichment (GSEApy)** | Mapped biomarkers to Reactome & KEGG pathways for biological validation. |

---

## Key Results

| Model | Type | Accuracy | AUROC |
|--------|-------|-----------|--------|
| Random Forest | Invasive (clinical + biomarker + pathology) | **0.866** | **0.89** |
| XGBoost | Invasive | **0.885** | **0.91** |
| Random Forest | Non-Invasive (clinical + biomarker only) | **0.824** | **0.85** |
| XGBoost | Non-Invasive | **0.841** | **0.87** |

 **Result:**  
>  Blood biomarkers alone achieved nearly the same accuracy as biopsy-based models — a major step toward *non-invasive kidney disease monitoring.*

---

## Top Biomarkers Identified (via SHAP)

| Biomarker | Role in Fibrosis |
|------------|----------------|
| **TNF-RII** | Inflammatory signaling and immune activation |
| **IL-6** | Cytokine driving inflammation and fibrosis |
| **KIM-1** | Marker of tubular injury and repair |
| **NGAL** | Reflects tubular stress and injury |
| **VEGF-D** | Involved in angiogenesis and vascular remodeling |
| **YKL-40 (CHI3L1)** | Linked to ECM remodeling and tissue repair |

---

##  Biological Insights

**Pathway Enrichment (Reactome / KEGG):**
- TNF signaling & cytokine–cytokine receptor interactions   
- Extracellular matrix organization & collagen remodeling   
- Angiogenesis & vascular repair pathways  

*Blood biomarkers reflect the same biological processes seen in kidney tissue — confirming that our model captures real biological signals, not just statistical correlations.*

---

## Technologies Used
- **Python**: `pandas`, `numpy`, `scikit-learn`, `xgboost`, `shap`, `gseapy`
- **Google Colab**
- **Reactome & KEGG** Databases
- **KPMP Atlas** datasets

---


---

## Team: *Kidney Tissue Atlas*

| Name | Program | Email |
|------|----------|--------|
| **Meghana Kusuru** | MS, Bioinformatics & Computational Biology | meghanak@udel.edu |
| **Sravya Buddha** | MS, Data Science | sravya@udel.edu |
| **Vinit Raju D** | MS, Data Science | dvinit@udel.edu |
| **Zainab Butul** | MS, Bioinformatics & Computational Biology | butul@udel.edu |
| **Aaron Onserioa** | MS, Bioinformatics Data Science | onserioa@udel.edu |

---

## Conclusion & Impact

This project shows that **blood biomarkers can mirror biopsy-level insights**, achieving nearly the same accuracy as invasive methods.  
By merging **machine learning, explainable AI, and biological validation**, we demonstrated that fibrosis severity can be predicted non-invasively — paving the way for **safer, faster, and more accessible kidney care**.

> **In short:** Our study proves that what’s in the blood can tell the same story as what’s in the biopsy.

---

##  License
This project is released under the [MIT License](LICENSE).

---

 **If you found this project inspiring, give it a star on GitHub!**


