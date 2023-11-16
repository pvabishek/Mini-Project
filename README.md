# Mini project 
## DATE:
# Credit_Data Analysis.
# Aim : Analysis Of Credit Data in Data Science.
## Procedure:
### Step:1 Importing necessary packages
### Step:2 read the data set
### Step:3 Execute the methods
### Step:4 run the program
### Step:5 get the output







# Program And Output:
# Importing necessary packages:
~~~
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
~~~

# read the data set:
~~~
df=pd.read_csv("/content/credit_data_1.csv")
df
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/8647ab28-1c0e-45e9-b455-c7dc78cc5af3)

~~~
df.head()
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/ea03864a-7c7e-4191-9906-d732b8f1a6f2)

~~~

df.info()
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/355ca917-f885-43bc-8ff6-2848e576a3b6)

~~~
df.tail()
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/42d26abd-6e3a-4e58-9f81-65154aea3633)

~~~
df.describe()
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/1f1122fd-6031-43d7-8cfe-24d5986b0c61)

~~~
df.shape
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/686642b4-0735-4671-84b4-98a9a05d36b5)

~~~
df['dependents'].value_counts()
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/8721bc98-84ce-4fa6-a77b-8df7e80eee82)


# label encoder:
~~~
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

df['dependents'] = le.fit_transform(df['dependents'])
df.head(10)
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/3d927422-d6e9-4bbb-8ce0-76478f2bbf70)


# data cleaning:
~~~
df.isnull().sum()
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/471b093e-8dc8-4e5f-ba7b-2e9d45fe2c8d)

~~~
missing_percentage = (df.isnull().sum())/(df.shape[0])*100
missing_percentage
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/459ad9e2-c93e-43ff-b8c6-4511af6ade70)

~~~
df.duplicated().value_counts()
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/2bb60574-124f-43ea-8659-be91368a869a)


# Univariate Analysis:
~~~
sns.boxplot(y="dependents",data=df)
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/95353a7b-0c9a-489d-be68-0baae8e29f7b)

~~~
sns.countplot(y="dependents",data=df)
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/71d310f1-7af1-4784-ac7d-c522f82a675e)

~~~
sns.histplot(y="dependents",data=df)
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/f0672ed2-a538-4697-a28f-07c0019b1903)


# Multivariate Analysis:

~~~
sns.scatterplot(df['income'],df['expenditure'])
~~~

![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/ef71da8c-7817-4de2-8144-77615913d5de)


~~~
sns.barplot(data=df, x='income', y='owner')
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/97f34d7a-d07d-4c1e-983a-27ea8d06ddf5)


~~~
df.corr()
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/3de43d8f-918f-4241-af4b-f7918f3ce423)

~~~
sns.heatmap(df.corr(),annot=True)
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/66b6cced-7910-45a6-9115-04f7780d75cf)

# Data Visualization:
~~~
plt.figure(figsize=(20, 7))
sns.lineplot(data=df, x='age', y='expenditure')
plt.show()
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/39e82ae1-a009-4fdb-90bd-ae290e28ce8c)

~~~
sns.kdeplot(x=df['active'],data=df)
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/a436a7b3-1317-4316-a70c-aac1925246dd)

~~~
sns.countplot(y="card",data=df)
~~~
![image](https://github.com/AaronDominic/Mini-Project/assets/143015231/4da8d842-a493-4f6e-89f1-32621b6c6d81)

### Result:
Hence the program to analyze the data set using data science is applied sucessfully.# Mini-Project
