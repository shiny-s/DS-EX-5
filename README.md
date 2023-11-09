# Feature_Encoding_Scaling
# Ex:05 Feature Generation
# AIM
To read the given data and perform Feature Generation process and save the data to a file.

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

# ALGORITHM
STEP 1
Read the given Data

STEP 2
Clean the Data Set using Data Cleaning Process

STEP 3
Apply Feature Generation techniques to all the feature of the data set

STEP 4
Save the data to the file

# PROGRAM
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
# Data.csv
```
import pandas as pd
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
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
# BMI.csv file
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```
# OUTPUT
For encoding.csv file

![1](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/5dfdcca5-dfae-493d-a4d6-cc4a77bc951d)
![2](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/01ff7849-ab07-4c2b-87f0-b19b502f0831)
![3](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/4e8a5586-98f6-4161-8112-c46b38cf9c87)
![4](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/33ea10bf-86af-4d12-9b1b-0ee632d026b1)
![5](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/be161fc7-5cb6-4acb-a9cf-74b9a7dc0612)
![6](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/1bbbf4f3-e6bb-4bae-b1e3-f96890786d7d)
![7](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/9b1de3b5-aa6a-4eb9-8aa5-c375ccabcca4)
![8](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/8b2c4625-b19f-4cbb-a553-ae62e189dac8)
![9](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/11b81e96-24e1-4fea-a540-54d5660fd812)
![10](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/9a137347-5496-466a-907a-c640f7623f03)
![11](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/10702476-4a60-4d43-9b31-0ad33da72799)
![12](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/004c94e9-aa0f-44ec-a740-51e521e63b78)
![13](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/2ba52097-fe7d-4214-ba4d-9bfacdfe30b1)
![14](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/dc40c74e-c74e-494e-b115-9064eb9f429e)
![15](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/adb146e6-6933-4781-baa8-53dadd5f6502)
![16](https://github.com/Krupa-Varsha-P/DS-EX-5/assets/100466625/03e869b3-00c0-4bb0-abea-d1649ea8507f)


# RESULT:
The Feature Generation process was performed and saved the data to a file.
