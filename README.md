# Ex03-Univariate-Analysis
# Aim:
To read the given data and perform the univariate analysis with different types of plots.
# Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

# Algorithm:
## Step1:
Read the given data.

## Step2:
Get the information about the data.

## Step3:
Remove the null values from the data.

## Step4:
Mention the datatypes from the data.

## Step5:
Count the values from the data.

## Step6:
Do plots like boxplots,countplot,distribution plot,histogram plot.

# Program:
## (1) Diabetes.csv
``` python
import pandas as pd
import numpy as np
import seaborn as sns
df = pd.read_csv("/diabetes.csv")
df
df.info()
df.isnull().sum()
df.dtypes
df.describe()
df['Glucose'].value_counts()
sns.boxplot(x="Glucose",data=df)
sns.countplot(x="Glucose",data=df)
sns.distplot(df['Glucose'])
sns.histplot(x="Glucose",data=df)
df.skew()
sns.distplot(df["Glucose"])
sns.histplot(x="Glucose",data = df)
df.kurtosis()
sns.boxplot(x="Glucose",data=df)
```
 
## (2) SuperStore.csv
```python
df2 = pd.read_csv("/SuperStore.csv")
df2.head()
df2.isnull().sum()
df2['Postal Code'] = df2["Postal Code"].fillna(df2['Postal Code'].mode()[0])
df2.isnull().sum()
df2.dtypes
df2.describe()
df2['Sales'].value_counts()
sns.boxplot(x="Sales",data=df2)
sns.countplot(x="Sales",data=df2)
sns.distplot(df2['Sales'])
sns.histplot(x="Sales",data=df2)
df2.skew()
sns.distplot(df2["Postal Code"])
sns.histplot(x="Postal Code",data = df2)
df2.kurtosis()
sns.boxplot(x="Row ID",data=df2)
```
# OUTPUT 
![output](o1.png)
![output](o2.png)
![output](o3.png)
![output](o4.png)
![output](o4.png)
![output](o5.png)
![output](o6.png)
![output](o7.png)
![output](o8.png)
![output](o9.png)
![output](o10.png)
![output](o11.png)
![output](o12.png)
![output](o13.png)
![output](o14.png)
![output](o15.png)
## RESULT:
Thus we have read the given data and performed the univariate analysis with different types of plots.