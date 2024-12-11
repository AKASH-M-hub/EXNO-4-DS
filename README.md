# EXNO:4-DS
# AIM:
To read the given data and perform Feature Scaling and Feature Selection process and save the
data to a file.

# ALGORITHM:
STEP 1:Read the given Data.
STEP 2:Clean the Data Set using Data Cleaning Process.
STEP 3:Apply Feature Scaling for the feature in the data set.
STEP 4:Apply Feature Selection for the feature in the data set.
STEP 5:Save the data to the file.

# FEATURE SCALING:
1. Standard Scaler: It is also called Z-score normalization. It calculates the z-score of each value and replaces the value with the calculated Z-score. The features are then rescaled with x̄ =0 and σ=1
2. MinMaxScaler: It is also referred to as Normalization. The features are scaled between 0 and 1. Here, the mean value remains same as in Standardization, that is,0.
3. Maximum absolute scaling: Maximum absolute scaling scales the data to its maximum value; that is,it divides every observation by the maximum value of the variable.The result of the preceding transformation is a distribution in which the values vary approximately within the range of -1 to 1.
4. RobustScaler: RobustScaler transforms the feature vector by subtracting the median and then dividing by the interquartile range (75% value — 25% value).

# FEATURE SELECTION:
Feature selection is to find the best set of features that allows one to build useful models. Selecting the best features helps the model to perform well.
The feature selection techniques used are:
1.Filter Method
2.Wrapper Method
3.Embedded Method

# CODING AND OUTPUT:
from google.colab import drive

drive.mount('/content/drive')

![image](https://github.com/user-attachments/assets/4900ad98-3562-4b76-98f7-59070731f596)

ls drive/MyDrive/'Colab Notebooks'/bmi.csv

![image](https://github.com/user-attachments/assets/3a7026f1-9cea-4230-a7ce-897929b1120a)

ls drive/MyDrive/'Colab Notebooks'/'income(1) (1).csv'

![image](https://github.com/user-attachments/assets/3e5342aa-8cd4-49c0-a284-07a93a2ffe16)

import pandas as pd

import numpy as np

from scipy import stats

df=pd.read_csv("drive/MyDrive/Colab Notebooks/bmi.csv")

df

![image](https://github.com/user-attachments/assets/66b01c1f-5c5d-4742-a3ba-c867496a4220)

df.head()

![image](https://github.com/user-attachments/assets/2cb24a8f-eb6c-4db1-9adb-be8d949b4e5c)

df.dropna()

![image](https://github.com/user-attachments/assets/bab1b2e5-9529-4c17-a4c1-b8f8ffd8e486)

max_vals = np.max(np.abs(df[['Height','Weight']]))

max_vals

max_vals

df1=pd.read_csv("drive/MyDrive/Colab Notebooks/bmi.csv")

df1

![image](https://github.com/user-attachments/assets/b3b19cd1-740d-4110-ad9a-1fab3251f31b)

from sklearn.preprocessing import StandardScaler

sc=StandardScaler()

df1[['Height','Weight']] = sc.fit_transform(df1[['Height','Weight']])

df.head(10)

![image](https://github.com/user-attachments/assets/7b7a58ec-ab92-4161-97f8-50c75c63ca9f)

from sklearn.preprocessing import MinMaxScaler

Scaler=MinMaxScaler()

df[['Height','Weight']]=Scaler.fit_transform(df[['Height','Weight']])

df.head(0)

![image](https://github.com/user-attachments/assets/c2be355a-0f40-4146-90e6-62dd9a892e3a)

df2=pd.read_csv("drive/MyDrive/Colab Notebooks/bmi.csv")

df2

![image](https://github.com/user-attachments/assets/501600e7-fd7e-46d7-a70d-e65cc3d4a5fc)

from sklearn.preprocessing import Normalizer

Scaler=Normalizer()

df2[['Height','Weight']]=Scaler.fit_transform(df2[['Height','Weight']])

df2

![image](https://github.com/user-attachments/assets/aaaa5ce3-949e-4b7c-89f3-d3e3f3b49932)

df3=pd.read_csv("drive/MyDrive/Colab Notebooks/bmi.csv")

df3

![image](https://github.com/user-attachments/assets/a4944ea6-2e3b-460f-96ab-3f41c7c9ed10)

from sklearn.preprocessing import MaxAbsScaler

Scaler=MaxAbsScaler()

df3[['Height','Weight']]=Scaler.fit_transform(df3[['Height','Weight']])

df3

![image](https://github.com/user-attachments/assets/731fc06f-c840-4992-ab59-9529c2a80cb9)

df4=pd.read_csv("drive/MyDrive/Colab Notebooks/bmi.csv")

from sklearn.preprocessing import RobustScaler

Scaler=RobustScaler()

df4[['Height','Weight']]=Scaler.fit_transform(df4[['Height','Weight']])

df4.head()

![image](https://github.com/user-attachments/assets/0913fa02-ca57-4421-8426-474eed5ed692)

import matplotlib

import matplotlib.pyplot as plt

import seaborn as sns

import statsmodels.api as sm

from sklearn.model_selection import train_test_split

from sklearn.linear_model import LinearRegression

from sklearn.feature_selection import RFE

from sklearn.linear_model import RidgeCV,LassoCV,Ridge,Lasso

from sklearn.feature_selection import SelectKBest

from sklearn.feature_selection import mutual_info_classif

from sklearn.feature_selection import mutual_info_regression

from sklearn.feature_selection import chi2

df=pd.read_csv('drive/MyDrive/Colab Notebooks/income(1) (1).csv')

df.columns

![image](https://github.com/user-attachments/assets/216b7e14-e997-43b9-9828-ad451d4bc71c)

df1.columns

![image](https://github.com/user-attachments/assets/16647dd2-97b4-40c8-8dfd-a78123f6180a)

import pandas as pd

from sklearn.feature_selection import SelectKBest

from sklearn.feature_selection import chi2

data=pd.read_csv('drive/MyDrive/Colab Notebooks/bmi.csv')

data=data.dropna()

df.columns

df

![image](https://github.com/user-attachments/assets/442c4b33-31a1-4f43-84db-d3bc4db52d50)

import pandas as pd

import numpy as np

from scipy.stats import chi2_contingency

import seaborn as sns

tips=sns.load_dataset('tips')

tips.head()

![image](https://github.com/user-attachments/assets/da8827a4-eec7-4d2c-bf63-b9ee39437774)



# RESULT:
     THUS THE ABOVE CODE IS EXECUETED SUCCESSFULLY

