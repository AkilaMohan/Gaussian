# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First,we want to import numpy,then import sys,assume a variable.
2. For gaussion elimination method,we want to make 2nd and 3rd column zero.
3. For that we want to make a range according to our program output.
4. Then print the program with correct from then the output will display.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: suryamalarv
RegisterNumber: 23013656
*/
```
```
import sys
import numpy as np 
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][j]==0.0:
        sys.exit("Divide by zero error")
    for j in range (i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```


## Output:
![image](https://github.com/AkilaMohan/Gaussian/assets/145742486/7b0c6129-40ab-4a7c-83cb-05358b2113f4)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

