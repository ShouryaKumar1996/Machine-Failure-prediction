# Machine-Failure-prediction

Machine Failure Prediction (ML Project) for TATA

🚀 Project Snapshot

Built a predictive maintenance model to identify machine failures in advance for Tata Steel–like industrial operations, helping reduce downtime, cost, and safety risks.

📊 Dataset: 136K+ training records
🎯 Problem: Binary classification (Failure vs No Failure)
⚠️ Challenge: Highly imbalanced data (~1.57% failures)
🏆 Best Model: XGBoost (ROC-AUC ~0.9366)
🎚️ Optimized Threshold: 0.40 (Recall ~81%)
💼 Business Impact

This solution enables:

🔻 Reduction in unplanned downtime
💰 Lower maintenance & repair costs
⚙️ Improved maintenance scheduling
📈 Higher Overall Equipment Effectiveness (OEE)
🦺 Enhanced plant safety

💡 Even preventing one critical failure/month can save lakhs in losses.

🧠 Key Contributions
Designed a complete ML pipeline from EDA → feature engineering → modeling → evaluation
Tackled class imbalance using threshold tuning and scale_pos_weight
Engineered domain-specific features to capture machine stress patterns
Applied SHAP for model explainability (critical for industrial trust)
Focused on recall optimization to minimize missed failures

📊 Model Performance
Model	ROC-AUC	Recall	Precision
Logistic Regression	0.87	High	Very Low
Random Forest	0.91	Medium	Medium
⭐ XGBoost	0.915 → 0.9366 (tuned)	High (~81%)	Balanced

⚙️ Approach
1. Data Understanding & EDA
Missing values, duplicates
Feature distributions
Class imbalance visualization
Correlation and failure pattern analysis
Outlier detection (Z-score, IQR)
2. Feature Engineering

Created high-impact features:

temp_diff
torque_per_rpm
temp_ratio
temp_interaction
high_wear_flag
3. Preprocessing
StandardScaler (numerical features)
OneHotEncoder (categorical)
Stratified 80–20 train-validation split
4. Model Development
Logistic Regression
Random Forest
XGBoost (selected)
5. Hyperparameter Tuning

Used RandomizedSearchCV on:

max_depth, learning_rate
n_estimators
subsample, colsample_bytree
scale_pos_weight
6. Threshold Optimization
Evaluated thresholds from 0.10 to 0.90
Finalized at 0.40 to maximize recall

Industrial priority: Missing a failure > false alarm

🔍 Model Explainability

Using SHAP, identified top drivers:

Torque per RPM
Temperature difference
Tool wear
Process temperature
Machine type

✔ Improves model trust for real-world deployment

📂 Dataset Summary

Files:

train.csv (136,429 rows)
test.csv (90,954 rows)

Features include:

Temperature (air & process)
Rotational speed, torque
Tool wear
Machine type
Failure indicators (TWF, HDF, PWF, OSF, RNF)

📈 Final Output
Trained on full dataset
Predictions generated on test set
Output:
id
Machine failure

🛠️ Tech Stack
Python
Pandas, NumPy
Scikit-Learn
XGBoost
SHAP
Matplotlib, Seaborn
Google Colab

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-ML-orange"/>
  <img src="https://img.shields.io/badge/XGBoost-Boosting-red"/>
  <img src="https://img.shields.io/badge/Google%20Colab-Notebook-yellow"/>
</p>

🔮 Future Scope
Real-time sensor integration
Vibration & acoustic analytics
API deployment (FastAPI / Flask)
Live monitoring dashboards
Continuous retraining pipelines

👤 Built by

Shourya Kumar

🔗 LinkedIn: https://www.linkedin.com/in/shouryadata/
