# Circuito-RC
import numpy as np

R = 10e3
C = 100e-9
Vp = 1

frecuencias = [10, 159, 1000]

RC = R * C

print("SOLUCION ANALITICA")
print("----------------------------")
print(" Frecuencia | Vout")

for f in frecuencias:

    w = 2 * np.pi * f

    Vout = Vp / np.sqrt(1 + (w * RC)**2)

    print(f"{f:8} Hz | {Vout:.3f} V")
