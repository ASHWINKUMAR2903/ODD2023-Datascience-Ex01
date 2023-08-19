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

# CODE and OUTPUT
## Data_set:
### Code:
```
import pandas as pd
df=pd.read_csv("/content/Data_set(1).csv")
print(df)

df.head(5)

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

df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()

df.isnull().sum()
```
### screenshot:
![1](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/30e35f7e-7dfd-4e63-8fd5-7dcc7df0f9d4)
![2](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/54ededb9-465b-49f8-bcd9-40fbcd485db0)
![3](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/22686061-2dd7-4711-99ad-e51a037a5fbf)
![4](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/d39c158b-0125-4429-9fc9-a91c88dc67f1)
![5](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/3c5eae32-236c-4b3c-8262-76b2ea15c555)
![6](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/752c1f91-6ece-4662-88bc-cf8536b5b663)
![7](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/5aff1d9c-2a1c-474b-a3ae-d7f4a49b3274)

## Loan_data:
### Code:
```
import pandas as pd
df=pd.read_csv("/content/Loan_Data(1).csv")
print(df)

df.head(5)

df.info()

df.isnull()

df.isnull().sum()

df['Loan_ID']=df['Loan_ID'].fillna(df['Education'].mode()[0])
df['Education']=df['Education'].fillna(df['Education'].mode()[0])
df['Married']=df['Married'].fillna(df['Education'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df.head()

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.head()

df.info()

df.isnull().sum()
```

### screenshots:
![1](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/9ae316f6-98a8-49f6-b682-564becef5da0)
![2](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/f0d44025-a1b5-48ac-9819-41212e89efd3)
![3](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/2aa27e9f-eb3f-4547-a09e-501cd686cab2)
![4](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/b54bbd0d-88ac-489d-b95a-95dc63aa02da)
![5](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/c2adf5f1-8b46-4c25-a477-2beb99dd3b50)
![6](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/4b08df70-f8e2-4f70-afd5-658f0d8d7a82)
![7](https://github.com/ASHWINKUMAR2903/ODD2023-Datascience-Ex01/assets/119407186/303c2bae-9b20-4408-840f-40e10a2d6566)

# RESULT
Thus the given data is read,cleansed and the cleaned data is saved into the file.
