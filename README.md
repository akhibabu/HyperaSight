# HyperaSight
# HyperaSight — AI-Powered Hypertension Risk Stratification

## Overview

HyperaSight is an AI-driven healthcare analytics platform designed to predict hypertension complication risk using patient-level clinical and insurance data. The system combines machine learning, explainable AI, and digital twin simulation to support proactive healthcare decision-making.

The platform identifies high-risk patients, explains prediction drivers, and simulates future outcomes under adherence and non-adherence scenarios.

---

## Features

* Hypertension complication risk prediction
* Risk tier classification (Low, Moderate, High, Critical)
* SHAP-based explainable AI insights
* Digital twin simulation (3-year projection)
* Cost impact analysis
* Interactive Gradio web interface
* Population-level analytics

---

## Dataset

The dataset contains structured healthcare insurance data including:

* Age
* Gender
* Medication adherence
* Systolic BP
* Diastolic BP
* Annual contribution
* Annual claim amount
* Healthcare units consumed
* Scheme type
* Comorbidity status
* Complication development

Filtered hypertensive population: 19,279 patients

---

## Machine Learning Model

Algorithm used:

* Random Forest Classifier

Training setup:

* 80/20 train-test split
* Class imbalance handled using class weights
* 12 feature inputs

Performance:

* Accuracy: 93.87%
* AUC-ROC: 0.855

---

## Risk Tier Classification

Predicted probability mapped into tiers:

* Low: < 0.35
* Moderate: 0.35 – 0.40
* High: 0.40 – 0.50
* Critical: ≥ 0.50

---

## Digital Twin Simulation

The digital twin module simulates patient risk and cost evolution:

Non-Adherent Scenario

* Risk increases by 8% per year
* Cost increases by 15% per year

Adherent Scenario

* Risk decreases by 5% per year
* Cost increases by 5% per year

Simulation horizon: 3 years

---

## Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* SHAP
* Matplotlib
* Seaborn
* Gradio
* Joblib
* Google Colab

---

## Project Structure

```
HyperaSight/
│
├── dataset/
│   └── HyperaSight_BP_Enhanced_Dataset.xlsx
│
├── model/
│   └── hypera_model.pkl
│
├── notebooks/
│   └── hyperasight_training.ipynb
│
├── app/
│   └── gradio_app.py
│
├── report/
│   └── HyperaSight_Project_Report.docx
│
└── README.md
```

---

## How to Run

### Install dependencies

```
pip install pandas numpy scikit-learn shap gradio matplotlib seaborn joblib
```

### Run the application

```
python gradio_app.py
```

The Gradio interface will open in the browser.

---

## Input Parameters

* Age
* Systolic BP
* Diastolic BP
* Adherence status
* Units consumed
* Annual claim amount

---

## Output

* Complication probability
* Risk tier classification
* SHAP feature explanation
* 3-year risk projection graph
* Cost trajectory simulation

---

## Applications

* Insurance risk management
* Preventive healthcare analytics
* Clinical decision support
* Population health monitoring
* Medication adherence intervention planning

---

## Future Improvements

* Real-time EHR integration
* Deep learning models
* Multi-disease prediction
* Cloud deployment
* API-based prediction service
* Dashboard analytics

---

## Authors

BCSE335L – Healthcare Data Analytics
School of Computer Science and Engineering
VIT Chennai

April 2026
