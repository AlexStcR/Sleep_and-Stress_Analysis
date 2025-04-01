# Sleep_and-Stress_Analysis
Occupational Impact on Sleep and Stress: A Health Insights Report

# Occupational Impact on Sleep and Stress Analysis

![Health Data Analysis](https://img.shields.io/badge/analysis-health%20metrics-blue) 
![Python](https://img.shields.io/badge/language-Python-green)

An exploratory data analysis examining relationships between occupation, sleep quality, stress levels, and blood pressure metrics.

## 📋 Project Overview
- **Objective**: Analyze how different professions affect health indicators
- **Dataset**: Sleep Health and Lifestyle Dataset (374 records, 13 features)
- **Key Metrics**: Sleep duration, stress levels, BMI, blood pressure, physical activity

## 🛠️ Tools Used
| Category        | Tools                          |
|-----------------|--------------------------------|
| Programming     | Python 3, Jupyter Notebook     |
| Data Processing | Pandas, NumPy                 |
| Visualization   | Matplotlib, Seaborn           |
| Version Control | Git, GitHub                   |

## 🔍 Step-by-Step Analysis

### 1. Data Preparation
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np

# Load dataset
df = pd.read_csv('Sleep_health_and_lifestyle_dataset.csv')
```

### 2. Data Cleaning
- Handled missing values in 'Sleep Disorder' column (replaced with 'None')

- Standardized BMI categories (merged 'Normal' and 'Normal Weight')

- Split 'Blood Pressure' into separate systolic/diastolic columns:
```python
df[['Systolic','Diastolic']] = df['Blood Pressure'].str.split('/', expand=True).astype(float)
```
### 3. Exploratory Analysis
  **Demographic Overview:**
   
-Age distribution (mean: 42.2 ± 8.7 years)

-Gender balance (50.5% male, 49.5% female)

-Occupation distribution (Top 3: Nurses, Doctors, Engineers)

**Health Metrics:**
```python
# Key statistics
df[['Sleep Duration','Quality of Sleep','Stress Level']].describe()
```
### 4. Visualization
**Generated plots for:**

-Occupation distribution by health metrics

-Stress levels across professions

-Blood pressure distribution

-Sleep disorder prevalence

### 5. Key Findings
**Sleep Patterns:**

-Avg. sleep duration: 7.1 ± 0.8 hours

-58.6% had no sleep disorders

**Stress Levels:**

-Highest in legal/education professions

-Strong correlation with sleep quality (r = -0.72)

**Blood Pressure:**

-28.9% of nurses had systolic pressure ≥130mmHg

-Significant occupation-based differences (p < 0.05)

## 📚 References
Pandas Documentation

Seaborn Visualization Guide

American Heart Association Blood Pressure Guidelines

## 🚀 How to Reproduce
Clone repository

Install requirements: pip install -r requirements.txt

Run Jupyter notebook: jupyter notebook notebooks/Analysis.ipynb




