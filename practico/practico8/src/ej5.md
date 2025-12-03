# Ejercicio 5

## Consigna

Verificar que la función $u(x,t)=e^{-a^2 k^2t}\sin(kx)$ satisface la ecuación del calor.

- $u_t=a^2u_{xx}$

## Resolución

La solución es bastante fácil, calcular $u_{xx}$ es lo primero:

- $u_x(x,t)=ke^{-a^2k^2t}\cos(kx)$
- $u_{xx}(x,t)=-k^2e^{-a^2k^2t}\sin(kx)$

Por otra parte, tenemos que calcular $u_t$:

- $u_t(x,t)=-a^2k^2e^{-a^2k^2t}\sin(kx)$

Esto efectivamente verifica que:

$$
\begin{aligned}
&u_t=a^2u_{xx}\\
&\iff\scriptstyle{(\text{reemplazando por lo calculado})}\\
&-a^2k^2e^{-a^2k^2t}\sin(kx)=a^2(-k^2e^{-a^2k^2t}\sin(kx))\\
&\iff\scriptstyle{(\text{operatoria})}\\
&-a^2k^2e^{-a^2k^2t}\sin(kx)=-a^2k^2e^{-a^2k^2t}\sin(kx)\\
\end{aligned}
$$

Como lo último se cumple, tenemos que la función $u(x,t)$ cumple con la ecuación del calor.