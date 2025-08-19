# Ejercicio 8

## Consigna

Hallar la solución de cada una de las siguientes ecuaciones diferenciales, con las condiciones iniciales dadas:

1. $y'' + 2y' + 2y = \cos(2x),\quad y(0) = 1,\ y'(0) = 0$
2. $y'' + 2y' + 2y = \sin(2x),\quad y(0) = 1,\ y'(0) = 0$
3. $y'' + 2y' + 2y = \cos(2x) + \sin(2x),\quad y(0) = 1,\ y'(0) = 0$
4. $y'' + y = 3x^2 - 5x,\quad y(0) = 1,\ y'(0) = 0$
5. $y'' + 4y' + 3y = 3e^x + x,\quad y(0) = 1,\ y'(0) = 0$
6. $y'' + y = (1 + x)^2,\quad y(0) = 1,\ y'(0) = 0$
7. $y'' + 2y' + y = x,\quad y(0) = 0,\ y'(0) = 0$
8. $y'' + y = \cos x,\quad y(0) = 0,\ y'(0) = 1$

## Resolución

### Ecuación 1

- $y'' + 2y' + 2y = \cos(2x),\quad y(0) = 1,\ y'(0) = 0$

Tenemos las siguientes ecuaciones por resolver:

- $(H)\quad y'' + 2y' + 2y=0$
- $(NH)\quad y'' + 2y' + 2y=cos(2x)$

#### Solución de $(H)$

Hallemos las raíces de la ecuación característica $\lambda^2+2\lambda+2=0$:

- $\lambda_1=-1+i$
- $\lambda_2=-1-i$

Como son imaginarias y diferentes, tenemos que la solución general es la siguiente:

- $y_H=C_1e^{-x}cos(x)+C_2e^{-x}sin(x)$ y su derivada:
- $y'_H=C_1(-e^{-x}cos(x)-e^{-x}sin(x))+C_2(-e^{-x}sin(x)+e^{-x}cos(x))$

#### Solución de $(NH)$

Buscamos una solución $y_P$ que tenga la siguiente forma:

- $y_P=Acos(2x)+Bsin(2x)$
- $y_P'=-2Asin(2x)+2Bcos(2x)$
- $y_P''=-4Acos(2x)-4Bsin(2x)$

Con esto podemos sustituir en la ecuación diferencial:

$$
\begin{aligned}
&y'' + 2y' + 2y = \cos(2x)\\
&\iff\\
&-4Acos(2x)-4Bsin(2x)+2(-2Asin(2x)+2Bcos(2x))+2(Acos(2x)+Bsin(2x))=cos(2x)\\
&\iff\\
&sin(2x)(-4B-4A+2B)+cos(2x)(-4A+4B+2A)=cos(2x)
\end{aligned}
$$

De donde obtenemos el siguiente sistema de ecuaciones:

$$
\begin{cases}
-4A-2B=0\\
-2A+4B=1
\end{cases}
$$

De donde obtenemos:

- $B=\frac{1}{5}$
- $A=-\frac{1}{10}$

Entonces la solución particular de $(NH)$ es la siguiente:

$y_P=-\frac{1}{10}cos(2x)+\frac{1}{5}sin(2x)$

#### Solución general de $(NH)$

- $y_G=y_H+y_P$
- $y_G=C_1e^{-x}cos(x)+C_2e^{-x}sin(x)-\frac{1}{10}cos(2x)+\frac{1}{5}sin(2x)$
- $y_G'=C_1(-e^{-x}cos(x)-e^{-x}sin(x))+C_2(-e^{-x}sin(x)+e^{-x}cos(x))+\frac{2}{10}sin(2x)+\frac{2}{5}cos(2x)$

Ahora usamos las condiciones iniciales:

- $y(0)=1$, entonces:

    $$
    \begin{aligned}
    &C_1e^{-0}cos(0)+C_2e^{-0}sin(0)-\frac{1}{10}cos(0)+\frac{1}{5}sin(0)=1\\
    &\iff\\
    &C_1-\frac{1}{10}=1\\
    &\iff\\
    &C_1=\frac{11}{10}\\
    \end{aligned}
    $$

- $y'(0)=0$, entonces:

    $$
    \begin{aligned}
    &C_1(-e^{-0}cos(0)-e^{-0}sin(0))+C_2(-e^{-0}sin(0)+e^{-0}cos(0))+\frac{2}{10}sin(0)+\frac{2}{5}cos(0)\\
    &\iff\\
    &-C_1+C_2+\frac{2}{5}=0\\
    &\iff\scriptstyle{(C_1=\frac{11}{10})}\\
    &-\frac{11}{10}+C_2+\frac{2}{5}=0\\
    &\iff\\
    &C_2=\frac{7}{10}\\
    \end{aligned}
    $$

Entonces la solución al problema es:

- $\frac{11}{10}e^{-x}cos(x)+\frac{7}{10}e^{-x}sin(x)-\frac{1}{10}cos(2x)+\frac{1}{5}sin(2x)$

### Ecuación 2

- $y'' + 2y' + 2y = \sin(2x),\quad y(0) = 1,\ y'(0) = 0$

Tenemos las siguientes ecuaciones por resolver:

- $(H)\quad y'' + 2y' + 2y=0$
- $(NH)\quad y'' + 2y' + 2y=\sin(2x)$

#### Solución de $(H)$

Hallemos las raíces de la ecuación característica $\lambda^2+2\lambda+2=0$:

- $\lambda_1=-1+i$
- $\lambda_2=-1-i$

Como son imaginarias y diferentes, tenemos que la solución general es la siguiente:

- $y_H=C_1e^{-x}\cos(x)+C_2e^{-x}\sin(x)$ y su derivada:
- $y'_H=C_1(-e^{-x}\cos(x)-e^{-x}\sin(x))+C_2(-e^{-x}\sin(x)+e^{-x}\cos(x))$

#### Solución de $(NH)$

Buscamos una solución $y_P$ que tenga la siguiente forma:

- $y_P=A\cos(2x)+B\sin(2x)$
- $y_P'=-2A\sin(2x)+2B\cos(2x)$
- $y_P''=-4A\cos(2x)-4B\sin(2x)$

Con esto podemos sustituir en la ecuación diferencial:

$$
\begin{aligned}
&y'' + 2y' + 2y = \sin(2x)\\
&\iff\\
&-4A\cos(2x)-4B\sin(2x)+2(-2A\sin(2x)+2B\cos(2x))+2(A\cos(2x)+B\sin(2x))=\sin(2x)\\
&\iff\\
&\sin(2x)(-4B-4A+2B)+\cos(2x)(-4A+4B+2A)=\sin(2x)
\end{aligned}
$$

De donde obtenemos el siguiente sistema de ecuaciones:

$$
\begin{cases}
-4A-2B=1\\
-2A+4B=0
\end{cases}
$$

De donde obtenemos que:

- $A=-\frac{1}{5}$
- $B=-\frac{1}{10}$

Entonces la solución particular de $(NH)$ es la siguiente:

- $y_P=-\frac{1}{5}\cos(2x)-\frac{1}{10}\sin(2x)$

#### Solución general de $(NH)$

- $y_G=y_H+y_P$
- $y_G=C_1e^{-x}cos(x)+C_2e^{-x}sin(x)-\frac{1}{5}cos(2x)-\frac{1}{10}sin(2x)$
- $y_G'=C_1(-e^{-x}cos(x)-e^{-x}sin(x))+C_2(-e^{-x}sin(x)+e^{-x}cos(x))-\frac{2}{5}sin(2x)-\frac{1}{5}cos(2x)$

Ahora usamos las condiciones iniciales:

- $y(0)=1$, entonces:

    $$
    \begin{aligned}
    &C_1e^{-0}cos(0)+C_2e^{-0}sin(0)-\frac{1}{5}cos(0)-\frac{1}{10}sin(0)=1\\
    &\iff\\
    &C_1-\frac{1}{5}=1\\
    &\iff\\
    &C_1=\frac{6}{5}\\
    \end{aligned}
    $$

- $y'(0)=0$, entonces:

    $$
    \begin{aligned}
    &C_1(-e^{-0}cos(0)-e^{-0}sin(0))+C_2(-e^{-0}sin(0)+e^{-0}cos(0))-\frac{2}{5}sin(0)-\frac{1}{5}cos(0)=0\\
    &\iff\\
    &-C_1+C_2-\frac{1}{5}=0\\
    &\iff\scriptstyle{(C_1=\frac{6}{5})}\\
    &-\frac{6}{5}+C_2-\frac{1}{5}=0\\
    &\iff\\
    &C_2=\frac{7}{5}\\
    \end{aligned}
    $$

Entonces la solución al problema es:

- $y_G=\frac{6}{5}e^{-x}cos(x)+\frac{7}{5}e^{-x}sin(x)-\frac{1}{5}cos(2x)-\frac{1}{10}sin(2x)$

### Ecuación 3

- $y'' + 2y' + 2y = \cos(2x) + \sin(2x),\quad y(0) = 1,\ y'(0) = 0$

Observemos que ya tenemos una solución general para:

- $y'' + 2y' + 2y = \cos(2x)$
- $y'' + 2y' + 2y = \sin(2x)$

Sumar las soluciones generales, nos da la solución general de la ecuación diferencial que queremos resolver, entonces hacemos eso:

$$
\begin{aligned}
&y_G=(C_1e^{-x}cos(x)+C_2e^{-x}sin(x)-\frac{1}{10}cos(2x)+\frac{1}{5}sin(2x))+(C_1e^{-x}cos(x)+C_2e^{-x}sin(x)-\frac{1}{5}cos(2x)-\frac{1}{10}sin(2x))\\
&y_G=C_1e^{-x}cos(x)+C_2e^{-x}sin(x)-\frac{3}{10}cos(2x)+\frac{1}{10}sin(2x)\\
\end{aligned}
$$

Calculamos también la derivada ya que la vamos a utilizar:

- $y'_G=C_1(-e^{-x}\cos(x)-e^{-x}\sin(x))+C_2(-e^{-x}\sin(x)+e^{-x}\cos(x))+\frac{3}{5}\sin(2x)+\frac{1}{5}\cos(2x)$, simplificando:
- $y'_G=C_1e^{-x}(-\cos(x)-\sin(x))+C_2e^{-x}(-\sin(x)+\cos(x))+\frac{3}{5}\sin(2x)+\frac{1}{5}\cos(2x)$

Ahora, aplicando las condiciones iniciales:

- $y(0)=1$, entonces:

    $$
    \begin{aligned}
    &C_1e^{-0}cos(0)+C_2e^{-0}sin(0)-\frac{3}{10}cos(0)+\frac{1}{10}sin(0)=1\\
    &\iff\\
    &C_1-\frac{3}{10}=1\\
    &\iff\\
    &C_1=\frac{13}{10}\\
    \end{aligned}
    $$

- $y'(0)=0$, entonces:

    $$
    \begin{aligned}
    &C_1e^{-0}(-\cos(0)-\sin(0))+C_2e^{-0}(-\sin(0)+\cos(0))+\frac{3}{5}\sin(0)+\frac{1}{5}\cos(0)=0\\
    &\iff\\
    &-C_1+C_2+\frac{1}{5}=0\\
    &\iff\scriptstyle{(C_1=\frac{13}{10})}\\
    &-\frac{13}{10}+C_2+\frac{1}{5}=0\\
    &\iff\\
    &C_2=\frac{11}{10}\\
    \end{aligned}
    $$

Entonces la solución al problema es:

- $y_G=\frac{13}{10}e^{-x}cos(x)+\frac{11}{10}e^{-x}sin(x)-\frac{3}{10}cos(2x)+\frac{1}{10}sin(2x)$

### Ecuación 4

- $y''+y=3x^2-5x,\quad y(0)=1,y'(0)=0$

Tenemos las siguientes ecuaciones por resolver:

- $(H)\quad y''+y=0$
- $(NH)\quad y''+y=3x^2-5x$

#### Solución de $(H)$

Hallemos las raíces de la ecuación característica $\lambda^2+1=0$:

- $\lambda_1=i$
- $\lambda_2=-i$

Como son imaginarias y diferentes, tenemos que la solución general es la siguiente:

- $y_H=C_1\cos(x)+C_2\sin(x)$ y su derivada:
- $y'_H=-C_1\sin(x)+C_2\cos(x)$

#### Solución de $(NH)$

Buscamos una solución $y_P$ que tenga la siguiente forma:

- $y_P=Ax^2+Bx+C$
- $y_P'=2Ax+B$
- $y_P''=2A$

Con esto podemos sustituir en la ecuación diferencial:

$$
\begin{aligned}
&y''+y=3x^2-5x\\
&\iff\\
&2A+Ax^2+Bx+C=3x^2-5x\\
&\iff\\
&Ax^2+Bx+(C+2A)=3x^2-5x
\end{aligned}
$$

De donde obtenemos el siguiente sistema de ecuaciones:

$$
\begin{cases}
A=3\\
B=-5\\
C+2A=0
\end{cases}
$$

De donde obtenemos que:

- $C=-6$

Entonces la solución particular de $(NH)$ es la siguiente:

- $y_P=3x^2-5x-6$

#### Solución general de $(NH)$

- $y_G=y_H+y_P$
- $y_G=C_1\cos(x)+C_2\sin(x)+3x^2-5x-6$
- $y_G'=-C_1\sin(x)+C_2\cos(x)+6x-5$

Ahora usamos las condiciones iniciales:

- $y(0)=1$, entonces:

    $$
    \begin{aligned}
    &C_1\cos(x)+C_2\sin(x)+3x^2-5x-6\\
    &\iff\\
    &C_1-6=1\\
    &\iff\\
    &C_1=7\\
    \end{aligned}
    $$

- $y'(0)=0$, entonces:

    $$
    \begin{aligned}
    &-C_1\sin(x)+C_2\cos(x)+6x-5=0\\
    &\iff\\
    &C_2-5=0\\
    &\iff\\
    &C_2=5
    \end{aligned}
    $$

Entonces la solución al problema es:

- $y_G=7\cos(x)+5\sin(x)+3x^2-5x-6$