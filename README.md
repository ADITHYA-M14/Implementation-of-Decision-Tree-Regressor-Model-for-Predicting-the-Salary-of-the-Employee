# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2. Import Decision tree classifier
3. Fit the data in the model
4. Find the accuracy score

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: ADITHYA M 
RegisterNumber: 212224230008
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
```
```
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
## Output :
<img width="958" height="299" alt="image" src="https://github.com/user-attachments/assets/4ec0ef8a-0855-4f67-b340-a0d4441dcab2" />
<img width="399" height="195" alt="image" src="https://github.com/user-attachments/assets/172614bf-ee85-4539-8a07-4e2512d1a62c" />
<img width="697" height="131" alt="image" src="https://github.com/user-attachments/assets/fd9979af-dfe1-47f9-86a6-29aaadd469ed" />
<img width="323" height="35" alt="image" src="https://github.com/user-attachments/assets/1e240ff9-40a4-4529-8aa5-d4d7315c4473" />
<img width="200" height="35" alt="image" src="https://github.com/user-attachments/assets/7589f94f-0fa6-4bf2-8d3e-9ee91a376927" />

## Result :
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.

