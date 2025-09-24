# Ejercicio 7

## Consigna

Estudiar la convergencia de las siguientes series alternadas. En caso de que sean convergentes, estudiar si también lo son absolutamente:

1. $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1}}{3^n}$
2. $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1} n}{n^2 + 1}$
3. $\sum_{n=1}^{+\infty} \tfrac{(-1)^n n}{6n - 5}$
4. $\sum_{n=1}^{+\infty} \tfrac{(-1)^n (n^3 + 2n^2 + 8n + 5)}{n^5 + 4n^3 + 15}$

## Resolución

El único criterio para clasificar series alternadas es el criterio de Leibnitz, veamos su enunciado a continuación:

Si $a_n$ es una sucesión monótona decreciente que tiende a 0, entonces la serie alternada $\sum(-1)^na_n$ es convergente.

### Serie #1

- $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1}}{3^n}$

Estudiemos primero convergencia absoluta. Es decir que queremos clasificar la siguiente serie:

- $\sum_{n=1}^{+\infty} \tfrac{1}{3^n}$

Esta es una sucesión geométrica:

- $\sum_{n=1}^{+\infty} (\tfrac{1}{3})^n$

Y como $\frac{1}{3}<1$ la serie converge.

Por lo tanto $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1}}{3^n}$ es absolutamente convergente, es decir, también es convergente.

### Serie #2

- $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1} n}{n^2 + 1}$

Estudiemos primero convergencia absoluta. Es decir que queremos clasificar la siguiente serie:

- $\sum_{n=1}^{+\infty}\tfrac{n}{n^2 + 1}$

Utilizando el criterio de equivalentes, tenemos que $\tfrac{n}{n^2 + 1}\sim\tfrac{1}{n}$, y como $\sum\tfrac{1}{n}$ diverge:

- $\sum\tfrac{n}{n^2+1}$ diverge también

Por lo tanto $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1} n}{n^2 + 1}$ NO es absolutamente convergente.

Ahora podemos pasar a estudiar convergencia, para lo que vamos a estudiar la monotonía de:

- $a_n=\frac{n}{n^2+1}$

La estrategia que emplearemos será probar que para todo $n\in\mathbb{N}$:

- $a_n\geq a_{n+1}$

Desarrollemos:

$$
\begin{aligned}
&a_n\geq a_{n+1}\\
&\iff\\
&\frac{n}{n^2+1}\geq\frac{n+1}{(n+1)^2+1}\\
&\iff\\
&n((n+1)^2+1)\geq(n+1)(n^2+1)\\
&\iff\\
&n(n+1)\cancel{(n+1)}+n\geq\cancel{(n+1)}(n^2+1)\\
&\iff\\
&n(n+1)+n\geq(n^2+1)\\
&\iff\\
&\cancel{n^2}+2n\geq \cancel{n^2}+1\\
\end{aligned}
$$

Y esto último es cierto $\forall n\in\mathbb{N}$ tal que $n\geq1$ que es el dominio en el que estamos trabajando.
Por lo que concluimos que $a_n$ es monótona decreciente.

Por otra parte, tenemos que:

- $\lim_{n\to\infty}\frac{n}{n^2+1}=0$

Entonces usando el criterio de Leibnitz, podemos concluir que la serie:

- $\sum_{n=1}^{+\infty} \tfrac{(-1)^{n+1} n}{n^2 + 1}$ es convergente.

### Serie #3

- $\sum_{n=1}^{+\infty} \tfrac{(-1)^n n}{6n - 5}$

Estudiemos primero convergencia absoluta. Es decir que queremos clasificar la siguiente serie:

- $\sum_{n=1}^{+\infty}\tfrac{n}{6n - 5}$

Inmediatamente podemos ver que la serie no es absolutamente convergente pues:

$$
\begin{aligned}
&\lim_{n\to\infty}\frac{n}{6n-5}\\
&\sim\\
&\lim_{n\to\infty}\frac{n}{6n}\\
&=\\
&\frac{1}{6}
\end{aligned}
$$

Como el término general no tiende a 0, la serie no puede ser convergente.
Concluimos que $\sum_{n=1}^{+\infty} \tfrac{(-1)^n n}{6n - 5}$ NO es absolutamente convergente.

Y ni siquiera entramos a estudiar convergencia, pues por el mismo argumento, la sucesión $a_n=\frac{n}{6n-5}$ no converge a 0.

### Serie #4

- $\sum_{n=1}^{+\infty} \tfrac{(-1)^n (n^3 + 2n^2 + 8n + 5)}{n^5 + 4n^3 + 15}$

Estudiemos primero convergencia absoluta. Es decir que queremos clasificar la siguiente serie:

- $\sum_{n=1}^{+\infty} \tfrac{n^3 + 2n^2 + 8n + 5}{n^5 + 4n^3 + 15}$

Por criterio de equivalentes, como $\tfrac{n^3 + 2n^2 + 8n + 5}{n^5 + 4n^3 + 15}\sim\tfrac{n^3}{n^5}\sim\tfrac{1}{n^2}$ la serie converge, pues $\sum\frac{1}{n^2}$ converge.

Por lo tanto $\sum_{n=1}^{+\infty} \tfrac{(-1)^n (n^3 + 2n^2 + 8n + 5)}{n^5 + 4n^3 + 15}$ es absolutamente convergente, es decir, también es convergente.