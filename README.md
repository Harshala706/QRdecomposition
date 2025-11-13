# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method
```
import numpy as np
import matplotlib.pyplot as plt
X = np.array(eval(input()))
Y = np.array(eval(input()))
xmean = np.mean(X)
ymean = np.mean(Y)
num, den = 0,0
for i in range(len(X)):
    num += (X[i]-xmean)*(Y[i]-ymean)
    den += (X[i]-xmean)**2
    slope = num/den
    c = ymean-slope*xmean
    y_pred = slope*X + c
    print(y_pred)
    plt.scatter(X,Y,color = "red")
    plt.plot(X,y_pred,color="blue")
    plt.show()








```

## Output

![WhatsApp Image 2025-11-13 at 11 01 44_329316d3](https://github.com/user-attachments/assets/e5a4786b-842f-455a-b932-353d29cb620c)

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
