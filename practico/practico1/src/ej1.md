# Ejercicio 1

## Consigna

Determinar los valores de $i^k$ para todo $k \in \mathbb{Z}$

## Resolución

Cálculemos:

- $i^0=1$
- $i^1=i$
- $i^2=-1$
- $i^3=i^2i=-i$
- $i^4=i^2i^2=1=i^0$

Con esto en mente, definiremos $i^k$ para todo entero $k\in\mathbb{N}$, ya que si la potencia es negativa podemos usar el resultado obtenido con la misma potencia pero positiva.

- Si $k$ es de la forma $k=4m$ para algún $m\in\mathbb{N}$, 
    - Entonces $i^k=1$
- Si $k$ es de la forma $k=4m+1$ para algún $m\in\mathbb{N}$, 
    - Entonces $i^k=i$
- Si $k$ es de la forma $k=4m+2$ para algún $m\in\mathbb{N}$, 
    - Entonces $i^k=-1$
- Si $k$ es de la forma $k=4m+3$ para algún $m\in\mathbb{N}$, 
    - Entonces $i^k=-i$

Esto concluye el ejercicio.