# Ejercicio 5

## Consigna

Sean $f$ y $g$ dos funciones derivables en $[a, +\infty)$ y tales que sus derivadas $f'$ y $g'$ son integrables en ese intervalo.  
Además, se cumple que $\lim_{x \to +\infty} f(x)g(x) = L \in \mathbb{R}$.

1. Probar que $\int_a^{+\infty} f'(x)g(x)dx$ converge si y solo si $\int_a^{+\infty} f(x)g'(x)dx$ converge.

2. Clasificar:

    - $\int_0^{+\infty} \frac{\sin t}{t}dt$ y $\int_1^{+\infty} \frac{\sin t}{t^2}dt$  
    - $\int_0^{+\infty} \sin(t^2)dt$ y $\int_1^{+\infty} |\sin(x^2)|dx$

    *Sugerencia:* escribir $\sin(t^2) = 2t \sin(t^2) \cdot \frac{1}{2t}$ y usar la fórmula de partes.

## Resolución

### Parte 1

- Probar que $\int_a^{+\infty} f'(x)g(x)dx$ converge si y solo si $\int_a^{+\infty} f(x)g'(x)dx$ converge.

Apliquemos la fórmula de integración por partes:

$$
\begin{aligned}
&\int_{a}^{+\infty}f'(x)g(x)dx=f(x)g(x)\Big|_a^{+\infty}-\int_{a}^{+\infty}f(x)g'(x)dx\\
&\iff\scriptstyle{(\text{operando})}\\
&\int_{a}^{+\infty}f'(x)g(x)dx=\left(\lim_{x\to+\infty}f(x)g(x)\right)-f(a)g(a)-\int_{a}^{+\infty}f(x)g'(x)dx\\
&\iff\scriptstyle{(\text{operando})}\\
&\int_{a}^{+\infty}f'(x)g(x)dx+\int_{a}^{+\infty}f(x)g'(x)dx=\left(\lim_{x\to+\infty}f(x)g(x)\right)-f(a)g(a)\\
&\iff\scriptstyle{(\text{por hipótesis})}\\
&\int_{a}^{+\infty}f'(x)g(x)dx+\int_{a}^{+\infty}f(x)g'(x)dx=L-f(a)g(a)\\
\end{aligned}
$$

**Atención:** En este punto uno se podría ver tentado de decir: tengo dos integrales impropias sumadas que me dan un número finito, entonces ambas tienen que ser convergentes.
Esto no es así, pensemoslo con límites que cumplen esto pero ninguna de las dos partes convergen:

- $f(x)=sen(x)$
- $g(x)=-sen(x)$

En este caso el límite de la suma es 0, pero ambos dos oscilan en el infinito.

**Continuación:** Lo que si podemos confirmar a partir de la igualdad, es que si una converge: entonces necesariamente la otra tiene que converger para que el resultado sea finito.

Esto prueba lo que queríamos verificar.

### Parte 2

- $\int_0^{+\infty} \frac{\sin t}{t}dt$ y $\int_1^{+\infty} \frac{\sin t}{t^2}dt$
- $\int_0^{+\infty} \sin(t^2)dt$ y $\int_1^{+\infty} |\sin(x^2)|dx$

#### Integral #1

- $\int_0^{+\infty} \frac{\sin t}{t}dt$

Separemos la integral en partes ya que es mixta:

- $\int_0^{+\infty} \frac{\sin t}{t}dt=\int_{0}^{1}\frac{\sin t}{t}dt+\int_{1}^{+\infty}\frac{\sin t}{t}$

Estudiamos primero en el intervalo $[1,+\infty)$:

$$
\begin{aligned}
&\int_1^{+\infty} \frac{\sin t}{t}dt\\
&=\scriptstyle{(\text{integración por partes }(*_1))}\\
&\frac{-\cos t}{t}\Big|_1^{+\infty}-\int_{1}^{+\infty}\frac{-\cos t}{t^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&-\cos1+\int_{1}^{+\infty}\frac{\cos t}{t^2}\\
\end{aligned}
$$

**Observación $(*_1)$:** Integramos por partes con:

- $u=\frac{1}{t}\to du=-\frac{1}{t^2}$
- $dv=\sin t\to v=-\cos t$

A partir del último punto de la igualdad podemos concluir que la integral converge pues $\int_{1}^{+\infty}\frac{\cos t}{t^2}$ es absolutamente convergente:

- $\lvert\frac{\cos t}{t^2}\rvert\leq\frac{1}{x^2}$

Nos resta estudiar el otro intervalo, acá no podemos usar partes porque la función a integrar se anula en 0.

Por Taylor, tenemos que el integrando cumple lo siguiente cuando $x\to0$:

- $\frac{\sin x}{x}\sim 1$

Por lo tanto, la integral será convergente, ya que en el único punto problemático la función a integrar se comporta como la función constante 1.

**Conclusión:** $\int_0^{+\infty} \frac{\sin t}{t}dt$ es convergente.

#### Integral #2

- $\int_1^{+\infty} \frac{\sin t}{t^2}dt$

Esta integral es muy simple porque converge absolutamente:

- $\lvert\frac{\sin t}{t^2}\rvert\leq\frac{1}{t^2}$

**Conclusión:** Por comparación, como $\int_{1}^{+\infty}\frac{1}{t^2}$ converge, entonces $\int_1^{+\infty} \frac{\sin t}{t^2}dt$ converge también.

#### Integral #3

- $\int_0^{+\infty} \sin(t^2)dt$

Para clasificarla (primero entre $1$ y $+\infty$), podemos realizarlo con el siguiente truco:

$$
\begin{aligned}
&\int_{1}^{+\infty}sin(x^2)dx\\
&=\\
&\int_{1}^{+\infty}\frac{1}{2x}sin(x^2)2xdx\\
&=\scriptstyle{(\text{integración por partes }(*_1))}\\
&\frac{-cos(x^2)}{2x}\Big|_1^{+\infty}-\int_{1}^{+\infty}\frac{\cos(x^2)}{2x^2}dx
\end{aligned}
$$

**Observación $(*_1)$:** Lo que hacemos es lo siguiente:

$$
\begin{cases}
u=\frac{1}{2x}\to du=-\frac{1}{2x^2}\\
dv=\sin(x^2)2xdx\to v=-cos(x^2)
\end{cases}
$$

Ahora queremos verificar si los dos términos de la integral que hallamos convergen o no para determinar la convergencia de la integral original.

**Primer término:** converge

$$
\begin{aligned}
&\frac{-cos(x^2)}{2x}\Big|_1^{+\infty}\\
&=\\
&\left(\lim_{n\to\infty}\frac{-cos(x^2)}{2x}\right)+\frac{cos(1)}{2}\\
&=\scriptstyle{(\lim_{n\to\infty}\frac{-cos(x^2)}{2x}\to0)}\\
&\frac{cos(1)}{2}\\
\end{aligned}
$$

**Segundo término:** converge

$$
\begin{aligned}
&\int_{1}^{+\infty}\frac{\cos(x^2)}{2x^2}dx\text{ es absolutamente convergente}\\
&\iff\\
&\int_{1}^{+\infty}\Big|\frac{\cos(x^2)}{2x^2}\Big|dx\text{ es convergente}\\
&\iff\\
&\frac{1}{2}\int_{1}^{+\infty}\Big|\frac{\cos(x^2)}{x^2}\Big|dx\text{ es convergente}\\
\end{aligned}
$$

Y esto último se cumple por criterio de comparación, pues:

- $\Big|\frac{\cos(x^2)}{x^2}\Big|\leq\frac{1}{x^2}$

Y cómo $\int_{1}^{+\infty}\frac{1}{x^2}dx$ es convergente, $\int_{1}^{+\infty}\frac{\cos(x^2)}{2x^2}dx$ es absolutamente convergente. Y por lo tanto también es convergente.

**Resumiendo:** Con esto último podemos concluir que la integral de $1$ a $+\infty$ es convergente, y observando que la integral de $0$ a $1$ es una integral que no tiene inconvenientes (continua y en un intervalo acotado), podemos afirmar que:

- $\int_{0}^{+\infty}sin(x^2)dx$ es convergente.