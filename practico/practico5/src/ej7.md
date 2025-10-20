# Ejercicio 7

## Consigna

Determinar para qué valores de $\alpha$ las siguientes integrales impropias son convergentes:

1. $\int_0^{+\infty} \frac{x^\alpha}{x + 1}dx$
2. $\int_0^{+\infty} \frac{dx}{(e^{x^2} - 1)^\alpha}$

## Resolución

### Integral #1

- $\int_0^{+\infty} \frac{x^\alpha}{x + 1}dx$

**Caso $\alpha\geq0$:**

Observemos que si $\alpha\geq0$, tenemos que la integral diverge por comparación con:

- $\int_{0}^{+\infty}\frac{1}{x}dx$, pues $\frac{x^{\alpha}}{x+1}\geq\frac{1}{x}$

**Caso $\alpha<0$:**

Por otra parte, si $\alpha<0$ tenemos que la integral es:

- $\int_{0}^{+\infty}\frac{1}{x^{-\alpha}(x+1)}dx$

Y con este valor de $\alpha$, el comportamiento de la función en $0$ está dado por:

- $\frac{1}{x^{-\alpha}}$

Por lo tanto podemos estudiar $\int_{0}^{1}\frac{1}{x^{-\alpha}}dx$ y descartar todos los valores de $\alpha\leq-1$, pues esta integral divergería en esos casos.

**Caso $\alpha\in(-1,0)$:**

Nos resta estudiar el intervalo $\alpha\in(-1,0)$ donde tenemos que separar nuevamente la integral en:

- $\int_{0}^{+\infty}\frac{1}{x^{-\alpha}(x+1)}dx=\int_{0}^{1}\frac{1}{x^{-\alpha}(x+1)}dx+\int_{1}^{+\infty}\frac{1}{x^{-\alpha}(x+1)}dx$

La segunda integral, se comporta como $\frac{1}{x^{-\alpha+1}}$ en $+\infty$, por lo que es convergente.

La primera integral, se comporta como $\frac{1}{x^{-\alpha}}$ en $0$. Por lo tanto es convergente (pues recordemos que $\alpha\in(-1,0)$)

**Conclusión:** La integral impropia $\int_0^{+\infty} \frac{x^\alpha}{x + 1}dx$ es convergente sii $\alpha\in(-1,0)$

### Integral #2

- $\int_0^{+\infty} \frac{dx}{(e^{x^2} - 1)^\alpha}$

La integral es mixta, por lo tanto la dividimos en:

- $\int_0^{+\infty} \frac{dx}{(e^{x^2} - 1)^\alpha}=\int_0^{1} \frac{dx}{(e^{x^2} - 1)^\alpha}+\int_1^{+\infty} \frac{dx}{(e^{x^2} - 1)^\alpha}$

Para el primer integrando, observemos que:

- $\lim_{u\to0}\frac{e^{u}-1}{u}=1$ por Taylor

Por lo que podemos aplicarlo en el primer integrando para obtener:

$$
\begin{aligned}
&\int_0^{1} \frac{dx}{(e^{x^2} - 1)^\alpha}\\
&\sim\\
&\int_0^{1} \frac{dx}{x^{2\alpha}}\\
\end{aligned}
$$

Por lo que esta integral converge sii:

- $2\alpha< 1\to\alpha<\frac{1}{2}$

Ahora para el segundo integrando, es un poco más fácil encontrar una equivalencia, apliquemos directamente:

$$
\begin{aligned}
&\int_1^{+\infty} \frac{dx}{(e^{x^2} - 1)^\alpha}\\
&\sim\\
&\int_1^{+\infty} \frac{dx}{e^{\alpha x^2}}\\
&\sim\\
&\int_1^{+\infty} e^{-\alpha x^2}dx\\
\end{aligned}
$$

Podemos distinguir algunos casos muy simplemente:

- Si $\alpha<0$: Claramente diverge, pues tenemos una función integrando con crecimiento exponencial.
- Si $\alpha=0$: El integrando equivale a $1$, por lo que en este caso la integral también diverge.

Para el último caso, calculemos la primitiva:

$$
\begin{aligned}
&\int e^{-\alpha x^2}dx\\
&=\\
&-\frac{1}{2\alpha}e^{-\alpha x^2}
\end{aligned}
$$

Entonces:

$$
\lim_{x\to+\infty}-\frac{1}{2\alpha}e^{-\alpha x^2}=0
$$

Con esto ya podemos observar que cuando $\alpha>0$, tenemos que la integral converge.

**Conclusión:** La integral $\int_0^{+\infty} \frac{dx}{(e^{x^2} - 1)^\alpha}$ converge sii:

- $0<\alpha<\frac{1}{2}$