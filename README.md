
# 🚗 Car Dataset - Data Analysis with Python

This beginner-level project involves cleaning and exploring a car dataset using **Python** and **Pandas**. The goal was to apply core data analysis techniques such as handling missing values, filtering data, and applying functions to modify columns.

---

## 📁 Dataset Overview

The dataset contains specifications of various car models, including attributes like Make, MPG (mileage), Weight, and Origin.

---

## 🛠️ Tools Used

- Python
- Pandas (Data analysis)
- Jupyter Notebook (or any Python IDE)

---

## ✅ Tasks Performed

### 1. **Data Import and Overview**
- Used `pd.read_csv()` to load the dataset.
- Explored data using `.head()`, `.shape`, and `.info()`.

### 2. **Data Cleaning**
- Checked for null values using `df.isnull().sum()`.
- Filled all missing values with the **mean** of their respective columns using `fillna()`.

### 3. **Exploratory Analysis**
- Used `value_counts()` to list all unique **Make** values and their occurrence counts.

### 4. **Filtering Data**
- Displayed records where `Origin` is **Asia** or **Europe** using `isin()`.

### 5. **Removing Outliers**
- Removed all rows where `Weight` > 4000.

### 6. **Column Transformation**
- Increased all values in the `'MPG_City'` column by **3** using the `apply()` function.

---

## 📌 Skills Practiced

- Identifying and handling missing data
- Using Pandas filtering and condition-based selection
- Applying functions to modify DataFrame columns
- Working with categorical data using `value_counts()`
- Basic data cleaning and preprocessing

---

## 📎 Sample Code Snippet

```python
# Fill missing values with column mean
df.fillna(df.mean(numeric_only=True), inplace=True)

# Filter by Origin
df[df['Origin'].isin(['Asia', 'Europe'])]

# Remove rows where Weight > 4000
df = df[df['Weight'] <= 4000]

# Increase MPG_City values by 3
df['MPG_City'] = df['MPG_City'].apply(lambda x: x + 3)
