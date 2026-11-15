# Seismic Safety ML Project

Machine learning project that predicts seismic hazard (Danger / No Danger) in coal mines using Logistic Regression and Random Forest.

Asansol Engineering College

## Problem
Coal mines face sudden tremors called seismic bumps. They put workers at risk and can stop production. This project uses seismic sensor readings to predict whether a shift is dangerous.

## Dataset
- File: seismic-bumps.csv
- 2,584 records, 19 columns, no missing values
- Target column class: 0 = No Danger (2,414), 1 = Danger (170)
- The data is imbalanced: only about 6.6% of records are Danger

## Steps
1. Data analysis: class distribution, histograms, scatter plot, correlation heatmap
2. Dropped nbumps6, nbumps7 and nbumps89 (always 0)
3. Encoded the categorical columns: seismic, seismoacoustic, shift, hazard
4. Stratified 80/20 train-test split and StandardScaler
5. SMOTE applied to the training data only
6. Trained both models and evaluated them on the test set

## Models and Results

| Metric | Logistic Regression | Random Forest |
|---|---|---|
| Accuracy | 0.7756 | 0.8975 |
| Precision | 0.1694 | 0.2564 |
| Recall | 0.6176 | 0.2941 |
| F1-Score | 0.2658 | 0.2739 |
| ROC-AUC | 0.7791 | 0.7031 |

## Conclusion
Random Forest has the best accuracy, precision and F1-score. Logistic Regression has the best recall and ROC-AUC, so it catches more real Danger cases. Because the data is imbalanced, accuracy alone is not enough, and recall matters most for mine safety.

## Future Scope
- Hyperparameter tuning and models like XGBoost, SVM and neural networks
- Class weights and threshold tuning
- Real-time sensor data for live alerts and a safety dashboard

## How to Run
1. Open the notebook in Google Colab
2. Upload the dataset file
3. Run all cells

Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, imbalanced-learn

## Team
- Pratima Maji
- Rounak Dutta
- Rudra Pratap Maji
- Soha Acharjee
