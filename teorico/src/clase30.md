# CLASE 30 - 02/12/2025

## Derivadas de orden superior

Sea $f:\mathbb{R}^2\to\mathbb{R}$ una función diferenciable. Las derivadas parciales son en sí mismas, también funciones definidas para cada punto del plano:

- $f_x:\mathbb{R}^2\to\mathbb{R}$, y
- $f_y:\mathbb{R}^2\to\mathbb{R}$

Por lo que entonces tiene sentido estudiar la derivabilidad de estas funciones.
Definamos entonces las derivadas de segundo de orden. Por ejemplo, si tomamos la función $f_x$ y hallamos su derivada respecto a $x$ en el punto $a$, entonces obtenemos la derivada de $f$ respecto de $x$ dos veces, evaluada en $a$. Esto es:

$$
\frac{\partial^2 f}{\partial x\partial x}(a)=\frac{\partial (\frac{\partial f}{\partial x})}{\partial x}(a)
$$

De igual manera, se definen las tres derivadas restantes, que también las denotamos de distintas formas:

- $\frac{\partial^2 f}{\partial x\partial x}(a)=\frac{\partial^2 f}{\partial x^2}(a)=f_{xx}(a)$
- $\frac{\partial^2 f}{\partial y\partial y}(a)=\frac{\partial^2 f}{\partial y^2}(a)=f_{yy}(a)$
- $\frac{\partial^2 f}{\partial x\partial y}(a)=f_{xy}(a)$
- $\frac{\partial^2 f}{\partial y\partial x}(a)=f_{yx}(a)$

Veamos un ejemplo para notar que las operaciones siguen siendo las naturales.

### Ejemplo 7.22

Consideremos la función de dos variables $f(x,y)=x\sin(y)+x^2y^2$ y calculemos sus derivadas.

- $f_x(x,y)=\sin(y)+2xy^2$
- $f_y(x,y)=x\cos(y)+2yx^2$

Luego, las derivadas de segundo orden son:

- $f_{xx}(x,y)=2y^2$
- $f_{yy}(x,y)=-x\sin(y)+2x^2$
- $f_{xy}(x,y)=\cos(y)+4xy$
- $f_{yx}(x,y)=\cos(y)+4yx$

Las derivadas de órden superior siguen la misma lógica, por ejemplo $f_{xxy}=4y$.

### Teorema 7.23 (Schwarz)

Si $f_{xy}$ y $f_{yx}$ existen en un entorno $B((x_0,y_0),\delta)$ y son continuas en $(x_0,y_0)$, entonces $f_{xy}(x_0,y_0)=f_{yx}(x_0,y_0)$.

#### Demostración

No se hace en el teórico, pero está hecha en las notas.

## Funciones en $\mathbb{R}^m$

Hasta ahora, hemos trabajado con funciones de $\mathbb{R}^n$ a $\mathbb{R}$, con especial énfasis en funciones definidas en $\mathbb{R}^2$. Veamos las generalizaciones correspondientes para funciones $f:\mathbb{R}^n\to\mathbb{R}^m$.
En estos casos, la imagen es un punto en $\mathbb{R}^m$, y por lo tanto tenemos $m$ funciones (una para cada coordenada), y cada una de ellas depende de las $n$ variables. Es decir:

$$
f(x_1,\ldots,x_n)=\left(f_1(x_1,\ldots,x_n),f_2(x_1,\ldots,x_n),\ldots,f_m(x_1,\ldots,x_n)\right)
$$

Donde $f_i:\mathbb{R}^n\to\mathbb{R}$.

### Ejemplo 7.26

Veamos un ejemplo de función $f:\mathbb{R}^3\to\mathbb{R}^2$, definida por $f(x,y,z)=(x+ye^z,cos(x+y)-z)$.

Con la noción de continuidad, no tenemos mayores problemas, como sabemos medir distancias tanto en el dominio como en el codominio, la definición dada en el capítulo anterior funciona sin variaciones.
Lo mismo sucede para la definición de diferenciabilidad, pero de todas maneras la escribiremos.

### Definición 7.27

Decimos que $f:\mathbb{R}^n\to\mathbb{R}^m$ es diferenciable en un punto $a\in\mathbb{R}^n$ sii existe una transformación $df_a:\mathbb{R}^n\to\mathbb{R}^m$ tal que:

$$
f(a+h)=f(a)+df_a(h)+r(h),\quad\text{con }\lim_{h\to0}\frac{r(h)}{\|h\|}=0
$$

Recordemos que el primer resultado importante que vimos sobre diferenciabilidad, el 7.13. Allí trabajando con funciones de $\mathbb{R}^2$ a $\mathbb{R}$, vimos que los elementos que de la transformación lineal que aparece en la definición de diferenciabilidad, son las derivadas parciales en el punto.

En este caso, lo que obtenemos (con las mismas cuentas que en el teorema 7.13), es que la matriz asociada a $df_a$ es la que tiene a las derivadas parciales de cada función, respecto a cada variable.
Es decir, es una matriz de $m$ filas y $n$ columnas (esto ya lo sabíamos, por el dominio y codominio de la transformación lineal), y en la entrada $(i,j)$ de la matriz encontramos la derivada de la función $f_i$ respecto de la variable $x_j$. Esta matriz lleva el nombre de _Matriz Jacobiana_, y se denota como $J_f(a)$, es decir, la Matriz Jacobiana de la función $f$ en el punto $a$.

Entonces, tenemos que:

$$
J_f(a)=\begin{pmatrix}
\frac{\partial f_1}{\partial x_1}(a)&\frac{\partial f_1}{\partial x_2}(a)&\ldots&\frac{\partial f_1}{\partial x_n}(a)\\
\vdots&\vdots&\ddots&\vdots\\
\frac{\partial f_m}{\partial x_1}(a)&\frac{\partial f_m}{\partial x_2}(a)&\ldots&\frac{\partial f_m}{\partial x_n}(a)\\
\end{pmatrix}
$$

O visto de otra forma:

$$
J_f(a)=\begin{pmatrix}
\nabla f_1(a)\\
\hline
\nabla f_2(a)\\
\hline
\vdots\\
\hline
\nabla f_m(a)\\
\end{pmatrix}
$$

### Ejemplo 7.28

Sea $f:\mathbb{R}^3\to\mathbb{R}^2$ definida como $f(x,y,z)=(x^2y+e^z,\sin(x)+yz)$. En este caso tenemos:

- $f_1(x,y,z)=x^2y+e^z$, y 
- $f_2(x,y,z)=\sin(x)+yz$.

Entonces la matriz Jacobiana en un punto genérico $(x,y,z)$ es:

$$
J_f(x,y,z)=\begin{pmatrix}
2xy&x^2&e^z\\
\cos(x)&z&y
\end{pmatrix}
$$

Cerremos ahora viendo una versión general de la regla de la cadena.

### Teorema 7.29 (regla de la cadena 3)

Sean $g:\mathbb{R}^k\to\mathbb{R}^n$, diferenciable en $a\in\mathbb{R}^k$, y $f:\mathbb{R}^n\to\mathbb{R}^m$, diferenciable en $g(a)$. Entonces $f\circ g:\mathbb{R}^k\to\mathbb{R}^m$ es diferenciable en $a$, y además su diferencial es $d(f\circ g)_a=df_{g(a)}\circ dg_a$.

Observemos que el diferencial de la composición es la composición de los diferenciales (evaluados en los puntos correctos), y por lo tanto, la matriz Jacobiana de $f\circ g$ es el producto de las matrices Jacobianas de $f$ y $g$:

- $J_{f\circ g}(a)=J_f(g(a))\cdot J_g(a)$

#### Demostración

No se hace en el teórico, pero está hecha en las notas.

#### Ejemplo 7.30

Consideremos por un lado la función $f:\mathbb{R}^3\to\mathbb{R}^2$ definida como $f(x,y,z)=(x^2y+e^z,\sin(x)+yz)$, de la cual calculamos su matriz Jacobiana en el ejemplo 7.28.

Por otro lado, sea $g:\mathbb{R}^2\to\mathbb{R}^3$ definida como $g(u,v)=(uv,e^u,\cos(v))$ y llamemos $h$ a la función que resulte de componerlas. Es decir $h:\mathbb{R}^2\to\mathbb{R}^2$ es $h=f\circ g$, o $h(u,v)=f(g(u,v))$.

En este caso, conocemos a las funciones $f$ y $g$ en su totalidad, por lo que podemos calcular explicitamente la composición y luego derivar. Sigamos este camino primero.
Queremos calcular:

- $h(u,v)=f(g(u,v))=f(uv,e^u,\cos(v))=(u^2v^2e^u+e^{\cos(v)},\sin(uv)+e^u\cos(v))$

Por lo tanto, podemos calcular su matriz Jacobiana:

- $\frac{\partial h_1}{\partial u}=v^2(u^2e^u+2ue^u)=e^uv^2u(u+2)$
- $\frac{\partial h_1}{\partial v}=u^2e^u2v-\sin(v)e^{\cos(v)}$
- $\frac{\partial h_2}{\partial u}=v\cos(uv)+e^u\cos(v)$
- $\frac{\partial h_2}{\partial v}=u\cos(uv)-e^u\sin(v)$

$$
J_h(u,v)=\begin{pmatrix}
e^uv^2u(u+2)&u^2e^u2v-\sin(v)e^{\cos(v)}\\
v\cos(uv)+e^u\cos(v)&u\cos(uv)-e^u\sin(v)\\
\end{pmatrix}
$$

Supongamos que queremos calcular la matriz Jacobiana para el punto $(1,\pi)$, entonces sustituyendo:

$$
J_h(1,\pi)=\begin{pmatrix}
3e\pi^2&2e\pi\\
-\pi-e&-1\\
\end{pmatrix}
$$

Por otro lado, podríamos calcular lo mismo usando la regla de la cadena:

- $J_h(u,v)=J_f((g(u,v)))\cdot J_g(u,v)$, o en particular:
- $J_h(1,\pi)=J_f((g(1,\pi)))\cdot J_g(1,\pi)$

Obteniendo las dos matrices Jacobianas involucradas:

$$
J_f(x,y,z)=\begin{pmatrix}
2xy&x^2&e^z\\
\cos(x)&z&y
\end{pmatrix};\\
J_g(u,v)=\begin{pmatrix}
v&u\\
e^u&0\\
0&-\sin(v)\\
\end{pmatrix}\\
$$

Notemos que $g(1,\pi)=(\pi,e,-1)$, esto es importante pues es el punto al que aplicamos $f$. Operando:

$$
\begin{aligned}
&J_h(1,\pi)\\
&=\scriptstyle{(\text{regla de la cadena 3})}\\
&J_f(\pi,e,-1)\cdot J_g(1,\pi)\\
&=\scriptstyle{(\text{sustituyendo por las matrices conocidas})}\\
&\begin{pmatrix}
2e\pi&\pi^2&e^{-1}\\
-1&-1&e
\end{pmatrix}\cdot\begin{pmatrix}
\pi&1\\
e&0\\
0&0\\
\end{pmatrix}\\
&=\scriptstyle{(\text{operando})}\\
&\begin{pmatrix}
2e\pi^2+e\pi^2&2e\pi\\
-\pi-e&-1
\end{pmatrix}\\
&=\scriptstyle{(\text{simplificando})}\\
&\begin{pmatrix}
3e\pi^2&2e\pi\\
-\pi-e&-1
\end{pmatrix}\\
\end{aligned}
$$

Notemos que esta matriz coincide con el resultado que hallamos yendo por el otro camino.