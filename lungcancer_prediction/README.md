# 🏥 Lung Cancer Prediction System

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3.0-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

A comprehensive machine learning system for predicting lung cancer risk based on patient characteristics and symptoms. This project implements and compares multiple ML models with thorough EDA and hyperparameter optimization.


## 📊 Project Overview

This project aims to build an accurate lung cancer prediction system using machine learning algorithms. The system analyzes patient data including demographics, lifestyle factors, and symptoms to assess lung cancer risk.

### Key Features
- ✅ Comprehensive Exploratory Data Analysis (EDA)
- ✅ Multiple ML Models (SVM, KNN, Random Forest)
- ✅ Hyperparameter Optimization (RandomizedSearchCV)
- ✅ Feature Importance Analysis
- ✅ Model Performance Comparison
- ✅ Production-Ready Model Deployment

## 📁 Dataset

The dataset used is `lung cancer.csv`, which contains patient information and symptoms.

### Features Description

| Feature | Type | Description |
|---------|------|-------------|
| **GENDER** | Categorical | Male/Female |
| **AGE** | Numerical | Patient's age in years |
| **SMOKING** | Binary | 1 = Smoker, 0 = Non-smoker |
| **YELLOW_FINGERS** | Binary | Presence of yellow fingers |
| **ANXIETY** | Binary | Anxiety symptoms |
| **PEER_PRESSURE** | Binary | Peer pressure influence |
| **CHRONIC DISEASE** | Binary | Chronic disease history |
| **FATIGUE** | Binary | Fatigue symptoms |
| **ALLERGY** | Binary | Allergy history |
| **WHEEZING** | Binary | Wheezing symptoms |
| **ALCOHOL CONSUMING** | Binary | Alcohol consumption |
| **COUGHING** | Binary | Coughing symptoms |
| **SHORTNESS OF BREATH** | Binary | Difficulty breathing |
| **SWALLOWING DIFFICULTY** | Binary | Swallowing problems |
| **CHEST PAIN** | Binary | Chest pain symptoms |
| **LUNG_CANCER** | Target | Yes/No (Target Variable) |

### Dataset Statistics
- **Total Samples**: 309 (after removing duplicates)
- **Features**: 15
- **Target Distribution**: 
  - Cancer Cases: ~85%
  - No Cancer: ~15%

## 🔍 Exploratory Data Analysis

### Key Insights from EDA

1. **Age Distribution**
   - Range: 18-90 years
   - Mean age: ~60 years
   - Most patients are in the 50-70 age range

2. **Gender Distribution**
   - Male: ~70%
   - Female: ~30%

3. **Smoking & Cancer Correlation**
   - Strong positive correlation between smoking and lung cancer
   - ~85% of smokers are diagnosed with lung cancer

4. **Feature Correlations**
   - Highest correlation: Smoking, Yellow Fingers, and Anxiety
   - Multiple symptoms show strong inter-correlation

### Visualizations
- 🔹 Age distribution histogram
- 🔹 Gender pie chart
- 🔹 Smoking vs Cancer count plot
- 🔹 Feature correlation heatmap
- 🔹 Symptom distribution plots
- 🔹 Boxplots for outlier detection

## 🤖 Models Implemented

### 1. Support Vector Classifier (SVC)

**Description**: A supervised learning model that finds the optimal hyperplane for classification.

###  2. K-Nearest Neighbors (KNN)
**Description**: Classifies data points based on the majority class of their k-nearest neighbors.

### 3. Random Forest Classifier ⭐ (Best Model)
**Description**: An ensemble learning method that constructs multiple decision trees and merges their predictions.


### 📊 Model Comparison
Model	Accuracy	Recall	Precision	F1-Score
Random Forest	92.5%	96.8%	97.5%	97.1%
SVC	89.2%	94.1%	95.8%	94.9%
KNN	88.9%	93.2%	95.3%	93.8%
🔑 Feature Importance (Top 10)
Based on Random Forest model:

Rank	Feature	Importance Score
1	SMOKING	0.187
2	YELLOW_FINGERS	0.165
3	ANXIETY	0.143
4	PEER_PRESSURE	0.112
5	CHRONIC DISEASE	0.098

