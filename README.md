# Ex03-Univariate-Analysis
# Aim:
To read the given data and perform the univariate analysis with different types of plots.
# Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
# Algorithm:
## Step1:
Read the given data.
# Step2:
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
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("/content/diabetes.csv")
df
df.info()
df.describe()
df.dtypes
plt.figure(figsize=(17,7))
sns.boxplot(data=df)
df.isnull().sum()
df['Insulin'].value_counts()
df['Age'].value_counts()
sns.boxplot(x='Insulin',data=df)
sns.countplot(x='Insulin',data=df)
sns.distplot(df['Insulin'])
sns.histplot(x='Insulin',data=df)
df.skew()
sns.histplot(x='DiabetesPedigreeFunction',data=df)
df.kurtosis()
sns.boxplot(x='BloodPressure',data=df)
sns.scatterplot(data=df) 
```
## (2) SuperStore.csv