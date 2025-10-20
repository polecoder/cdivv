# Ejercicio 8

## Consigna

Usando el **criterio serie-integral**, clasificar las siguientes series:

1. $\sum_{n=1}^{\infty} n e^{-n^2}$
2. $\sum_{n=2}^{\infty} \frac{1}{n \sqrt{\log(n)}}$
3. $\sum_{n=1}^{\infty} \frac{\log(n)}{n^2}$

## Resolución

### Serie #1

- $\sum_{n=1}^{\infty} n e^{-n^2}$

Consideremos la función $f:[1,+\infty)\to\mathbb{R}$, definida por $f(x)=xe^{-x^2}$. Lo primero que hay que hacer para es determinar si la función es decreciente. Para esto, hallemos su derivada:

$$
\begin{aligned}
&(xe^{-x^2})'\\
&=\scriptstyle{(\text{regla del producto})}\\
&-2x^2e^{-x^2}+e^{-x^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&e^{-x^2}(-2x^2+1)
\end{aligned}
$$

Observemos que quién determina el signo es el polinomio $-2x^2+1$, pues en el intervalo que queremos evaluar la función $e^{-x^2}$ es siempre positiva.

Veamos intervalo a intervalo como se comporta el signo entonces:

- $(-\infty, \frac{-1}{\sqrt{2}}):$ Negativo
- $(-\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}})$: Positivo
- $(\frac{1}{\sqrt{2}}, +\infty):$ Negativo

Por lo tanto, en el intervalo que nos interesa $[1,+\infty)$, la derivada es negativa. Entonces la función es decreciente.

Por lo tanto podemos estudiar la primitiva para determinar el comportamiento de la serie.

$$
\begin{aligned}
&\int_{1}^{+\infty}xe^{-x^2}dx\\
&=\scriptstyle{(\text{cambio de variable }t=-x^2;dt=-2xdx)}\\
&-\frac{1}{2}\int_{1}^{+\infty}e^tdt\\
&=\scriptstyle{(\text{deshaciendo el cambio de variable})}\\
&-\frac{1}{2}e^{-x^2}\Big|_1^{+\infty}
\end{aligned}
$$

Y dicho límite en $+\infty$ claramente tiende a $0$. Por lo que entonces $\int_{1}^{+\infty}xe^{-x^2}dx$ es convergente, y utilizando el criterio serie-integral:

**Conclusión:** $\sum_{n=1}^{\infty} n e^{-n^2}$ es convergente

### Conclusión

Las demás partes son análogas, es calcular la integral impropia para inferir el resultado sobre las series.