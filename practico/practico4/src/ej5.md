# Ejercicio 6

## Consigna

Usar el **criterio de la raíz** para estudiar la convergencia de las siguientes series:

1. $\sum_{n=1}^{+\infty} \tfrac{2n - 1}{(\sqrt{2})^n}$
2. $\sum_{n=1}^{+\infty} \left(\tfrac{n+1}{2n - 1}\right)^n$

## Resolución

### Serie #1

- $\sum_{n=1}^{+\infty} \tfrac{2n - 1}{(\sqrt{2})^n}$

Utilicemos el criterio de la raíz para clasificar la serie:

$$
\begin{aligned}
&\lim_{n\to\infty}\sqrt[n]{\frac{2n - 1}{(\sqrt{2})^n}}\\
&=\\
&\lim_{n\to\infty}\frac{\sqrt[n]{2n - 1}}{\sqrt[n]{(\sqrt{2})^n}}\\
&=\\
&\lim_{n\to\infty}\frac{\sqrt[n]{2n - 1}}{\sqrt{2}}\\
&=\\
&\frac{1}{\sqrt{2}}\lim_{n\to\infty}(2n-1)^{\frac{1}{n}}\\
&=\\
&\frac{1}{\sqrt{2}}\lim_{n\to\infty}e^{log((2n-1)^{\frac{1}{n}})}\\
&=\\
&\frac{1}{\sqrt{2}}\lim_{n\to\infty}e^{\frac{1}{n}\log(2n-1)}\\
&=\\
&\frac{1}{\sqrt{2}}\lim_{n\to\infty}e^{\frac{\log(2n-1)}{n}}\\
&=\\
&\frac{1}{\sqrt{2}}\lim_{n\to\infty}e^0\\
&=\\
&\frac{1}{\sqrt{2}}
\end{aligned}
$$

Por lo tanto, como $L<1:\sum_{n=1}^{+\infty} \tfrac{2n - 1}{(\sqrt{2})^n}$ es convergente.

### Serie #2

- $\sum_{n=1}^{+\infty} \left(\tfrac{n+1}{2n - 1}\right)^n$

Utilicemos el criterio de la raíz para clasificar la serie:

$$
\begin{aligned}
&\lim_{n\to\infty}\sqrt[n]{\left(\frac{n+1}{2n-1}\right)^n}\\
&=\\
&\lim_{n\to\infty}\frac{n+1}{2n-1}\\
&=\\
&\lim_{n\to\infty}\frac{n}{2n}\\
&=\\
&\frac{1}{2}\\
\end{aligned}
$$

Por lo tanto, como $L<1:\sum_{n=1}^{+\infty} \left(\tfrac{n+1}{2n - 1}\right)^n$ es convergente.