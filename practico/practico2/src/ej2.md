# Ejercicio 2

## Consigna

Resolver las siguientes ecuaciones diferenciales mediante el cambio de variables $u(x) = \frac{y(x)}{x}$, de forma de llevarlas a ecuaciones de variables separadas del tipo $u' = A(u)B(x)$:

1. $x^2 y' + y(y - x) = 0$
2. $(x + y) y' = x - y$

## Resolución

### Parte 1

- $x^2 y' + y(y - x) = 0$

El cambio de variables a utilizar es el siguiente:

- $u(x)=\frac{y(x)}{x}$, por lo tanto:
- $u'(x)=\frac{x\cdot y'(x)-y(x)}{x^2}$

En base a esto, veamos de despejar $y'$ e $y$ para sustituirlas por una expresión en función de $u$ y $x$:

- $y(x)=x\cdot u(x)$

Veamos para $y'(x)$:

$$
\begin{aligned}
&y'(x)=\frac{u'(x)x^2+y(x)}{x}\\
&\iff\\
&y'(x)=\frac{u'(x)x^2+x\cdot u(x)}{x}\\
&\iff\\
&y'(x)=u'(x)x+u(x)\\
\end{aligned}
$$

Ahora si, sustituimos en la ecuación diferencial:

$$
\begin{aligned}
&x^2 y' + y(y - x) = 0\\
&\iff\scriptstyle{(y=xu;y'=u'x+u)}\\
&x^2(u'x+u)+xu(xu-x)=0\\
&\iff\\
&x^2(u'x+u)+x^2u(u-1)=0\\
&\iff\\
&x^3u'+x^2u+x^2u^2-x^2u=0\\
&\iff\\
&x^3u'+x^2u^2=0\\
&\iff\scriptstyle{(\text{divido por }x^2\neq0)}\\
&xu'+u^2=0\\
&\iff\\
&u'=\frac{-u^2}{x}\\
\end{aligned}
$$

Donde esto último si es de variables separables, operando:

$$
\begin{aligned}
&u'=\frac{-u^2}{x}\\
&\iff\\
&\frac{u'}{-u^2}=\frac{1}{x}\\
&\iff\\
&\int\frac{u'}{-u^2}dx=\int\frac{1}{x}dx\\
&\iff\scriptstyle{(v=u(x);dv=u'(x)dx)}\\
&\int\frac{u'}{-u^2}dx=ln|x|+k_1\\
&\iff\\
&\int-v^{-2}dv=ln|x|+k_1\\
&\iff\\
&-(\frac{v^{-1}}{-2+1}+k_2)=ln|x|+k_1\\
&\iff\\
&\frac{1}{v}-k_2=ln|x|+k_1\\
&\iff\scriptstyle{(C=k_1+k_2)}\\
&v=\frac{1}{ln|x|+C}\\
&\iff\scriptstyle{(\text{deshaciendo el cambio de variable})}\\
&u=\frac{1}{ln|x|+C}\\
\end{aligned}
$$

Y ahora recordando que $y=ux$:

- $y=\frac{x}{ln|x|+C}$

### Parte 2

- $(x + y) y' = x - y$

El cambio de variables a utilizar es el siguiente:

- $u(x)=\frac{y(x)}{x}$, por lo tanto:
- $u'(x)=\frac{x\cdot y'(x)-y(x)}{x^2}$

En base a esto, veamos de despejar $y'$ e $y$ para sustituirlas por una expresión en función de $u$ y $x$:

- $y(x)=x\cdot u(x)$

Veamos para $y'(x)$:

$$
\begin{aligned}
&y'(x)=\frac{u'(x)x^2+y(x)}{x}\\
&\iff\\
&y'(x)=\frac{u'(x)x^2+x\cdot u(x)}{x}\\
&\iff\\
&y'(x)=u'(x)x+u(x)\\
\end{aligned}
$$

Ahora si, sustituimos en la ecuación diferencial:

$$
\begin{aligned}
&(x+y)y'=x-y\\
&\iff\\
&(x+xu)(u'x+u)=x-xu\\
&\iff\\
&x(1+u)(u'x+u)=x(1-u)\\
&\iff\scriptstyle{(\text{dividimos por }x\neq0)}\\
&(1+u)(u'x+u)=1-u\\
&\iff\\
&u'x+u+uu'x+u^2=1-u\\
&\iff\\
&u'(x+xu)=1-2u-u^2\\
&\iff\\
&u'x(1+u)=1-2u-u^2\\
&\iff\\
&u'=\frac{1-2u-u^2}{x(1+u)}\\
&\iff\\
&u'=\frac{1-2u-u^2}{1+u}\cdot\frac{1}{x}\\
\end{aligned}
$$

Donde esto último si es de variables separables, operando:

$$
\begin{aligned}
&u'\frac{1+u}{1-2u-u^2}=\frac{1}{x}\\
&\iff\\
&\int u'\frac{1+u}{2-(u+1)^2}dx=\int\frac{1}{x}dx\\
&\iff\scriptstyle{(\text{v=1+u(x);dv=u'(x)dx})}\\
&\int \frac{v}{2-v^2}dv=ln|x|+k_1\\
&\iff\scriptstyle{(w=2-v^2;dw=-2vdv)}\\
&-\frac{1}{2}\int\frac{dw}{w}=ln|x|+k_1\\
&\iff\\
&-\frac{1}{2}ln|w|+k_2=ln|x|+k_1\\
&\iff\scriptstyle{(\text{deshaciendo cambio de variables})}\\
&-\frac{1}{2}ln|2-v^2|+k_2=ln|x|+k_1\\
&\iff\scriptstyle{(\text{deshaciendo cambios de variables})}\\
&ln|2-(1+u)^2|+k_2=-2(ln|x|+k_1)\\
&\iff\scriptstyle{(C=-2(k_1-k_2))}\\
&ln|2-(1+u)^2|=ln|x^{-2}|+C\\
&\iff\\
&2-(1+u)^2=\pm C|\frac{1}{x^2}|\\
&\iff\scriptstyle{(K=\pm C)}\\
&(1+u)^2=2-\frac{K}{x^2}\\
&\iff\\
&u=-1\pm\sqrt{2-\frac{K}{x^2}}\\
\end{aligned}
$$

Y ahora recordando que $y=ux$:

- $y=-x\pm\sqrt{2x^2-K}$