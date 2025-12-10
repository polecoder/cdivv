# CLASE 31 - 09/12/2025

## Desarrollo de Taylor

Veremos la versión para varias variables del Teorema de Taylor, que ya fue estudiado para el caso de funciones a valores reales.
Tengamos presente antes de empezar, que es una herramienta muy útil en cualquier aplicación, especialmente en ingeniería, ya que muchas veces somos capaces de hacer cálculos de naturaleza más simple (por ejemplo para funciones lineales o para ecuaciones de orden dos, etc.).
Comenzaremos repasando los resultados conocidos en una variable.

### Repaso en $\mathbb{R}$

Si $f:\mathbb{R}\to\mathbb{R}$ es una función de clase $C^{k+1}$, entonces:

$$
f(x_0+h)=f(x_0)+f'(x_0)h+\frac{f''(x_0)}{2}h^2+\frac{f'''(x_0)}{3!}h^3+\ldots+\frac{f^{(k)}(x_0)}{k!}h^k+r(h)
$$

Siendo $r$ una función que cumple que $\lim_{h\to0}\frac{r(h)}{h^k}=0$.
Es decir, localmente (cuando $h$ tiende a cero) la función puede ser apróximada por un polinomio.

Observemos que con los primeros dos términos de la aproximación (o mirando el desarrollo de Taylor con $k=1$) tenemos la definición de diferenciabilidad.
La propiedad del resto nos dice que el error de la aproximación tiende a cero más rápido que $h^k$. Esto, que muchas veces es olvidado en un enunciado rápido del resultado, es de lo más importante del Teorema (de forma similar a lo que hablamos cuando definimos diferenciabilidad).

En varias variables, ya lo tenemos hecho para orden uno: es la definición de diferenciabilidad. Si pensamos en funciones de $\mathbb{R}^2$ a $\mathbb{R}$, esto equivale a aproximar la superficie del gráfico de la función por un plano, como ya vimos.
Tendríamos que ver que podemos hacer para mejorar la aproximación cuando salimos del orden uno.

### Diferenciales de orden superior

Veremos cómo son los diferenciales de orden superior, y el desarrollo de Taylor para funciones de dos variables.
Recordemos que si $f$ es diferenciable en $a$, el diferencial es la transformación lineal que mejor aproxima localmente: $df_a(\Delta x,\Delta y)=f_x(a)\Delta x+f_y(a)\Delta y$.

Consideremos una función $f\in C^2$, definimos el diferencial segundo en $a$ como la función $d^2f_a:\mathbb{R}^2\to\mathbb{R}$ definida por:

$$
d^2f_a(\Delta x,\Delta y)=f_{xx}(a)\Delta x^2+2f_{xy}(a)\Delta x\Delta y+f_{yy}(a)\Delta y^2
$$

Como pedimos que la función sea de clase $C^2$, las derivadas cruzadas son iguales, por eso aparece dos veces el término $f_{xy}(a)\Delta x\Delta y$.
También podemos escribir esta expresión de forma matricial, para esto definimos la matriz Hessiana, que se denota $H$, de la siguiente forma:

$$
H=\begin{pmatrix}
f_{xx}(a)&f_{xy}(a)\\
f_{yx}(a)&f_{yy}(a)\\
\end{pmatrix}
$$

Entonces, si denotamos al vector de incrementos $v=(\Delta x,\Delta y)$, resulta que:

- $d^2f_a(\Delta x,\Delta y)=vHv^t$

De forma similar se definen los diferenciales de orden superior. Por ejemplo, si todas las derivadas conmutan (es decir que $f$ es de clase $C^3$):

- $d^3f_a(\Delta x,\Delta y)=f_{xxx}(a)\Delta x^3+3f_{xxy}(a)\Delta x^2\Delta y+3f_{yyx}(a)\Delta x\Delta y^2+ f_{yyy}(a)\Delta y^3$

### Teorema 7.31 (Taylor)

Sea $f:\mathbb{R}^m\to\mathbb{R}$ una función de clase $C^{k+1}$ en un entorno de $a\in\mathbb{R}^m$. Entonces:

$$
f(a+h)=f(a)+df_a(h)+\frac{d^2f_a(h)}{2}+\frac{d^3f_a(h)}{3!}+\ldots+\frac{d^kf_a(h)}{k!}+r_k(h)
$$

Donde el resto $r_k$ es una función que cumple que $\lim_{h\to(0,0,\ldots,0)}\frac{r_k(h)}{\|h\|^k}=0$.

Por ejemplo, en el caso de una función de dos variables, el desarrollo de Taylor de orden dos resulta:

$$
\begin{aligned}
f(x_0+\Delta x,y_0+\Delta y)=\ &f(x_0,y_0)+f_x(\Delta x,\Delta y)\Delta x+f_y(\Delta x,\Delta y)\Delta y+\\
&\frac{1}{2}[f_{xx}(\Delta x,\Delta y)\Delta x^2+2f_{xy}(\Delta x,\Delta y)\Delta x\Delta y+f_{yy}(\Delta x,\Delta y)\Delta y^2]
\end{aligned}
$$

#### Ejemplo 7.32

Calculemos el desarrollo de Taylor de segundo orden de $f(x,y)=\log(1+2x+y)$ alrededor del punto $a=(1,2)$. Primero calculamos $f(1,2)=\log(5)$. Ahora vamos con las derivadas:

- $f_x(x,y)=\frac{2}{1+2x+y}\implies f_x(1,2)=\frac{2}{5}$
- $f_y(x,y)=\frac{1}{1+2x+y}\implies f_y(1,2)=\frac{1}{5}$
- $f_{xx}(x,y)=\frac{-4}{(1+2x+y)^2}\implies f_{xx}(1,2)=\frac{-4}{25}$
- $f_{xy}(x,y)=\frac{-2}{(1+2x+y)^2}\implies f_{xy}(1,2)=\frac{-2}{25}$
- $f_{yy}(x,y)=\frac{-1}{(1+2x+y)^2}\implies f_{yy}(1,2)=\frac{-1}{25}$

Por lo tanto, el desarrollo de Taylor en $a$ resulta:

$$
f(1+\Delta x,2+\Delta y)=\log(5)+\frac{2}{5}\Delta x+\frac{1}{5}\Delta y+\frac{1}{2}\left[-\frac{4}{25}\Delta x^2-\frac{4}{25}\Delta x\Delta y-\frac{1}{25}\Delta y^2\right]+r(\Delta x,\Delta y)
$$

Con $\lim_{(\Delta x,\Delta y)\to(0,0)}\frac{r(\Delta x,\Delta y)}{\|(\Delta x,\Delta y)\|^2}$.
