# Ejercicio 7

## Consigna

Sea $f:\mathbb{R}^2\to\mathbb{R}$ la función dada por:

$$
f(x,y)=\begin{cases}
(x^2+y^2)\sin\frac{1}{x}+e^{xy} &\text{si }x\neq0\\
1 &\text{si }x=0
\end{cases}
$$

Estudiar continuidad y diferenciabilidad en los puntos $(0,0)$, $(0,1)$ y $(1,0)$, hallando las derivadas parciales cuando existan.

## Resolución

### Continuidad

Lo primero que notamos para estudiar la continuidad es que en el punto $(1,0)$ la función es continua, pues no se anula en dicho punto.

Entonces estudiaremos la continuidad para $(0,0)$ y $(0,1)$ notando en particular que el límite de la función en dichos puntos solo existe cuando $x^2+y^2=0$, pues si ese término es distinto de cero, el término $(x^2+y^2)\sin\frac{1}{x}$ oscila.

Con solo esta observación tenemos de gratis que:

- $f$ no es continua en $(0,1)$
- Y como $f$ no es continua en dichos puntos, tampoco es diferenciable (si lo fuera $f$ sería continua en estos puntos)

Resta entonces, estudiar este límite para el punto $(0,0)$ y verificar si es continua. Operemos:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}f(x,y)\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{(x,y)\to(0,0)}(x^2+y^2)\sin\frac{1}{x}+e^{xy}\\
&=\scriptstyle{((x^2+y^2)\sin\frac{1}{x}\to0\text{ cuando }(x,y)\to(0,0))}\\
&\lim_{(x,y)\to(0,0)}e^{xy}\\
&=\scriptstyle{(\text{operatoria})}\\
&1
\end{aligned}
$$

Como el límite corresponde con el valor funcional en $(0,0)$, la función es continua en este punto.

Resumiendo:

- La función $f$ es continua para los puntos $(0,0)$ y $(1,0)$
- La función $f$ NO es continua en el punto $(0,1)$

### Diferenciabilidad

Antes de empezar, claramente la función no es diferenciable en $(0,1)$, pues en este punto no es continua.
Estudiaremos los otros puntos por separado.

#### Punto $(1,0)$

La estrategia para este punto, será ver que pasa con las derivadas parciales cerca de él. Esto es bastante directo pues la función no se anula en este punto, por lo que el calculo es directo:

- $f_x(x,y)=-\frac{1}{x^2}(x^2+y^2)\cos\frac{1}{x}+2x\sin\frac{1}{x}+ye^{xy}$
- $f_y(x,y)=2y\sin\frac{1}{x}+xe^{xy}$

Donde podemos observar que ambas son continuas y están bien definidas para cualquier punto tal que $x\neq0$.
Cómo las derivadas parciales existen y son continuas para un determinado entorno, $f$ es diferenciable en $(1,0)$

#### Punto $(0,0)$

La estrategia para este punto, será diferente al punto anterior, lo que haremos será hallar el diferencial de la función en este punto, y con él verificar que el límite de la definición nos da cero.
Para esto empezamos calculando las derivadas parciales:

$$
\begin{aligned}
&f_x(0,0)\\
&=\scriptstyle{(\text{definición de derivada parcial})}\\
&\lim_{h\to0}\frac{f(h,0)-f(0,0)}{h}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{h\to0}\frac{h^2\sin\frac{1}{h}+1-1}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}h\sin\frac{1}{h}\\
&=\scriptstyle{(\text{límite de cero por acotado})}\\
&0
\end{aligned}
$$

La derivada parcial respecto de $y$ se obtiene análogamente, por lo tanto:

- $f_x(0,0)=f_y(0,0)=0$

Por lo tanto si la función es diferenciable, el candidato a diferencial es la transformación lineal nula. Planteemos la definición y hallemos el resto a partir de eso:

$$
\begin{aligned}
&f(\Delta x,\Delta y)=f(0,0)+0\Delta x+0\Delta y+r(\Delta x+\Delta y)\\
&f(\Delta x,\Delta y)-f(0,0)=r(\Delta x+\Delta y)\\
\end{aligned}
$$

Veamos entonces si el resto cumple con la propiedad fundamental del resto:

$$
\begin{aligned}
&\lim_{(\Delta x,\Delta y)\to0}\frac{r(\Delta x,\Delta y)}{\|(\Delta x,\Delta y)\|}\\
&=\scriptstyle{(\text{sustituyendo por la función resto})}\\
&\lim_{(\Delta x,\Delta y)\to0}\frac{f(\Delta x,\Delta y)-f(0,0)}{\|(\Delta x,\Delta y)\|}\\
&=\scriptstyle{(\text{sustituyendo por la función }f)}\\
&\lim_{(\Delta x,\Delta y)\to0}\frac{(\Delta x^2+\Delta y^2)\sin\frac{1}{\Delta x}+e^{\Delta x\Delta y}-1}{\|(\Delta x,\Delta y)\|}\\
&=\scriptstyle{(\text{notando que cuando }u\to0;\ e^u\sim u)}\\
&\lim_{(\Delta x,\Delta y)\to0}\frac{(\Delta x^2+\Delta y^2)\sin\frac{1}{\Delta x}+\Delta x\Delta y}{\|(\Delta x,\Delta y)\|}\\
&=\scriptstyle{(\text{notando que }\Delta x^2+\Delta y^2=\|(\Delta x,\Delta y)\|^2)}\\
&\lim_{(\Delta x,\Delta y)\to0}\|(\Delta x,\Delta y)\|\sin\frac{1}{\Delta x}+\frac{\Delta x\Delta y}{\|(\Delta x,\Delta y)\|}\\
&=\scriptstyle{(\text{límite de cero por acotado})}\\
&\lim_{(\Delta x,\Delta y)\to0}\frac{\Delta x\Delta y}{\|(\Delta x,\Delta y)\|}\\
&=\scriptstyle{(\text{desarrollo de la norma y polares: }\Delta x=\rho\cos\theta;\ \Delta y=\rho\sin\theta)}\\
&\lim_{\rho\to0}\frac{\rho^2\cos\theta\sin\theta}{\sqrt{\rho^2\cos^2\theta+\rho^2\sin^2\theta}}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{\rho\to0}\frac{\rho^2\cos\theta\sin\theta}{\sqrt{\rho^2(\cos^2\theta+\sin^2\theta)}}\\
&=\scriptstyle{(\text{operatoria: }\cos^2\theta+\sin^2\theta=1)}\\
&\lim_{\rho\to0}\frac{\rho^2\cos\theta\sin\theta}{\rho}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{\rho\to0}\rho\cos\theta\sin\theta\\
&=\scriptstyle{(\text{límite de cero por acotado})}\\
&0
\end{aligned}
$$

Como el límite da cero, la función $r(\Delta x,\Delta y)$ cumple con la propiedad fundamental del resto, y por tanto la función es diferenciable en $(0,0)$

### Derivadas parciales en $(0,1)$

Lo único que nos faltó en todo el desarrollo son las derivadas parciales en $(0,1)$. Se obtienen fácilemente con la definición:

$$
\begin{aligned}
&f_x(0,1)\\
&=\scriptstyle{(\text{definición de derivada parcial})}\\
&\lim_{h\to0}\frac{f(h,1)-f(0,1)}{h}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{h\to0}\frac{(h^2+1)\sin1+e^h-1}{h}\\
&=\scriptstyle{(\text{notando que cuando }u\to0;\ e^u\sim u)}\\
&\lim_{h\to0}\frac{(h^2+1)\sin1+h}{h}\\
&=\scriptstyle{(\text{operando})}\\
&\lim_{h\to0}\frac{h(h\sin1+1)+\sin1}{h}\\
&=\scriptstyle{(\text{operando})}\\
&\lim_{h\to0}h\sin1+1+\frac{\sin1}{h}\\
&=\scriptstyle{(\text{operando})}\\
&+\infty
\end{aligned}
$$

No nos queda forma de simplificar el término que se va a infinito, por lo tanto la derivada parcial con respecto de $x$ no existe para este punto.
Veamos la derivada parcial con respecto de $y$:

$$
\begin{aligned}
&f_y(0,1)\\
&=\scriptstyle{(\text{definición de derivada parcial})}\\
&\lim_{h\to0}\frac{f(0,1+h)-f(0,1)}{h}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{h\to0}\frac{1-1}{h}\\
&\scriptstyle{(\text{operatoria})}\\
&0
\end{aligned}
$$

Por lo tanto si existe la derivada con respecto de $y$ para este punto.

### Conclusión

A modo de resumen, obtuvimos:

- **Continuidad**: La función es continua en $(0,0)$ y $(1,0)$, pero no en $(0,1)$
- **Existencia de derivadas parciales**: Existen en $(0,0)$ y $(1,0)$, pero en $(0,1)$ solo existe la derivada parcial con respecto de $y$.
- **Diferenciabilidad**: La función es diferenciable en $(0,0)$ y $(1,0)$, pero no en $(0,1)$