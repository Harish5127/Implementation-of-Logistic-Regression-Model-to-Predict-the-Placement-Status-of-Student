# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import the necessary libraries from python to execute the given code.
2. perform the logistic Regression on the given datasets.
3. perform the necessary opration to get the placement status whether placed or not placed.
4. print the predictive value of the model odf placement status.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Harish R
RegisterNumber: 212224230085
*/
```
```
import pandas as pd
from sklearn.metrics import accuracy_score,classification_report
data=pd.read_csv("C:\\Users\\admin\\OneDrive\\Attachments\\New folder (2)\\Placement_Data.csv")
data.head()
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
data1.isnull()
data1.duplicated().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1['gender']=le.fit_transform(data1['gender'])
data1['ssc_b']=le.fit_transform(data1['ssc_b'])
data1['hsc_b']=le.fit_transform(data1['hsc_b'])
data1['hsc_s']=le.fit_transform(data1['hsc_s'])
data1['degree_t']=le.fit_transform(data1['degree_t'])
data1['workex']=le.fit_transform(data1['workex'])
data1['specialisation']=le.fit_transform(data1['specialisation'])
data1['status']=le.fit_transform(data1['status'])
data1
x=data1.iloc[:,:-1]
x
y=data1['status']
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lrt.predict(x_test)
y_predfrom sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy
from sklearn.metrics import classification_report 
classification_report1=classification_report(y_test,y_pred) 
print(classification_report1)
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])
```

## Output:

![Screenshot 2025-03-19 220608](https://github.com/user-attachments/assets/b8a6f37c-2b6a-4a73-819d-8759e7756cce)
![Screenshot 2025-03-19 220625](https://github.com/user-attachments/assets/587a6b43-6d3c-41d1-8e4f-84977e0841a6)
![Screenshot 2025-03-19 220638](https://github.com/user-attachments/assets/e833d2d7-8f7c-4a27-b664-b07f49dfe2aa)
![Screenshot 2025-03-19 220659](https://github.com/user-attachments/assets/5a1cee94-1bcf-441a-9b64-848bf32ea720)
![Screenshot 2025-03-19 220713](https://github.com/user-attachments/assets/ebb47125-4628-431f-ac2a-29d16e39243c)
![Screenshot 2025-03-19 220731](https://github.com/user-attachments/assets/66979fe7-fcab-4ef8-a90f-64174f1b7b78)
![Screenshot 2025-03-19 220743](https://github.com/user-attachments/assets/d2c5282b-b4ed-49f3-9d42-821643fb0ee0)
![Screenshot 2025-03-19 220800](https://github.com/user-attachments/assets/c3fbabda-989a-4ce2-9b70-eec242ffa219)



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
