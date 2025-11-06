# Ejercicio 2

## Consigna

Hallar el dominio y los conjuntos de nivel de las siguientes funciones:

1. $\tfrac{x}{x-y-z}$
2. $\sin(x^2 + y^2 + z^2)$

## Resolución

### Función #1

- $\tfrac{x}{x-y-z}$

El dominio de esta función es el siguiente:

- $D=\{(x,y,z): x\neq y+z\}\subset\mathbb{R}^3$

Veamos ahora los conjuntos de nivel:

- Si $a\neq1$, entonces $\frac{x}{x-y-z}=a\to x=ax-a(y+z)\to x=\frac{-a(y+z)}{-a+1}$.
    Por lo tanto $C_a=\{(x,y,z)\in D: \frac{-a(y+z)}{-a+1}\}$

- Por otro lado, si $a=1$, tenemos que $\frac{x}{x-y-z}=1\to -y-z=0$.
    Por lo tanto $C_1=\{(x,y,z)\in D: -y=z\}$

### Función #2

- $\sin(x^2 + y^2 + z^2)$

Veamos los conjuntos de nivel, para esto observemos rápidamente que si $a\notin[0,1], C_a=\emptyset$, pues $\sin$ oscila en esos valores.

- Si $a\in[0,1]$, entonces: $\sin(x^2 + y^2 + z^2)=a\to x^2=\arcsin(a)-y^2-z^2\to x=\pm\sqrt{\arcsin(a)-y^2-z^2}$.
    Por lo tanto $C_a=\{(x,y,z)\in\mathbb{R}^3: x=\pm\sqrt{\arcsin(a)-y^2-z^2}\}$

Otra forma de verlo:

- $C_a=\{(x,y,z)\in\mathbb{R}^3: \|(x,y,z)\|^2=\arcsin(a)\}$