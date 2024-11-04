# Task 2: Perform data cleaning and exploratory data analysis (EDA) on a dataset of your choice, such as the Titanic dataset from Kaggle. Explore the relationships between variables and identify patterns and trends in the data.

The notebook includes additional steps for handling missing values, feature transformations, and column reduction. Here’s an updated README that incorporates these steps.

---

# EDA and Data Cleaning - README

This README details the steps for Exploratory Data Analysis (EDA) and data cleaning, including data loading, exploration, visualization, feature engineering, and handling missing values.

### Contents
1. [Setup and Data Loading](#setup-and-data-loading)
2. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
   - Summary Statistics
   - Visualizations
3. [Data Cleaning and Transformation](#data-cleaning-and-transformation)
   - Feature Engineering
   - Handling Missing Values

---

### 1. Setup and Data Loading

1. **Library Imports**: Essential libraries (`numpy`, `pandas`, `matplotlib`, `seaborn`) are imported for data handling and visualization.
2. **Data Loading**: The dataset is loaded into a DataFrame (`df`) using `pd.read_csv()`.

### 2. Exploratory Data Analysis (EDA)

EDA explores the dataset structure, including data types, summary statistics, and feature distributions.

1. **Data Summary**:
   - `df.info()`: Provides an overview of columns, data types, and non-null counts.
   - `df.describe()`: Displays summary statistics for numerical columns.
   - `df.nunique()`: Shows the number of unique values in each column.
   - `df.isnull().sum()`: Counts missing values for each column.

2. **Visualizations**:
   - **Categorical Distributions**: Bar plots visualize the distribution of categorical features (`Survived`, `Pclass`, `Sex`, `Cabin`, `Embarked`).
   - **Cabin and Ticket Analysis**: Separate distributions for the newly created `cabin_cat` and `ticket_cat` columns reveal patterns related to cabin categories and ticket prefixes.

### 3. Data Cleaning and Transformation

This section focuses on feature engineering, missing value imputation, and column reduction.

1. **Feature Engineering**:
   - **Cabin and Ticket Features**: `Cabin` and `Ticket` columns are transformed:
     - `cabin_num` and `cabin_cat`: Capture the numerical and alphabetical portions of `Cabin`.
     - `ticket_num` and `ticket_cat`: Capture the numerical and alphabetical portions of `Ticket`.
   - **Dropping Original Columns**: After extraction, unnecessary columns (`Name`, `ticket_num`, `ticket_cat`, `PassengerId`) are removed.

2. **Handling Missing Values**:
   - **Imputation**:
     - `KNNImputer` fills missing values for numerical columns (`Age`, `Fare`).
     - `SimpleImputer` with `most_frequent` strategy imputes categorical columns (`cabin_num`, `cabin_cat`).
   - **Transformation Pipeline**: A `ColumnTransformer` applies the imputers to the relevant columns, resulting in `df_transformed`, the cleaned and transformed DataFrame.

---
