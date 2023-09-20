# Ex03-Univariate-Analysis
# Aim:
To read the given data and perform the univariate analysis with different types of plots.

# Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
# Algorithm:
# Step1:
Read the given data.
# Step2:
Get the information about the data.
# Step3:
Remove the null values from the data.
# Step4:
Mention the datatypes from the data.
# Step5:
Count the values from the data.
# Step6:
Do plots like boxplots,countplot,distribution plot,histogram plot.
# Program:
```
Developed by:Tharika S
Reg no:212222230159

import pandas as pd
import numpy as np
import seaborn as sns

df=pd.read_csv('superstore.csv')
df

df.head()
df.info()
df.describe()
df.isnull().sum()

df.dtypes

df['Postal Code'].value_counts()

sns.boxplot(x='Postal Code', data=df)
sns.countplot(x='Postal Code',data=df)
sns.distplot(df["Postal Code"])
sns.histplot(x='Postal Code',data=df)
```
# Output:
# Dataset:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/199eb0f1-006c-4b72-8435-c325fb33c550)
# Head:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/ace045ee-2506-43c0-85ea-b6cc3e2f6778)
# Info:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/1cb936ab-1dd2-4af3-a706-50ad034dc387)
# Describe:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/cc8d3a1f-52ef-41d5-9e6f-6dae99bba1e1)
# isnull:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/23e1abee-8b4b-4441-b0ef-5e1e4d06bc21)
# Data Types:
# Value Count:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/5de81fac-1dda-4610-9067-df99e3773bf6)
# Boxplot:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/bff90961-a387-4d78-a2c8-aae66dcf50de)
# Countplot:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/241fcc61-dbe8-4579-aae6-255ae345e9d6)
# Distplot:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/b73cbe3d-6f91-4048-969f-7aad9b99f969)
# Histplot:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/8dc913ca-cc2e-4101-87e5-ef0802d91ddc)
# Result:
Thus we have read the given data and performed the univariate analysis with different types of plots.





