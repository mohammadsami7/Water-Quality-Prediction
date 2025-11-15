# Water-Quality-Prediction
🌊 Water Quality Prediction Using Machine Learning

This project focuses on predicting whether a given water sample is safe or unsafe for drinking based on several chemical and biological parameters. The system uses multiple supervised machine learning models and evaluates their performance using various metrics.

The project is part of an internship work and aligns with modern approaches for automating environmental monitoring through AI.

📌 Overview

The increasing industrialization, urban expansion, and agricultural activities have led to contamination of global water sources. Traditional laboratory-based water quality testing is expensive and time-consuming.

This project aims to automate water safety classification using machine learning.
Several ML models were trained to predict water potability using contaminants like:

Arsenic

Ammonia

Aluminium

Barium

Cadmium

Chromium

Copper

Fluoride

Lead

Bacteria

Viruses

Uranium
...and many others.

After experimentation, Random Forest produced the highest prediction accuracy.

📚 Dataset

Source: Kaggle — Water Potability Dataset

Samples: Chemical + Biological contaminants

Target Feature:

is_safe → 1 (Safe), 0 (Unsafe)

Key Parameters

Aluminium

Ammonia

Arsenic

Barium

Cadmium

Chromium

Copper

Fluoride

Lead

Mercury

Nitrates

Bacteria

Viruses

Perchlorate

Radium

Selenium

Silver

Uranium

A derived feature:

trace_material = bacteria + viruses

🛠️ Methodology
1. Data Preprocessing

✔ Replaced invalid values (#NUM!)
✔ Converted object → numeric datatypes
✔ Balanced data using SMOTE
✔ Feature scaling using StandardScaler
✔ Added new feature (trace_material)
✔ Stratified train–test split (80/20)

2. Exploratory Data Analysis

Count plots and pie charts for class distribution

Correlation heatmap

Distribution analysis of contaminants

Identified class imbalance (unsafe: 88.56%, safe: 11.4%)

3. Models Implemented

The following classification algorithms were trained:

Logistic Regression

K-Nearest Neighbors (KNN)

Decision Tree

Random Forest

Support Vector Machine (SVM)

XGBoost

Each model was hyperparameter-tuned for improved performance.

4. Model Evaluation

Metrics used:

Accuracy

Precision

Recall

F1-Score

ROC-AUC

Confusion Matrix

10-Fold Stratified Cross-Validation

🔥 Best Performing Model
Model	Accuracy
Random Forest	95%
XGBoost	92%
Others	Lower performance

Random Forest performed best due to its ability to handle nonlinear relationships and high-dimensional data.

🧰 Tech Stack
Languages & Tools

Python

Pandas

NumPy

Matplotlib / Seaborn / Plotly

Scikit-learn

XGBoost

Imbalanced-learn (SMOTE)

Jupyter Notebook / VS Code


🧪 How to Run the Project
1. Clone the Repository
git clone https://github.com/your-username/water-quality-ml.git
cd water-quality-ml

2. Install Dependencies
pip install -r requirements.txt

3. Run the Notebook

Open Jupyter Notebook and run:

WaterQualityPrediction.ipynb


Or run script version:

python main.py
