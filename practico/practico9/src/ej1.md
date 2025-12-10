# Ejercicio 1

## Consigna

Sean $g:\mathbb{R}\to\mathbb{R}$ y $h:\mathbb{R}\to\mathbb{R}$ definidas como:

- $g(x) = e^x$  
- $h(x) = \sin(x)$  

1. Hallar el polinomio de Taylor de orden 2 de $g$ y $h$ en $x = 0$.
2. Considere ahora $f:\mathbb{R}^2\to\mathbb{R}$ definida como $f(x,y) = g(x)h(y)$. Calcular $df$ y $d^2 f$ en $(0,0)$ y escribir el desarrollo de Taylor de orden 2 de $f$ en $(0,0)$.

**Observación:** $T_2 f$ en $(0,0)$ puede obtenerse multiplicando los polinomios de Taylor de orden 2 de $g$ y $h$, y luego removiendo los términos de orden mayor a 2. Este procedimiento es válido para cualquier orden, para cualquier par de funciones $g$ y $h$, y puede utilizarse para realizar cálculos de manera más eficiente.

## Resolución

### Parte 1

- Hallar el polinomio de Taylor de orden 2 de $g$ y $h$ en $x = 0$.

Para empezar calculemos las derivadas que vamos a necesitar (tengamos en cuenta que estamos en una función de $\mathbb{R}$ a $\mathbb{R}$):

- $g_x(x)=e^x\implies g_x(0)=1$
- $h_x(x)=\cos x\implies h_x(0)=1$
- $g_{xx}(x)=e^x\implies g_{xx}(0)=1$
- $h_{xx}(x)=-\sin x\implies h_{xx}(0)=0$

Recordemos que en este tipo de funciones el diferencial es más simple (llamamos $k$ al punto donde evaluamos la función):

- $dg_x(k)=e^xk$
- $dh_x(k)=k\cos x$
- $d^2g_x(k)=e^xk^2$
- $d^2h_x(k)=-k\sin x$

#### Función $g$

Planteemos el desarrollo de Taylor de orden dos para $g$, utilizando los diferenciales que calculamos anteriormente (llamamos $k$ al incremento en el punto):

$$
\begin{aligned}
&g(0+k)\\
&=\scriptstyle{(\text{teorema de Taylor})}\\
&g(0)+dg_0(k)+\frac{d^2g_0(k)}{2}+r(k)\\
&=\scriptstyle{(\text{sustituyendo por lo que kallamos})}\\
&1+k+\frac{k^2}{2}+r(k)
\end{aligned}
$$

Que corresponde con lo que hallamos usando la definición para funciones de cálculo uno.

#### Función $h$

Planteemos el desarrollo de Taylor de orden dos para $g$, utilizando los diferenciales que calculamos anteriormente (llamamos $k$ al incremento en el punto):

$$
\begin{aligned}
&h(0+k)\\
&=\scriptstyle{(\text{teorema de Taylor})}\\
&h(0)+dh_0(k)+\frac{d^2h_0(k)}{2}+r(k)\\
&=\scriptstyle{(\text{sustituyendo por lo que kallamos})}\\
&0+k+0+r(k)\\
&=\scriptstyle{(\text{operatoria})}\\
&k+r(k)
\end{aligned}
$$

Que también corresponde con lo que hallamos usando la definición para funciones de cálculo uno.

### Parte 2

- Considere ahora $f:\mathbb{R}^2\to\mathbb{R}$ definida como $f(x,y) = g(x)h(y)$. Calcular $df$ y $d^2 f$ en $(0,0)$ y escribir el desarrollo de Taylor de orden 2 de $f$ en $(0,0)$.

La estrategia para resolver esta parte será usar la observación indicada en la consigna. Con esta podremos hallar directamente el desarrollo de Taylor de orden dos de $f$ en $(0,0)$. Luego hallaremos $df$ y $d^2f$ en $(0,0)$.

$$
\begin{aligned}
&f(0+\Delta x,0+\Delta y)\\
&=\scriptstyle{(\text{por la observación de la consigna})}\\
&T_2g(\Delta x)T_2h(\Delta y)\\
&=\scriptstyle{(\text{sustituyendo por los desarrollos conocidos})}\\
&\left(1+\Delta x+\frac{\Delta x^2}{2}\right)\Delta y\\
&=\scriptstyle{(\text{operatoria})}\\
&\Delta y+\Delta x\Delta y+r(\Delta x,\Delta y)
\end{aligned}
$$

Recordemos que eliminamos el término con órden mayor a dos (recordemos que contamos los órdenes de ambas variables sumados), de igual forma que agregamos el resto también.

Vayamos por otro lado con los diferenciales, tenemos que la función $f$ está definida por $f(x,y)=e^x\sin y$, calculemos las derivadas que necesitamos:

- $f_x(x,y)=e^x\sin y$
- $f_y(x,y)=e^x\cos y$
- $f_{xx}(x,y)=e^x\sin y$
- $f_{xy}(x,y)=e^x\cos y$
- $f_{yy}(x,y)=-e^x\sin y$

Con esto, tenemos que:

- $df_{(0,0)}(\Delta x,\Delta y)=f_x(0,0)\Delta x+f_y(0,0)\Delta y=0+\Delta y=\Delta y$
- $d^2f_{(0,0)}(\Delta x,\Delta y)=f_{xx}(0,0)\Delta x^2+2f_{xy}(0,0)\Delta x\Delta y+f_{yy}(0,0)\Delta y^2=0+2\Delta x\Delta y+0=2\Delta x\Delta y$

Por completitud, planteemos el teorema de Taylor para verificar que lo que hallamos inicialmente es correcto:

$$
\begin{aligned}
&f(0+\Delta x,0+\Delta y)\\
&=\scriptstyle{(\text{teorema de Taylor})}\\
&f(0,0)+df_{(0,0)}(\Delta x,\Delta y)+\frac{d^2f_{(0,0)}(\Delta x,\Delta y)}{2}\\
&=\scriptstyle{(\text{reemplazando por valores conocidos})}\\
&0+\Delta y+\frac{2\Delta x\Delta y}{2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\Delta y+\Delta x\Delta y+r(\Delta x,\Delta y)
\end{aligned}
$$

Por lo tanto, el razonamiento que hicimos con la observación es correcto.
Esto concluye el ejercicio.