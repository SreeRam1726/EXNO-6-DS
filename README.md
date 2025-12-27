# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

```
 import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()

```

<img width="1555" height="263" alt="image" src="https://github.com/user-attachments/assets/c419f1e5-c9ce-4cd1-9db4-377ccde19e11" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')

```

<img width="695" height="570" alt="image" src="https://github.com/user-attachments/assets/5e486dc2-2b04-4f85-ae63-959deffad43e" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')

```

<img width="688" height="584" alt="image" src="https://github.com/user-attachments/assets/5831acd1-e376-4599-b241-f2a5f7ce9c24" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

```

<img width="1628" height="719" alt="image" src="https://github.com/user-attachments/assets/38e0c54a-f16a-414c-a66e-c3c659e6f73e" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()

```

<img width="768" height="583" alt="image" src="https://github.com/user-attachments/assets/e0bd397f-849a-45a0-be2e-30fa89d07470" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

```

<img width="748" height="570" alt="image" src="https://github.com/user-attachments/assets/b4e67a53-c933-42f4-9837-25ed993689e6" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

```

<img width="762" height="560" alt="image" src="https://github.com/user-attachments/assets/42cec6c5-9f46-4037-b5cc-db5e55f89d35" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")

```

<img width="1630" height="702" alt="image" src="https://github.com/user-attachments/assets/2becbf1b-6b7d-4b08-b4d6-dcf19d551f25" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

```

<img width="803" height="579" alt="image" src="https://github.com/user-attachments/assets/a8a9fb1f-f2ad-44f2-aa4e-cba03125c6e9" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()

```

<img width="768" height="705" alt="image" src="https://github.com/user-attachments/assets/2d234ebe-0121-45b4-8a59-25aa91bdac96" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

```

<img width="785" height="638" alt="image" src="https://github.com/user-attachments/assets/3fd3374d-c7f6-4ef4-a6da-495a34d74cb9" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.

