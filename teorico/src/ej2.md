# Ejercicio 2

## Consigna

Sea

$$
f(x,y) = e^{\sin(x)+y}, \qquad g(x,y) = \sin(x) + y.
$$

1. Calcular el desarrollo de Taylor de orden 3 de $g$ en $(0,0)$.
2. Calcular el desarrollo de Taylor de orden 3 de $f$ en $(0,0)$.

**Observación:** $T_3(f)$ puede obtenerse componiendo $T_3 h \circ T_3 g$, donde $h(x) = e^x$, y luego removiendo los términos de orden mayor a 3.

## Resolución

### Parte 1

- Calcular el desarrollo de Taylor de orden 3 de $g$ en $(0,0)$

Para el desarrollo de orden tres de $g$, necesitamos hallar hasta $d^3g$, por lo que primero calcularemos todas las derivadas que necesitaremos:

- $g_x(x,y)=\cos x\implies g_x(0,0)=1$
- $g_y(x,y)=1\implies g_x(0,0)=1$
- $g_{xx}(x,y)=-\sin x\implies g_{xx}(0,0)=0$
- $g_{xy}(x,y)=0\implies g_{xy}(0,0)=0$
- $g_{yy}(x,y)=0\implies g_{yy}(0,0)=0$
- $g_{xxx}(x,y)=-\cos x\implies g_{xxx}(0,0)=-1$
- $g_{xxy}(x,y)=0\implies g_{xxy}(0,0)=0$
- $g_{yyx}(x,y)=0\implies g_{yyx}(0,0)=0$
- $g_{yyy}(x,y)=0\implies g_{yyy}(0,0)=0$

Con esto podemos calcular los diferenciales que necesitamos:

- $dg_{(0,0)}(\Delta x,\Delta y)=0+1\cdot\Delta x+1\cdot\Delta y=\Delta x+\Delta y$
- $d^2g_{(0,0)}(\Delta x,\Delta y)=0+0+0=0$
- $d^3g_{(0,0)}(\Delta x,\Delta y)=-\Delta x^3+0+0+0=-\Delta x^3$

Por lo tanto, podemos realizar el desarrollo de Taylor:

$$
\begin{aligned}
&g(0+\Delta x,0+\Delta y)\\
&=\scriptstyle{(\text{teorema de Taylor})}\\
&0+\Delta x+\Delta y+0-\frac{\Delta x^3}{3!}+r(\Delta x,\Delta y)\\
&=\scriptstyle{(\text{operatoria})}\\
&\Delta x+\Delta y-\frac{\Delta x^3}{6}+r(\Delta x,\Delta y)\\
\end{aligned}
$$

### Parte 2

- Calcular el desarrollo de Taylor de orden 3 de $f$ en $(0,0)$.

La estrategia para esta parte, será utilizar la observación de la consigna para el desarrollo. Notemos bien que $f$ es exactamente $h\circ g$ con $h(x)=e^x$.

En el ejercicio uno (en realidad en cálculo uno también) ya sabemos quién es el desarrollo de Taylor de orden tres de $h$ para cuando $x$ tiende a cero:

- $h(0+\Delta x)=1+\Delta x+\frac{\Delta x^2}{2}+\frac{\Delta x^3}{6}+r(\Delta x)$

Con esto estamos en condiciones de usar la observación:

$$
\begin{aligned}
&f(0+\Delta x,0+\Delta y)\\
&=\scriptstyle{(\text{por la observación de la consigna})}\\
&T_3h\circ T_3g\\
&=\scriptstyle{(\text{sustituyendo por lo que conocemos (ya eliminando los términos con órden mayor a 3)})}\\
&1+\Delta x+\Delta y-\frac{\Delta x^3}{6}+\frac{\Delta x^2+2\Delta x\Delta y+\Delta y^2}{2}+\frac{\Delta x^3+3\Delta x^2\Delta y+3\Delta x\Delta y^2+\Delta y^3}{6}\\
&=\scriptstyle{(\text{operatoria})}\\
&1+\Delta x+\Delta y+\frac{\Delta x^2+\Delta y^2}{2}+\Delta x\Delta y+\frac{\Delta y^3}{6}+\frac{\Delta x^2\Delta y+\Delta x\Delta y^2}{2}\\
\end{aligned}
$$

Esto concluye el ejercicio.