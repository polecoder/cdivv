# Ejercicio 4

## Consigna

1. Hallar la solución general de las siguientes ecuaciones diferenciales:

    1. $y'' - 5y' + 6y = 0$
    2. $y'' + y' = 0$
    3. $y'' + 4y' + 5y = 0$
    4. $y'' + 2y' + y = 0$

2. Resolver los siguientes problemas de valores iniciales:

    1. $y'' - 5y' + 6y = 0,\quad y(1) = e^2,\ y'(1) = 3e^2$
    2. $y'' - 6y' + 5y = 0,\quad y(0) = 3,\ y'(0) = 11$
    3. $y'' + 4y' + 5y = 0,\quad y(0) = 1,\ y'(0) = 0$
    4. $y'' + 8y' - 9y = 0,\quad y(1) = 2,\ y'(1) = 0$

## Resolución

Se harán la parte 1 y 2 simultaneamente, ya que los valores iniciales solo son un pasito extra.

### Ecuación 1

- $y'' - 5y' + 6y = 0,\quad y(1) = e^2,\ y'(1) = 3e^2$

Buscamos las raíces de la ecuación característica $\lambda^2-5\lambda+6=0$:

- $\lambda_1=3$
- $\lambda_2=2$

Como son reales y diferentes, tenemos que la solución general es la siguiente:

- $y=C_1e^{3x}+C_2e^{2x}$ y su derivada:
- $y'= 3C_1e^{3x}+2C_2e^{2x}$

Ahora podemos usar los valores iniciales para obtener la solución que nos piden.
Utilizándolos obtenemos el siguiente sistema de ecuaciones:

$$
\begin{cases}
C_1e^3+C_2e^2=e^2\\
3C_1e^3+2C_2e^2=3e^2\\
\end{cases}
$$

Es decir:

$$
\begin{aligned}
&\left(
\begin{array}{cc|c}
e^3&e^2&e^2\\
3e^3&2e^2&3e^2
\end{array}
\right)\\
&\sim\scriptstyle{(\text{F2-3F1})}\\
&\left(
\begin{array}{cc|c}
e^3&e^2&e^2\\
0&-e^2&0
\end{array}
\right)
\end{aligned}
$$

De donde obtenemos que:

- $C_2=0$
- $C_1=\frac{1}{e}$

Por lo tanto la solución es:

$$
\begin{aligned}
y(x)&=\frac{1}{e}e^{3x}\\
&=e^{3x-1}
\end{aligned}
$$

### Ecuación 2

- $y'' - 6y' + 5y = 0,\quad y(0) = 3,\ y'(0) = 11$

Buscamos las raíces de la ecuación característica $\lambda^2-6\lambda+5=0$:

- $\lambda_1=1$
- $\lambda_2=5$

Como son reales y diferentes, tenemos que la solución general es la siguiente:

- $y=C_1e^x+C_2e^{5x}$ y su derivada:
- $y'= C_1e^x+5C_2e^{5x}$

Ahora podemos usar los valores iniciales para obtener la solución que nos piden.
Utilizándolos obtenemos el siguiente sistema de ecuaciones:

$$
\begin{cases}
C_1+C_2=3\\
C_1+5C_2=11
\end{cases}
$$

Es decir:

$$
\begin{aligned}
&\left(
\begin{array}{cc|c}
1&1&3\\
1&5&11\\
\end{array}
\right)\\
&\sim\scriptstyle{(\text{F2-F1})}\\
&\left(
\begin{array}{cc|c}
1&1&3\\
0&4&8\\
\end{array}
\right)\\
\end{aligned}
$$

De donde obtenemos que:

- $C_2=2$
- $C_1=1$

Por lo tanto la solución es:

$$
\begin{aligned}
y(x)=e^x+2e^{5x}
\end{aligned}
$$

### Ecuación 3

- $y'' + 4y' + 5y = 0,\quad y(0) = 1, y'(0) = 0$

Buscamos las raíces de la ecuación característica $\lambda^2+4\lambda+5=0$:

- $\lambda_1=-2+i$
- $\lambda_2=-2-i$

Como son imaginarias y diferentes, tenemos que la solución general es la siguiente:

- $y=C_1e^{-2x}cos(x)+C_2e^{-2x}sin(x)$ y su derivada:
- $y'= C_1(-2e^{-2x}cos(x)-e^{-2x}sin(x))+C_2(-2e^{-2x}sin(x)+e^{-2x}cos(x))$

Ahora podemos usar los valores iniciales para obtener la solución que nos piden.
Utilizándolos obtenemos el siguiente sistema de ecuaciones:

$$
\begin{cases}
C_1=1\\
-2C_1+C_2=0
\end{cases}
$$

De donde obtenemos que:

- $C_1=1$
- $C_2=2$

Por lo tanto la solución es:

$$
\begin{aligned}
y(x)=e^{-2x}cos(x)+2e^{-2x}sin(x)
\end{aligned}
$$

### Ecuación 4

- $y'' + 8y' - 9y = 0,\quad y(1) = 2, y'(1) = 0$

Buscamos las raíces de la ecuación característica $\lambda^2+8\lambda-9=0$:

- $\lambda_1=1$
- $\lambda_2=-9$

Como son reales y diferentes, tenemos que la solución general es la siguiente:

- $y=C_1e^x+C_2e^{-9x}$ y su derivada:
- $y'= C_1e^x-9C_2e^{-9x}$

Ahora podemos usar los valores iniciales para obtener la solución que nos piden.
Utilizándolos obtenemos el siguiente sistema de ecuaciones:

$$
\begin{cases}
C_1e+C_2e^{-9}=2\\
C_1e+-9C_2e^{-9}=0
\end{cases}
$$

Es decir:

$$
\begin{aligned}
&\left(
\begin{array}{cc|c}
e&e^{-9}&2\\
e&-9e^{-9}&0\\
\end{array}
\right)\\
&\sim\scriptstyle{(\text{F2-F1})}\\
&\left(
\begin{array}{cc|c}
e&e^{-9}&2\\
0&-10e^{-9}&-2\\
\end{array}
\right)\\
\end{aligned}
$$

De donde obtenemos que:

- $C_2=\frac{-2}{-10e^{-9}}=\frac{1}{5}e^9$
- $C_1=\frac{9}{5e}=\frac{9}{5}e^{-1}$

Por lo tanto la solución es:

$$
\begin{aligned}
y(x)&=\frac{9}{5}e^{-1}e^x+\frac{1}{5}e^9e^{-9x}\\
&=\frac{9}{5}e^{x-1}+\frac{1}{5}e^{-9x+9}
\end{aligned}
$$