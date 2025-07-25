# Ejercicio 3

## Consigna

Expresar en notación binómica:

1. $e^{i\frac{\pi}{2}}$
2. $3e^{\pi i}$
3. $\frac{1 - e^{\frac{\pi}{2}i}}{1 + e^{\frac{\pi}{2}i}}$
4. $(i + 1)^{100}$

## Resolución

### Parte 2

- $z=3e^{i\pi}$
    - Módulo: $|z|=3$
    - Argumento: $\theta=\pi$

Para hallar la notación binómica utilizamos que:

- $a=|z|\cdot cos\theta = 3\cdot cos(\pi)=-3$
- $b=|z|\cdot sen\theta = 3\cdot sen(\pi)0$

Por lo tanto:

- $z=-3+0i$

### Parte 3

- $z=\frac{1 - e^{\frac{\pi}{2}i}}{1 + e^{\frac{\pi}{2}i}}$

Antes que nada, obtengamos la notación binómica de $e^{i\frac{\pi}{2}}$ para obtener una expresión más fácil:

- Módulo: $|e^{i\frac{\pi}{2}}|=1$
- Argumento: $|e^{i\frac{\pi}{2}}|=\frac{\pi}{2}$

Entonces:

- $a = 1\cdot cos(\frac{\pi}{2})=0$
- $b = 1\cdot sen(\frac{\pi}{2})=1$

Por lo tanto:

- $e^{i\frac{\pi}{2}}=i$

Ahora, volviendo a $z$, tenemos que:

$$
\begin{aligned}
z&=\frac{1-i}{1+i}\\
&=\frac{1-i}{1+i}\cdot\frac{1-i}{1-i}\\
&=\frac{1-2i-1}{2}\\
&=\frac{-2i}{2}\\
&=-i
\end{aligned}
$$

### Parte 4

- $z=(i + 1)^{100}$

Claramente es imposible calcular esto con la notación binómica que tenemos, y recordando que para calcular productos, la notación polar es mucho más práctica, transformemos $i+1$ a dicha notación para facilitar el cálculo:

- $i+1=\sqrt{2}e^{i\frac{\pi}{2}}$

Por lo tanto:

$$
\begin{aligned}
z&=(\sqrt{2}e^{i\frac{\pi}{4}})^{100}\\
&=\sqrt{2}^{100}e^{i\frac{100\pi}{4}}\\
&=2^{50}e^{i25\pi}
\end{aligned}
$$

Lo que nos deja el siguiente módulo y argumento:

- Módulo: $2^{50}$
- Argumento: $25\pi\sim\pi$

Entonces ahora hallemos $a,b$ para la notación binómica:

- $a=2^{50}cos(\pi)=-2^{50}$
- $b=2^{50}sen(\pi)=0$

Entonces $z=-2^{50}$