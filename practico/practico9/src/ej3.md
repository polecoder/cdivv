# Ejercicio 3

## Consigna

Calcular los siguientes límites:

1. $\lim_{(x,y)\to(0,0)} \frac{xy - \sin(x)\sin(y)}{x^2 + y^2}$
2. $\lim_{(x,y)\to(0,0)} \frac{e^{x^2+y(y+1)}-(1+y+\frac{y^2}{2})}{x^2 + y^2}$

## Resolución

### Parte 1

- $\lim_{(x,y)\to(0,0)} \frac{xy - \sin(x)\sin(y)}{x^2 + y^2}$

Bueno claramente la estrategia para los límites es usar el desarrollo de Taylor de las funciones que nos están perjudicando, en este caso es bastante fácil de observar que el problema lo tenemos con $\sin(x)\sin(y)$, por lo que haremos el desarrollo de Taylor para esa función.

Llamemos $f(x,y)=\sin x\sin y$. Queremos calcular su desarrollo de Taylor en $(0,0)$. Al calcular las derivadas nos vamos a dar cuenta que necesitamos por lo menos hasta el segundo diferencial:

- $f_x(x,y)=\cos x\sin y\implies f_x(0,0)=0$
- $f_y(x,y)=\sin x\cos y\implies f_y(0,0)=0$
- $f_{xx}(x,y)=-\sin x\sin y\implies f_{xx}(0,0)=0$
- $f_{xy}(x,y)=\cos x\cos y\implies f_{xy}(0,0)=1$
- $f_{yy}(x,y)=-\sin x\sin y\implies f_{yy}(0,0)=0$

Entonces:

- $df_{(0,0)}(\Delta x,\Delta y)=0$
- $d^2f_{(0,0)}(\Delta x,\Delta y)=0+2\Delta x\Delta y+0=2\Delta x\Delta y$

Con esto podemos plantear el desarrollo de Taylor para $(0,0)$:

$$
\begin{aligned}
&f(\Delta x,\Delta y)\\
&=\scriptstyle{(\text{teorema de Taylor})}\\
&0+0+\frac{2\Delta x\Delta y}{2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\Delta x\Delta y+r(\Delta x,\Delta y)\\
\end{aligned}
$$

Por lo tanto, podemos usar lo que hallamos para sustituir en el límite:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)} \frac{xy-\sin(x)\sin(y)}{x^2 + y^2}\\
&=\scriptstyle{(\text{cuando }(x,y)\to(0,0);\ \sin x\sin y\ \sim \ xy)}\\
&\lim_{(x,y)\to(0,0)} \frac{xy-xy}{x^2 + y^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&0
\end{aligned}
$$

### Parte 2

- $\lim_{(x,y)\to(0,0)} \frac{e^{x^2+y(y+1)}-(1+y+\frac{y^2}{2})}{x^2 + y^2}$

La estrategia para este caso difiere un poco de lo que teníamos en la parte anterior. El problema claramente está en el término con $e^u$. Teniendo en cuenta la propiedad que vimos en el ejercicio dos, podríamos trabajar con eso.

Recordemos que la propiedad nos decía que dada $f=h\circ g$, entonces $T_kf=T_kh\circ T_kg$, en base a esto necesitaríamos calcular los diferenciales de $g$ que la definiremos por $g(x,y)=x^2+y(y+1)$. Vayamos con las derivadas:

- $g_x(x,y)=2x\implies g_x(0,0)=0$
- $g_y(x,y)=2y+1\implies g_y(0,0)=1$
- $g_{xx}(x,y)=2\implies g_{xx}(0,0)=2$
- $g_{xy}(x,y)=0\implies g_{xy}(0,0)=0$
- $g_{yy}(x,y)=2\implies g_{yy}(0,0)=2$

Entonces:

- $dg_{(0,0)}(\Delta x,\Delta y)=0+\Delta y=\Delta y$
- $d^2g_{(0,0)}(\Delta x,\Delta y)=2\Delta x^2+0+2\Delta y^2$

Por lo tanto, el desarrollo de Taylor de grado dos es:

$$
\begin{aligned}
&g(0+\Delta x,0+\Delta y)\\
&=\scriptstyle{(\text{teorema de Taylor})}\\
&0+\Delta y+\frac{2\Delta x^2+2\Delta y^2}{2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\Delta y+\Delta x^2+\Delta y^2
\end{aligned}
$$

**Nota:** Aquí tengamos en cuenta que nos apuramos demasiado (o no pensamos antes de calcular) para empezar a trabajar. La función $g$ es una función polinómica, obviamente el Teorema de Taylor nos devolverá la misma función.

Ahora si, teniendo en cuenta la propiedad que mencionamos anteriormente, operamos:

$$
\begin{aligned}
&f(0+\Delta x,0+\Delta y)\\
&=\scriptstyle{(\text{por la observación de la consigna})}\\
&T_2h\circ T_2g\\
&=\scriptstyle{(\text{sustituyendo por lo conocido (ya eliminando los términos con órden mayor a 2)})}\\
&1+\Delta y+\Delta x^2+\Delta y^2+\frac{\Delta y^2}{2}
&=\scriptstyle{(\text{operatoria})}\\
&1+\Delta y+\Delta x^2+\frac{3\Delta y^2}{2}
\end{aligned}
$$

Por lo tanto, podemos usar lo que hallamos para sustituir en el límite:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)} \frac{e^{x^2+y(y+1)}-(1+y+\frac{y^2}{2})}{x^2 + y^2}\\
&=\scriptstyle{(\text{cuando }(x,y)\to(0,0);\ e^{x^2+y(y+1)}\ \sim \ 1+y+x^2+\frac{3y^2}{2})}\\
&\lim_{(x,y)\to(0,0)} \frac{1+y+x^2+\frac{3y^2}{2}-(1+y+\frac{y^2}{2})}{x^2 + y^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{(x,y)\to(0,0)} \frac{x^2+\frac{3y^2}{2}-\frac{y^2}{2}}{x^2 + y^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{(x,y)\to(0,0)} \frac{x^2+y^2}{x^2 + y^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&1
\end{aligned}
$$