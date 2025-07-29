# Ejercicio 8

## Consigna

Sea $\{z_1, \dots, z_8\}$ el conjunto de raíces octavas de $2^8$, es decir, $z_k^8 = 2^8$ para $k = 1,\dots,8$. Determinar cuáles afirmaciones son verdaderas y cuáles falsas:

1. $z_i = 2$ para todo $i = 1,\dots,8$  
2. Existen al menos dos raíces $z_j,\ z_k$ tales que $z_j = -z_k$  
3. Existen al menos dos raíces $z_l,\ z_m$ tales que $\bar{z}_l = z_m$  
4. Se cumple que $z_1 z_2 \cdots z_8 = 2^8$

## Resolución

Antes de empezar a evaluar las afirmaciones, hallemos las raíces octavas de $2^8$.

Sea $z=re^{i\theta}$, entonces tenemos que:

- $(re^{i\theta})^8 = 2^8$

De donde derivamos las siguientes ecuaciones:

- $r^8=2^8\to r=2$ y,
- $8\theta=2k\pi\to\theta=\frac{k\pi}{4}\quad\text{con }k\in\mathbb{Z}$

Entonces las raíces octavas de $2^8$ son las siguientes:

- $z_0=2$
- $z_1=2e^{i\frac{\pi}{4}}$
- $z_2=2e^{i\frac{\pi}{2}}=2i$
- $z_3=2e^{i\frac{3\pi}{4}}$
- $z_4=2e^{i\pi}=-2$
- $z_5=2e^{i\frac{5\pi}{4}}$
- $z_6=2e^{i\frac{3\pi}{2}}=-2i$
- $z_7=2e^{i\frac{7\pi}{4}}$

### Afirmación 1

- $z_i = 2$ para todo $i = 1,\dots,8$ 

Claramente FALSO.

### Afirmación 2

- Existen al menos dos raíces $z_j,\ z_k$ tales que $z_j = -z_k$

Esto es VERDADERO, pues $z_0=2$ y $z_4=-2$

### Afirmación 3

- Existen al menos dos raíces $z_l,\ z_m$ tales que $\bar{z}_l = z_m$

Esto es VERDADERO, pues $z_2=2i$ y $z_6=-2i$.

### Afirmación 4

- Se cumple que $z_1 z_2 \cdots z_8 = 2^8$

Para esto habría que verificar que la suma de argumentos de las raíces sea $0+2k\pi$ para algún $k\in\mathbb{Z}$, verifiquemos:

$$
\begin{aligned}
&\sum_{i=0}^{7}\frac{i\pi}{4}=\frac{28\pi}{4}=7\pi
\end{aligned}
$$

Como el argumento no es $0+2k\pi$ para algún $k\in\mathbb{Z}$ podemos afirmar que el resultado no es real. Por lo tanto esta afirmación es FALSA.