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
# Program(superstore.csv):
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

# Program(diabetes.csv):
```
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('diabetes.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x="Glucose",data=df)
Glucose_q1 = df['Glucose'].quantile(0.25)
Glucose_q3 = df['Glucose'].quantile(0.75)
Glucose_IQR = Glucose_q3 - Glucose_q1
Glucose_low = Glucose_q1 - 1.5 * Glucose_IQR
Glucose_high = Glucose_q3 + 1.5 * Glucose_IQR
df=df[((df['Glucose']>=Glucose_low)&(df['Glucose']<=Glucose_high))]
sns.countplot(x="Glucose",data=df)
sns.distplot(df['Glucose'])
sns.histplot(x="Glucose",data=df)

```
# Output:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/e45e4ceb-f115-4e5f-818e-5cf874c6f5da)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/ffc09caa-3cc6-4f05-af72-e4df54d2e74e)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/7040cc9d-725a-4190-85ca-47f24c4d9f6d)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/b27451cc-8529-484a-b473-b4af65034510)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/3fd7d60d-cd8b-4838-9360-4ba04e9f4051)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/10ea81c7-69d9-4ac2-b50a-bcac6e35c8e6)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/5c3e31fa-c659-4b49-81e7-e8be8ff3038c)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/f18e3d44-e0c1-485f-9a96-db361739b018)

# Program(employee.csv):
```
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('diabetes.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x="Glucose",data=df)
Glucose_q1 = df['Glucose'].quantile(0.25)
Glucose_q3 = df['Glucose'].quantile(0.75)
Glucose_IQR = Glucose_q3 - Glucose_q1
Glucose_low = Glucose_q1 - 1.5 * Glucose_IQR
Glucose_high = Glucose_q3 + 1.5 * Glucose_IQR
df=df[((df['Glucose']>=Glucose_low)&(df['Glucose']<=Glucose_high))]
sns.countplot(x="Glucose",data=df)
sns.distplot(df['Glucose'])
sns.histplot(x="Glucose",data=df)
```
# Output:
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/e87755f5-6039-4c9e-b4da-01bd812a5f02)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/85ca249b-4ee9-4d9d-b906-0f1826ebc6b6)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/ed176c96-dbe7-4e97-80d6-bfdefc0d1b28)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/fda372be-424f-443a-aaea-f055896dc8b8)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/8a92531e-fa21-474d-8926-54e826356252)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/180ac0d2-2140-493e-9475-a8cee86ca16a)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/257a510e-5f96-4c8b-bcc9-2d490c23af99)
![image](https://github.com/tharikasankar/ODD2023-DataScience-Ex-03/assets/119475507/12ba7467-5490-4f97-bf2a-b515568315bd)

# Result:
Thus we have read the given data and performed the univariate analysis with different types of plots.





