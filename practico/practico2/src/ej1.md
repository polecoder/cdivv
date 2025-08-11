# Ejercicio 1

## Consigna

Hallar la solución general de las siguientes ecuaciones diferenciales de variables separables:

1. $y' = y^2 - 1$
2. $(1 + y^2) y y' + (1 + y^2) = 0$
3. $x e^{2y} y' - (1 + e^{2y}) = 0$

## Resolución

### Parte 1

- $y' = y^2 - 1$

$$
\begin{aligned}
&y' = y^2 - 1\\
&\iff\\
&\frac{y'}{y^2-1}=1\\
&\iff\\
&\int\frac{y'}{y^2-1}dx=\int1dx\\
&\iff\scriptstyle{(\text{u=y(x),du=y'(x)dx})}\\
&\int\frac{1}{u^2-1}du=x + k_1\\
&\iff\scriptstyle{(\text{fracciones simples})}\\
&\int\frac{1}{2}\left(\frac{1}{u-1}-\frac{1}{u+1}\right)du=x + k_1\\
&\iff\\
&\frac{1}{2}\left(\int\frac{1}{u-1}du-\int\frac{1}{u+1}du\right)=x + k_1\\
&\iff\\
&\frac{1}{2}(ln|u-1|+k_2-ln|u+1|+k_3)=x + k_1\\
&\iff\scriptstyle{(C_1=\frac{1}{2}(k_2+k_3))}\\
&\frac{1}{2}ln\left\lvert\frac{u-1}{u+1}\right\rvert+C_1=x + k_1\\
&\iff\scriptstyle{(C_2=2k_1-C_1)}\\
&ln\left\lvert\frac{u-1}{u+1}\right\rvert=2x + C_2\\
&\iff\\
&\frac{u-1}{u+1}=\pm e^{2x+C_2}\\
&\iff\scriptstyle{(K=\pm e^C_2)}\\
&\frac{u-1}{u+1}=Ke^{2x}\\
&\iff\\
&u-1=Ke^{2x}(u+1)\\
&\iff\\
&u-1=Ke^{2x}u+Ke^{2x}\\
&\iff\\
&u-Ke^{2x}u=Ke^{2x}+1\\
&\iff\\
&u(1-Ke^{2x})=Ke^{2x}+1\\
&\iff\scriptstyle{(\text{suponemos que }1-Ke^{2x}\neq0)}\\
&u=\frac{1+Ke^{2x}}{1-Ke^{2x}}\\
&\iff\scriptstyle{(\text{deshago cambio de variable})}\\
&y(x)=\frac{1+Ke^{2x}}{1-Ke^{2x}}\\
\end{aligned}
$$

### Parte 2

- $(1 + y^2) y y' + (1 + y^2) = 0$

$$
\begin{aligned}
&(1 + y^2) y y' + (1 + y^2) = 0\\
&\iff\scriptstyle{(\forall x\in\mathbb{R}:(1 + y^2)>0)}\\
&y'y=\frac{-(1+y^2)}{(1+y^2)}\\
&\iff\\
&y'y=-1\\
&\iff\\
&\int y'ydx=\int-1dx\\
&\iff\scriptstyle{(u=y(x);du=y'(x)dx)}\\
&\int udu=-x+k_1\\
&\iff\\
&\frac{u^2}{2}=-x+k_1\\
&\iff\scriptstyle{(C=k_1-k_2)}\\
&u=\sqrt{2}\sqrt{-x+C}\\
&\iff\scriptstyle{(\text{deshago cambio de variable})}\\
&y(x)=\sqrt{2}\sqrt{-x+C}\\
\end{aligned}
$$

### Parte 3

- $x e^{2y} y' - (1 + e^{2y}) = 0$

$$
\begin{aligned}
&x e^{2y} y' - (1 + e^{2y}) = 0\\
&\iff\\
&y'=\frac{1+e^{2y}}{e^{2y}}\cdot\frac{1}{x}\\
&\iff\\
&\frac{e^{2y}y'}{1+e^{2y}}=\frac{1}{x}\\
&\iff\\
&\int\frac{e^{2y}y'}{1+e^{2y}}dx=\int\frac{1}{x}dx\\
&\iff\scriptstyle{(u=y(x);du=y'(x)dx)}\\
&\int\frac{e^{2u}}{1+e^{2u}}du=ln|x|+k_1\\
&\iff\scriptstyle{(\text{preparando otro cambio de variable})}\\
&\frac{1}{2}\int\frac{2e^{2u}}{1+e^{2u}}du=ln|x|+k_1\\
&\iff\scriptstyle{(v=1+e^{2u};dv=2e^{2u}du)}\\
&\frac{1}{2}\int\frac{dv}{v}=ln|x|+k_1\\
&\iff\\
&\frac{1}{2}ln|v|+k_2=ln|x|+k_1\\
&\iff\scriptstyle{(\text{deshago cambios de variable})}\\
&\frac{1}{2}ln|1+e^{2y}|+k_2=ln|x|+k_1\\
&\iff\scriptstyle{(C=2(k_1-k_2))}\\
&ln|1+e^{2y}|=2ln|x|+C\\
&\iff\scriptstyle{(n\cdot ln(x)=ln(x^n)\text{ y }(1+e^{2y})>0)}\\
&1+e^{2y}=e^{ln|x^2|+C}\\
&\iff\scriptstyle{(x^2>0\text{ y }K=e^C)}\\
&1+e^{2y}=Kx^2\\
&\iff\\
&e^{2y}=Kx^2-1\\
&\iff\\
&2y=ln(Kx^2-1)\\
&\iff\\
&y=\frac{1}{2}ln(Kx^2-1)\\
\end{aligned}
$$