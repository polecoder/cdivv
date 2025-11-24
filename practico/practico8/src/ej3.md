# Ejercicio 3

## Consigna

Calcular las derivadas parciales de cada una de las siguientes funciones $f=f(x,y)$, especificando en qué puntos existen:

1. $a x^\alpha + b y^\beta$
2. $\tfrac{3x}{y} + \tfrac{4y}{x}$
3. $x^2y^{3/2}$
4. $\arctan(xy)$
5. $\log\left(\tfrac{x+y}{x^2}\right)$
6. $e^y \sin(x)$
7. $\max\{|x|,|y|\}$
8. $\max\{x^2, y^3\}$

## Resolución

### Estrategia

Lo que tenemos que hacer para cada función es determinar los puntos problemáticos (donde no está definida), ya que en esos puntos no existirán las derivadas parciales.
Luego habrá que verificar donde no están bien definidas las funciones derivadas parciales.

### Función #1

- $ax^\alpha+by^\beta$

#### Derivada respecto de $x$

$$
\begin{aligned}
&\frac{\partial f}{\partial x}\\
&=\scriptstyle{(\text{operatoria})}\\
&a\alpha x^{\alpha-1}
\end{aligned}
$$

Redondeando:

- Si $\alpha\geq1$, la función está bien definida para todo $x$.
- Si $\alpha<1$, la función está bien definida para todo $x\neq0$.

#### Derivada respecto de $y$

$$
\begin{aligned}
&\frac{\partial f}{\partial y}\\
&=\scriptstyle{(\text{operatoria})}\\
&b\beta y^{\beta-1}\\
\end{aligned}
$$

Redondeando:

- Si $\beta\geq1$, la función está bien definida para todo $y$
- Si $\beta<1$, la función está bien definida para todo $y\neq0$

#### Conclusión

- Si $\alpha,\beta\geq1$, existen las derivadas parciales para todo punto $(x,y)\in\mathbb{R}^2$
- Si $\alpha<1$, existen las derivadas parciales para todo punto $(x,y)\in\{(x,y)\in\mathbb{R}^2:x\neq0\}$
- Si $\beta<1$, existen las derivadas parciales para todo punto $(x,y)\in\{(x,y)\in\mathbb{R}^2:y\neq0\}$

### Función #2

- $\tfrac{3x}{y}+\tfrac{4y}{x}$

Notemos que la función está bien definida en el conjunto $\{(x,y)\in\mathbb{R}^2:x\neq0,y\neq0\}$

#### Derivada respecto de $x$

$$
\begin{aligned}
&\frac{\partial f}{\partial x}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{3}{y}-\frac{4y}{x^2}\\
\end{aligned}
$$

#### Derivada respecto de $y$

$$
\begin{aligned}
&\frac{\partial f}{\partial x}\\
&=\scriptstyle{(\text{operatoria})}\\
&-\frac{3x}{y^2}+\frac{4}{x}\\
\end{aligned}
$$

#### Conclusión

Las derivadas parciales existen para todo punto en el conjunto $\{(x,y)\in\mathbb{R}^2:x\neq0,y\neq0\}$.

### Función #3

- $x^2y^{3/2}$

Notemos que la función está bien definida en el conjunto $\{(x,y)\in\mathbb{R}^2:y^3\geq0\}$

#### Derivada respecto de $x$

$$
\begin{aligned}
&\frac{\partial f}{\partial x}\\
&=\scriptstyle{(\text{operatoria})}\\
&2xy^{3/2}
\end{aligned}
$$

#### Derivada respecto de $y$

$$
\begin{aligned}
&\frac{\partial f}{\partial y}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{3x^2y^{1/2}}{2}
\end{aligned}
$$

Notemos el detalle de que esta función está bien definida para el conjunto $\{(x,y)\in\mathbb{R}^2:y\geq0\}$.
Pero este conjunto es equivalente al que teníamos anteriormente: $\{(x,y)\in\mathbb{R}^2:y^3\geq0\}$

#### Conclusión

Las derivadas parciales existen para todo punto en el conjunto $\{(x,y)\in\mathbb{R}^2:y^3\geq0\}$

### Función #4

- $\arctan(xy)$

#### Derivada respecto de $x$

$$
\begin{aligned}
&\frac{\partial f}{\partial x}\\
&=\scriptstyle{(\text{regla de la cadena: }f=arctan(x);f'=\frac{1}{1+x^2};g=xy;g'=y)}\\
&\frac{y}{1+y^2x^2}
\end{aligned}
$$

Notemos el detalle de que esta función está bien definida para todo $\mathbb{R}^2$, pues $1+y^2x^2$ no se anula para ningún punto $(x,y)\in\mathbb{R}^2$.

#### Derivada respecto de $y$

$$
\begin{aligned}
&\frac{\partial f}{\partial x}\\
&=\scriptstyle{(\text{regla de la cadena: }f=arctan(x);f'=\frac{1}{1+x^2};g=xy;g'=x)}\\
&\frac{x}{1+x^2y^2}
\end{aligned}
$$

#### Conclusión

Las derivadas parciales existen para todo punto en $\mathbb{R}^2$

### Función #5

- $\log\left(\tfrac{x+y}{x^2}\right)=\log(x+y)-\log(x^2)=\log(x+y)-2\log(x)$

Notemos que la función solo está bien definida en el conjunto: $\{(x,y)\in\mathbb{R}^2:x>-y, x>0\}$

#### Derivada respecto de $x$

$$
\begin{aligned}
&\frac{\partial f}{\partial x}\\
&=\scriptstyle{(\text{regla de la cadena: }f=\log(x); f'=\frac{1}{x}; g=x+y; g'=1)}\\
&\frac{1}{x+y}-\frac{2}{x}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{x-2x-2y}{x(x+y)}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{-x-2y}{x(x+y)}\\
\end{aligned}
$$

Está función solo está bien definida en el conjunto que ya vimos anteriormente.

#### Derivada respecto de $y$

$$
\begin{aligned}
&\frac{\partial f}{\partial y}\\
&=\scriptstyle{(\text{regla de la cadena: }f=\log(x); f'=\frac{1}{x}; g=x+y; g'=1)}\\
&\frac{1}{x+y}-2\log(x)\\
\end{aligned}
$$

Está función solo está bien definida en el conjunto que ya vimos anteriormente.

#### Conclusión

Las derivadas parciales existen para todo punto en el conjunto $\{(x,y)\in\mathbb{R}^2:x>-y, x>0\}$

### Función #6

- $e^y\sin(x)$

#### Derivada respecto de $x$

$$
\begin{aligned}
&\frac{\partial f}{\partial x}\\
&=\scriptstyle{(\text{operatoria})}\\
&e^y\cos(x)
\end{aligned}
$$

#### Derivada respecto de $y$

$$
\begin{aligned}
&\frac{\partial f}{\partial y}\\
&=\scriptstyle{(\text{operatoria})}\\
&e^y\sin(x)
\end{aligned}
$$

#### Conclusión

Las derivadas parciales existen para todo punto en $\mathbb{R}^2$