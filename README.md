# Behind the Buy

## Overview
Behind the Buy is a data analysis project that explores customer shopping behavior to uncover useful insights.  
The project focuses on cleaning raw data, analyzing patterns, and understanding what drives customer purchases.
## Objective
- Understand customer behavior  
- Analyze purchase patterns  
- Handle missing data properly  
- Find relationships between variables  

---


## Dataset
customer_shopping_behavior.csv  
Includes customer details, product categories, ratings, and discount usage  


---

## Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy  

---

## Dataset
customer_shopping_behavior.csv  

---

## Complete Workflow

```python
import pandas as pd
import numpy as np

# Load data
df = pd.read_csv("customer_shopping_behavior.csv")

# Understand data
print(df.info())
print(df.describe())

# Handle missing values (category-wise median)
df["Review Rating"] = df.groupby("Category")["Review Rating"] \
    .transform(lambda x: x.fillna(x.median()))

# Clean column names
df.columns = df.columns.str.lower().str.replace(" ", "_")

# Feature engineering (age groups)
labels = ["Young Adult", "Adult", "Middle-aged", "Senior"]
df["age_group"] = pd.qcut(df["age"], q=4, labels=labels)

# Correlation analysis
correlation = df.corr(numeric_only=True)
print(correlation)

# Basic insights
print("Average Rating:", df["review_rating"].mean())
print("Unique Categories:", df["category"].nunique())


