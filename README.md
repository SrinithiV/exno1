# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
## DATA CLEANING PROCESS
```py
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df
```

```py
df.head(5)
```

```py
df.tail(5)
```

```py
df.info()
```

```py
df.describe()
```

```py
df.shape
```

```py
df.isnull().sum()
```

```py
df.nunique()
```

```py
df['GENDER'].value_counts()
```

```py
df.dropna(how='any').shap
```

```py
df.shape
```

```py
x1=df.dropna(how='any')
x1
```

```py
x2=df.dropna(how='all')
x2
```

```py
tot=df.dropna(subset=['TOTAL'],how='any')
tot
```

```py
tot=df.dropna(subset=['M1','M2','M3','M4'],how='any')
tot
```

```py
s=df.fillna(method='ffill')
s
```

```py
df.isna().sum()
```

```py
df['M1']
```

```py
df.isnull()
```

```py
df.notnull()
```

```py
x1=df.dropna(axis=0)
x1
```

```py
df.duplicated()
```

```py
m=df.drop_duplicates(inplace=False)
m
```

```py
import seaborn as sns
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
```
![image](https://github.com/user-attachments/assets/a12b151a-9edc-4281-92b2-543d7bb21fa4)

```py
df.dropna(inplace=True)
```
```py
sns.heatmap(df.isnull(), yticklabels=False, annot=True)
```
![image](https://github.com/user-attachments/assets/d8b6d2f3-9dac-4148-947a-3cdb68a20297)

```py
df.loc[0:3]
```

```py
df.dtypes
```

```py
df.filter(regex='a', axis=1)
```

```py
```


# Result
   Thus the program to perform data cleaning and save the cleaned data to a file is successfully executed.
