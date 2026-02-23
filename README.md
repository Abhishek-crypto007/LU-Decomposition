# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the required Python libraries and read the given square matrix.
2. Initialize the lower triangular matrix L and upper triangular matrix U.
3. Perform LU decomposition using row operations to compute L and U.
4. Display the L and U matrices and terminate the program.

## Program:
(i) To find the L and U matrix
```
'''Program to find L and U matrix using LU decomposition.
Developed by: ABHISHEK S
RegisterNumber: 212225100001
'''
import numpy as np
from scipy.linalg import lu
A=np.array(eval(input()))
P,L,U=lu(A)
print(L)
print(U)
```
(ii) To find the LU Decomposition of a matrix
```
'''Program to solve a matrix using LU decomposition.
Developed by: ABHISHEK S
RegisterNumber: 212225100001
'''
# To print X matrix (solution to the equations)
import numpy as np
from scipy.linalg import lu_factor,lu_solve
A=np.array(eval(input()))
B=np.array(eval(input()))
lu,pivot= lu_factor(A)
x=lu_solve((lu,pivot),B)
print(x)
```


## Output:
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/bf63d6df-703c-4f64-9f55-2c35a242f5e5" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/4821db99-1edf-46d9-bce1-24f5b6595dee" />


## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

