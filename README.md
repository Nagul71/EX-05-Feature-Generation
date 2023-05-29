# EX-05-Feature-Generation

## AIM:

To read the given data and perform Feature Generation process and save the data to a file.

# Explanation:

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

# ALGORITHM:

### STEP 1

Read the given Data

### STEP 2

Clean the Data Set using Data Cleaning Process

### STEP 3

Apply Feature Generation techniques to all the feature of the data set

### STEP 4

Save the data to the file

# CODE:

## Data:

```python
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

## Encoding data:

```python
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

## Titanic Dataset:

```python
df2 = pd.read_csv("titanic_dataset.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Sex'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])
df2
```

# OUTPUT:

# Encoding Data.csv

![Screenshot 2023-05-29 222952](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/2fb083de-58ab-4f61-a077-cf3edc1c11e4)

![Screenshot 2023-05-29 223010](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/06af4c6c-362d-4847-9bca-8e9e1cebacdd)

![Screenshot 2023-05-29 223015](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/b0f6cf80-0a9c-410f-8b50-caafa943adc3)

![Screenshot 2023-05-29 223021](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/aa6654f2-c836-4399-b0dd-7c61f728a436)

![Screenshot 2023-05-29 223036](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/5abbaec5-673a-4403-8286-a5b45200cb83)




# Data.csv
![Screenshot 2023-05-29 223043](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/c49f7143-b954-42f7-a79c-01e32ed3ba5b)
![Screenshot 2023-05-29 223049](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/20edf401-4869-4e84-8d11-840125b80ae7)
![Screenshot 2023-05-29 223056](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/70255e27-626d-4904-9b41-2fbae9497974)

![Screenshot 2023-05-29 223102](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/0d1d7b5d-b384-46c7-abd5-7aa6f0c247f1)
![Screenshot 2023-05-29 223112](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/c4f33653-80a5-4630-98aa-23c3a45f4ac4)
![Screenshot 2023-05-29 223119](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/2f9aa3a7-235c-41c7-a4c4-a3473b649a25)
![Screenshot 2023-05-29 223125](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/bd4b4e52-3cee-459a-9549-61f5c614a58b)


# titanic_dataset.csv
![Screenshot 2023-05-29 223134](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/8b243f03-040f-4c66-8d18-b886dc3de50f)
![Screenshot 2023-05-29 223147](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/fdea3edc-84da-4650-bb60-cf20e62e305f)
![Screenshot 2023-05-29 223202](https://github.com/Nagul71/EX-05-Feature-Generation/assets/118661118/3ab098c5-72e9-46c4-b84e-f9b1bd47cf4c)


# Result:

Thus the Feature Generation and Feature Scaling process is applied to the given data set.
