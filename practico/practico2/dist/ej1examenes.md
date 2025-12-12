# Ejercicio 1 - Evaluaciones anteriores

## Consigna

Sea $y(x)$ la solución a la ecuación diferencial:

- $y''(x)-y'(x)-2y(x)=-2x^2+3$, que además cumple:
- $y(0)=0$
- $y'(0)=2$

Entonces:

1. $y(1)=e^2-e^{-1}$
2. $y(1)=\frac{e^2-e^{-1}}{2}$
3. $y(1)=e^{-1}-e^2+1$
4. $y(1)=\frac{e^2-e^{-1}}{e^2+e^{-1}}$
5. $y(1)=e^2-1$

## Resolución

Separemos el problema en las dos ecuaciones diferenciales que queremos resolver:

- $(H)\quad y''(x)-y'(x)-2y(x)=0$
- $(NH)\quad y''(x)-y'(x)-2y(x)=-2x^2+3$

### Homogénea

- $(H)\quad y''(x)-y'(x)-2y(x)=0$

Para resolver la homogénea queremos obtener las raíces de la ecuación característica:

- $\lambda^2-\lambda-2=0$

Para esto usamos Bháskara:

$$
\begin{aligned}
&\lambda=\frac{1\pm\sqrt{1+8}}{2}\\
&\iff\scriptstyle{(\text{operatoria})}\\
&\lambda=\frac{1\pm3}{2}\\
\end{aligned}
$$

Esto resulta en:

- $\lambda_1=2$
- $\lambda_2=-1$

Como las raíces son reales y diferentes, tenemos que la forma de la solución para la homogénea es:

- $y_H(x)=K_1e^{2x}+K_2e^{-x}$, y su derivada:
- $y_H'(x)=2K_1e^{2x}-K_2e^{-x}$

### No homogénea

- $(NH)\quad y''(x)-y'(x)-2y(x)=-2x^2+3$

Ahora queremos encontrar una solución particular para esta ecuación. Buscamos claramente algo polinómico.

- $y_P(x)=Ax^2+Bx+C$
- $y_P'(x)=2Ax+B$
- $y_P''(x)=2A$

Sustituimos esto en la ecuación:

$$
\begin{aligned}
&2A-(2Ax+B)-2(Ax^2+Bx+C)=-2x^2+3\\
&\iff\scriptstyle{(\text{separando términos según órdenes})}\\
&-2Ax^2+(-2A-2B)x+(2A-B-2C)=-2x^2+3
\end{aligned}
$$

Esto nos deja con el sistema:

$$
\begin{cases}
-2A=-2\\
-2A-2B=0\\
2A-B-2C=3
\end{cases}
$$

De donde sacamos que:

- $A=1$
- $B=-1$
- $C=0$

Por lo tanto la solución particular es:

- $y_P(x)=x^2-x$

### General

Tenemos la solución general de la homogénea, y una solución particular de la no homogénea. Con esto tenemos que una forma de la solución general es:

$$
\begin{aligned}
&y_G(x)=y_H(x)+y_P(x)\\
&\iff\scriptstyle{(\text{reemplazando por lo conocido})}\\
&y_G(x)=K_1e^{2x}+K_2e^{-x}+x^2-x\\
\end{aligned}
$$

También vamos a precisar su derivada así que:

- $y_G'(x)=2K_1e^{2x}-K_2e^{-x}+2x-1$

Usemos las condiciones iniciales:

- $y(0)=0$
- $y'(0)=2$

Entonces:

$$
\begin{aligned}
&y_G(0)=K_1e^0+K_2e^0\\
&\iff\scriptstyle{(\text{reemplazando lo conocido})}\\
&0=K_1e^0+K_2e^0\\
&=\scriptstyle{(\text{operatoria})}\\
&0=K_1+K_2\\
\end{aligned}
$$

Por otra parte:

$$
\begin{aligned}
&y_G'(0)=2K_1e^0-K_2e^0-1\\
&\iff\scriptstyle{(\text{reemplazando lo conocido})}\\
&2=2K_1e^0-K_2e^0-1\\
&\iff\scriptstyle{(\text{operatoria})}\\
&3=2K_1-K_2
\end{aligned}
$$

Vayamos con el sistema de ecuaciones entonces:

$$
\left(\begin{array}{cc|c}
1&1&0\\
2&-1&3\\
\end{array}\right)\sim
\left(\begin{array}{cc|c}
1&1&0\\
0&-3&3\\
\end{array}\right)
$$

De donde obtenemos que:

- $K_2=-1$
- $K_1=1$

Por lo tanto, la función solución es:

- $y_G(x)=e^{2x}-e^{-x}+x^2-x$

Calculemos $y(1)$:

$$
\begin{aligned}
&y_G(1)=e^2-e^{-1}\\
\end{aligned}
$$

Por lo tanto la respuesta correcta es la respuesta uno (o A).