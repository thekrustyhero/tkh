# tkh
Teste de programação em Python 
""" A partir de agora estes codigos são codigos que eu desenvolvi para aprendizado.
|||||||||| Vou utilizar os codigos, acima em novos exemplos.
"""

from matplotlib import pyplot as plt
import math

def calcular_raizes(a, b, c):
    delta = b**2 - 4*a*c
    if delta < 0:
        return None # raízes complexas
    elif delta == 0:
        x = -b / (2*a)
        return x, None
    else:
        x1 = (-b + math.sqrt(delta)) / (2*a)
        x2 = (-b - math.sqrt(delta)) / (2*a)
        return x1, x2

a = float(input("Digite o valor de a: "))
b = float(input("Digite o valor de b: "))
c = float(input("Digite o valor de c: "))

# Calcular as raízes usando a função calcular_raizes
raizes = calcular_raizes(a, b, c)
if raizes is None:
    print("Não existem raízes reais.")
else:
    print(f"As raízes são: {raizes}")

# Calcular o valor de y para alguns valores de x
x_values = []
y_values = []
for x in range(-10, 11):
    y = a*x**2 + b*x + c
    x_values.append(x)
    y_values.append(y)

# Plotar a parábola
plt.plot(x_values, y_values, color='blue')
plt.title("Gráfico da equação.")
plt.xlabel("x")
plt.ylabel("y")
plt.show()
