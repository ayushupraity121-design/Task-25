# Task 25: Basic Data Cleaning - AI & ML Track

## Overview
This project fulfills **Task 25: Basic Data Cleaning** by taking a real-world dataset (Titanic), inspecting its structure, removing duplicates, handling missing values, correcting data types, and exporting both the raw and cleaned datasets.

---

## Deliverables Included
1. **`original_dataset.csv`**: The raw, unprocessed dataset loaded directly from Seaborn (`titanic`).
2. **`cleaned_dataset.csv`**: The final cleaned dataset ready for exploratory data analysis and machine learning.
3. **`data_cleaning.ipynb`**: The complete Jupyter Notebook containing the step-by-step cleaning workflow.
4. **`README.md`**: This documentation file describing all data-cleaning decisions.

---

## Step-by-Step Data Cleaning Workflow

### 1. Inspection
- Loaded the dataset and examined its initial shape (`891 rows × 15 columns`).
- Inspected column data types, non-null counts, and the first few rows to understand the structure.

### 2. Duplicate Removal
- Checked for identical duplicate rows across the dataset.
- Removed duplicate entries to prevent data leakage and model bias during training.

### 3. Missing Value Treatment
- **High Missing Data Column (`deck`)**: Dropped the `deck` column due to a critically high proportion of missing values.
- **Numerical Imputation (`age`)**: Imputed missing values in the `age` column using the median age to avoid distortion from extreme outliers.
- **Categorical Imputation (`embark_town` / `embarked`)**: Filled missing categorical values using the statistical mode (most frequent category).

### 4. Data Type Correction
- Ensured target and indicator variables like `survived` are cast to integer types.
- Converted descriptive text columns (such as `class`) into appropriate categorical data types for memory efficiency.

---

## How to Run
1. Open the project folder in **VS Code**.
2. Open `data_cleaning.ipynb` using the Jupyter extension.
3. Run the cells sequentially to reproduce the entire data cleaning pipeline and generate the output files.