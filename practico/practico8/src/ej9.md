# Ejercicio 9

## Consigna

Sea $f:\mathbb{R}^2\to\mathbb{R}$ definida como:

$$
f(x,y) =
\begin{cases}
(x^2 + y^2)\sin\left(\dfrac{1}{x^2 + y^2}\right) & (x,y)\neq(0,0) \\
0 & (x,y) = (0,0)
\end{cases}
$$

1. Probar que existen derivadas parciales en todos los puntos y calcularlas.  
2. Probar que $f$ es diferenciable.  
3. Probar que $f$ no es de clase $C^1$.

## Resolución

### Parte 1

Queremos probar que existen derivadas parciales en todos los puntos. La estrategia es bastante simple, para $(0,0)$ usaremos la definición, mientras que para cualquier otro punto se calcula directamente:

**Derivadas auxiliares:**

- $\frac{\partial (\frac{1}{x^2+y^2})}{\partial x}=-\frac{1}{(x^2+y^2)^2}2x=-\frac{2x}{(x^2+y^2)^2}$
- $\frac{\partial (\frac{1}{x^2+y^2})}{\partial y}=-\frac{1}{(x^2+y^2)^2}2y=-\frac{2y}{(x^2+y^2)^2}$

**Derivada respecto de $x$**:

$$
\begin{aligned}
&f_x(x,y)\\
&=\scriptstyle{(\text{operatoria})}\\
&2x\sin\left(\frac{1}{x^2+y^2}\right)-\frac{2x\cancel{(x^2+y^2)}}{(x^2+y^2)^{\cancel{2}}}\cos\left(\frac{1}{x^2+y^2}\right)\\
&=\scriptstyle{(\text{operatoria})}\\
&2x\sin\left(\frac{1}{x^2+y^2}\right)-\frac{2x}{x^2+y^2}\cos\left(\frac{1}{x^2+y^2}\right)\\
\end{aligned}
$$

**Derivada respecto de $y$**:

$$
\begin{aligned}
&f_y(x,y)\\
&=\scriptstyle{(\text{operatoria})}\\
&2y\sin\left(\frac{1}{x^2+y^2}\right)-\frac{2y\cancel{(x^2+y^2)}}{(x^2+y^2)^{\cancel{2}}}\cos\left(\frac{1}{x^2+y^2}\right)\\
&=\scriptstyle{(\text{operatoria})}\\
&2y\sin\left(\frac{1}{x^2+y^2}\right)-\frac{2y}{x^2+y^2}\cos\left(\frac{1}{x^2+y^2}\right)\\
\end{aligned}
$$

Esto es válido para cualquier punto $(x,y)\neq(0,0)$. Vayamos con ese caso ahora.

$$
\begin{aligned}
&f_x(0,0)\\
&=\scriptstyle{(\text{definición de derivada parcial})}\\
&\lim_{h\to0}\frac{f(h,0)-f(0,0)}{h}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{h\to0}\frac{h^2\sin(\frac{1}{h^2})}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}h\sin\left(\frac{1}{h^2}\right)\\
&=\scriptstyle{(\text{límite de cero por acotado})}\\
&0
\end{aligned}
$$

El razonamiento para $f_y(0,0)$ es análogo.
Con esto concluimos que las derivadas parciales existen para todo punto $(x,y)$.

### Parte 2

Para probar que la función es diferenciable, notaremos primero que:

- La función $f$ es diferenciable para todo punto $(x,y)\neq(0,0)$ ya que sus derivadas parciales son continuas en dichos puntos.

Entonces el problema está en $(0,0)$, si la función es diferenciable en este punto, entonces el candidato a diferencial es la transformación lineal nula (por lo que sabemos de las derivadas parciales en este punto). Por lo tanto podemos despejar el resto al plantear la definición:

$$
\begin{aligned}
&f(\Delta x,\Delta y)=f(0,0)+0\Delta x+0\Delta y+r(\Delta x,\Delta y)\\
&f(\Delta x,\Delta y)=r(\Delta x,\Delta y)
\end{aligned}
$$

Ahora, queremos verificar que el resto cumple la propiedad fundamental:

$$
\begin{aligned}
&\lim_{(\Delta x,\Delta y)\to0}\frac{r(\Delta x,\Delta y)}{\|(\Delta x,\Delta y)\|}\\
&=\scriptstyle{(\text{sustituyendo la función resto})}\\
&\lim_{(\Delta x,\Delta y)\to0}\frac{f(\Delta x,\Delta y)}{\|(\Delta x,\Delta y)\|}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{(\Delta x,\Delta y)\to0}\frac{(\Delta x^2 + \Delta y^2)\sin\left(\dfrac{1}{\Delta x^2 + \Delta y^2}\right)}{\|(\Delta x,\Delta y)\|}\\
&=\scriptstyle{(\text{notando que }\Delta x^2+\Delta y^2=\|(\Delta x,\Delta y)\|^2)}\\
&\lim_{(\Delta x,\Delta y)\to0}\|(\Delta x,\Delta y)\|\sin\left(\dfrac{1}{\Delta x^2 + \Delta y^2}\right)\\
&=\scriptstyle{(\text{límite de cero por acotado})}\\
&0
\end{aligned}
$$

Como el resto cumple con la propiedad fundamental, la función es diferenciable para $(0,0)$ (y por lo tanto para todos los puntos).

### Parte 3

Queremos probar que $f$ no es de clase $C^1$. Para ser de clase $C^1$ tendríamos que tener que $f_x(x,y)$ y $f_y(x,y)$ son funciones continuas.
Centraremos nuestro foco en una de ellas, porque nos bastará para probar que la función $f$ no es de clase $C^1$, tomaremos $f_x(x,y)$.

Por lo que vimos en las partes anteriores, podríamos definir a la función $f_x(x,y):\mathbb{R}^2\to\mathbb{R}$ de la siguiente forma:

$$
f(x,y) =
\begin{cases}
2x\sin\left(\frac{1}{x^2+y^2}\right)-\frac{2x}{x^2+y^2}\cos\left(\frac{1}{x^2+y^2}\right) & (x,y)\neq(0,0) \\
0 & (x,y) = (0,0)
\end{cases}
$$

Veamos el límite cuando $(x,y)\to(0,0)$ para verificar si la función es continua en dicho punto.

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}2x\sin\left(\frac{1}{x^2+y^2}\right)-\frac{2x}{x^2+y^2}\cos\left(\frac{1}{x^2+y^2}\right)\\
&=\scriptstyle{(\text{límite direccional cuando }x=y^2)}\\
&\lim_{y\to0}2y^2\sin\left(\frac{1}{y^2(y^2+1)}\right)-\frac{2y^2}{y^2(y^2+1)}\cos\left(\frac{1}{y^2(y^2+1)}\right)\\
&=\scriptstyle{(\text{operatoria y límite de cero por acotado})}\\
&\lim_{y\to0}-\frac{2}{y^2+1}\cos\left(\frac{1}{y^2(y^2+1)}\right)\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{y\to0}-2\cos\left(\frac{1}{y^2(y^2+1)}\right)\\
\end{aligned}
$$

Pero este límite oscila, pues $\cos\left(\frac{1}{y^2(y^2+1)}\right)$ oscila cuando $y\to0$ , y por lo tanto no existe.

**Nota:** Me compliqué con la elección del límite direccional, podría haber elegido $y=0$ y hubiera sido más directo.

Con esto, podemos concluir que la función no es de clase $C^1$.