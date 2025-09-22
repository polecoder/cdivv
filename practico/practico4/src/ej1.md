# Ejercicio 1

## Consigna

Indicar si las siguientes series son convergentes o no, hallando su suma en caso de serlo:

1. $\sum_{n=0}^{+\infty} \left(\frac{1}{3}\right)^n$
2. $\sum_{n=1}^{+\infty} \left(\frac{1}{\sqrt{3}}\right)^{n+3}$
3. $\sum_{n=1}^{+\infty} 5^{n+1}$
4. $\sum_{n=1}^{+\infty} \frac{3}{n(n+3)}$
5. $\sum_{n=1}^{+\infty} \log\left(\frac{n^2 + 2n + 1}{n^2}\right)$
6. $\sum_{n=1}^{+\infty} \frac{n}{(n+1)(n+2)(n+3)}$
7. $\sum_{n=1}^{\infty} \frac{n \arctan(n+1) - (n+1)\arctan(n)}{n(n+1)}$

## Resolución

### Recordatorio

Recordemos que una serie geométrica es una serie con la siguiente cara:

- $\sum_{n=0}^{+\infty}q^n$

Sabemos que:

- Si $q<1$ entonces la serie converge a $\lim \frac{1+q^{n+1}}{1-q}=\frac{1}{1-q}$
- Si $q>1$ entonces la serie diverge

### Serie #1

- $\sum_{n=0}^{+\infty} \left(\frac{1}{3}\right)^n$

Esta serie es geométrica, por lo que como $q<1$ sabemos que:

- $\sum_{n=0}^{+\infty} \left(\frac{1}{3}\right)^n$ converge a $\frac{3}{2}$

### Serie #2

- $\sum_{n=1}^{+\infty} \left(\frac{1}{\sqrt{3}}\right)^{n+3}$

Esta serie también se parece mucho a la geométrica, pero no lo es exactamente.
Operaremos para llegar a la forma deseada:

$$
\begin{aligned}
&\sum_{n=1}^{+\infty} \left(\frac{1}{\sqrt{3}}\right)^{n+3}\\
&=\scriptstyle{(\text{operatoria})}\\
&\sum_{n=1}^{+\infty} \left(\frac{1}{\sqrt{3}}\right)^4\left(\frac{1}{\sqrt{3}}\right)^{n-1}\\
&=\scriptstyle{(\text{operatoria})}\\
&\left(\frac{1}{\sqrt{3}}\right)^4\cdot\sum_{n=1}^{+\infty} \left(\frac{1}{\sqrt{3}}\right)^{n-1}\\
&=\scriptstyle{(\text{operatoria y reindización de la sumatoria})}\\
&\frac{1}{9}\cdot\sum_{n=0}^{+\infty} \left(\frac{1}{\sqrt{3}}\right)^{n}\\
\end{aligned}
$$

Entonces ahora podemos calcular a que converge usando la fórmula para las series geométricas:

- $\sum_{n=0}^{+\infty} \frac{1}{9}\left(\frac{1}{\sqrt{3}}\right)^n$ converge a $\frac{1}{9(\frac{\sqrt{3}-1}{\sqrt{3}})}$

### Serie #3

- $\sum_{n=1}^{+\infty} 5^{n+1}$

Esta serie claramente diverge, pues su término general no tiende a 0.

### Serie #4

- $\sum_{n=1}^{+\infty} \frac{3}{n(n+3)}$

Busquemos expresar el término general de la serie usando fracciones simples:

$$
\begin{aligned}
&\frac{3}{n(n+3)}=\frac{A}{n}+\frac{B}{n+3}
\\
&\iff\\
&\begin{cases}
A=1\\
B=-1
\end{cases}
\end{aligned}
$$

Entonces podemos expresar la serie como:

- $\sum_{n=1}^{+\infty} \frac{1}{n}-\frac{1}{n+3}$

Ahora podemos expandir los primeros términos para ver a que equivale la serie:

$$
\left(1-\cancel{\frac{1}{4}}\right)+\left(\frac{1}{2}-\cancel{\frac{1}{5}}\right)+\left(\frac{1}{3}-\cancel{\frac{1}{6}}\right)+\left(\cancel{\frac{1}{4}}-\cancel{\frac{1}{7}}\right)+\\
+\left(\cancel{\frac{1}{5}}-\cancel{\frac{1}{8}}\right)+\ldots+\left(\cancel{\frac{1}{n-3}}-\cancel{\frac{1}{n}}\right)+\left(\cancel{\frac{1}{n-2}}-\frac{1}{n+1}\right)+\\+\left(\cancel{\frac{1}{n-1}}-\frac{1}{n+2}\right)+\left(\cancel{\frac{1}{n}}-\frac{1}{n+3}\right)
$$

Por lo tanto la reducida enésima es:

$$
1+\frac{1}{2}+\frac{1}{3}-\frac{1}{n+1}-\frac{1}{n+2}-\frac{1}{n+3}
$$

Y tomando límite:

- $\lim\sum_{i=1}^n\frac{1}{n}-\frac{1}{n+3}=\frac{11}{6}$

Concluyendo:

- $\sum_{n=1}^{+\infty} \frac{3}{n(n+3)}$ converge a $\frac{11}{6}$

### Serie #5

- $\sum_{n=1}^{+\infty} \log\left(\frac{n^2 + 2n + 1}{n^2}\right)$

Simplifiquemos la expresión del término general:

$$
\begin{aligned}
&\log\left(\frac{n^2 + 2n + 1}{n^2}\right)\\
&=\scriptstyle{(\text{factorización de polinomios})}\\
&\log\left(\frac{(n+1)^2}{n^2}\right)\\
&=\scriptstyle{(\text{propiedades de logaritmos})}\\
&\log((n+1)^2)-\log(n^2)\\
&=\scriptstyle{(\text{operatoria})}\\
&2\log(n+1)-2\log(n)\\
\end{aligned}
$$

Por lo tanto se puede simplificar la reducida enésima a:

$$
\begin{aligned}
&\sum_{i=1}^n2\log(n+1)-2\log(n)\\
&=\\
&2\log(n+1)-2\log(1)
\end{aligned}
$$

Por lo tanto, al tomar límite observamos que esta serie diverge.

### Serie #6

Se resuelve por fracciones simples, similar a la serie #4.

### Serie #7

- $\sum_{n=1}^{\infty} \frac{n \arctan(n+1) - (n+1)\arctan(n)}{n(n+1)}$

Simplifiquemos la expresión del término general:

$$
\begin{aligned}
&\frac{n \arctan(n+1) - (n+1)\arctan(n)}{n(n+1)}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{n \arctan(n+1)}{n(n+1)}- \frac{(n+1)\arctan(n)}{n(n+1)}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{\arctan(n+1)}{n+1}- \frac{\arctan(n)}{n}\\
\end{aligned}
$$

Por lo tanto se puede simplificar su reducida enésima a:

$$
\begin{aligned}
&\sum_{i=1}^n \frac{\arctan(n+1)}{n+1}- \frac{\arctan(n)}{n}\\
&=\\
&\frac{\arctan(n+1)}{n+1}-\arctan(1)
\end{aligned}
$$

Tomando límite:

- $\lim\frac{\arctan(n+1)}{n+1}-\arctan(1)=-arctan(1)=\frac{-\pi}{4}$

Concluyendo:

- $\sum_{n=1}^{\infty} \frac{n \arctan(n+1) - (n+1)\arctan(n)}{n(n+1)}$ converge a $\frac{-\pi}{4}$