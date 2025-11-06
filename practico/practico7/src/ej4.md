# Ejercicio 4

## Consigna

Probar que en los siguientes casos no existe $\lim_{(x,y)\to(0,0)} f(x,y)$:

1. $f(x,y) = \tfrac{x^2 - y^2}{x^2 + y^2}$
2. $f(x,y) = \tfrac{2x^3y}{(x^2 + y^2)^2}$
3. $f(x,y) =
\begin{cases}
\tfrac{xy}{x + y}, & \text{si } x + y \neq 0 \\
0, & \text{si } x + y = 0
\end{cases}$
4. $f(x,y) =
\begin{cases}
1, & \text{si } 0 < y < x^2 \\
0, & \text{en otro caso}
\end{cases}$

## Resolución

### Función #1

- $f(x,y) = \tfrac{x^2 - y^2}{x^2 + y^2}$

Verifiquemos los límites direccionales para cuando $y=mx$.

$$
\begin{aligned}
&\lim_{x\to 0}\frac{x^2-m^2x^2}{x^2+m^2x^2}\\
&=\\
&\lim_{x\to 0}\frac{(1-m^2)x^2}{(1+m^2)x^2}\\
&=\\
&\lim_{x\to 0}\frac{(1-m^2)}{(1+m^2)}\\
&=\\
&\frac{(1-m^2)}{(1+m^2)}\\
\end{aligned}
$$

Por lo tanto, el límite depende siempre del valor de $m$. Esto no puede pasar pues el valor del límite tiene que ser único.

### Función #2

- $f(x,y) = \tfrac{2x^3y}{(x^2 + y^2)^2}$

Transformemos a coordenadas polares.

- $x=\rho\cos\theta$
- $y=\rho\sin\theta$

Entonces ahora operamos:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}\frac{2x^3y}{(x^2 + y^2)^2}\\
&=\\
&\lim_{\rho\to0}\frac{2\rho^3\cos^3(\theta)\rho\sin(\theta)}{(\rho^2\cos^2\theta+\rho^2\sin^2\theta)^2}\\
&=\\
&\lim_{\rho\to0}\frac{2\rho^3\cos^3(\theta)\rho\sin(\theta)}{(\rho^2(\cos^2\theta+\sin^2\theta))^2}\\
&=\\
&\lim_{\rho\to0}\frac{2\rho^3\cos^3(\theta)\rho\sin(\theta)}{(\rho^2)^2}\\
&=\\
&\lim_{\rho\to0}\frac{2\rho^3\cos^3(\theta)\rho\sin(\theta)}{\rho^4}\\
&=\\
&\lim_{\rho\to0}\frac{2\rho^4\cos^3(\theta)\sin(\theta)}{\rho^4}\\
&=\\
&\lim_{\rho\to0}2\cos^3(\theta)\sin(\theta)\\
&=\\
&2\cos^3(\theta)\sin(\theta)\\
\end{aligned}
$$

Pero esta expresión es totalmente dependiente de $\theta$, por lo tanto el límite puede tender a diferentes valores según la dirección de la que nos acerquemos. Esto no puede pasar porque el límite es único.

### Función #3

- $f(x,y) =
\begin{cases}
\tfrac{xy}{x + y}, & \text{si } x + y \neq 0\\
0, & \text{si } x + y = 0
\end{cases}$

En este caso también probaremos con los límites direccionales para cuando $y=mx$.

$$
\begin{aligned}
&\lim_{x\to 0}\frac{xmx}{x+mx}\\
&=\\
&\lim_{x\to 0}\frac{xmx}{x(1+m)}\\
&=\\
&\lim_{x\to 0}\frac{mx}{1+m}\\
&=\\
&0
\end{aligned}
$$

Esto no nos permite descartar que el límite exista, pero sabemos que si o si tiene que ser 0 si efectivamente existe.
Probemos ahora cuando $y=x^2-x$:

$$
\begin{aligned}
&\lim_{x\to0}\frac{x(x^2-x)}{x+x^2-x}\\
&=\\
&\lim_{x\to0}\frac{x^2(x-1)}{x^2}\\
&=\\
&\lim_{x\to0}(x-1)\\
&=\\
&-1\\
\end{aligned}
$$

Entonces encontramos una dirección para la que el límite no es 0, por lo que podemos concluir que el límite no existe.

### Función #4

- $f(x,y) =
\begin{cases}
1, & \text{si } 0 < y < x^2 \\
0, & \text{en otro caso}
\end{cases}$

Consideremos dos direcciones:

- $y=\frac{1}{2}x^2$
- $y=x^2$

**Primera dirección: $y=\frac{1}{2}x^2$:**

- En este caso, tenemos que $f(x,y)=1$, por lo tanto el límite cuando $(x,y)\to(0,0)$ es $1$

**Segunda dirección: $y=x^2$:**

- En este caso, tenemos que $f(x,y)=0$, por lo tanto el límite cuando $(x,y)\to(0,0)$ es $0$

Como obtuvimos dos resultados diferentes, el límite no puede existir.