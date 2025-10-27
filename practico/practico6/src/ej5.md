# Ejercicio 5

## Consigna

Sean $A$ y $B$ dos conjuntos de $\mathbb{R}^n$. Se define el conjunto suma:

$$
A + B = \{a + b : a \in A,\ b \in B\}
$$

1. Demostrar que si $A$ es abierto, $A + B$ es abierto.
2. ¿Qué se puede decir de $A + B$ si $A$ es cerrado?

## Resolución

### Parte 1

- Demostrar que si $A$ es abierto, $A + B$ es abierto.

Consideremos un punto genérico $a+b\in A+B$, queremos demostrar que este punto es interior a $A+B$, es decir que existe $\delta>0$ tal que $B(a+b,\delta)\subset A+B$.

Como $A$ es abierto, tenemos que:

- Para $\delta_0>0:B(a,\delta_0)\subset A$

Haciendo un bosquejo de la situación en la que estamos parados, podemos darnos cuenta de que el candidato a $\delta$ para la bola $B(a+b,\delta)$ es $\delta_0$.
Por lo tanto ahora lo que queremos ver es que la bola mencionada está completamente incluida en $A+B$, para lo que consideramos $x\in B(a+b,\delta_0)$ y probamos que pertenece a $A+B$.

Para que $x\in A+B$, entonces $x=x_a+x_b$ con $x_a\in A$ y $x_b\in B$.
Podemos tomar $x_b=b$ que trivialmente pertenece a $B$ por como elegimos a $b$, lo que nos dejaría con:

- $x_a=x-b$

Para terminar la demostración, tenemos que probar que $x_a\in A$, para lo que va a ser más fácil probar que $x_a\in B(a,\delta_0)$ (completamente incluida en $A$ porque $A$ es abierto).

Como $x\in B(a+b,\delta_0)$, tenemos que $d(a+b,x)<\delta_0$, además podemos operar de la siguiente forma:

$$
d(a+b,x)=d(a+b,x_a+b)=\|a+b-x_a-b\|=\|a-x_a\|=d(a,x_a)< \delta_0
$$

Entonces, como $d(a,x_a)<\delta_0$, $x_a\in B(a,\delta_0)\subset A$. Por lo que $x_a\in A$, y entonces $x\in A+B$.

### Parte 2

- ¿Qué se puede decir de $A + B$ si $A$ es cerrado?

No se puede decir nada en este caso sobre $A+B$, veamos dos casos de conjuntos que cumplen con la hipótesis pero el comportamiento de $A+B$ es distinto:

#### Caso 1: $A+B$ cerrado

- $A=\{(x,y)\in\mathbb{R}^2:0\leq x\leq 1, 1\leq y\leq 2\}$
- $B=\{(1,1)\}$
- $A+B=\{(x,y)\in\mathbb{R}^2:1\leq x\leq 2, 2\leq y\leq 3\}$

Donde $A+B$ es claramente cerrado.

#### Caso 2: $A+B$ abierto

- $A=\{-n: n\in\mathbb{N}, n\geq 2\}$
- $B=\{n+\frac{1}{n}:n\in\mathbb{N}, n\geq 2\}$

Recordemos que un conjunto cerrado contiene a todos sus puntos de acumulación. Verificaremos que $A+B$ es abierto probando que $0\notin A+B$ pero que $0$ es un punto de acumulación de $A+B$.

Lo primero se verifica fácil pues $B$ no contiene numeros enteros, y restarle un número entero a uno racional nunca dará 0.
Para lo segundo, observemos que en $A+B$ tenemos una sucesión de elementos de la forma $(-n)+(n+\frac{1}{n})=\frac{1}{n}$ para $n\geq2$, la cual converge a $0$.
