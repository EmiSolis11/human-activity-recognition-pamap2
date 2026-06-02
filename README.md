# Human Activity Recognition using PAMAP2

Human Activity Recognition (HAR) system developed in Python using wearable sensor data from the PAMAP2 dataset.

The project implements a complete Machine Learning pipeline including:

- Data cleaning and preprocessing
- Sensor data fusion
- Missing value handling
- Feature extraction from time windows
- Feature selection and dimensionality reduction
- Leave-One-Subject-Out (LOSO) validation
- Multiple classification models
- Ensemble learning techniques

## Project Overview

The goal of this project is to automatically recognize physical activities performed by a person using data collected from wearable sensors.

Activities include:

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

The system uses inertial and cardiovascular sensor data from the PAMAP2 Physical Activity Monitoring dataset.

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

## Dataset

Dataset used:

PAMAP2 Physical Activity Monitoring Dataset

Sensors:

- Wrist IMU
- Chest IMU
- Ankle IMU
- Heart Rate Monitor

Original dataset size:

- 2.8+ million samples
- 54 sensor attributes
- 9 subjects

---

## Data Processing Pipeline

### 1. Data Cleaning

- Subject identification
- Removal of transition activities
- Quaternion removal
- Missing value interpolation
- Heart rate validation

### 2. Exploratory Data Analysis

- Histograms
- KDE distributions
- Correlation matrices
- Scatter matrices
- Class distribution analysis

### 3. Feature Engineering

Window segmentation:

- 3-second windows
- 300 samples per window
- 90% purity filter

Extracted features:

- Mean
- Standard deviation
- Maximum value
- Correlation between axes
- Signal magnitude
- AUC
- Magnitude variation

Final feature dataset:

- 6,396 activity windows
- 208 engineered features

---

## Machine Learning Models

Models evaluated:

- Logistic Regression
- Perceptron
- Random Forest

Dimensionality Reduction:

- PCA
- Kernel PCA
- SelectKBest Feature Selection

Validation Strategy:

- Leave-One-Subject-Out (LOSO)

---

## Results

| Model | Accuracy |
|---------|---------|
| Logistic Regression + Feature Selection | 84.49% |
| Perceptron + Feature Selection | 85.31% |
| Random Forest | 89.34% |
| Random Forest + Feature Selection | **89.43%** |

Best model:

**Random Forest + Feature Selection**

Accuracy:

**89.43% ± 4.66%**

---

## Ensemble Learning

Methods evaluated:

- Bagging (Random Forest)
- Soft Voting
- AdaBoost

Best ensemble:

**Bagging Random Forest**

Accuracy:

**90.19%**

F1-score:

**0.9061**

---

## Key Findings

- LOSO validation provides realistic generalization to unseen subjects.
- Feature Selection improved model stability.
- PCA reduced performance significantly.
- Random Forest consistently outperformed linear models.
- Ensemble methods provided marginal gains over the best standalone classifier.

---

## Repository Structure

```text
project/
│
├── data/
├── notebooks/
├── src/
│   ├── preprocessing.py
│   ├── feature_extraction.py
│   ├── models.py
│   └── evaluation.py
│
├── results/
│   ├── figures/
│   ├── confusion_matrix/
│   └── reports/
│
├── README.md
└── requirements.txt
