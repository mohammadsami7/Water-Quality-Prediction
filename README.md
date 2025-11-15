# Water Quality Prediction using Machine Learning
🌊 Water Quality Prediction Using Machine Learning

This project predicts whether a water sample is safe or unsafe for drinking using various chemical and biological parameters. Multiple supervised machine learning models were trained and evaluated to automate water quality assessment.
This work is part of an internship project aligned with modern AI-based environmental monitoring.

📌 Overview:<br>
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

**📚Dataset:**<br>
Source: Kaggle (Water Potability Dataset)
Type: Chemical + biological contaminant features
Target column:
is_safe → 1 (Safe), 0 (Unsafe)
Key Parameters Used:
Aluminium, Ammonia, Arsenic, Barium, Cadmium, Chromium, Copper, Fluoride, Lead, Mercury, Nitrates, Bacteria, Viruses, Perchlorate, Radium, Selenium, Silver, Uranium.

Derived Feature
trace_material = bacteria + viruses

**🛠️Methodology:**<br>
**1.Data Preprocessing:**<br>
✔ Removed invalid values (#NUM!)<br>
✔ Converted object → numeric types<br>
✔ Balanced dataset using SMOTE<br>
✔ Scaled features using StandardScaler<br>
✔ Added new feature: trace_material<br>
✔ 80/20 stratified train–test split<br>

**2. Exploratory Data Analysis (EDA):**<br>
Class distribution (count plot + pie chart)
Correlation heatmap
Contaminant distribution plots
Identified class imbalance (unsafe: 88.56%, safe: 11.4%)

**3.Models Implemented:**<br>

1.Logistic Regression<br>
2.K-Nearest Neighbors (KNN)<br>
3.Decision Tree<br>
4.Random Forest<br>
5.Support Vector Machine (SVM)<br>
6.XGBoost<br>
Hyperparameter tuning was applied to optimize each model.<br>

**4.Model Evaluation:**<br>
Metrics Used:

Accuracy
Precision
Recall
F1-Score
ROC-AUC

Confusion Matrix
10-Fold Stratified Cross-Validation

**🔥Best Performing Model:**<br>
Model	Accuracy
Random Forest	95%
XGBoost	92%
Others	Lower

**🧰 Tech Stack:**<br>

Python
Pandas
NumPy 
Matplotlib / Seaborn / Plotly
Scikit-learn
XGBoost
Imbalanced-learn (SMOTE)
Jupyter Notebook / VS Code
