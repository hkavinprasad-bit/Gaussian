# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module to use the built-in functions for calculation
2. Prepare the lists from each linear equations and assign in np.array()
3. Using the row.append(float(input())) and a.append(row)
4.End the program 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: 
RegisterNumber: 
*/'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by:H.Kavin prasad
RegisterNumber:212225040178
'''
n=int(input())

a = []
for i in range(n):
    row = []
    for j in range(n+1):
        row.append(float(input()))
    a.append(row)

for k in range(n):
    for i in range(k+1, n):
        factor = a[i][k] / a[k][k]
        for j in range(k, n+1):
            a[i][j] = a[i][j] - factor * a[k][j]

x= [0]*n

for i in range(n-1, -1, -1):
    s = 0
    for j in range(i+1, n):
        s += a[i][j] * x[j]
        
    x[i] = (a[i][n] - s) / a[i][i]
    
for i in range(n):
    print(f"X{i} = {x[i]:.2f}", end=" ")
 
```

## Output:
![gaussian elimination]()
<img width="1919" height="975" alt="Screenshot 2026-03-25 144729" src="https://github.com/user-attachments/assets/85f1774e-3380-43d1-bd36-2364e566ce6a" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

