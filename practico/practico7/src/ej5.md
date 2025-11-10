# Ejercicio 5

## Consigna

1. Probar que si $\lim_{x\to p} f(x) = 0$ y $g$ es una función acotada en una bola reducida de centro $p$, entonces $\lim_{x\to p} f(x)g(x) = 0$.

2. Calcular los límites de las siguientes funciones para $(x,y)\to(0,0)$:

    1. $x \sin\left(\tfrac{1}{x^2 + y^2}\right)$
    2. $\tfrac{xy^2}{x^2 + y^2}$
    3. $\tfrac{xy^3}{x^2 + y^4} = y \tfrac{xy^2}{x^2 + y^4}$

## Resolución

### Parte 1

- Probar que si $\lim_{x\to p} f(x) = 0$ y $g$ es una función acotada en una bola reducida de centro $p$, entonces $\lim_{x\to p} f(x)g(x) = 0$.

Escribamos el significado de las hipótesis para trabajar con ellas.

#### Hipótesis #1

- $\lim_{x\to p} f(x) = 0$

Esto significa que $\forall\varepsilon>0,\exists\delta>0$ tal que $\forall x\in B^*(p,\delta)\cap D: |f(x)|<\varepsilon$

#### Hipótesis #2

- $g$ es una función acotada en una bola reducida de centro $p$

Esto significa que existen $K>0$ y $r>0$ tales que $\forall x\in B^*(p,r)$ se cumple que $|g(x)|<K$ 

#### Razonamiento

Por la primer hipótesis, podemos considerar $\varepsilon:=\frac{\varepsilon}{K}$, para el cual tenemos que:

- $\exists\delta_{\varepsilon}>0$ tal que $\forall x\in B^*(p,\delta_{\varepsilon})\cap D: |f(x)|<\frac{\varepsilon}{K}$

Ahora consideremos $\delta_0:=\max\{\delta_{\varepsilon}, r\}$. Entonces para este $\delta_0$ se van a cumplir simultaneamente las siguientes condiciones:

- $\forall x\in B^*(p,\delta_0)\cap D: |f(x)|<\frac{\varepsilon}{K}$
- $\forall x\in B^*(p,\delta_0)$ se cumple que $|g(x)|<K$

Entonces en particular, para todo $x\in B^*(p,\delta_0)\cap D$:

- $|f(x)g(x)|=|f(x)||g(x)|<\frac{\varepsilon}{K}K=\varepsilon$

Por lo tanto, obtuvimos lo que queríamos probar, es decir que:

- $\forall\varepsilon>0,\exists\delta>0$ tal que $\forall x\in B^*(p,\delta_0)\cap D:|f(x)g(x)|<\varepsilon$

Esto concluye esta parte del ejercicio.

### Parte 2

- Calcular los límites de las siguientes funciones para $(x,y)\to(0,0)$:

    1. $x \sin\left(\tfrac{1}{x^2 + y^2}\right)$
    2. $\tfrac{xy^2}{x^2 + y^2}$
    3. $\tfrac{xy^3}{x^2 + y^4} = y \tfrac{xy^2}{x^2 + y^4}$

#### Límite #1

- $x \sin\left(\tfrac{1}{x^2 + y^2}\right)$

Notemos que:

- Si $(x,y)\to(0,0)$ entonces $x\to0$.
- $\sin(\frac{1}{x^2+y^2})$ siempre está acotada entre $0$ y $1$

Por lo tanto podemos aplicar lo probamos en la primer parte del ejercicio para concluir que:

- $\lim_{x\to(0,0)}x \sin\left(\tfrac{1}{x^2 + y^2}\right)=0$

#### Límite #2

- $\tfrac{xy^2}{x^2 + y^2}$

Consideremos el cambio por coordenadas polares:

- $x=\rho\cos\theta$
- $y=\rho\sin\theta$

Entonces:

$$
\begin{aligned}
&\frac{xy^2}{x^2 + y^2}\\
&=\\
&\frac{\rho^3cos(\theta)\sin^2(\theta)}{\rho^2}\\
&=\\
&\rho\cos(\theta)\sin^2(\theta)
\end{aligned}
$$

Por lo tanto el límite que queremos calcular equivale a:

- $\lim_{\rho\to0}\rho\cos(\theta)\sin^2(\theta)$

Y tenemos que:

- Cuando $\rho\to0$ entonces $\rho\to0$ (trivial)
- $\cos(\theta)\sin^2(\theta)$ es una función siempre acotada para cualquier valor de $\theta$

#### Límite #3

- $\tfrac{xy^3}{x^2 + y^4} = y \tfrac{xy^2}{x^2 + y^4}$

La resolución consiste en encontrar una cota, pero al revisar las soluciones se ve muy absurdo obtener esas cotas de la nada.
Voy a saltear esta parte del ejercicio, revisar en las soluciones del práctico.