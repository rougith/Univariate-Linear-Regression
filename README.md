# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
developed by : Rougith D
register no: 25017014
```
```
import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()


```
## Output

<img width="783" height="650" alt="{55E5E12B-A5FF-454F-95DB-E5B4B6F30846}" src="https://github.com/user-attachments/assets/e5e66a00-7d86-4b7b-ae86-85dfee4bd001" />

<img width="799" height="573" alt="{BFA2D58F-8698-48DA-8D0C-1374DE4A8D2D}" src="https://github.com/user-attachments/assets/f5018fa0-5347-444b-aed8-827c6da6b754" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
