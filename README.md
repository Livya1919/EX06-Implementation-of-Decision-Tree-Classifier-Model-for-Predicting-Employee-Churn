# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the Dataset: Use pandas to load the dataset (CSV, Excel, etc.) into a DataFrame.
2. Handle Missing Values: Identify and fill or drop missing values.
3. Encode Categorical Variables: Use label encoding or one-hot encoding for categorical data (e.g., department, gender).
4. Split the Dataset: Divide the dataset into features (X) and target (y), then split into training and testing sets.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Livya Dharshini G
RegisterNumber: 2305001013  
*/
import pandas as pd
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv("/content/Employee_EX6.csv")
data=df.copy()
data
le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data
x=data.drop(['Departments','left'],axis=1)
y=data['left']
clf=DecisionTreeClassifier()
clf.fit(x,y)
plt.figure(figsize=(80,80))
plot_tree(clf,feature_names=x.columns,class_names=['LEFT','NOT LEFT'],filled=True)
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/71685175-61c7-426f-99a8-3b127d0873f9)
![image](https://github.com/user-attachments/assets/a083bc1d-0dc7-4522-a1bb-bf9732a753e4)




## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
