# EX-05-Feature-Generation
## AIM:

To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation:

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

# ALGORITHM:

### STEP 1:
Read the given Data
### STEP 2:
Clean the Data Set using Data Cleaning Process
### STEP 3:
Apply Feature Generation techniques to all the feature of the data set
### STEP 4:
Save the data to the file

# PROGRAM:
```
DEVELOPED BY:YOGABHARATHI S
REGISTER NO:212222230179
```
# Encoding Data.csv :
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
# Data.csv:
```
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
# bmi.csv:
```
df=pd.read_csv("/content/bmi.csv")
df
df = pd.get_dummies(df, prefix=['Index'] ,columns=['Index'])
df
be = BinaryEncoder()
data2 = be.fit_transform(df['Gender'])
df = pd.concat([df,data2],axis=1)
df
```

# OUPUT:
## Encoding Data.csv : 
### Initial data:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/b356bf7b-89c6-4e2a-b716-f919d7b044ae)

### Unique value:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/2cedb19e-3a64-45b6-a436-677c5e864d95)

### Ordinal Encoder:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/d2b0db16-c47a-4e8e-8778-fe930c57ef8f)

### Label Encoder:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/85d909b0-203a-42ac-96f1-29331c3d6051)

### Binary Encoder:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/ebf9e477-c262-43c0-bbb8-0f1c1b629c9d)
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/5830fdb9-d02c-4a74-a5ef-872734a912cf)

## Data.csv:
### Initial data:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/a42d1eb4-003a-4358-8bda-59b5f774ca46)

### Unique value:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/16c63618-a054-4613-a968-eb66236a15c9)

![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/ac533543-787f-40bc-bbdd-0d61fdf12828)

### Ordinal Encoder:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/8ea862f9-92cc-4416-bba5-f6807698bd0d)

![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/7cbf074a-5411-4741-9af9-fd14b11c8ab1)

### Label Encoder:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/7f6c2066-8c6a-4810-8057-a70e39aaa68c)

### Binary Encoder:

![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/7494a2f8-ff38-4f52-a773-e9e9889a6471)

![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/34aad8ef-cd73-4ac4-8a6d-7286d086fa4a)

## bmi.csv:'
### Initial data:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/36d8f821-9d7b-46ac-883f-eb3d2358d8fe)

### Binary Encoder:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/75cf7ebe-c34d-484b-b92f-ae8b22186c70)

### Dummies:
![image](https://github.com/Yogabharathi3/EX-05-Feature-Generation/assets/118899387/47a2f6e1-88f1-478d-bd62-3a3c618a2727)

# RESULT:
The Feature Generation process was performed and saved the data to a file.
