# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
train = pd.read_csv('/content/titanic_dataset.csv')
train.head()
![image](https://github.com/23007965/EXNO2DS/assets/138971238/ee24e4c9-c16e-465f-a433-0d300604b652)
train.isnull()
![image](https://github.com/23007965/EXNO2DS/assets/138971238/68c1f184-9d1a-4dd8-82a3-24eb11c37caf)
sns.heatmap(train.isnull(),yticklabels=False,cbar=False,cmap='viridis')
![image](https://github.com/23007965/EXNO2DS/assets/138971238/a1de2e68-b568-4e8d-906f-7a422d40bbca)
sns.set_style('whitegrid')
sns.countplot(x='Survived',data=train)
![image](https://github.com/23007965/EXNO2DS/assets/138971238/3b4507b3-a7bf-48fc-8270-b26379fbf691)
sns.set_style('whitegrid')
sns.countplot(x='Survived',hue='Sex',data=train,palette='RdBu_r')
![image](https://github.com/23007965/EXNO2DS/assets/138971238/469b3dca-a3ec-4c5b-843c-2c8e93182317)
sns.set_style('whitegrid')
sns.countplot(x='Survived',hue='Pclass',data=train,palette='rainbow')
![image](https://github.com/23007965/EXNO2DS/assets/138971238/7973fba3-5ac5-41a9-a662-1255b5861e31)
sns.distplot(train['Age'].dropna(),kde=False,color='darkred',bins=40)
![image](https://github.com/23007965/EXNO2DS/assets/138971238/e0b9dcea-6c55-40e7-b3f4-92261a27508e)
train['Age'].hist(bins=30,color='darkred',alpha=0.3)
![image](https://github.com/23007965/EXNO2DS/assets/138971238/8b44c6eb-269b-48b1-9188-b0aecd20d381)
sns.countplot(x='SibSp',data=train)
![image](https://github.com/23007965/EXNO2DS/assets/138971238/af9fabfe-5995-4644-a694-df3fdc7d26e7)
train['Fare'].hist(color='green',bins=40,figsize=(8,4))
![image](https://github.com/23007965/EXNO2DS/assets/138971238/932efb7a-42f5-436e-8c10-b3fb194643e2)
```

# RESULT
        <<INCLUDE YOUR RESULT HERE>>
