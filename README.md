## Calculate CLV Including Demographics Data

Changes from original code listed below:

- **1 - Data Prep**
    - Join in demographics
    - Transform binned numerical columns to numerical
    - Add **Region** to replace high cardinality **ST** column
    - Add **demog_ownrent** to list of categorical columns to encode
    - Save *combined_df* as pickle instead of CSV so types are preserved
- **2 - Churn Modeling**
    - Read in *combined_df* as pickle not CSV
    - Add **demog_ownrent** to list of variables to exclude in model fitting since it was encoded
    - Turn dimensionality reduction code into a *while loop*
    - Hyperparameter tuning for gradient boosting model
- **3 - Margin Modeling**
    - Read in *combined_df* as pickle not CSV
    - Add **demog_ownrent** to list of variables to exclude in model fitting since it was encoded
    - Turn dimensionality reduction code into a *while loop*
    - Hyperparameter tuning for gradient boosting model
- **4 - CLV Calculations**
    - Read in *combined_df* as pickle not CSV