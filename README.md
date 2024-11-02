# Task 1: Create a bar chart or histogram to visualize the distribution of a categorical or continuous variable, such as the distribution of ages or genders in a population.

This notebook contains the data visualization and exploration of the Titanic dataset, focusing on both categorical and numerical variables.

## Contents

1. **Data Import and Exploration**:
   - Loaded necessary libraries (`pandas`, `matplotlib`, `seaborn`).
   - Loaded and inspected the dataset structure using `.info()`, `.describe()`, and `.head()`.

2. **Data Preparation**:
   - Separated columns into **numerical** (e.g., `Age`, `SibSp`, `Parch`, `Fare`) and **categorical** (e.g., `Survived`, `Pclass`, `Sex`, `Embarked`) for focused analysis.
   - Engineered additional features from `Cabin` and `Ticket` columns to create `cabin_num`, `cabin_cat`, and `ticket_num` for enhanced analysis.

3. **Visualization**:
   - **Categorical Variables**:
     - Created bar plots to show distributions of `Survived`, `Pclass`, `Sex`, `Embarked`, and other categorical features.
   - **Numerical Variables**:
     - Generated histograms and density plots to visualize distributions of continuous variables like `Age` and `Fare`.

4. **Observations**:
   - Observed patterns in survival rates based on class, gender, and other demographics.
   - Identified distributions and potential outliers in age and fare data.

---

This notebook provides an introductory analysis and visualization of the Titanic dataset, making it easier to understand its key features and patterns. 

--- 
