# AIM

To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 
# ALGORITHM

### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file


# CODE
df=pd.read_csv("/content/data[1].csv")

df.info()

df.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

df['Ord_2'] = le.fit_transform(df['Ord_2'])

sns.set(style ="darkgrid")

sns.countplot(df['Ord_2'])

from sklearn.preprocessing import OneHotEncoder

enc = OneHotEncoder()

enc = enc.fit_transform(df[['City']]).toarray()

encoded_colm = pd.DataFrame(enc)

df = pd.concat([df, encoded_colm], axis=1)

df = df.drop(['City'], axis=1)

df.head(10)

df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2'])

df.head(10)

df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1'])

df.head(10)

# OUPUT

![01](https://user-images.githubusercontent.com/114581999/195504564-df2ffe85-a61e-4ec2-b363-4c444f7f67b8.png)

![02](https://user-images.githubusercontent.com/114581999/195504957-bc83112d-6277-4381-a6d8-51432ea6048d.png)

![03](https://user-images.githubusercontent.com/114581999/195504993-280f9587-147e-4036-9b61-a3d2f39797eb.png)

![04](https://user-images.githubusercontent.com/114581999/195505033-fac94fc0-51c7-415e-b373-699e581e0e29.png)

![05](https://user-images.githubusercontent.com/114581999/195505070-29cb2e68-3f66-4751-9acc-b3b58b60582a.png)

# ENCODING DATASET

![image](https://user-images.githubusercontent.com/114581999/195505291-af862fc1-4fff-4585-9b72-ee4fa9b0beff.png)

![07](https://user-images.githubusercontent.com/114581999/195505727-a6af1e6f-89a3-40aa-9dc6-bc05e318d4af.png)

![08](https://user-images.githubusercontent.com/114581999/195505776-3c4c2e59-4a61-4f80-93da-472e2e8f7deb.png)

![09](https://user-images.githubusercontent.com/114581999/195505792-ba03e237-0d15-4c87-9941-f4564ba3918d.png)

# TITANIC DATASET

![image](https://user-images.githubusercontent.com/114581999/195506099-81405cc6-d008-4578-a43f-43ea82e958ad.png)

![image](https://user-images.githubusercontent.com/114581999/195506210-63f7db6d-9a94-44fd-9162-f226c74fdf57.png)

![image](https://user-images.githubusercontent.com/114581999/195506320-c898611d-b192-4d36-8ad3-d5d7f7d3118c.png)

![image](https://user-images.githubusercontent.com/114581999/195506371-731aeba7-1295-49c2-a087-2c1379e90dc5.png)

![image](https://user-images.githubusercontent.com/114581999/195506528-374190fb-f344-4023-bc8d-64eedb856315.png)

![image](https://user-images.githubusercontent.com/114581999/195506618-71ff0060-6fc2-4185-b1f6-6979b341110d.png)

![image](https://user-images.githubusercontent.com/114581999/195506886-51d42f01-7544-49f6-ab6b-f2a66f3acfc1.png)






