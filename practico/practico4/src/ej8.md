# Ejercicio 8

## Consigna

Estudiar la convergencia de las siguientes series:

1. $\sum_{n=1}^{+\infty} \tfrac{n}{(n+1)(n+2)}$
2. $\sum_{n=1}^{+\infty} \tfrac{n}{(n+1)\log(n+1)}$
3. $\sum_{n=1}^{+\infty} \tfrac{n^3}{e^n}$
4. $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1}}{\sqrt{n}}$

## Resolución

### Serie #1

- $\sum_{n=1}^{+\infty} \tfrac{n}{(n+1)(n+2)}$

Es una serie de términos positivos, por lo que estudiemos convergencia usando el criterio de equivalencia:

- $\tfrac{n}{(n+1)(n+2)}\sim \tfrac{n}{n^2}=\tfrac{1}{n}$

Y como $\sum\frac{1}{n}$ diverge:

- $\sum_{n=1}^{+\infty} \tfrac{n}{(n+1)(n+2)}$ también diverge.

### Serie #2

- $\sum_{n=1}^{+\infty} \tfrac{n}{(n+1)\log(n+1)}$

Es una serie de términos positivos, por lo que lo primero que haremos será simplificar la expresión del término general:

$$
\begin{aligned}
&\frac{n}{(n+1)\log(n+1)}\\
&=\\
&\frac{n}{n\log(n+1)+\log(n+1)}\\
&=\\
&\frac{1}{\log(n+1)+\log(n+1)}\\
&=\\
&\frac{1}{2\log(n+1)}\\
\end{aligned}
$$

Ahora podemos usar la siguiente desigualdad de logaritmo $\forall x\geq0$:

- $\log(1+x)\leq x$

Y por consecuente obtenemos que:

- $\frac{1}{2\log(n+1)}\geq\frac{1}{2n}\sim\frac{1}{n}$

Entonces como tenemos que $\sum\frac{1}{n}$ diverge, por comparación:

- $\sum_{n=1}^{+\infty} \tfrac{n}{(n+1)\log(n+1)}$ diverge también

### Serie #3

- $\sum_{n=1}^{+\infty} \tfrac{n^3}{e^n}$

Es una serie de términos positivos, por lo que lo primero que haremos será utilizar el criterio de la raíz enésima:

$$
\begin{aligned}
&\lim\sqrt[n]{\frac{n^3}{e^n}}\\
&=\\
&\lim\frac{\sqrt[n]{n^3}}{e}\\
&=\\
&\frac{1}{e}\lim e^{\log(n^{\frac{3}{n}})}\\
&=\\
&\frac{1}{e}\lim e^{\frac{3}{n}\log(n)}\\
&=\\
&\frac{1}{e}\lim e^{\frac{3\log(n)}{n}}\\
&=\\
&\frac{1}{e}\\
\end{aligned}
$$

Como $\frac{1}{e}<1$, la serie:

- $\sum_{n=1}^{+\infty} \tfrac{n^3}{e^n}$ converge

### Serie #4

- $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1}}{\sqrt{n}}$

Es una serie alternada, por lo que primero estudiaremos convergencia absoluta clasificando la siguiente serie:

- $\sum_{n=1}^{+\infty} \tfrac{1}{\sqrt{n}}$

Podemos usar el criterio de comparación y tenemos lo siguiente:

- Como $\sqrt{n}\leq n$, tenemos que $\frac{1}{\sqrt{n}}\geq\frac{1}{n}\quad\forall n\in\mathbb{N}$

Entonces como $\sum\frac{1}{n}$ diverge, $\sum\frac{1}{\sqrt{n}}$ también diverge.
Por lo que la serie $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1}}{\sqrt{n}}$ NO es absolutamente convergente.

Para verificar si la misma es convergente, vamos a probar que $\frac{1}{\sqrt{n}}$ es monótona decreciente, es decir que:

- $\frac{1}{\sqrt{n}}\geq\frac{1}{\sqrt{n+1}}$

Esto es directo, pues $\sqrt{x}$ es una función creciente, por lo que $\sqrt{n}\leq\sqrt{n+1}$, es decir que $\frac{1}{\sqrt{n}}\geq\frac{1}{\sqrt{n+1}}$.

Además tenemos que $\lim\frac{1}{\sqrt{n}}=0$.
Por lo tanto, por el criterio de Leibnitz tenemos que $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1}}{\sqrt{n}}$ es convergente.