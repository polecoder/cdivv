# Ejercicio 8

## Consigna

Calcular:

1. $\lim_{(x,y)\to(1,2)}\tfrac{x^2+xy+1}{x^2-x-y}$
2. $\lim_{(x,y)\to(0,0)}xy\log|y|$
3. $\lim_{(x,y)\to(1,1)}\tfrac{x^2+xy-2y^2}{x^2-y^2}$
4. $\lim_{(x,y)\to(0,0)}\tfrac{x^3+y^3}{x^2+y^2}$
5. $\lim_{(x,y)\to(0,0)}\tfrac{e^{x-y}-1}{x^2-y^2}$
6. $\lim_{(x,y)\to(0,0)}\tfrac{\log(1+x^2+y^2)}{x^2+y^2+x^3y}$

## Resolución

### Límite #1

- $\lim_{(x,y)\to(1,2)} \tfrac{x^2+xy+1}{x^2-x-y}$

Simplemente sustituimos:

$$
\begin{aligned}
&\lim_{(x,y)\to(1,2)} \frac{x^2+xy+1}{x^2-x-y}\\
&=\\
&\lim_{(x,y)\to(1,2)} \frac{1+2+1}{1-1-2}\\
&=\\
&\lim_{(x,y)\to(1,2)} \frac{4}{-3}\\
&=\\
&-\frac{4}{3}
\end{aligned}
$$

Por lo tanto, $\lim_{(x,y)\to(1,2)} \tfrac{x^2+xy+1}{x^2-x-y}=-\frac{4}{3}$

### Límite #2

- $\lim_{(x,y)\to(0,0)} xy\log|y|$

Notemos que el límite se puede separar en dos factores:

- $x$
- $y\log|y|$

Donde la primera tiende claramente a $0$, mientras que la segunda se puede deducir por órdenes ($x$ crece más rápido que $\log(x)$), también tiende a $0$.
Por lo tanto tenemos que $\lim_{(x,y)\to(0,0)} xy\log|y|=0$.

### Límite #3

- $\lim_{(x,y)\to(1,1)} \tfrac{x^2+xy-2y^2}{x^2-y^2}$

Podemos operar con la función:

$$
\begin{aligned}
&\frac{x^2+xy-2y^2}{x^2-y^2}\\
&=\\
&\frac{(x-y)(x+2y)}{(x+y)(x-y)}\\
&=\\
&\frac{x+2y}{x+y}
\end{aligned}
$$

Por lo tanto:

- $\lim_{(x,y)\to(1,1)} \tfrac{x^2+xy-2y^2}{x^2-y^2}=\lim_{(x,y)\to(1,1)} \frac{x+2y}{x+y}=\frac{3}{2}$

### Límite #4

- $\lim_{(x,y)\to(0,0)} \tfrac{x^3+y^3}{x^2+y^2}$

Consideremos el cambio por polares:

- $x=\rho\cos\theta$
- $y=\rho\cos\theta$

Entonces:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}\frac{x^3+y^3}{x^2+y^2}\\
&=\\
&\lim_{\rho\to0}\frac{\rho^3(\cos^3(\theta)+\sin^3(\theta))}{\rho^2}\\
&=\\
&\lim_{\rho\to0}\rho(\cos^3(\theta)+\sin^3(\theta))\\
\end{aligned}
$$

Como $\cos^3(\theta)+\sin^3(\theta)$ está acotada para cualquier $\theta$ y $\rho\to0$, podemos concluir que $\lim_{(x,y)\to(0,0)} \tfrac{x^3+y^3}{x^2+y^2}=0$

### Límite #5

- $\lim_{(x,y)\to(0,0)}\tfrac{e^{x-y}-1}{x^2-y^2}$

**Nota:** Recordemos que $e^u-1\sim u$ cuando $u\to0$

Aplicando la nota, tenemos que:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}\frac{e^{x-y}-1}{x^2-y^2}\\
&=\\
&\lim_{(x,y)\to(0,0)}\frac{x-y}{(x+y)(x-y)}\\
&=\\
&\lim_{(x,y)\to(0,0)}\frac{1}{x+y}\\
\end{aligned}
$$

Entonces esto tiende a infinito, pero qué pasa con el signo? Si nos acercamos de con $x=0^-$ e $y=0^-$, tendremos que el límite es $-\infty$. 
Sin embargo si nos acercamos por el lado positivo tendremos que el límite es $+\infty$.

Con esta observación, podemos concluir que el límite no existe.

### Límite #6

- $\lim_{(x,y)\to(0,0)}\tfrac{\log(1+x^2+y^2)}{x^2+y^2+x^3y}$

**Nota:** Recordemos que $\log(1+u)\sim u$ cuando $u\to 0$.

Aplicando la nota, tenemos que:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}\frac{\log(1+x^2+y^2)}{x^2+y^2+x^3y}\\
&=\\
&\lim_{(x,y)\to(0,0)}\frac{x^2+y^2}{x^2+y^2+x^3y}
\end{aligned}
$$

Ahora podemos pasar a polares:

- $x=\rho\cos\theta$
- $y=\rho\sin\theta$

Entonces:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}\frac{x^2+y^2}{x^2+y^2+x^3y}\\
&=\\
&\lim_{\rho\to0}\frac{\rho^2}{\rho^2+\rho^4\cos^3\theta\sin\theta}\\
&=\\
&\lim_{\rho\to0}\frac{1}{1+\rho^2\cos^3\theta\sin\theta}\\
&=\\
&1
\end{aligned}
$$

Por lo tanto, podemos concluir que $\lim_{(x,y)\to(0,0)}\tfrac{\log(1+x^2+y^2)}{x^2+y^2+x^3y}=1$