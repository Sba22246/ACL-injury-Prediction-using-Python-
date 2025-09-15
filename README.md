# ACL-injury-Prediction-using-Python-
Thesis for Msc in DAta analytics . Data from Football manager 2017 and other websites . 
⚽ Soccer Injury Prediction Project


"Predicting ACL Injury Risk in Soccer Players Using Machine Learning"

📌 Overview

This project predicts ACL injuries in professional soccer players using machine learning. It analyzes the impact of player attributes, club characteristics, and position on injury risk. Models include:

Random Forest (RF)

Decision Tree (DT)

K-Nearest Neighbors (KNN)

Key analyses:

Model training & evaluation

Precision-Recall and ROC curves

Confusion matrix analysis

Feature importance comparison

SHAP analysis for interpretability

📊 Dataset

The dataset contains:

Player demographics: age, height, weight

Player attributes: agility, stamina, natural fitness, etc.

Club characteristics: club_value, club_country

Player positions & foot: role_Defender, foot_right

Target variable: ACL injury (0 = No injury, 1 = ACL injury)

Preprocessing steps:

Handling missing values

SMOTE oversampling for class imbalance

Train-test split

🧰 Models & Performance
Random Forest (RF)
<img width="1409" height="845" alt="image" src="https://github.com/user-attachments/assets/ae749ef9-43b1-47f2-bb62-2719c403af29" />


Recall: 0.17

Precision: 0.06

ROC-AUC: 0.56

Decision Tree (DT)

Recall: 0.17

Precision: 0.11

ROC-AUC: 0.58

K-Nearest Neighbors (KNN)

High accuracy on training (98%), low minority class performance pre-SMOTE

ROC-AUC: 0.5 (imbalanced test set)

Feature importance approximated via distance metrics

📈 Evaluation

Confusion Matrix Example:

ROC Curve:

Precision-Recall Curve:

SMOTE improved minority class predictions during training, highlighting the importance of handling imbalanced data.

🔍 Feature Importance & Interpretation
Feature	RF Importance	DT Importance	KNN Importance
club_value	0.10	0.18	0.10
age	0.10	0.11	0.10
role_Defender	0.09	0.12	0.09
weight	0.04	0.02	0.04

SHAP Summary Plot:

Key insights:

club_value and age have the highest influence

Physical characteristics (height, weight) moderately impact prediction

Player position & foot are lower but non-negligible contributors

🚀 Usage

Install dependencies:

pip install -r requirements.txt


Run the Jupyter Notebook:

jupyter notebook


Explore analyses in soccer_injury_analysis.ipynb.

🌟 Future Improvements

Implement Bayesian optimization for hyperparameter tuning

Explore ensemble models for better minority class performance

Incorporate additional features like training load or match minutes

Compare KNN with XGBoost or LightGBM

👤 Author

Thomas Lennon
