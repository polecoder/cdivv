# Ejercicio 7

## Consigna

Dibuje el dominio, los conjuntos de nivel y la gráfica de las siguientes funciones:

1. $x^2 + y^2$
2. $x^2 - y^2$
3. $x^2$
4. $y/x$
5. $xy$
6. $\max\{x^2, y^3\}$
7. $\max\{x^2, x + y\}$

## Resolución

### Aclaración

No haremos gráficas de las funciones para este ejercicio, aunque la estrategia para hacerlo es relativamente fácil:

1. Obtener los conjuntos de nivel.
2. Obtener el comportamiento de la función en los ejes (mandando a 0) a alguna de las dos variables. 

### Función #1

- $x^2 + y^2$

Veamos los conjuntos de nivel:

- Si $a<0$ entonces $C_a=\emptyset$, la función es la suma de dos valores siempre positivos, nunca puede dar menos de 0.
- Si $a\geq 0$, entonces quiero estudiar cuando $x^2+y^2=a$.
    Notemos que $x^2+y^2=\|(x,y)\|^2$, por lo tanto lo que queremos estudiar es $\|(x,y)\|^2=a$.
    De esto se desprende que $C_a=\{(x,y):\|(x,y)\|=\sqrt{a}\}$

### Función #2

- $x^2 - y^2$

Veamos los conjuntos de nivel:

Para este caso quizás es más fácil calcular el conjunto de nivel algunos valores de $a$.

**Caso $a=0: x^2-y^2=0$:**

Por lo tanto $x^2=y^2$, es decir que $x=y$. Entonces:

- $C_0=\{(x,y): x=y\}$

**Caso $a>0$: $x^2-y^2=a$:**

Despejando: $x^2=a+y^2\to x=\pm\sqrt{a+y^2}$.
Entonces tenemos que $C_a=\{(x,y): x=\pm\sqrt{a+y^2}\}$.

**Caso $a<0:x^2-y^2=a$:**

Despejando $-y^2=a-x^2\to y=\pm\sqrt{x^2-a}$.
Entonces tenemos que $C_a\{(x,y):y=\pm\sqrt{x^2-a}\}$

Notemos que en los casos donde $a\neq0$ elegimos de forma cuidadosa a quién despejar para evitar la posibilidad de que el radicando sea negativo.

### Función #3

- $x^2$

Veamos los conjuntos de nivel:

- Si $a<0: C_a=\emptyset$
- Si $a>0$, tenemos que $x^2=a\leftrightarrow x=\pm\sqrt{a}$, por lo tanto $C_a=\{(x,y)\in\mathbb{R}^2:x=\sqrt{a}\}$

### Función #4

- $y/x$

En este caso es importante observar que el dominio no puede ser todo $\mathbb{R}^2$ como en los casos anteriores, así que lo miramos con más detalle en este caso:

- $D=\{(x,y)\in\mathbb{R}^2: x\neq 0\}\subset\mathbb{R}^2$

Ahora si, veamos los conjuntos de nivel:

- Para cualquier $a$, tenemos que $\frac{y}{x}=a\to y=ax$, por lo tanto $C_a=\{(x,y)\in D:y=ax\}$

### Función #5

- $xy$

Veamos los conjuntos de nivel:

- Si $a=0$, se ve fácilmente que $C_a=\{(x,y)\in\mathbb{R}^2:x=0\}\cup\{(x,y)\in\mathbb{R}^2:y=0\}$
- Si $a\neq0$, tenemos que $xy=a\to y=\frac{a}{x}$, por lo tanto (con cuidado): $C_a=\{(x,y)\in \mathbb{R^2}: x\neq0, y=\frac{a}{x}\}$
