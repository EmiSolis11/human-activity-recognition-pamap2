# Human Activity Recognition using PAMAP2

Machine Learning pipeline for Human Activity Recognition (HAR) using wearable sensor data from the PAMAP2 dataset.

## Overview

This project develops and evaluates multiple machine learning models capable of recognizing human physical activities from wearable sensor data.

The pipeline includes:

- Data Cleaning
- Missing Value Handling
- Exploratory Data Analysis
- Feature Engineering
- Feature Selection
- Dimensionality Reduction
- Leave-One-Subject-Out Validation
- Ensemble Learning

---

## Dataset

PAMAP2 Physical Activity Monitoring Dataset

### Activities

- Lying
- Sitting
- Standing
- Walking
- Running
- Cycling
- Nordic Walking
- Ascending Stairs
- Descending Stairs
- Vacuum Cleaning
- Ironing
- Rope Jumping

### Sensors

- Wrist IMU
- Chest IMU
- Ankle IMU
- Heart Rate Monitor

---

## Project Pipeline

![Pipeline](images/pipeline.png)

---

## Feature Engineering

Sensor signals were segmented into fixed windows and transformed into statistical descriptors.

Extracted features include:

- Mean
- Standard Deviation
- Maximum Value
- Signal Magnitude
- Axis Correlations
- Area Under Curve (AUC)
- Magnitude Variation

Final dataset:

- 208 engineered features

---

## Validation Strategy

Leave-One-Subject-Out (LOSO)

This validation strategy evaluates model generalization on unseen subjects and provides a realistic estimate of real-world performance.

---

## Models Evaluated

- Logistic Regression
- Perceptron
- Random Forest
- Random Forest + Feature Selection
- PCA + Classifiers
- Kernel PCA + Classifiers
- AdaBoost
- Soft Voting
- Bagging Random Forest

---

## Results

| Model | Accuracy |
|---------|---------|
| Logistic Regression + Feature Selection | 84.49% |
| Perceptron + Feature Selection | 85.31% |
| Random Forest | 89.34% |
| Random Forest + Feature Selection | 89.43% |
| Bagging Random Forest | 90.19% |

Best model:

**Bagging Random Forest**

Accuracy:

**90.19%**

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- SciPy

---

## Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- Machine Learning
- Ensemble Learning
- Feature Selection
- Dimensionality Reduction
- Cross Validation
- Statistical Analysis

---

## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── notebooks
│   └── Human_Activity_Recognition_PAMAP2.ipynb
├── report
│   └── PAMAP2_eg15.pdf
└── images
    ├── pipeline.png
    ├── model_comparison.png
    └── confusion_matrix.png
```

---

## Author

Emiliano Solís Ek
Marco Magaña Mis

Computer Engineering Student

Universidad Autónoma de Yucatán
