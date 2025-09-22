# Ejercicio 4

## Consigna

Usar el **criterio del cociente** para estudiar la convergencia de las siguientes series:

1. $\sum_{n=1}^{+\infty} \tfrac{2n - 1}{(\sqrt{2})^n}$
2. $\sum_{n=1}^{+\infty} \tfrac{n!}{n^n}$

## Resolución

### Serie #1

- $\sum_{n=1}^{+\infty} \tfrac{2n - 1}{(\sqrt{2})^n}$

Utilicemos el criterio del cociente:

$$
\begin{aligned}
&\lim_{n\to\infty}\frac{2n}{(\sqrt{2})^{n+1}}\cdot\frac{(\sqrt{2})^n}{2n-1}\\
&=\\
&\lim_{n\to\infty}\frac{2n}{\sqrt{2}(2n-1)}\\
&=\\
&\lim_{n\to\infty}\frac{2n}{2n\sqrt{2}}\\
&=\\
&\frac{1}{\sqrt{2}}
\end{aligned}
$$

Entonces, como $L<1:\sum_{n=1}^{+\infty} \tfrac{2n - 1}{(\sqrt{2})^n}$ converge.

### Serie #2

- $\sum_{n=1}^{+\infty} \tfrac{n!}{n^n}$

Utilicemos el criterio del cociente:

$$
\begin{aligned}
&\lim_{n\to\infty}\frac{(n+1)!}{(n+1)^{n+1}}\cdot \frac{n^n}{n!}\\
&=\\
&\lim_{n\to\infty}\frac{n^n}{(n+1)^n}\\
&=\\
&\lim_{n\to\infty}\left(\frac{n}{n+1}\right)^n\\
&=\\
&\lim_{n\to\infty}\left(\frac{n}{n(1+\frac{1}{n})}\right)^n\\
&=\\
&\lim_{n\to\infty}\left(\frac{1}{1+\frac{1}{n}}\right)^n\\
&=\\
&\lim_{n\to\infty}\frac{1}{(1+\frac{1}{n})^n}\\
&=\\
&\frac{1}{e}\\
\end{aligned}
$$

Donde la última igualdad es un resultado teórico de sucesiones.

Concluyendo, como $L<1:\sum_{n=1}^{+\infty} \tfrac{n!}{n^n}$ converge.