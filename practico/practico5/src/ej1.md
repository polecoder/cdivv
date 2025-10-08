# Ejercicio 1

## Consigna

1. Sean $a > 0$ y $f : [a, +\infty) \to \mathbb{R}$ una función continua tal que $f(t) \ge 0$. Definimos $F(x) = \int_a^x f(t)\,dt$. Demostrar que:

    - $F(x)$ es creciente.
    - $\int_{a}^{+\infty}f(t)dt$ converge sii $F(x)$ está acotada superiormente.

2. Sea $g : [a, +\infty) \to \mathbb{R}$ una función continua que verifica $0 \le f(t) \le g(t)$ para todo $t \ge a$.

    1. Probar que si $\int_a^{+\infty} g(t)\,dt$ converge, entonces $\int_a^{+\infty} f(t)\,dt$ también converge.
    2. Si $\int_a^{+\infty} f(t)\,dt$ diverge, entonces $\int_a^{+\infty} g(t)\,dt$ diverge.

## Resolución

### Parte 1

Para esta parte queremos demostrar que:

- $F(x)$ es creciente.
- $\int_{a}^{+\infty}f(t)dt$ converge sii $F(x)$ está acotada superiormente.

Lo primero viene dado gratis, pues la función $f(t)\geq0$ por hipótesis, esto significa que al aumentar $x$ voy a estar sumando un poquito más de area a la integral.

Para la segunda parte, expandamos un poco sobre lo que tenemos que probar.
En primer lugar, que $\int_{a}^{+\infty}f(t)dt$ sea convergente, significa que:

- $\lim_{x\to\infty}F(x)=L<\infty$

En este caso como $F(x)$ es creciente, por definición de límite se tiene que:

- $F(x)\leq L$ para todo $x\in\mathbb{R}$

Es decir que $F(x)$ está acotada superiormente.

Ahora, partamos del otro lado, si $F(x)$ está acotada superiormente, es decir:

- $F(x)<K$ para todo $x\in\mathbb{R}$

Considerando $K$ como el supremo del conjunto de cotas superiores, tenemos que:
Dado $\varepsilon>0$, existe $x_0\in[a,+\infty)$ tal que $\forall x>x_0: x\in(K-\varepsilon, K]$.
Esto último la definición de límite para $K$, solo considerando un lado del entorno, por lo que necesariamente $F(x)$ converge a $K$.