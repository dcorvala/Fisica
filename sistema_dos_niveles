
# Usé módulos numpy, math 

import numpy as np
import math
from math import factorial

# Armé la función para calcular el combinatorio

def nucomb(m, n):
  return factorial(m) // (factorial(n) * (factorial(m - n)))

# Defino los valores de las variables

M=8
g1=6
g2=6
L=g1+g2
epsilon1=-1
epsilon2=+1

nivel1=[]
nivel2=[]
E=[]
deg=[]

# El programita

if g1>=M and g2>=M:
    for i in range(M+1):
      nivel1.append(M-i)
      nivel2.append(i)
      E.append((epsilon1)*nivel1[i]+(epsilon2)*nivel2[i])
      deg.append(nucomb(g1, nivel1[i])*nucomb(g2, nivel2[i]))
elif g1>=M and g2==M:
    for i in range(M-g1, M+1):
      nivel1.append(M-i)
      nivel2.append(i)
      E.append((epsilon1)*nivel1[i-(M-g1)]+(epsilon2)*nivel2[i-(M-g1)])
      deg.append(nucomb(g1, nivel1[i-(M-g1)])*nucomb(g2, nivel2[i-(M-g1)]))
else:
    i=0
    while i <= g2-(M-g1):
         nivel1.append(g1-i)
         nivel2.append(M-g1+i)
         E.append((epsilon1)*nivel1[i]+(epsilon2)*nivel2[i])
         deg.append(nucomb(g1, nivel1[i])*nucomb(g2, nivel2[i]))
         i=i+1

# Hacemos la prueba

print("n1:", nivel1)
print("n2:",nivel2)
print(":",E)
print("degeneracion en energía", deg)
