# Ejercicio 5

## Consigna

Sabiendo que $a_n \geq 0$ y que $\sum a_n$ converge, indicar si las siguientes series son convergentes o no, explicando por qué:

1. $\sum \tfrac{1}{a_n}$
2. $\sum a_n^2$
3. $\sum \sqrt{a_n}$
4. $\sum \log(1 + a_n)$

## Resolución

### Serie #1

- $\sum \tfrac{1}{a_n}$

Consideremos para este caso que $a_n>0$, de lo contrario la sucesión no queda bien definida para todo $n\in\mathbb{N}$

Analizando el término general, como $a_n\to0$, vamos a tener que:

$$
\lim_{n\to\infty} \frac{1}{a_n}=\infty
$$

Y como el término general no tiende a 0, la serie es divergente.

### Serie #2

- $\sum a_n^2$

Considerando que $a_n$ converge, tenemos que a partir de cierto $n_0\in\mathbb{N},\forall n>n_0$ se cumple la siguiente desigualdad:

- $0\leq a_n\leq 1$

Entonces, a partir de este $n_0$ se va a cumplir la siguiente desigualdad:

- $a_n^2\leq a_n$, por lo visto en la anterior desigualdad.

Entonces, utilizando el criterio de comparación, como $\sum a_n$ converge:

- $\sum a_n^2$ también converge.

### Serie #3

- $\sum \sqrt{a_n}$

Esta serie no necesariamente converge, veámoslo con el contraejemplo: $\sum\frac{1}{n^2}$.
La serie mencionada converge, pero al tomar raíz obtenemos lo siguiente:

- $\sum \sqrt{\frac{1}{n^2}}=\sum\frac{1}{n}$

Y sabemos que $\sum\frac{1}{n}$ diverge.

Por otra parte podemos ver otro ejemplo en el que la serie resultante si converge:

- $\sum\frac{1}{n^4}$

Por lo que no podemos afirmar nada sobre esta serie.

### Serie #4

- $\sum \log(1 + a_n)$

**Observación:** Si $x\geq0$, entonces:

- $\log(1+x)\leq x$

Utilizamos entonces la observación con $a_n=x$, dado que $\lim_{n\to\infty} a_n=0$, obteniendo:

- $\sum\log(1+a_n)\leq\sum a_n$

Y por criterio de comparación, como $a_n$ converge, entonces:

- $\sum\log(1+a_n)$ también converge.