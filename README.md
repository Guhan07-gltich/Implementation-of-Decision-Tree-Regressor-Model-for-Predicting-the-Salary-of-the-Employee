# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Open Jupyter Notebook. 
2.Create a new Python notebook.
3.Type the Python program in the cell. 
4.Press Shift + Enter to run the code and view the output. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Rajalakshmi V
RegisterNumber: 212225040327 
*/
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor, plot_tree
data = pd.read_csv("Salary (1).csv")
X = data.drop("Salary", axis=1)
y = data["Salary"]
X = pd.get_dummies(X, drop_first=True)
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42)
model = DecisionTreeRegressor(random_state=42)
model.fit(X_train, y_train)
plt.figure(figsize=(25,12))
plot_tree(
    model,
    feature_names=X.columns,
    filled=True
)

plt.title("Decision Tree Regressor")
plt.show()

```

## Output:
<img width="1290" height="611" alt="image" src="https://github.com/user-attachments/assets/4090b2f0-d149-450b-89ef-e6333affbc87" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
