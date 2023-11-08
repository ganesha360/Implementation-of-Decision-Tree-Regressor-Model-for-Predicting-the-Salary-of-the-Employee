# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the libraries and read the data frame using pandas.

2.Calculate the null values present in the dataset and apply label encoder.

3.Determine test and training data set and apply decison tree regression in dataset.

4.calculate Mean square error,data prediction and r2.

## Program:
```PYTHON
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: GANESH R
RegisterNumber:  212222240029
*/
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: A.Anbuselvam
RegisterNumber: 212222240009
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
## data.head():
![ML1](https://github.com/ganesha360/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120884552/46ddc0cc-57d4-4f55-8207-300caa6a26af)

## data.info():

![ML2](https://github.com/ganesha360/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120884552/3495b687-3a9c-4964-8dc7-42d5b6bf7012)

## isnull() & sum() function:

![ML3](https://github.com/ganesha360/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120884552/d0659c59-4a1b-4c34-a413-1ad78d18bd74)


## data.head() for position:

![ML4](https://github.com/ganesha360/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120884552/1ce86894-dc16-448e-8660-23c8905e2ef7)

## MSE value:

![ML5](https://github.com/ganesha360/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120884552/11a5be37-716e-4769-ab16-ef59752a4221)

## R2 value:

![ML6](https://github.com/ganesha360/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120884552/b2691ce7-a67f-4ede-99f7-a0cce0d90049)

## Prediction value:

![ML7](https://github.com/ganesha360/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/120884552/11be8f9b-841f-487d-ac1f-5a2388e26d9b)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
