# Ejercicio 5

## Consigna

Calcular el polinomio de Taylor de grado 3 de $f(x,y,z) = \frac{yz}{x}$ en el punto $(1,0,0)$.

## Resolución

La estrategia para este ejercicio será usar la propiedad del producto para polinomios de Taylor que ya vimos en anteriores ejercicios. Notemos que $f(x,y,z)=\frac{1}{x}\cdot yz$

Por lo que es un producto de las funciones:

- $h(x)=\frac{1}{x}$
- $g(y,z)=yz$

Como $g$ es una función polinómica, tenemos que en $(0,0)$:

- $T_3g(y,z)=yz$

Por otro lado, como en queremos evaluar con $x=1$, veremos ese desarrollo de Taylor para $h$:

- $T_3h(x)=1-(x-1)+(x-1)^2-(x-1)^3$

Con esto, ya estamos en condiciones de usar la propiedad del producto:

$$
\begin{aligned}
&T_3f(x,y,z)\\
&=\scriptstyle{(\text{propiedad del producto})}\\
&T_3h(x)\cdot T_3g(y,z)\\
&=\scriptstyle{(\text{reemplazando por lo conocido (ya eliminando los términos de grado mayor a tres)})}\\
&yz-(x-1)yz\\
&=\scriptstyle{(\text{operatoria})}\\
&2yz-xyz
\end{aligned}
$$