# Ejercicio 4

## Consigna

Hallar el polinomio de Taylor de grado 3 en $(0,0)$ de las siguientes funciones:

1. $f(x,y) = \arctan\left(\frac{y}{x^2 + 1}\right)$
2. $f(x,y)= e^x \cos(y)$
3. $f(x,y)= \log(xy + 1)$

## Resolución

### Parte 1

- $f(x,y) = \arctan\left(\frac{y}{x^2 + 1}\right)$

Vamos a saltear esta parte por la complejidad de los cálculos. No es demasiado díficil, pero no es lo más importante de estudiar para este momento.

### Parte 2

- $f(x,y)= e^x \cos(y)$

La resolución para este ejercicio es más fácil usando la propiedad que vimos en el ejercicio uno. La propiedad nos dice que dada $f(x)=g(x)h(x)$, entonces $T_3f=T_3g\cdot T_3h$ removiendo todos los términos de órden mayor a tres.

Entonces trabajamos con las funciones:

- $g(x)=e^x$
- $h(y)=\cos y$

Son funciones de cálculo uno, veamos directamente su desarrollo de Taylor en $0$:

- $T_3g(x)=1+x+\frac{x^2}{2}+\frac{x^3}{6}$
- $T_3h(y)=1+0+\frac{y^2}{2}+0=1-\frac{y^2}{2}$

Por lo tanto, utilizando la propiedad vista anteriormente:

$$
\begin{aligned}
&T_3f(\Delta x,\Delta y)\\
&=\scriptstyle{(\text{propiedad descrita al inicio})}\\
&T_3g(\Delta x)\cdot T_3h(\Delta y)\\
&=\scriptstyle{(\text{operatoria (ya eliminando términos de órden mayor a tres)})}\\
&1+x+\frac{x^2}{2}+\frac{x^3}{6}-\frac{y^2}{2}-\frac{y^2x}{2}\\
\end{aligned}
$$

### Parte 3

- $f(x,y)= \log(xy + 1)$

La estrategia para esta parte será usar la propiedad que ya vimos sobre la composición, teniendo que $f(x,y)=h(g(x,y))$ con:

- $h(x)=\log(x)$
- $g(x,y)=xy+1$

Lo bueno es que ya tenemos parte del problema resuelto, pues $g$ es una función polinómica, por lo tanto su diferencial de grado tres es exactamente si misma:

- $T_3g(\Delta x,\Delta y)=\Delta x\Delta y+1$

Por otra parte, cómo tenemos que $g(0,0)=1$ (que es el punto para el que queremos calcular el desarrollo de Taylor), queremos obtener $T_3h$ para el punto $x=1$. Al ser una función de cálculo uno, sabemos que esto está dado por:

- $T_3h(\Delta x)=0+(\Delta x-1)-\frac{(\Delta x-1)^2}{2}+\frac{(\Delta x-1)^3}{6}$

**Nota:** Los $-1$ que vemos, son parte de la definción, solo que por lo general trabajamos en el punto $x=0$, cuando esto no es cierto, a las variables que multiplican a los coeficientes hay que restarles el punto en el que evaluamos Taylor.

Entonces, ahora tenemos todos los ingredientes para usar la propiedad de la composición que conocemos:

$$
\begin{aligned}
&T_3f(\Delta x,\Delta y)\\
&=\scriptstyle{(\text{propiedad de la composición})}\\
&T_3h\circ T_3g\\
&=\scriptstyle{(\text{reemplazando lo conocido (ya eliminando términos de grado mayor a tres)})}\\
&0+\Delta x\Delta y\\
&=\scriptstyle{(\text{operatoria})}\\
&\Delta x\Delta y\\
\end{aligned}
$$