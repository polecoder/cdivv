# Ejercicio 3

## Consigna

Sea $y(x)$ la solución a la ecuación diferencial

$$
\frac{y'(x)e^{x^2}}{x} = -2(1 + y^2(x))
$$

que cumple $y(0) = 0$. Entonces:

(A) $y(\sqrt{2}) = -e$  
(B) $y(\sqrt{2}) = \tan(1 + e^2)$  
(C) $y(\sqrt{2}) = \tan(1)$  
(D) $y(\sqrt{2}) = 1$
(E) $y(\sqrt{2}) = \tan(e^{-2}-1)$

## Resolución

Queremos resolver la ecuación diferencial planteada, para esto veamos a que podemos llegar despejando:

$$
\begin{aligned}
&\frac{y'(x)e^{x^2}}{x} = -2(1 + y^2(x))\\
&\iff\scriptstyle{(\text{operatoria})}\\
&y'(x)e^{x^2}=-2x(1+y^2(x))\\
&\iff\scriptstyle{(\text{operatoria})}\\
&\frac{y'(x)}{1+y^2(x)}=-2xe^{-x^2}\\
\end{aligned}
$$

Perfecto, es una ecuación de variables separables, por lo tanto podemos resolverla operando:

$$
\begin{aligned}
&\frac{y'(x)}{1+y^2(x)}=-2xe^{-x^2}\\
&\iff\scriptstyle{(\text{integrando ambas partes respecto de }x)}\\
&\int\frac{y'(x)}{1+y^2(x)}dx=\int-2xe^{-x^2}dx\\
&\iff\scriptstyle{(\text{cambio de variable: }u=y(x)dx;\ du=y'(x)dx)}\\
&\int\frac{1}{1+u^2}du=\int-2xe^{-x^2}dx\\
&\iff\scriptstyle{(\text{cambio de variable: }v=-x^2;\ dv=-2xdx)}\\
&\int\frac{1}{1+u^2}du=\int e^vdv\\
&\iff\scriptstyle{(\text{operatoria})}\\
&\arctan(u)+k_1=e^v+k_2\\
&\iff\scriptstyle{(\text{operatoria})}\\
&u=\tan(e^v+k_2-k_1)\\
&\iff\scriptstyle{(\text{operatoria})}\\
&u=\tan(e^v+C)\\
&\iff\scriptstyle{(\text{deshaciendo cambios de variable})}\\
&y(x)=\tan(e^{-x^2}+C)\\
\end{aligned}
$$

Apliquemos la condición inicial: $y(0) = 0$:

- $\tan(e^0+C)=0\implies\tan(1+C)=0$

De donde concluimos que $C=-1$, por lo tanto tenemos que:

- $y(\sqrt{2})=\tan(e^{-\sqrt{2}^2}-1)=\tan(e^{-2}-1)$

Con esto concluimos que la respuesta correcta es la opción (E).