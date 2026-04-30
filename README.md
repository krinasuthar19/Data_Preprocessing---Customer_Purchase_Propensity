# Customer Purchase Propensity - Data Preprocessing Pipeline

## Project Overview

This project focuses on building a complete data preprocessing and feature engineering pipeline for customer purchase data. The goal is to transform raw data from multiple sources into a clean and structured dataset suitable for machine learning.

The problem is framed as a **binary classification task**, where the objective is to predict whether a customer will make a purchase (`1`) or not (`0`).

---

## Step 1: Project Planning & Problem Framing

- **Data Analysis:** Process of collecting, cleaning, and interpreting data to extract useful insights.  
- **Data Science Workflow:** Data Collection → Cleaning → EDA → Feature Engineering → Modeling.  
- **Problem Framing:** Predict customer purchase behavior as a binary classification problem.

---

## Step 2: Data Import and Understanding

- Loaded data from multiple sources:
  - CSV (customers)
  - JSON (transactions)
  - SQL (products)
  - API (user data)
- Merged datasets using `customer_id` and `product_id`
- Explored data using `.head()`, `.info()`, and `.describe()`

---

## Step 3: Exploratory Data Analysis (EDA)

- **Univariate Analysis:** Histograms and skewness detection  
- **Bivariate Analysis:** Correlation with target (`purchased`) and boxplots  
- **Multivariate Analysis:** Heatmaps, pairplots, grouped statistics  

---

## Step 4: Handling Missing Data

- Applied multiple imputation techniques:
  - Simple Imputer (mean, most frequent)
  - Random Sample Imputation with indicator
  - KNN Imputer
  - MICE (Iterative Imputer)
  - Complete Case Analysis
- Final clean dataset created with no missing values  

---

## Step 5: Outlier Detection & Handling

- Applied:
  - Z-score method
  - IQR method
  - Percentile method
  - Winsorization
- IQR/Winsorization selected as most effective  

---

## Step 6: Handling Mixed & Date/Time Variables

- Converted date column to datetime format  
- Created feature: `days_since_last_purchase`  
- Extracted numeric values from mixed IDs  

---

## Step 7: Encoding Categorical Data

- Label Encoding (binary variables)  
- One-Hot Encoding (nominal variables)  
- Ordinal Encoding (ordered categories)  
- Binning for numerical grouping  

---

## Step 8: Feature Scaling

- Applied:
  - StandardScaler  
  - MinMaxScaler  
  - MaxAbsScaler  
  - RobustScaler  
  - Normalizer  
- Used ColumnTransformer for combined transformations  

---

## Step 9: Feature Construction & Transformation

- Created interaction feature: `purchase_per_day`  
- Applied:
  - Log transformation  
  - Power transformation  
- Performed:
  - Binning (income groups)  
  - Binary feature creation (`frequent_buyer`)  

---

## Step 10: Final Output

- Final dataset exported as:  
  **processed_customer_data.csv**
- Dataset is:
  - Clean (no missing values)
  - Outliers handled
  - Feature-engineered
  - Ready for machine learning  

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- SQLite  
- Requests API  

---

## Key Insights

- Raw data contained missing values, outliers, and inconsistent formats  
- Income and amount features showed high skewness  
- No strong direct correlation between most features and purchase behavior  
- Feature engineering significantly improved dataset quality  

---

## Conclusion

A complete data preprocessing pipeline was implemented to convert raw data into a clean, structured, and machine learning-ready dataset. This project demonstrates practical handling of real-world data challenges including missing values, outliers, encoding, scaling, and feature engineering.

---

## Author

Krina Suthar
