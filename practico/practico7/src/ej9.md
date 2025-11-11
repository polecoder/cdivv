# Ejercicio 9

## Consigna

Sea $f(x,y) = \tfrac{ax+y+by^2}{\sin y+\log(1+x)}, \quad a,b \in \mathbb{R}$.

1. Determinar $a$ y $b$ para que todos los límites direccionales de $f$ en $(0,0)$ sean iguales.  
2. Para esos valores, probar que $f$ carece de límite.

## Resolución

### Parte 1

- Determinar $a$ y $b$ para que todos los límites direccionales de $f$ en $(0,0)$ sean iguales.  

Para esta parte, veamos de acercanos a $(0,0)$ cuando $y=mx$.

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}\frac{ax+y+by^2}{\sin y+\log(1+x)}\\
&=\scriptstyle{(\text{sustituyendo }y=mx)}\\
&\lim_{x\to0}\frac{ax+mx+bm^2x^2}{\sin(mx)+\log(1+x)}\\
&=\scriptstyle{(\text{operando})}\\
&\lim_{x\to0}\frac{x(a+m+bm^2x)}{\sin(mx)+\log(1+x)}\\
&=\scriptstyle{(\text{si }u\to0, \log(1+u)\sim u)}\\
&\lim_{x\to0}\frac{x(a+m+bm^2x)}{\sin(mx)+x}\\
&=\scriptstyle{(\text{aplicamos L'Hopital }(*_1))}\\
&\lim_{x\to0}\frac{2bm^2x+a+m}{\cos(mx)m+1}\\
&=\scriptstyle{(\cos(mx)\to1; 2bm^2x\to0)}\\
&\frac{a+m}{m+1}\\
\end{aligned}
$$

**Nota $(*_1)$:**

- $f(x)=x(a+m+bm^2x)$
- $f'(x)=xbm^2+bm^2x+a+m=2bm^2x+a+m$
- $g(x)=\sin(mx)+x$
- $g'(x)=\cos(mx)m+1$

Bien, llegados a este punto, tenemos un problema si $m=-1$, pero por ahora podemos concluir que si $m\neq-1$, entonces necesariamente $a=1$ ya que la expresión que hallamos no puede depender de $m$.
Ahora podemos usar que $a=1$. Retomamos desde un punto avanzado.

$$
\begin{aligned}
&\lim_{x\to0}\frac{x(1+m+bm^2x)}{\sin(mx)+x}\\
&=\scriptstyle{(a=1;m=-1)}\\
&\lim_{x\to0}\frac{bm^2x^2}{\sin(-x)+x}\\
&=\scriptstyle{(x\in\mathbb{R}:\sin(-x)=-\sin(x))}\\
&\lim_{x\to0}\frac{bm^2x^2}{-\sin(x)+x}\\
&=\scriptstyle{(\text{si }x\to0,\sin(x)\sim x)}\\
&\lim_{x\to0}\frac{bm^2x^2}{-x+x}\\
\end{aligned}
$$

Seguimos con la indeterminación... Esto es porque se nos están escapando detalles del comportamiento de las funciones del denominador en $x\to0$, recordemos que estamos apróximando ambas por Taylor, por lo que si encontramos una indeterminación, significa que la aproximación que estamos haciendo no es suficiente para obtener el resultado que buscamos. Expandamos ambas las aproximaciones y veamos que sucede.

- Cuando $x\to0$, entonces $\sin(x)\sim sin(0)+\cos(0)x-\frac{\sin(0)}{2!}x^2-\frac{\cos(0)}{3!}x^3=x-\frac{x^3}{3!}$
- Cuando $x\to0$, entonces $\log(1+x)\sim \log(1)+\frac{1}{1}x-\frac{\frac{1}{1}}{2!}x^2=x-\frac{x^2}{2!}$

Ahora podemos retomar el límite con esta noción:

$$
\begin{aligned}
&\lim_{x\to0}\frac{bm^2x^2}{-\sin(x)+\log(1+x)}\\
&=\scriptstyle{(\text{razonamiento anterior con Taylor})}\\
&\lim_{x\to0}\frac{bm^2x^2}{\frac{x^3}{6}-\frac{x^2}{2}}\\
&=\scriptstyle{(\text{término dominante cerca de }0)}\\
&\lim_{x\to0}\frac{bm^2x^2}{-\frac{x^2}{2}}\\
&=\scriptstyle{(\text{operando})}\\
&\lim_{x\to0}\frac{2bm^2x^2}{-x^2}\\
&=\scriptstyle{(\text{operando})}\\
&-2bm^2\\
&=\scriptstyle{(m=-1)}\\
&-2b\\
\end{aligned}
$$

Todavía no podemos concluir nada sobre $b$, calculemos otro límite direccional para cuando $x=0$:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}\frac{ax+y+by^2}{\sin y+\log(1+x)}\\
&=\scriptstyle{((x,y)=(0,y))}\\
&\lim_{y\to 0}\frac{y+by^2}{\sin y}\\
&=\scriptstyle{(\text{operando y si }y\to0; \sin y\sim y)}\\
&\lim_{y\to 0}\frac{y(1+by)}{y}\\
&=\scriptstyle{(\text{operando})}\\
&\lim_{y\to 0}1+by\\
&=\scriptstyle{(\text{operando})}\\
&1\\
\end{aligned}
$$

Entonces, cómo todos los límites direccionales tienen que ser iguales:

- $-2b=1\to b=-\frac{1}{2}$

Concluyendo, $a=1$ y $b=-\frac{1}{2}$

### Parte 2

- Para esos valores, probar que $f$ carece de límite.

Queremos probar que $\tfrac{x+y-\frac{1}{2}y^2}{\sin y+\log(1+x)}$ no tiene límite.
La mejor estrategia para este caso es encontrar una dirección en la cual el límite no da $1$ (que es lo que nos dió en la parte anterior).

Esto resulta ser bastante simple, consideremos $x=-y+\frac{1}{2}y^2$, entonces:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}\frac{x+y-\frac{1}{2}y^2}{\sin y+\log(1+x)}\\
&=\scriptstyle{(\text{usando que }x=-y+\frac{1}{2}y^2)}\\
&\lim_{y\to0}\frac{-y+\frac{1}{2}y^2+y-\frac{1}{2}y^2}{\sin y+\log(1-y+\frac{1}{2}y^2)}\\
&=\scriptstyle{(\text{operando})}\\
&\lim_{y\to0}\frac{0}{\sin y+\log(1-y+\frac{1}{2}y^2)}\\
&=\scriptstyle{(\text{operando})}\\
&0
\end{aligned}
$$

Por lo tanto, $f$ no tiene límite en $(0,0)$, ya que encontramos dos direcciones que tienen distinto límite.