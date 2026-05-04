##import pandas as pd 
##import numpy as np

# this is used for importing libraries

## df = pd.read_csv("customer_shopping_behavior.csv")

# used  to read the csv file 

## df.info()
# used to check non null value and data type

## df.describe(include="all")
 # take statistic for full df

# df.isna()
# check null if exist 

## perform eda and remove null through median 
# df["Review Rating"] = df.groupby("Category")["Review Rating"].transform(lambda x :x.fillna(x.median()))


## df.columns = df.columns.str.lower()
## df.columns =df.columns.str.replace(" ","_")

# convert uppercase to lower and remove extra space



# labels =["Young Adult","Adult","Middle-aged","Senior"]
# df["age_group"]=pd.qcut(df["Age"],q=4,labels=labels)

## qcut used to divide into catagory on basis of k 

## (df["discount_applied"]==df["promo_code_used"]).all()
## check correlation



