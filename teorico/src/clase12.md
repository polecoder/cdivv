# CLASE 12 - 18/09/2025

## Series

### Proposición (condición necesaria de convergencia)

Si $\sum a_n$ converge, entonces $\lim_{n\to\infty} a_n=0$.

#### Demostración

Suponemos que $\sum a_n$ converge, es decir que:

- $\lim s_n = S$

Y a partir de esto, la siguiente subsucesión también converge al mismo punto:

- $\lim s_{n-1} = S$

Con esto podemos construir la prueba observando que:

- $a_n=s_n-s_{n-1}$, entonces:
- $\lim a_n=\lim s_n - \lim s_{n-1}=0$

Lo que concluye la prueba.

### Ejemplo 1

- $\sum \frac{1}{n(n+1)}$

Por fracciones simples, podemos reescribir la serie de la siguiente forma:

- $\sum(\frac{1}{n}-\frac{1}{n+1})$

Esto nos permite llegar al siguiente razonamiento con la reducida enésima:

$$
\begin{aligned}
s_n&=\left(1-\cancel{\frac{1}{2}}\right)+\left(\cancel{\frac{1}{2}}-\cancel{\frac{1}{3}}\right)+\left(\cancel{\frac{1}{3}}-\cancel{\frac{1}{4}}\right)+\ldots+\left(\cancel{\frac{1}{n}}-\frac{1}{n-1}\right)\\
&= 1-\frac{1}{n+1}
\end{aligned}
$$

Y por lo tanto se tiene que:

- $\lim_{n\to\infty}s_n=1$

Entonces:

- $\sum_{i=1}^{+\infty} \frac{1}{n(n+1)}=1$

### Ejemplo 2

- $\sum \log(1+\frac{1}{n})$

Simplificando un poco podemos llegar a una expresión más amigable:

$$
\begin{aligned}
&\log\left(1+\frac{1}{n}\right)\\
&=\\
&\log\left(\frac{n+1}{n}\right)\\
&=\\
&\log(n+1)-\log(n)\\
\end{aligned}
$$

Y con esto, todo indica a que tenemos otra serie convergente, ya que nos pasará algo muy similar que en el ejemplo anterior con la reducida enésima:

$$
\begin{aligned}
s_n&=(\cancel{\log(2)}-\log(1))+(\cancel{\log(3)}-\cancel{\log(2)})+(\cancel{\log(4)}-\cancel{\log(3)})+\ldots+(\log(n+1)-\cancel{\log(n)})\\
&=\log(n+1)-\log(1)
\end{aligned}
$$

Y por lo tanto se tiene que:

- $\lim_{n\to\infty} s_n=+\infty$

Entonces la serie $\sum \log(1+\frac{1}{n}) = +\infty$, o sea diverge.

## Series de términos positivos

Comenzaremos con los resultados más fuertes de este tema, que son para series de términos poisitivos, es decir:

- $\sum a_n$ con $a_n\geq0$

Tengamos presente que entonces las series de términos positivos tienen reducida enésima monótona creciente. Esto implica que la serie puede converger o diverger, pero no oscilar.

### Proposición 3.38 (criterio de comparación)

Sean $\sum a_n$ y $\sum b_n$, series de términos positivos tales que $a_n\leq b_n\quad\forall n>n_0$ con $n_0\in\mathbb{N}$. Entonces:

- Si $\sum b_n$ converge, entonces $\sum a_n$ converge también
- Si $\sum a_n$ diverge, entonces $\sum b_n$ diverge también

#### Demostración

Llamemos:

- $A_n=a_1+a_2+\ldots+a_n$
- $B_n=b_1+b_2+\ldots+b_n$

Entonces a partir de $n_0$, tenemos que $A_n-A_{n_0}\leq B_n-B_{n_0}$.

**Punto 1:**

Si $B_n$ converge a $L$, entonces $L$ es cota de $A_n$ y por lo tanto tenemos que $A_n$ está acotada. Además como es monótona creciente, podemos decir que converge.

**Punto 2:**

Si $A_n$ diverge, en particular no está acotada, por lo tanto $B_n$ tampoco está acotada. Además como es creciente, podemos decir que diverge.

##### Observación

Observar que en esta demostración (y esto es general para las series), los primeros $n_0$ términos no importan. Los que importan son los "últimos" términos de la serie. La convergencia de la serie se juega en el infinito.

#### Ejemplos 3.39

##### Caso #1

Estudiemos la serie denóminada como armónica:

- $\sum \frac{1}{n}$

Observando que $\forall x$ se tiene que $\log(1+x)\leq x$, en particular se tiene también que:

- $\log(1+\frac{1}{n})\leq \frac{1}{n}$

Como ambas son de términos positivos, podemos utilizar el criterio de comparación.
En un ejemplo anterior ya observamos que $\sum\log(1+\frac{1}{n})$ diverge, y por lo tanto usando el criterio se tiene que $\sum\frac{1}{n}$ también diverge.

##### Caso #2

Si $\alpha<1$, entonces $\frac{1}{n^{\alpha}}<\frac{1}{n}$. Y como $\sum\frac{1}{n}$ diverge, por el criterio de comparación

- $\sum\frac{1}{n^{\alpha}}$ también diverge