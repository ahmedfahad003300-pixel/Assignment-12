Attempt

-The CSV file reveals the prices of different in different cities at different time intervals 
-I found some characteristics of the CSV file using the following code

import pandas as pd
raw=pd.read_csv(r"C:\Users\ADMIN\Downloads\teaching_prices_clean.csv")
raw
raw.shape

raw.columns

raw.nunique()     (number of unique items in each column)


MO=raw[raw.duplicated(keep=False)]
print(MO)                                 

# Count of duplicate rows
print(raw.duplicated().sum())


print(raw["price"].dtype)
print(raw["item"].dtype)           (checking of datatype of each variable)
print(raw["city"].dtype)
print(raw["date"].dtype)


print(raw.isna().sum())          (counting the number of empty cells)
