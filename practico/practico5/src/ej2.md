# Ejercicio 2

## Consigna

Clasificar y hallar la integral en caso de convergencia:

1. $\int_2^{+\infty} \frac{dx}{x \log^{\alpha}(x)}$
2. $\int_0^{+\infty} x^3 e^{-x^2}dx$
3. $\int_0^1 \frac{1}{x^2}\sin(\frac{1}{x})dx$
4. $\int_{-\infty}^{+\infty} \frac{dx}{1 + x^2}$
5. $\int_{-\infty}^{+\infty} \frac{dx}{e^x + e^{-x}}$

## Resolución

### Integral #1

- $\int_2^{+\infty} \frac{dx}{x \log^{\alpha}(x)}$

Esta integral es equivalente a la siguiente:

- $\int_2^{+\infty} \frac{dx}{x (\log(x))^{\alpha}}$

Por lo tanto podemos avanzar con un cambio de variable:

$$
\begin{aligned}
&\lim_{x\to+\infty}F(x)\\
&=\\
&\int_{2}^{+\infty}\frac{dx}{x\log(x)^{\alpha}}\\
&=\scriptstyle{(\text{cambio de variable }u=\log(x);du=\frac{1}{x}dx)}\\
&\int_{\log(2)}^{+\infty}\frac{du}{u^{\alpha}}\\
\end{aligned}
$$

A partir de este punto tenemos que distinguir entre dos casos según el valor de $\alpha$:

**Caso 1: $\alpha=1$**

$$
\begin{aligned}
&\int_{\log(2)}^{+\infty}\frac{du}{u}\\
&=\\
&\log(u)\Big|_{\log(2)}^{+\infty}\\
&=\\
&\lim_{u\to\infty}\log(u)-\log(\log(2))
\end{aligned}
$$

Por lo tanto en este caso la integral diverge.

**Caso 2: $\alpha\neq1$**

$$
\begin{aligned}
&\int_{\log(2)}^{+\infty}\frac{du}{u^{\alpha}}\\
&=\\
&\int_{\log(2)}^{+\infty}u^{-\alpha}du\\
&=\\
&\int_{\log(2)}^{+\infty}\frac{u^{1-\alpha}}{1-\alpha}du\\
&=\\
&\frac{u^{1-\alpha}}{1-\alpha}\Big|_{\log(2)}^{+\infty}\\
&=\\
&\lim_{u\to\infty}\frac{u^{1-\alpha}}{1-\alpha}-\frac{\log(2)^{1-\alpha}}{1-\alpha}
\end{aligned}
$$

Por lo tanto el comportamiento para este caso queda determinado por el límite:

- $\lim_{u\to\infty}\frac{u^{1-\alpha}}{1-\alpha}$

Y este tiene el siguiente comportamiento:

- Si $1-\alpha<0$ (es decir si $\alpha>1$), entonces el límite es 0, y la integral converge a $\frac{1}{(\alpha+1)\log(2)^{\alpha-1}}$
- Si $1-\alpha>0$, entonces el límite es $+\infty$, por lo que la integral diverge.

Esto define el comportamiento de la integral que queríamos clasificar, resumiendo: $\int_2^{+\infty} \frac{dx}{x \log^{\alpha}(x)}$

- Converge a $\frac{1}{(\alpha+1)\log(2)^{\alpha-1}}$ si $\alpha >1$
- Diverge si $\alpha\leq1$

### Integral #2

- $\int_0^{+\infty} x^3 e^{-x^2}dx$

Avancemos con un cambio de variable:

$$
\begin{aligned}
&\lim_{x\to+\infty}F(x)\\
&=\\
&\int_0^{+\infty} x^3 e^{-x^2}dx\\
&=\\
&\int_0^{+\infty} \frac{1}{2x}x^3 e^{-x^2}2xdx\\
&=\\
&\int_0^{+\infty} \frac{x^2}{2}e^{-x^2}2xdx\\
&=\scriptstyle{(\text{cambio de variable }t=x^2;dt=2xdx)}\\
&\int_0^{+\infty} \frac{t}{2} e^{-t}dt\\
&=\\
&\frac{1}{2}\int_0^{+\infty}te^{-t}dt\\
&=\scriptstyle{(\text{integración por partes }(*_1))}\\
&\frac{1}{2}\left(-te^{-t}\Big|_0^{+\infty}-\int_{0}^{+\infty}-e^{-t}\right)\\
&=\\
&\frac{1}{2}\left(-te^{-t}\Big|_0^{+\infty}-e^{-t}\Big|_0^{+\infty}\right)\\
&=\\
&\frac{1}{2}\left(0-(-1)\right)\\
&=\\
&\frac{1}{2}\\
\end{aligned}
$$

**Observación $(*_1)$:** Utilizamos lo siguiente:

- $u=t\to du=1$
- $dv=e^{-t}\to v=-e^{-t}$

Por lo tanto, la integral converge a $\frac{1}{2}$.

### Integral #3

- $\int_0^1 \frac{1}{x^2}\sin(\frac{1}{x})dx$

Avancemos con un cambio de variable:

$$
\begin{aligned}
&F(x)\\
&=\\
&\int_x^1 \frac{1}{t^2}\sin\left(\frac{1}{t}\right)dt\\
&=\scriptstyle{(\text{cambio de variable }u=\frac{1}{t};du=-\frac{1}{t^2}dt)}\\
&-\int_{\frac{1}{x}}^1 \sin(u)du\\
&=\\
&-\left(\cos(u)\Big|_{\frac{1}{x}}^1\right)\\
&=\\
&-\left(cos(1)-cos\left(\frac{1}{x}\right)\right)\\
\end{aligned}
$$

Al tomar límite, observamos que la expresión no tiene límite cuando $x\to+\infty$. Por lo que podemos concluir que la integral oscila.

### Integral #4

- $\int_{-\infty}^{+\infty} \frac{dx}{1 + x^2}$

Es una integral mixta, por lo que vamos a trabajar con ella separando como corresponde:

$$
\begin{aligned}
&\int_{-\infty}^{+\infty} \frac{dx}{1 + x^2}\\
&=\\
&\int_{-\infty}^{0} \frac{dx}{1 + x^2}+ \int_{0}^{+\infty} \frac{dx}{1 + x^2}
\end{aligned}
$$

A partir de este punto tenemos que estudiar las dos impropias que nos resultaron:

**Integrando #1:**

$$
\begin{aligned}
&\int_{-\infty}^{0} \frac{1}{1 + x^2}dx\\
&=\\
&\arctan(x)\Big|_{-\infty}^0\\
&=\\
&0+\frac{\pi}{2}\\
&=\\
&\frac{\pi}{2}\\
\end{aligned}
$$

**Integrando #2:**

$$
\begin{aligned}
&\int_{0}^{+\infty} \frac{dx}{1 + x^2}\\
&=\\
&\arctan(x)\Big|_0^{+\infty}\\
&=\\
&\frac{\pi}{2}-0\\
&=\\
&\frac{\pi}{2}\\
\end{aligned}
$$

Por lo tanto, juntando ambas partes, tenemos que la integral impropia $\int_{-\infty}^{+\infty} \frac{dx}{1 + x^2}$ converge a $\pi$.
