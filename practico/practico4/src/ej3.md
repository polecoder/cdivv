# Ejercicio 3

## Consigna

Determinar si las siguientes series son convergentes o divergentes aplicando el **criterio del equivalente**:

1. $\sum_{n=0}^{+\infty} \tfrac{1}{n^2 + 1}$
2. $\sum_{n=1}^{+\infty} \tfrac{n^2 + 1}{n^3}$
3. $\sum_{n=1}^{+\infty} \tfrac{\log(n+1) - \log(n)}{10n + 1}$

## Resolución

### Serie #1

- $\sum_{n=0}^{+\infty} \tfrac{1}{n^2 + 1}$

Veamos a que es equivalente el término general:

$$
\begin{aligned}
\frac{1}{n^2+1}\sim\frac{1}{n^2}
\end{aligned}
$$

Entonces como $\sum\frac{1}{n^2}$ es convergente, también lo es $\sum\tfrac{1}{n^2 + 1}$.

### Serie #2

- $\sum_{n=1}^{+\infty} \tfrac{n^2 + 1}{n^3}$

Veamos a que es equivalente el término general:

$$
\begin{aligned}
&\frac{n^2 + 1}{n^3}\sim\frac{n^2}{n^3}\sim\frac{1}{n}
\end{aligned}
$$

Entonces como $\sum\tfrac{1}{n}$ es divergente, también lo es $\sum\tfrac{n^2+1}{n^3}$.

### Serie #3

- $\sum_{n=1}^{+\infty} \tfrac{\log(n+1) - \log(n)}{10n + 1}$

Veamos a que es equivalente el término general:

$$
\begin{aligned}
&\frac{\log(n+1) - \log(n)}{10n + 1}\\
&=\scriptstyle{(\text{propiedades de logarítmos})}\\
&\frac{\log(\frac{n+1}{n})}{10n + 1}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{\log(1+\frac{1}{n})}{10n + 1}\\
\end{aligned}
$$

Por desarrollo de Taylor, tenemos que si $x\to0$, entonces $\log(1+x)\to x$. Entonces aplicando en nuestro caso:

$$
\begin{aligned}
&\frac{\log(1+\frac{1}{n})}{10n + 1}\\
&=\scriptstyle{(\text{por el argumento anterior})}\\
&\frac{\frac{1}{n}}{10n + 1}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{1}{(10n + 1)n}\\
\end{aligned}
$$

Y observemos que:

- $\frac{1}{(10n + 1)n}\sim\frac{1}{n^2}$

Entonces como $\sum\frac{1}{n^2}$ converge, también lo hace $\sum_{n=1}^{+\infty} \tfrac{\log(n+1) - \log(n)}{10n + 1}$