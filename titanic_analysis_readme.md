# 🚢 Titanic Passenger Survival Analysis & EDA

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458.svg)
![Matplotlib/Seaborn](https://img.shields.io/badge/Matplotlib%2FSeaborn-Data_Visualization-ff69b4.svg)

## 📌 Project Overview
This project focuses on Exploratory Data Analysis (EDA) and data preprocessing for the widely recognized historical Titanic passenger dataset. The primary goal is to clean the raw data, engineer appropriate features, and uncover demographic correlations with passenger survival rates. 

By the end of this pipeline, the dataset is fully structured, numerically encoded, and ready to be fed directly into binary classification machine learning models (such as Logistic Regression or Random Forests).

## 📊 Dataset Description
The dataset contains information on 891 passengers and 12 initial features detailing their socio-economic status, demographics, and ultimate survival outcome.

**Key Features include:**
* `Survived`: Survival indicator (0 = No, 1 = Yes) - **Target Variable**
* `Pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
* `Sex`: Biological sex of the passenger
* `Age`: Age in years
* `Fare`: Passenger fare paid for the ticket
* `Embarked`: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

## 🛠️ Data Preprocessing Pipeline

To prepare the data for predictive modeling, several critical cleaning and encoding steps were executed:

### 1. Handling Missing Values
* **`Cabin`:** Dropped entirely due to excessive missing data (>75%).
* **`Age`:** Imputed missing values using the median age grouped by passenger class (`Pclass`) to preserve demographic variance.
* **`Embarked`:** Filled the minimal missing values with the mode ('S').

### 2. Feature Encoding & Selection
* Converted the categorical `Sex` variable into a binary numerical format (Male = 0, Female = 1).
* Applied One-Hot Encoding to the `Embarked` column to prevent models from assuming an ordinal relationship between ports.
* Dropped columns irrelevant to statistical survival modeling (`PassengerId`, `Name`, `Ticket`).

## 📈 Key Insights & Visualizations

Through our EDA using Matplotlib and Seaborn, two major historical trends were statistically validated:

1. **Survival by Gender:** There is a stark contrast in survival outcomes based on sex. The vast majority of male passengers perished, while being female showed a strong positive correlation with survival, aligning with the "women and children first" evacuation protocol.
2. **Age Distribution by Survival:** Kernel Density Estimates (KDE) revealed a distinct spike in survival for ages 0–10 (infants and young children were prioritized). Conversely, young adults (ages 20–30) suffered the highest density of casualties relative to their population on the ship.

## 🚀 Next Steps
With a fully clean and structurally sound dataset, the immediate next step is to divide the data into training and testing sets and apply predictive algorithms:
* Baseline Model: Logistic Regression
* Ensemble Model: Random Forest Classifier

## 💻 Technologies Used
* **Python** (Core language)
* **Pandas** (Data manipulation and cleaning)
* **Matplotlib & Seaborn** (Data visualization)

---
*This report and code pipeline were generated as part of a foundational data science portfolio project.*