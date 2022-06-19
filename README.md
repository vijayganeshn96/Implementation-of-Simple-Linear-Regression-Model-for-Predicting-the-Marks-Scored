# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to implement the simple linear regression model for predicting the marks scored.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the packages required.
2. Read the datas from the file.
3. Assign the values to x,y and decler other datas.
4. Predict the scores of student.
5. Print the predicted datas.
6. Plot the points in the graph.
7. Get the best fit line.
8. Label the axis.
9. Draw a graph for Study hours vs Scores,
10. End .

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Vijay Ganesh N
RegisterNumber:  212221040177
*/

import numpy as np
import pandas as pd
import matplotlib.pyplot as py
data=pd.read_csv("student_scores .csv")
data.head()
data.isnull().sum()
x=data.Hours
x.head()
y=data.Scores
y.head()
n=len(x)
m=0
c=0
L=0.01
loss=[]
for i in range(10000):
    ypred=m*x+c
    MSE=(1/n)*sum((ypred-y)*2)
    dm=(2/n)*sum(x*(ypred-y))
    dc=(2/n)*sum(ypred-y)
    c=c-L*dc
    m=m-L*dm
    loss.append(MSE)
print(m,c)
y_pred=m*x+c
py.scatter(x,y,color="red")
py.plot(x,y_pred)
py.xlabel("study hours")
py.ylabel("Scores")
py.title("Study hours vs Scores")
py.plot(loss)
py.xlabel("iterations")
py.ylabel("loss")

```

## Output:
#### DATA HEAD:
![output](https://github.com/vijayganeshn96/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/blob/main/exp1.png)
#### X.HEAD:
![output](https://github.com/vijayganeshn96/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/blob/main/Screenshot%202022-05-02%20114349.png)
#### Y.HEAD
![output](https://github.com/vijayganeshn96/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/blob/main/Screenshot%202022-05-02%20114428.png)
#### GRAPH 1
![output](https://github.com/vijayganeshn96/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/blob/main/Screenshot%202022-05-02%20114502.png)
#### GRAPH 2
![output](https://github.com/vijayganeshn96/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/blob/main/Screenshot%202022-05-02%20114535.png)
## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
