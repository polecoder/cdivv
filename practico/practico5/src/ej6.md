# Ejercicio 6

## Consigna

Clasificar:

1. $\int_{-\infty}^{+\infty} e^{-x^2}dx$
2. $\int_0^1 \frac{e^{-x}}{x}dx$
3. $\int_0^1 \frac{\log(x)}{\sqrt{x}}dx$
4. $\int_1^{+\infty} \frac{\sin(x)}{x^2}dx$
5. $\int_0^{+\infty} \sin^2(t)dt$
6. $\int_0^{+\infty} \frac{x}{\sqrt{x^4 + 1}}dx$
7. $\int_{-\infty}^{+\infty} \frac{x}{\cosh(x)}dx$
8. $\int_{-1}^{1} \frac{dx}{x^2 - 1}$
9. $\int_0^{+\infty} \frac{\cos(x)}{\sqrt{x}}dx$
10. $\int_0^{+\infty} \frac{e^{-\sqrt{x}}}{\sqrt{x}}dx$
11. $\int_0^{+\infty} e^{x^2-\frac{1}{x^2}}dx$
12. $\int_{-1}^{1} \frac{e^{-\frac{1}{x - 1}}}{(x - 1)^2}dx$
13. $\int_0^{\frac{\pi}{2}} \frac{dx}{\sin^\alpha(x)\cos^\beta(x)}$, con $\alpha, \beta \in \mathbb{R}$

## Resolución

### Integral #1

- $\int_{-\infty}^{+\infty} e^{-x^2}dx$

La integral no tiene puntos problemáticos, pero tenemos que separar en dos para contemplar los intervalos infinitos.

- $\int_{-\infty}^{+\infty}\frac{1}{e^{x^2}}dx=\int_{-\infty}^{0}\frac{1}{e^{x^2}}dx+\int_{0}^{+\infty}\frac{1}{e^{x^2}}dx$

Observemos además que la función es par, es decir que:

- $f(-x)=f(x)$, se verifica:
- $f(-x)=e^{-(-x)^2}=e^{-x^2}=f(x)$

Por lo que basta con estudiar:

- $\int_{0}^{+\infty}\frac{1}{e^{x^2}}dx$

Para esto sabemos que a partir de $x=1$ se cumple la siguiente desigualdad:

- $e^{x^2}\geq x^2$

Tomando opuestos:

- $\frac{1}{e^{x^2}}\leq\frac{1}{x^2}$

Por lo tanto para el intervalo $[1,+\infty)$ podemos decir que la integral impropia es convergente por comparación con $\int_{1}^{+\infty}\frac{1}{x^2}dx$.

Por último nos resta el intervalo $[0,1]$, que es directo pues es una integral de CDIV en un intervalo donde la función es continua (es un número).

**Conclusión:** La integral impropia $\int_{-\infty}^{+\infty} e^{-x^2}dx$ es convergente pues:

- La función integrando es par.
- La integral impropia $\int_{0}^{+\infty} e^{-x^2}dx$ es convergente por comparación.

### Integral #2

- $\int_0^1 \frac{e^{-x}}{x}dx$

Por Taylor, podemos expresar $e^{-x}$ cerca de 0 de la siguiente forma:

- $e^{-x}=1-\frac{1}{1!}x+\frac{1}{2!}x^2-\ldots$

Entonces la función que queremos integrar cerca de 0 es:

$$
\begin{aligned}
&\frac{1-x+\frac{x^2}{2}}{x}\\
&=\\
&\frac{1}{x}-1+\frac{x}{2}-\ldots
\end{aligned}
$$

Entonces al integrar en el intervalo $[0,1]$, se observa que el único término problemático es $\frac{1}{x}$. Por lo que la convergencia de la integral se juega ahí, pero ya la sabemos clasificar:

- $\int_{0}^{1}\frac{1}{x}dx$ diverge, pues $\alpha=1$

**Conclusión:** La integral impropia $\int_{0}^{1}\frac{e^{-x}}{x}dx$ diverge.

### Integral #3

- $\int_0^1 \frac{\log(x)}{\sqrt{x}}dx$

Este ejemplo nos lleva a formalizar un aspecto importante de la integración por partes de integrales impropias. Este método se puede usar sii:

- $udu$ y $vdu$ son integrables.
- Los límites "frontera" existen y son finitos.

En este caso se puede hacer y veremos porque:

$$
\begin{aligned}
&\int_0^1 \frac{\log(x)}{\sqrt{x}}dx\\
&=\\
&\int_{0}^{1}\log(x) x^{-\frac{1}{2}}dx\\
&=\scriptstyle{(\text{integración por partes }(*_1))}\\
&2\sqrt{x}\log(x)\Big|_0^1-\int_{0}^{1}\frac{2\sqrt{x}}{x}dx\\
&=\\
&2\log(1)-\lim_{x\to0^+}2\sqrt{x}\log(x)-2\int_{0}^{1}\frac{1}{\sqrt{x}}dx\\
&=\\
&0-0-2\int_{0}^{1}x^{-\frac{1}{2}}dx\\
&=\\
&-2\cdot\left(2\sqrt{x}\Big|_0^1\right)\\
&=\\
&4
\end{aligned}
$$

**Observación $(*_1)$:**

- $u=\log x\to du=\frac{1}{x}$
- $dv=x^{\frac{-1}{2}}\to v=\frac{x^{\frac{1}{2}}}{\frac{1}{2}}=2\sqrt{x}$

Cómo los límites frontera existen, podemos realizar esta integral por partes.

**Conclusión:** La integral impropia $\int_0^1 \frac{\log(x)}{\sqrt{x}}dx$ es convergente.

### Integral #4

- $\int_1^{+\infty} \frac{\sin(x)}{x^2}dx$

Ya hecha en ejercicios anteriores, se resuelve por convergencia absoluta.

### Integral #5

- $\int_0^{+\infty} \sin^2(t)dt$

Usando la siguiente identidad trigonométrica:

- $\sin^2 x + \cos^2 x = 1$

Tenemos que:

$$
\begin{aligned}
&\int_0^{+\infty} \sin^2(t)dt\\
&=\\
&\int_0^{+\infty} 1-\cos^2(t)dt\\
&=\\
&\int_0^{+\infty} 1dt+\int_{0}^{+\infty}\cos^2(t)dt\\
\end{aligned}
$$

Donde claramente $\int_0^{+\infty} 1dt$ diverge.

**Conclusión:** $\int_0^{+\infty} \sin^2(t)dt$ diverge.

### Integral #6

- $\int_0^{+\infty} \frac{x}{\sqrt{x^4 + 1}}dx$

Esta integral también ya se hizo en el teórico, es muy simple y se resuelve por comparación.

Es divergente.

### Integral #7

- $\int_{-\infty}^{+\infty} \frac{x}{\cosh(x)}dx$

**Recordatorio:** Observemos que:

- $\cosh(x)=\frac{e^x+e^{-x}}{2}$

Bajo este contexto, la integral impropia con la que estamos trabajando es:

- $\int_{-\infty}^{+\infty} \frac{2x}{e^x+e^{-x}}dx$

Observemos que la función es impar, es decir:

- $f(-x)=-f(x)$, verificando:
- $f(-x)=\frac{-2x}{e^{-x}+e^x}=-(\frac{-2x}{e^x+e^{-x}})=-f(x)$

Lo que implica que podemos trabajar en uno solo de los intervalos infinitos, por lo que la convergencia se juega en:

- $\int_{0}^{+\infty}\frac{2x}{e^x+e^{-x}}dx$

Tenemos que la función en $+\infty$ es equivalente a $\frac{x}{e^x}$, es decir que tendríamos que estudiar la convergencia de la integral impropia:

- $\int_{0}^{+\infty}xe^{-x}dx$

Veamos esta integral por partes utilizando:

- $u=x\to du=1$
- $dv=e^{-x}\to v=-e^{-x}$

$$
\begin{aligned}
&\int_{0}^{+\infty}xe^{-x}dx\\
&=\\
&-xe^{-x}\Big|_0^{+\infty}-\int_{0}^{+\infty}-e^{-x}\\
&=\\
&0-0-\left(e^{-x}\Big|_0^{+\infty}\right)\\
&=\\
&0+1\\
&=\\
&1
\end{aligned}
$$

Entonces esta integral impropia converge.

**Conclusión:** La integral $\int_{-\infty}^{+\infty} \frac{x}{\cosh(x)}dx$ es convergente pues:

- La función integrando es par.
- La integral $\int_{0}^{+\infty}xe^{-x}dx$ es convergente.

### Integral #8

- $\int_{-1}^{1} \frac{dx}{x^2 - 1}$

Tenemos puntos problemáticos en $1$ y $-1$, por lo que tenemos que separar la integral de la siguiente forma:

- $\int_{-1}^{1}\frac{1}{x^2-1}dx=\int_{-1}^{0}\frac{1}{x^2-1}dx+\int_{0}^{1}\frac{1}{x^2-1}dx$

Veamos de hallar una primitiva:

$$
\begin{aligned}
&\int\frac{1}{x^2-1}dx\\
&=\scriptstyle{(\text{fracciones simples})}\\
&\int\frac{1}{2}\cdot\left(\frac{-1}{x+1}+\frac{1}{x-1}\right)dx\\
&=\\
&\frac{1}{2}\int\frac{-1}{x+1}+\frac{1}{x-1}dx\\
&=\\
&\frac{1}{2}\left(-1\cdot\int\frac{1}{x+1}dx+\int\frac{1}{x-1}dx\right)\\
&=\\
&\frac{1}{2}(-\log|x+1|+\log|x-1|)\\
&=\\
&\frac{1}{2}\log\Big|\frac{x-1}{x+1}\Big|\\
\end{aligned}
$$

Entonces evaluemos la primitiva en los intervalos que corresponden.

**Intervalo #1: $(-1,0]$**

$$
\begin{aligned}
&\left(\frac{1}{2}\log\Big|\frac{x-1}{x+1}\Big|\right)\Big|_{-1}^0\\
&=\\
&=\frac{1}{2}\log1-\lim_{x\to-1^+}\left(\frac{1}{2}\log\Big|\frac{x-1}{x+1}\Big|\right)\\
&=\\
&\frac{1}{2}\log1+\infty
\end{aligned}
$$

Como en este intervalo la integral ya diverge, podemos saltar directo a la conclusión:

**Conclusión:** La integral impropia $\int_{-1}^{1} \frac{dx}{x^2 - 1}$ es divergente.

### Integral #9

- $\int_0^{+\infty} \frac{\cos(x)}{\sqrt{x}}dx$

Empecemos separando la integral mixta en:

- $\int_0^{+\infty} \frac{\cos(x)}{\sqrt{x}}dx = \int_0^{1} \frac{\cos(x)}{\sqrt{x}}dx + \int_1^{+\infty} \frac{\cos(x)}{\sqrt{x}}dx$

Donde nos vamos a centrar en la segunda integral dado que la primera es absolutamente convergente, pues por comparación:

- $\lvert\frac{\cos x}{\sqrt{x}}\rvert\leq\frac{1}{\sqrt{x}}$

Entonces veamos de calcular una primitiva para la parte que no podemos clasificar todavía:

$$
\begin{aligned}
&\int\frac{\cos x}{\sqrt{x}}dx\\
&=\\
&\int\cos x\cdot x^{-\frac{1}{2}}dx\\
&=\scriptstyle{(\text{integración por partes }(*_1))}\\
&\sin(x)x^{-\frac{1}{2}}\Big|_1^{+\infty}+\frac{1}{2}\int_{1}^{+\infty}\frac{\sin x}{x^{\frac{3}{2}}}dx\\
&=\\
&0-\sin(1)+\frac{1}{2}\int_{1}^{+\infty}\frac{\sin x}{x^{\frac{3}{2}}}dx\\
\end{aligned}
$$

**Observación $(*_1)$:**

- $u=x^{-\frac{1}{2}}\to du=-\frac{1}{2}x^{-\frac{3}{2}}=-\frac{1}{2}\cdot\frac{1}{x^{\frac{3}{2}}}$
- $dv=cos(x)\to v=\sin(x)$

Donde la última integral $\int_{1}^{+\infty}\frac{\sin x}{x^{\frac{3}{2}}}dx$ es absolutamente convergente, pues:

- $\lvert\frac{\sin x}{x^{\frac{3}{2}}}\rvert\leq\frac{1}{x^{\frac{3}{2}}}$

**Conclusión:** La integral impropia $\int_0^{+\infty} \frac{\cos(x)}{\sqrt{x}}dx$ es convergente pues:

- $\int_0^{1} \frac{\cos(x)}{\sqrt{x}}dx$ es absolutamente convergente y,
- $\int_{1}^{+\infty}\frac{\sin x}{x^{\frac{3}{2}}}dx$ es absolutamente convergente

### Integral #10

- $\int_0^{+\infty} \frac{e^{-\sqrt{x}}}{\sqrt{x}}dx$

Separemos la integral mixta según los puntos problemáticos:

- $\int_0^{+\infty} \frac{e^{-\sqrt{x}}}{\sqrt{x}}dx= \int_0^1 \frac{e^{-\sqrt{x}}}{\sqrt{x}}dx+\int_1^{+\infty} \frac{e^{-\sqrt{x}}}{\sqrt{x}}dx$

Ninguna de las dos se puede resolver facilmente, por lo que calcularemos la primitiva:

$$
\begin{aligned}
&\int \frac{e^{-\sqrt{x}}}{\sqrt{x}}dx\\
&=\scriptstyle{(\text{cambio de variable }x=t^2; dx=2tdt;\sqrt{x}=t)}\\
&\int \frac{e^{-t}}{t}2tdt\\
&=\\
&2\int e^{-t}dt\\
&=\\
&-2e^{-t}\\
&=\scriptstyle{(\text{deshaciendo el cambio de variable})}\\
&-2e^{-\sqrt{x}}
\end{aligned}
$$

Entonces queremos evaluar la primitiva en los intervalos que obtuvimos al principio:

**Intervalo #1:**

$$
\begin{aligned}
&-2e^{-\sqrt{x}}\Big|_0^1\\
&=\\
&\frac{-2}{e}+2e^0\\
&=\\
&\frac{-2}{e}+2\\
\end{aligned}
$$

Por lo que esta parte es convergente.

**Intervalo #2:**

$$
\begin{aligned}
&-2e^{-\sqrt{x}}\Big|_1^{+\infty}\\
&=\\
&0+\frac{2}{e}
\end{aligned}
$$

Por lo que esta parte también es convergente.

**Conclusión:** La integral impropia $\int_0^{+\infty} \frac{e^{-\sqrt{x}}}{\sqrt{x}}dx$ es convergente.

### Integral #11

- $\int_0^{+\infty} e^{x^2-\frac{1}{x^2}}dx$

Esta integral diverge, pues cuando $x\to\infty$ tenemos que:

- $e^{x^2-\frac{1}{x^2}}\sim e^{x^2}$

Que es una función no acotada, obviamente diverge.
