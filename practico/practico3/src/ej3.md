# Ejercicio 3

## Consigna

Encontrar los límites de las siguientes sucesiones $(a_n)_{n \in \mathbb{N}}$:

1. $a_n = \frac{\cos(n)}{n}$
2. $a_n = \sqrt{n + 1} - \sqrt{n}$
3. $a_n = \frac{2n - 5}{n + 3 - 5^{1/n}}$
4. $a_n = \sqrt[n]{\alpha^n + \beta^n}, \quad \alpha, \beta \in \mathbb{R}^+$
5. $a_n = \sin\left(\frac{1}{n}\right)\cos(n)$
6. $a_n = \frac{n^\alpha}{e^n}, \quad \alpha \in \mathbb{R}$
7. $a_n = \frac{3^n + (-2)^n}{3^{n+1} + (-2)^{n+1}}$

## Resolución

### Sucesión #1

- $a_n = \frac{\cos(n)}{n}$

$$
\begin{aligned}
&\lim_{n\to\infty}\frac{\cos(n)}{n}\\
&=\scriptstyle{(\text{operando})}\\
&\lim_{n\to\infty}\cos(n)\cdot\frac{1}{n}\\
&=\scriptstyle{(cos(n)\text{ acotado y }\lim\frac{1}{n}=0)}\\
&0
\end{aligned}
$$

### Sucesión #2

- $a_n = \sqrt{n + 1} - \sqrt{n}$

$$
\begin{aligned}
&\lim_{n\to\infty}\sqrt{n + 1} - \sqrt{n}\\
&=\scriptstyle{(\text{sustitución por sucesiones equivalentes})}\\
&\lim_{n\to\infty}\sqrt{n} - \sqrt{n}\\
&=\scriptstyle{(\text{operando})}\\
&0
\end{aligned}
$$

### Sucesión #3

- $a_n = \frac{2n - 5}{n + 3 - 5^{1/n}}$

$$
\begin{aligned}
&\lim_{n\to\infty}\frac{2n - 5}{n + 3 - 5^{1/n}}\\
&=\scriptstyle{(\text{sustitución por sucesiones equivalentes})}\\
&\lim_{n\to\infty}\frac{2n}{n}\\
&=\scriptstyle{(\text{operando})}\\
&2\\
\end{aligned}
$$

### Sucesión #4

- $a_n = \sqrt[n]{\alpha^n + \beta^n}, \quad \alpha, \beta \in \mathbb{R}^+$

En este caso hay que dar algún pasito más, consideremos:

- $M=\max\{\alpha,\beta\}$

Y lo siguiente:

$$
\begin{aligned}
&M^n\leq\alpha^n+\beta^n\leq 2M^n\\
&\iff\scriptstyle{(\text{tomando raíz enésima})}\\
&M\leq\sqrt[n]{\alpha^n+\beta^n}\leq2^{\frac{1}{n}}M\\
&\iff\scriptstyle{(\text{tomando el límite})}\\
&\lim_{n\to\infty}M\leq\lim_{n\to\infty}\sqrt[n]{\alpha^n+\beta^n}\leq\lim_{n\to\infty}2^{\frac{1}{n}}M\\
&\iff\scriptstyle{(\text{operando y considerando }2^{\frac{1}{n}}\to1)}\\
&M\leq\lim_{n\to\infty}\sqrt[n]{\alpha^n+\beta^n}\leq M
\end{aligned}
$$

Por el teorema del Sándwich entonces:

- $\lim_{n\to\infty}\sqrt[n]{\alpha^n+\beta^n}=M=max\{\alpha,\beta\}$

### Sucesión #5

- $a_n = \sin\left(\frac{1}{n}\right)\cos(n)$

$$
\begin{aligned}
&\lim_{n\to\infty}\sin\left(\frac{1}{n}\right)\cos(n)\\
&=\scriptstyle{(\text{sustitución por sucesiones equivalentes})}\\
&\lim_{n\to\infty}\frac{1}{n}\cos(n)\\
&=\scriptstyle{(\text{límite ya conocido})}\\
&0\\
\end{aligned}
$$

### Sucesión #6

- $a_n = \frac{n^\alpha}{e^n}, \quad \alpha \in \mathbb{R}$

Este límite es teórico, por órden de crecimiento se tiene que $e^n$ crece más rapido que $n^{\alpha}$ para cualquier $\alpha\in\mathbb{R}$:

$$
\begin{aligned}
&\lim_{n\to\infty}\frac{n^\alpha}{e^n}\\
&=\scriptstyle{(\text{órden de crecimiento})}\\
&0
\end{aligned}
$$

### Sucesión #7

- $a_n = \frac{3^n + (-2)^n}{3^{n+1} + (-2)^{n+1}}$

Antes de empezar, factorizemos la sucesión de una forma más conveniente:

$$
\begin{aligned}
&\frac{3^n + (-2)^n}{3^{n+1} + (-2)^{n+1}}\\
&=\scriptstyle{(\text{sacando factor común }3^n)}\\
&\frac{3^n(1+(\frac{-2}{3})^n)}{3^n(3+(-2)(\frac{-2}{3})^n)}\\
&=\scriptstyle{(\text{sacando factor común })}\\
&\frac{1+(\frac{-2}{3})^n}{3+(-2)(\frac{-2}{3})^n}\\
\end{aligned}
$$

Ahora busquemos el límite:

$$
\begin{aligned}
&\lim_{n\to\infty} \frac{1+(\frac{-2}{3})^n}{3+(-2)(\frac{-2}{3})^n}\\
&=\scriptstyle{(\text{como }(\frac{-2}{3})^n\to0)}\\
&\frac{1}{3}
\end{aligned}
$$

**Observación:** Esta idea es clave para rematar el ejercicio:

- $(\frac{-2}{3})^n\to0$

Y la misma nace de que cuando trabajamos con límites en infinito, cualquier número $x\in(-1,1)$ elevado a $n$ tiende a 0.