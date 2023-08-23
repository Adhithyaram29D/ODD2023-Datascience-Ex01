# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE 
Data set:
```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("/Data_set.csv")
df.head(10)
df.info()
df.describe()
df.isnull().sum()
df=df.dropna(subset=['show_name'])
df.head()
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df.head()
df=df.dropna(subset=['current_overall_rank'])
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
```
Loan Set:
```
import pandas as pd
import numpy as np
df=pd.read_csv('/content/Loan_data.csv')
df.info()
df=df.dropna(subset="Gender")
df.head()
df = df.dropna(subset=["Dependents"])
df.head()
df['Self_Employed'] = df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df.head()
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head(5)
df['Loan_Amount_Term'] = df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.head(5)
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].min())
df.head()
df.info()
```
## OUTPUT
# Data_Set.csv:
## Non NULL Before:
![Screenshot 2023-08-23 160021](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/ac3ee639-7861-45a7-bfcf-e4d09b5048ee)

![Screenshot 2023-08-23 160527](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/61699c04-b00f-44c7-b1cd-f547c4ed1061)

![Screenshot 2023-08-23 160618](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/1fcba8bc-5b2a-49c6-ab3d-a89a0de441b6)

![Screenshot 2023-08-23 160651](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/fe2bb36f-a30e-422d-bd69-00638c78a030)

![Screenshot 2023-08-23 160720](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/335d1ac0-6ed8-4864-9e57-9f94daaff8df)

![Screenshot 2023-08-23 160819](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/8ff4f1f3-d568-42b6-8194-0838f5f39495)

![Screenshot 2023-08-23 160848](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/7b781222-3db1-4b98-a2a9-754fc8b46085)

## Non NULL After:
![Screenshot 2023-08-23 160918](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/c26fc030-86ba-4753-886f-4c0a1fe22bed)

## Loan_data.csv:
## Non NULL Before:
![Screenshot 2023-08-23 161206](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/7df7a710-ecfd-4a78-aa14-f81659a0f24b)

![Screenshot 2023-08-23 161318](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/7de3cddf-b2c9-4182-a1e6-4070d010bfe5)

![Screenshot 2023-08-23 161402](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/64628d07-7543-43b0-aa94-d0ce1191d690)

![Screenshot 2023-08-23 161507](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/22335e8f-ebf1-4fc3-b40c-a12dacb24673)

![Screenshot 2023-08-23 161536](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/3133f293-2520-4321-a8d2-40580c920d10)

![Screenshot 2023-08-23 161630](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/e3e0f979-d63e-4403-9680-cb5468793d12)

![Screenshot 2023-08-23 161703](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/97143749-08e0-4d3f-8312-445a6773c6f3)

## Non NULL After:
![Screenshot 2023-08-23 161741](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex01/assets/119393540/fa4136e7-a738-4ee0-8211-81e7265fe566)

## Result:
Thus the given data is read,cleansed and the cleaned data is saved into the file.
