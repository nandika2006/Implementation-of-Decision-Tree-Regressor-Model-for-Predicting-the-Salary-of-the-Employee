# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas

2.Import Decision tree classifier

3.Fit the data in the model

4.Find the accuracy score
## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: NANDIKA S 
RegisterNumber: 212224230175
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
```
```
R2 score:  0.48611111111111116
```
```
dt.predict([[5,6]])
```



## Output:
<img width="546" height="426" alt="image" src="https://github.com/user-attachments/assets/c7524a17-7f92-443e-826d-92ef07050333" />

<img width="439" height="262" alt="image" src="https://github.com/user-attachments/assets/ba84a491-3335-4e75-9c9d-4cd312732716" />

<img width="258" height="287" alt="image" src="https://github.com/user-attachments/assets/b7d20beb-3e79-492c-b0f7-8566fe26da8e" />


<img width="245" height="35" alt="image" src="https://github.com/user-attachments/assets/e83573f8-494e-4e21-9752-c054d86aa21e" />

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
