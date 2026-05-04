# Behind the Buy

## Overview
Behind the Buy is a data analysis project that explores customer shopping behavior to uncover useful insights.  
The project focuses on cleaning raw data, analyzing patterns, and understanding what drives customer purchases.

---

## Objective
- Understand customer behavior
- Analyze purchase patterns
- Handle missing data properly
- Find relationships between variables

---

## Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy

---

## Dataset
customer_shopping_behavior.csv  
Includes customer details, product categories, ratings, and discount usage

---

## Step 1: Load Data
```python
import pandas as pd
import numpy as np

df = pd.read_csv("customer_shopping_behavior.csv")



