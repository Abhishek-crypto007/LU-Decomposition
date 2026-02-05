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
import ast
import numpy as np
def lu(A):
    A=np.array(A, dtype=float)
    n=len(A)
    L=np.eye(n)
    U=A.copy()
    P=np.eye(n)
     
    for  i in range(n):
        p = i + np.argmax(abs(U[i:, i]))
        U[[i,p]] = U[[p,i]]
        P[[i,p]] = P[[p,i]]
        L[[i,p], :i] = L[[p,i], :i]
        
        for j in range(i+1,n):
            L[j,i] = U[j,i] / U[i,i]
            U[j] -= L[j,i]*U[i]
    
    return P,L,U        
# A= [list(map(float, input().split())) for _ in range(3)]
A= ast.literal_eval(input())
_,L,U= lu(A) 
print(L)
print(U)
```
(ii) To find the LU Decomposition of a matrix
```
'''Program to find L and U matrix using LU decomposition.
Developed by: ABHISHEK S
RegisterNumber: 212225100001
'''
import numpy as np
from scipy.linalg import lu,solve
A=np.array([[3,2,7],[2,3,1],[3,4,1]], dtype=float)
b=np.array([4,5,7], dtype=float)
P,L,U=lu(A)
y=np.linalg.solve(L,np.dot(P,b))
x=np.linalg.solve(U,y)
print(x)
```


## Output:
<img width="1366" height="768" alt="Screenshot (161)" src="https://github.com/user-attachments/assets/7c666005-dedd-480b-96ba-3484e2afb448" />
<img width="1366" height="768" alt="Screenshot (162)" src="https://github.com/user-attachments/assets/1b73871c-13bc-4e48-9c20-d2660cbdc74c" />


## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

