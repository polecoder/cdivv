# Ejercicio 3

## Consigna

Dibuje el dominio y los conjuntos de nivel de las siguientes funciones:

1. $\tfrac{1}{\sqrt{x^2 + y^2}}$
2. $\log\left(\tfrac{1 - x^2 - y^2}{x^2 + y^2}\right)$
3. $\tan\left(\tfrac{x^2}{y}\right)$
4. $\arctan\left(\tfrac{x^2}{y}\right)$

## Resolución

### Función #1

- $\tfrac{1}{\sqrt{x^2 + y^2}}$

Veamos el dominio de la función:

- $D=R^2\setminus\{(0,0)\}$

Veamos ahora los conjuntos de nivel:

- Si $a<0$ entonces $C_a=\emptyset$, pues ambos el numerador y denominador siempre son positivos
- Si $a=0$ también $C_0=\emptyset$, pues el numerador es constante $1$.
- Si $a>0$, entonces $\frac{1}{\sqrt{x^2+y^2}}\to 1=a(x^2+y^2)$.
    Por lo tanto $C_a=\{(x,y)\in D: \|(x,y)\|^2=\frac{1}{a}\}$

### Función #2

- $\log\left(\tfrac{1 - x^2 - y^2}{x^2 + y^2}\right)$

Veamos el dominio de la función, para esto tenemos dos partes que verificar, primero que el denominador de la fracción no se anule, y luego que el término al que aplicamos logarítmo sea mayor que $0$.

**Primera restricción:**

Queremos excluir $(x,y)=(0,0)$ pues es el único punto que anula la fracción.

**Segunda restricción:**

- $\tfrac{1 - x^2 - y^2}{x^2 + y^2}>0$

Esto sucede sii $1-x^2-y^2>0$, es decir sii:

- $x^2+y^2<1$

Entonces juntando las restricciones, tenemos que:

- $D=\{(x,y)\in\mathbb{R}^2: \|(x,y)\|^2<1\}\setminus \{(0,0)\}$

Ahora vayamos por los conjuntos de nivel, para esto tenemos que hacer un despeje:

$$
\begin{aligned}
&\log\left(\frac{1-x^2-y^2}{x^2+y^2}\right)=a\\
&\iff\\
&\frac{1-x^2-y^2}{x^2+y^2}=e^a\\
&\iff\\
&1-x^2-y^2=e^a(x^2+y^2)\\
&\iff\\
&1=e^ax^2+e^ay^2+x^2+y^2\\
&\iff\\
&1=x^2(e^a+1)+y^2(e^a+1)\\
&\iff\\
&1=(e^a+1)(x^2+y^2)\\
&\iff\\
&\frac{1}{e^a+1}=x^2+y^2\\
\end{aligned}
$$

Por lo tanto, tenemos que los conjuntos de nivel para cualquier $a$ son:

- $C_a=\{(x,y)\in D: \|(x,y)\|^2=\frac{1}{e^a+1}\}$

### Función #3

- $\tan\left(\tfrac{x^2}{y}\right)$

Veamos el dominio de la función, para esto observemos que la función $\tan(x)$ está bien definida sii $x\neq \frac{\pi}{2}+2k\pi$ para todo $k\in\mathbb{Z}$. Apliquemos esta idea a la función.

$$
\begin{aligned}
&\frac{x^2}{y}\neq\frac{\pi}{2}+2k\pi\\
&\iff\\
&\frac{x^2}{y}\neq\frac{(4k+1)\pi}{2}\\
&\iff\\
&x^2\neq\frac{(4k+1)\pi}{2}y\\
&\iff\\
&x^2\cdot\frac{2}{(4k+1)\pi}\neq y\\
&\iff\\
&\frac{2x^2}{(4k+1)\pi}\neq y\\
\end{aligned}
$$

Además $y$ tiene que ser distinto de $0$ pues sino anularía la fracción. Entonces:

$D=\{(x,y)\in\mathbb{R}^2: y\neq0, y\neq \frac{2x^2}{(4k+1)\pi}\}$

Ahora podemos pasar a los conjuntos de nivel:

- Si $a=0$, entonces $C_0=\{(x,y)\in D: x=0\}$
- Si $a\neq0$, vale el siguiente razonamiento:

$$
\begin{aligned}
&\tan\left(\frac{x^2}{y}\right)=a\\
&=\\
&\frac{x^2}{y}=\arctan(a)\\
&=\\
&y=\frac{x^2}{\arctan(a)}
\end{aligned}
$$

- Por lo tanto, si $a\neq0$, entonces $C_a=\{(x,y)\in D: y=\frac{x^2}{\arctan(a)}\}$

### Función #4

- $\arctan\left(\tfrac{x^2}{y}\right)$

Para el dominio solamente tenemos que excluir los puntos tales que $y=0$, pues la función $\arctan(x)$ está definida para todo $x\in\mathbb{R}$.

- $D=\{(x,y)\in\mathbb{R}: y\neq0\}$

Veamos ahora los conjuntos de nivel:

- Si $a\notin(-\frac{\pi}{2},\frac{\pi}{2})$, entonces $C_a=\emptyset$, pues $\arctan(x)$ solo devuelve valores en ese intervalo.
- Si $a\in(-\frac{\pi}{2},\frac{\pi}{2})\setminus\{(0,0)\}$, entonces podemos obtener su conjunto de nivel operando:

$$
\begin{aligned}
&\arctan\left(\frac{x^2}{y}\right)=a\\
&\iff\\
&\frac{x^2}{y}=\tan(a)\\
&\iff\\
&y=\frac{x^2}{\tan(a)}
\end{aligned}
$$

- Por lo tanto $a\in(-\frac{\pi}{2},\frac{\pi}{2})\setminus\{(0,0)\}$, entonces $C_a=\{(x,y)\in D:y=\frac{x^2}{\tan(a)}\}$

- Si $a=0$, entonces $C_0=\{(x,y)\in D: x=0\}$
