# Ex-07-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
import pandas as pd
import seaborn as sns
df=pd.read_csv("/content/SuperStore (1).csv")
df.info()
df.isnull().sum()

![Screenshot 2022-11-21 181753](https://user-images.githubusercontent.com/95408668/203059215-458dd1d2-4e45-41f0-a0de-ca7b01d56059.jpg)

![Screenshot 2022-11-21 181857](https://user-images.githubusercontent.com/95408668/203059933-1ec29636-70b8-4d41-933d-3cefc45f2611.jpg)

import matplotlib.pyplot as plt
import numpy as np
sns.distplot(df['Sales'])
plt.axvline(x=np.mean(df['Sales']), c='red', ls='--', label='mean')
plt.axvline(x=np.percentile(df['Sales'],25),c='green', ls='--', label = '25th percentile:Q1')
plt.axvline(x=np.percentile(df['Sales'],75),c='orange', ls='--',label = '75th percentile:Q3' )
plt.legend()

![Screenshot 2022-11-21 181941](https://user-images.githubusercontent.com/95408668/203060016-f70f7b56-bf58-44f3-948a-0389867f5a07.jpg)

sns.boxplot(x=df['Segment'], y=df['Sales'])

![Screenshot 2022-11-21 182008](https://user-images.githubusercontent.com/95408668/203060582-651ec338-0f36-44bd-acd6-9ce132ab87b1.jpg)

sns.scatterplot(x=df['City'], y=df['Sales'])

![Screenshot 2022-11-21 182029](https://user-images.githubusercontent.com/95408668/203060664-eb712449-253e-4823-9196-676d6687ae17.jpg)

sns.boxplot(df['Region'], df['Sales'])

![Screenshot 2022-11-21 182051](https://user-images.githubusercontent.com/95408668/203060699-8cdd6d19-babc-4ea3-b261-6d8a0b3c562f.jpg)


