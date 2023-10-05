# Ex 01 DS Data Cleansing


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
```
NAME:DIVYA.K
REGISTER NO:21222230035
```
```
import pandas as pd
df=pd.read_csv("SAMPLEDS - Sheet1.csv");
df
df.shape
df.info()
df.head()
df.tail()
df.isnull().sum()
df.dropna(how='any').shape
x=df.dropna(how='any')
x

y=df.dropna(how='all')
y
tot=df.dropna(subset=['TOTAL'],how='any')
tot
t1=df.dropna(subset=['M1','M2','M3','M4'])
t1
df.fillna(0)
df.fillna(method='ffill')
df.fillna(method='bfill')
mn=df.TOTAL.mean()
mn
df.TOTAL.fillna(mn,inplace=True)
df
i=df.M1.interpolate()
i
df.M1.fillna(i,inplace=True)
df
md=df.M2.median()
md
m=df.M2.mode()
m
df.M2.fillna(md,inplace=True)
df
df.duplicated()
df.drop_duplicates(inplace=True)
df
df['cd']=pd.to_datetime(df['DOB'])
df

for x in df.index:
  if df.loc[x,"AVG"]>100:
    df.drop(x,inplace=True)
df
```

# OUTPUT

![263434109-b04bc09b-aad9-4e08-bb4f-ffc33d0a57bd](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/6eeec873-af0b-4248-b8fc-f3975c88ab0f)

![263434122-e9191dd7-fd76-49cf-9572-6a95c1fdec31](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/1899cc40-c197-4d06-ad60-ae951dab8c83)

![263434174-fc5646bc-5f09-4449-a810-d1a96af0e759](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/56ffade7-e4c7-4130-80bb-742646290ca1)

![263434193-ca663b59-7790-4de7-8813-0ba1e9a2f20d](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/d1701050-b7d1-4334-8274-29ebceacdd8c)

![263434212-459aae91-2394-4437-bd3e-fd769c0b19c1](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/abf17bcc-8b02-43ed-b5e2-ec46cceace08)

![264390625-7a74c202-8c08-4e34-bf58-0d74a6592a1f](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/9f1d9945-3a75-48b6-9969-0f645f0f9a01)

![264390924-04f9e304-b435-4e93-85ba-4c07407b3424](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/1561db76-7be8-4948-b945-d9f65ce6cda8)


![264391104-50d5dd78-1448-44f9-91dc-e73daaaf32ba](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/a651f845-aec8-4875-a4c8-dab447bba487)

![264391251-f84ee951-285d-4c8b-acc9-0f3a3f575fc5](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/ceed69cd-f26c-4868-aae2-5cb82b33b16d)

![264391391-d0a40e81-1a2a-4d3e-bf07-9c9e5ef53609](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/8b8d9e9a-0485-45a7-89aa-68da1df35bea)

![264391546-96705cb6-fbb7-49bc-9760-8d21a9f68afc](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/ce631ac1-3ed7-4485-b11b-3385e1164b25)

![264391800-95c12089-8421-4ed5-8f0a-406df11fe301](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/b0b4115f-5208-4fd7-a55e-f680a20f91cd)

![264391914-51a38697-0154-47c6-8a19-deae3f27fc03](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/2826dce2-c665-41d5-b090-69def9ecb589)

![264392035-4227fcf7-13fc-449c-81dc-f7f636b9f24d](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/97f6432f-49a0-4ae4-bb92-6c3d4378607c)

![264392142-89333abe-f635-4dbb-8883-33facbfce7fa](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/3db60321-839d-4392-ba82-aa1c9eedbccb)

![264392346-4fe12bc3-8493-4219-b10d-5c2bdc9227fb](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/bfe6b378-4712-4d2c-a090-4cf2c7190293)

![264392515-c8d2bf8b-6a27-4dfd-bb96-60c6dbfce3c6](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/734feddc-fe57-4943-a0ec-02faf5fc29b6)

![264392625-decae851-1b73-4f34-8495-38b23aeb6a6e](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/b065d903-8d9b-47cc-b649-7b42bf7718ea)

![264392809-c18987d5-1c58-4c04-a13d-dfc1aa474d1d](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/175e9723-a316-456d-88d0-fca1f20939d2)

![264392962-6d413529-a351-492b-9812-ea04110bb6f2](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/c53a1c35-4da4-45ae-9780-0c40c4943a50)

![264393106-3ac63188-fe54-4bd0-944a-48f460cf5bdb](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/f75b8d86-28ed-4ff9-a32a-2792dd016707)

![264393225-b08e8841-7e81-4fd6-b47e-ea1b5da72310](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/f3535dc5-820b-4f82-b59b-f63226c3230e)

![264393340-725b9178-0e45-4dde-9a15-86849618a668](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/e0934743-0346-4b8d-88ec-f46d1f4fc4bf)

![264393481-1512188d-b0e6-4eea-be7f-5827e8e270dc](https://github.com/divyakumars/ODD2023-Datascience-Ex01/assets/119393621/c9422ce2-baeb-4e7e-b727-c007e9f3d80d)


# RESULT
Thus the given data is read,cleansed and the cleaned data is saved into the file.





  
