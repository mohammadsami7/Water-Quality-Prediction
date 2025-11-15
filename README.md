# Water Quality Prediction using Machine Learning
🌊 Water Quality Prediction Using Machine Learning

This project predicts whether a water sample is safe or unsafe for drinking using various chemical and biological parameters. Multiple supervised machine learning models were trained and evaluated to automate water quality assessment.
This work is part of an internship project aligned with modern AI-based environmental monitoring.

📌 Overview
Industrialization, urban development, and agricultural activities have contributed to large-scale freshwater contamination. Traditional lab-based water testing is slow and expensive.
This project automates water safety classification using machine learning. The model uses various contaminants such as:

Arsenic
Ammonia
Aluminium
Barium
Cadmium
Chromium
Copper
Fluoride
Lead
Mercury
Bacteria
Viruses
Uranium
…and many more.

After experimentation, Random Forest achieved the best accuracy.

📚 Dataset
Source: Kaggle (Water Potability Dataset)
Type: Chemical + biological contaminant features
Target column:
is_safe → 1 (Safe), 0 (Unsafe)
Key Parameters Used:
Aluminium, Ammonia, Arsenic, Barium, Cadmium, Chromium, Copper, Fluoride, Lead, Mercury, Nitrates, Bacteria, Viruses, Perchlorate, Radium, Selenium, Silver, Uranium.

Derived Feature
trace_material = bacteria + viruses

🛠️ Methodology
**1.Data Preprocessing:**
✔ Removed invalid values (#NUM!)
✔ Converted object → numeric types
✔ Balanced dataset using SMOTE
✔ Scaled features using StandardScaler
✔ Added new feature: trace_material
✔ 80/20 stratified train–test split

**2. Exploratory Data Analysis (EDA):**
Class distribution (count plot + pie chart)
Correlation heatmap
Contaminant distribution plots
Identified class imbalance (unsafe: 88.56%, safe: 11.4%)

**3.Models Implemented:**

1.Logistic Regression
2.K-Nearest Neighbors (KNN)
3.Decision Tree
4.Random Forest
5.Support Vector Machine (SVM)
6.XGBoost
Hyperparameter tuning was applied to optimize each model.

**4.Model Evaluation:**
Metrics Used:

Accuracy
Precision
Recall
F1-Score
ROC-AUC

Confusion Matrix
10-Fold Stratified Cross-Validation

**🔥Best Performing Model:**
Model	Accuracy
Random Forest	95%
XGBoost	92%
Others	Lower

**🧰 Tech Stack:**

Python
Pandas
NumPy
Matplotlib / Seaborn / Plotly
Scikit-learn
XGBoost
Imbalanced-learn (SMOTE)
Jupyter Notebook / VS Code
