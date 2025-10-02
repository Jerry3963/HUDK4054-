# Titanic Survival Analysis – ReadMe Metadata  
**HUDK4054 Individual Assignment #2: Write ReadMe Style Metadata**

---

## Project Information  
- **Title**: Titanic Survival Analysis  
- **Author**: Jerry Zhu (ORCID: 0009-0005-0476-3544)  
- **Instructor**: Prof. Yasemin Gulbahar Guven  
- **Affiliation**: Teachers College, Columbia University  
- **Date**: 2025-09-30  
- **Context**: HUDK4054 Course Assignment – Metadata & ReadMe  
- **Role**: Data Creator & Data Manager – Jerry Zhu  

---

## Project Abstract  
The Titanic disaster of 1912 provides one of the most widely studied datasets in data science education.  
The purpose of this project is to analyze survival patterns of Titanic passengers and investigate how demographic and socio-economic factors influenced survival.  

By using the Kaggle Titanic dataset, this study aims to:  
1. Explore survival rates across gender, passenger class, and age groups.  
2. Evaluate the predictive power of logistic regression in classifying survival outcomes.  
3. Demonstrate how metadata standards (DDI) can improve documentation of social science datasets.  

---

## Dataset Overview and Features  
- **Source**: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)  
- **File Type**: CSV  
- **Size**: 891 rows × 12 columns  
- **Collection**: Historical passenger data from Titanic disaster (1912)  

### Key Files  
- `train.csv` – Passenger demographic and survival data  
- `test.csv` – Passenger data without survival labels (for prediction)  

---

## Data Dictionary  

| Variable      | Description                           | Type     | Notes |  
|---------------|---------------------------------------|----------|-------|  
| PassengerId   | Unique passenger identifier           | Nominal  | Sequential integer |  
| Survived      | Survival indicator (0 = No, 1 = Yes) | Binary   | Outcome variable |  
| Pclass        | Ticket class (1, 2, 3)               | Ordinal  | Proxy for socio-economic status |  
| Name          | Full passenger name                  | String   | Includes titles (Mr., Mrs., etc.) |  
| Sex           | Gender                               | Nominal  | Male/Female |  
| Age           | Age in years                         | Interval | Missing values imputed by median |  
| SibSp         | # of siblings/spouses aboard         | Discrete | Ranges from 0 to 8 |  
| Parch         | # of parents/children aboard         | Discrete | Ranges from 0 to 6 |  
| Ticket        | Ticket number                        | Nominal  | Not standardized |  
| Fare          | Passenger fare                       | Ratio    | Skewed distribution |  
| Cabin         | Cabin number                         | Nominal  | Many missing values |  
| Embarked      | Port of embarkation (C, Q, S)        | Nominal  | C = Cherbourg, Q = Queenstown, S = Southampton |  

---

## Methodological Information  

**Data Processing**  
- Missing values in *Age* imputed using median.  
- *Categorical variables* (Sex, Embarked, Pclass) encoded for modeling.  
- Outliers in *Fare* distribution log-transformed for visualization.  

**Analysis**  
- Logistic Regression model built to predict survival outcomes.  
- Data visualization (bar plots, histograms) used to explore survival by gender, class, and age group.  

**Python Libraries Used**  
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score, confusion_matrix

**Models and Results**

### 1. Overall Survival Summary  
- **Overall Survival Rate**: ~38%  
- **Female Survival Rate**: ~74%  
- **Male Survival Rate**: ~19%  
- **Children (<18) Survival Rate**: ~52%  
- **Adult (≥18) Survival Rate**: ~37%  

---

### 2. Survival by Gender × Child  
- Female children: highest survival rate  
- Male children: higher than adult males but lower than females  
- Adult males: lowest survival rate  

---

### 3. Survival by Class  
- **1st class**: highest (~63%)  
- **2nd class**: medium (~47%)  
- **3rd class**: lowest (~24%)  

---

### 4. Age Statistics  
- Survivors: Median ~28, Mean ~28.3  
- Non-survivors: Median ~28, Mean ~30.6  
- Standard deviation ~14 for both groups  
- Mode clustered in 20–30 age range  

---

### 5. Survival by Age Group  
- **0–9 years**: >60% survival rate  
- **10–19 years**: ~40% survival rate  
- **20–39 years**: lowest (~30–35%)  
- **40+ years**: slightly higher (~35–40%)  

---

### 6. Visualizations  
Three charts were generated and embedded in the Excel output:  
1. Bar chart – Survival Rate by Gender  
2. Bar chart – Survival Rate by Class  
3. Line chart – Survival Rate by Age Group  

---

### Conclusion  
- Gender and class are the strongest predictors of survival.  
- Children (especially 0–9 years old) had a clear survival advantage, consistent with “women and children first” policies.  
- Socio-economic status, reflected by passenger class, played a decisive role.  
- Age had limited overall influence, except for young children.  

---

## Data Storage and Sharing  
- **Primary Storage**: CSV files stored locally and on GitHub/Kaggle.  
- **Backup Strategy**: 3-2-1 rule (local machine + GitHub repo + Kaggle copy).  
- **License**: Open Data (CC0 1.0).  
- **Access**: Publicly available via Kaggle.  
- **DOI**: N/A – dataset link provided above.  

---

## Reflection  

### Metadata Standard  
- DDI (Data Documentation Initiative) was chosen because it is widely accepted in social science and suitable for demographic datasets.  

### Template/Software  
- Created using GitHub ReadMe Markdown format.  

### Challenges & Solutions  
- **Challenge**: Balancing technical details with readability.  
  - **Solution**: Wrote in technical-first style, then simplified for accessibility.  
- **Challenge**: Handling missing values (*Age*, *Cabin*).  
  - **Solution**: Applied median imputation and explicitly documented missingness.  

