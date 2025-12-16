# Ejercicio 1 (evaluaciones anteriores)

## Consigna

Considere las siguientes afirmaciones sobre series:

1. $\sum_{n=1}^{+\infty} \frac{1}{n \log\left(1 + \frac{1}{n}\right)}$ es convergente.
2. $\sum_{n=1}^{+\infty} \frac{(-1)^n n}{3^n}$ es absolutamente convergente.
3. $\sum_{n=2}^{+\infty} \frac{\log(2)\log(3)\log(4)\cdots\log(n)}{n!}$ es convergente.

Entonces:

(A) Solamente las afirmaciones (1) y (2) son verdaderas.  
(B) Solamente las afirmaciones (2) y (3) son verdaderas.  
(C) Todas las afirmaciones son verdaderas.  
(D) Solamente la afirmación (2) es verdadera.  
(E) Solamente las afirmaciones (1) y (3) son verdaderas.

## Resolución

### Serie #1

- $\sum_{n=1}^{+\infty} \frac{1}{n \log\left(1 + \frac{1}{n}\right)}$

Veamos que sucede con el término general cuando $n\to+\infty$, teniendo presente la siguiente observación:

- $(*_1)$ Cuando $u\to0$, $\log(1+u)\sim u$

Por lo tanto cuando $n\to+\infty$ el término general es equivalente a:

$$
\begin{aligned}
&\lim_{n\to+\infty}a_n\\
&=\scriptstyle{(\text{definición del término general})}\\
&\lim_{n\to+\infty}\frac{1}{n\log\left(1+\frac{1}{n}\right)}\\
&=\scriptstyle{(\text{usando la observación }*_1)}\\
&\lim_{n\to+\infty}\frac{1}{n\cdot\frac{1}{n}}\\
&=\scriptstyle{(\text{operatoria})}\\
&1
\end{aligned}
$$

Por lo tanto el término general tiende a uno cuando $n$ tiende a infinito, con esto concluimos que la serie no puede ser convergente.

### Serie #2

- $\sum_{n=1}^{+\infty} \frac{(-1)^n n}{3^n}$

Queremos ver si es absolutamente convergente, es decir si:

- $\sum_{n=1}^{+\infty} \frac{n}{3^n}$ es convergente.

Para esto usaremos el criterio de la raíz enésima:

$$
\begin{aligned}
&\lim_{n\to+\infty}\sqrt[n]{\frac{n}{3^n}}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{n\to+\infty}\frac{\sqrt[n]{n}}{3}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{1}{3}\lim_{n\to+\infty}n^{\frac{1}{n}}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{1}{3}\lim_{n\to+\infty}e^{\log(n^{\frac{1}{n}})}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{1}{3}\lim_{n\to+\infty}e^{\frac{1}{n}\log(n)}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{1}{3}\lim_{n\to+\infty}e^{\frac{\log(n)}{n}}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{1}{3}
\end{aligned}
$$

Como el resultado $\frac{1}{3}<1$, el resultado nos dice que la serie es convergente.
Por lo tanto, la serie original es absolutamente convergente.

### Serie #3

- $\sum_{n=2}^{+\infty} \frac{\log(2)\log(3)\log(4)\cdots\log(n)}{n!}$

Para verificar si esta serie es convergente, usaremos el criterio del cociente:

$$
\begin{aligned}
&\lim_{n\to+\infty}\frac{\cancel{\log(2)}\cdots\cancel{\log(n)}\log(n+1)}{(n+1)!}\cdot\frac{n!}{\cancel{\log(2)}\cdots\cancel{\log(n)}}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{n\to+\infty}\frac{\log(n+1)\cancel{n!}}{\cancel{n!}(n+1)}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{n\to+\infty}\frac{\log(n+1)}{(n+1)}\\
&=\scriptstyle{(\text{por órdenes})}\\
&0
\end{aligned}
$$

Como el límite es menor que $1$, entonces la serie es convergente.
Concluimos que la respuesta correcta es:

(B) Solamente las afirmaciones (2) y (3) son verdaderas.
