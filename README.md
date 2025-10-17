# 🧠 Pancreatic Cancer Prognosis Using Clinical Data

This repository contains a machine learning mini-project focused on predicting **pancreatic cancer prognosis** using **clinical data**.  
The goal is to analyze patient survival outcomes through **risk stratification** and **survival prediction** using statistical and ML models such as **Naive Bayes** and the **Cox Proportional Hazards (CoxPH)** model.

---

## 📘 Project Overview

Pancreatic cancer has one of the lowest survival rates among all cancers. Early identification of high-risk patients can significantly improve treatment planning and clinical decision-making.

This project demonstrates:
- How to preprocess and analyze clinical datasets for survival modeling  
- How to predict short-term prognosis categories (e.g., high vs. low risk) using **Naive Bayes classification**  
- How to perform **survival analysis** using the **Cox Proportional Hazards model**  
- Visualization of Kaplan–Meier survival curves to interpret model performance  

---

## 📂 Project Structure
<img width="703" height="559" alt="image" src="https://github.com/user-attachments/assets/61ce42e4-c06f-447a-8f08-6c5e4c71d88c" />
---

## 🧩 Methodology

### Step 1: Data Preprocessing
- Load and clean clinical data (missing value handling, encoding categorical variables)
- Split data into training and validation sets
- Perform normalization and transformation where necessary

### Step 2: Naive Bayes Classification
- Used to classify patients into **high-risk** and **low-risk** groups
- Threshold sweep performed to optimize classification balance accuracy
- Outputs include confusion matrices and threshold–accuracy plots

### Step 3: Cox Proportional Hazards Model
- Utilizes survival times and censoring information
- Estimates the **hazard ratio** associated with clinical variables
- Helps interpret **time-dependent survival probability**
- Visualized through **Kaplan–Meier survival curves**

---

## ⚙️ Installation

Clone this repository and install dependencies:

```bash
git clone https://github.com/yourusername/ml-mini-project.git
cd ml-mini-project
pip install -r requirements.txt
```


## 🚀 Usage

### Running the Jupyter Notebook

To explore the full workflow and reproduce results:

```bash
jupyter notebook pancreatic_cancer_prognosis_using_cilinical_data.ipynb
```

## 📈 Results Summary

### 🔹 Step 2 — Naive Bayes Classification
**Objective:**  
Classify patients into **High-Risk** and **Low-Risk** prognosis categories based on clinical variables.

**Key Outputs:**
- `nb_threshold_sweep_balacc.png` — Balanced accuracy vs. threshold visualization  
- `nb_threshold_sweep_results.csv` — Summary of performance metrics for various thresholds  
- `nb_predictions_best_threshold.csv` — Predictions at the optimal threshold  
- `step2_summary.txt` — Model evaluation and findings  

**Findings:**  
The Naive Bayes model effectively separated patients into risk categories.  
Threshold tuning improved balanced accuracy, showing stable performance across validation data.  
It served as a reliable baseline classifier before survival modeling.

---

### 🔹 Step 3 — Cox Proportional Hazards Model
**Objective:**  
Estimate **hazard ratios** and **time-dependent survival probabilities** to understand which clinical features most influence patient survival.

**Key Outputs:**
- `coxph_clinical_summary.csv` — Detailed regression coefficients and p-values  
- `step3_cox_report.txt` — Complete model summary and diagnostics  
- `km_clinical_median_risk.png` — Kaplan–Meier survival plot for risk groups  

**Findings:**  
The Cox model successfully identified key prognostic factors that significantly affected survival outcomes.  
Kaplan–Meier analysis revealed distinct survival distributions between high- and low-risk groups, confirming the effectiveness of prior classification.  
The proportional hazards assumption was found to hold for most variables.

---

### 🔹 Overall Outcome
Combining **Naive Bayes** classification and **CoxPH survival analysis** provided a comprehensive approach to prognosis prediction:
- Naive Bayes simplified early risk classification.  
- CoxPH offered interpretable survival insights with statistical rigor.  
- Together, they enhanced the reliability and interpretability of pancreatic cancer prognosis modeling.

---

### 🏁 Visual Summary
| Model | Key Metric | Output File | Description |
|--------|-------------|--------------|--------------|
| Naive Bayes | Balanced Accuracy | `nb_threshold_sweep_balacc.png` | Visualizes performance improvement by threshold tuning |
| CoxPH | Hazard Ratios, p-values | `coxph_clinical_summary.csv` | Identifies significant clinical predictors |
| Kaplan–Meier | Survival Curves | `km_clinical_median_risk.png` | Shows survival differences between risk groups |

---

✅ **Conclusion:**  
The project demonstrates how integrating classification and survival analysis techniques enables effective and interpretable prediction of patient outcomes using clinical data.





