# HUDK4054-Individual Assignment #2: Write Readme Style Metadata
# Project Title: Titanic Survival Analysis

## General Information
- **Author**: Jerry Zhu (ORCID: 0009-0005-0476-3544)
- **Date**: 2025-09-30
- **Context**: HUDK4054 Course Assignment – Metadata & ReadMe
- **Purpose**: Analyze survival patterns of Titanic passengers based on demographic and socio-economic factors.

## Data & File Overview
- **Source**: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- **Files**: CSV, 891 rows × 12 columns
- **Key Columns**:
  - `PassengerId`: Passenger unique identifier  
  - `Survived`: Survival indicator (0 = No, 1 = Yes)  
  - `Pclass`: Ticket class (1, 2, 3)  
  - `Sex`: Gender  
  - `Age`: Age in years  
  - `Fare`: Passenger fare  

## Sharing & Access
- **License**: Open Data (CC0 1.0)  
- **Access**: Public Kaggle Dataset  
- **DOI**: N/A (see dataset link: https://www.kaggle.com/c/titanic/data)


## Methodological Information
- **Collection**: Historical passenger data from Titanic disaster (1912)  
- **Processing**:  
  - Missing values in `Age` imputed using median.  
  - Categorical variables encoded for analysis.  
- **Analysis**: Logistic regression + survival rate visualization (gender, class, age groups).

## Data-Specific Information (Data Dictionary)
| Variable     | Description                       | Type     | Notes                    |
|--------------|-----------------------------------|----------|--------------------------|
| PassengerId  | Unique passenger ID               | Nominal  | Sequential integer       |
| Survived     | Survival (1 = Yes, 0 = No)        | Binary   | Outcome variable         |
| Pclass       | Ticket class                      | Ordinal  | 1 = upper, 3 = lower     |
| Sex          | Gender                            | Nominal  | Male/Female              |
| Age          | Age in years                      | Interval | Some missing values      |
| Fare         | Ticket fare                       | Ratio    | Skewed distribution      |

## Reflection
- **Metadata Standard**: DDI chosen because it is widely used in social science and supports structured metadata for demographic data.  
- **Template/Software**: Created with GitHub ReadMe Markdown.  
- **Challenges**: The hardest part was balancing technical details with clarity for non-technical readers.  
- **Solution**: Wrote in technical style first, then simplified into accessible language.
