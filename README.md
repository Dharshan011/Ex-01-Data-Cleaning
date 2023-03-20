# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
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
df.isnull().sum()
# OUPUT

Data:
![Screenshot 2023-03-12 210503](https://user-images.githubusercontent.com/113497491/226259193-b79697d3-0e3b-499d-950d-3f96181d3e91.png)
![Screenshot 2023-03-20 112229](https://user-images.githubusercontent.com/113497491/226259346-b2f3dca5-56bf-46d1-8935-b70a219ef05a.png)
![Screenshot 2023-03-20 112249](https://user-images.githubusercontent.com/113497491/226259405-b3ee0075-4a9b-436f-98bd-d31f668a50f8.png)
![Screenshot 2023-03-20 112313](https://user-images.githubusercontent.com/113497491/226259472-8c25e882-57b8-476c-874a-0f182121027e.png)
![Screenshot 2023-03-20 112329](https://user-images.githubusercontent.com/113497491/226259507-1ef39f58-6363-4d1d-aeb8-fb53192ceb5d.png)
![Screenshot 2023-03-20 112348](https://user-images.githubusercontent.com/113497491/226259540-bef5fc14-3831-4776-8a65-53872976089d.png)
![Screenshot 2023-03-20 112358](https://user-images.githubusercontent.com/113497491/226259559-ee75734a-5669-4dbd-9084-a89cb69fc21a.png)

### RESULT:
 
 Thus,the given data is read,cleansed and the cleaned data is saved into the file.
