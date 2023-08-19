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

## LOAN_DATA.CSV
```
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```
## DATA_SET.CSV
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
```
# OUTPUT
## FOR LOAN_DATA:
## DATA
```
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
```
![data set](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/451a714c-f8ad-48db-9b17-c6b722c7f10b)


## NON NULL BEFORE
```
df.info
```
![non null](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/4b45652d-d9f0-4689-953d-039dd592490a)


## MODE
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![mode](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/39d5cecc-7fbf-4207-b336-5a1a5f557a33)


## MEAN
```
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![mean](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/855ff6ab-c3e6-4984-963b-76f0277dca2c)


## MEDIAN
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```

![median](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/33306e4a-431f-497f-8237-4be422f0c731)

## NON NULL AFTER

```
df.info()
```
![non null after](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/95c0da45-5e16-4e77-9417-ad8945ee8cf2)


```
df.isnull().sum()
```
![isnull](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/8d3bf6ba-a987-4f9b-806a-6c51332b4c60)


## FOR DATA_SET:
## DATA
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
```
![data set](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/fbb6d664-3217-497b-948e-d172781d7cea)


## NON NULL BEFORE
```
df.info()
```
![non null](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/6104fd51-a998-41be-b71f-dd269c39eb0f)


```
df.isnull()
```
![null](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/026ab1f3-1d6d-40a4-b3f5-3ecbb309c5a9)


```
df.isnull().sum()
```
![nullsum](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/9da95591-02e6-442e-89fb-80d1ec6e8688)

## MODE
```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![mode](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/b5366692-0c9e-401a-8a61-2628ef282b56)


## MEAN
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![mean](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/1d328ce4-093a-493a-a2e4-46a26eedbdd7)

## MEDIAN
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![median](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/18d0dfe7-6f2c-4939-98ec-ab2f8a5288ec)


## NON NULL AFTER
```
df.info()
```

![null after](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/9b49251e-149a-4714-9d04-a89746392250)

```
df.isnull()
```
![dfnull](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/22d6d5d3-5aac-4b17-94a7-a9fb0ce24feb)


```
df.isnull().sum()
```
![dfsum](https://github.com/KRISHNARAJ-D/ODD2023-Datascience-Ex01/assets/119559695/2163cd38-3da0-4a98-b00b-8f3714894c90)


# RESULT
Thus,the given data is read,cleansed and the cleaned data is saved into the file.

