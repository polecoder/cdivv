# Ejercicio 1

## Consigna

Estudiar la continuidad de cada función y la existencia de las derivadas direccionales respectivas.

1. $f(x,y) =
\begin{cases}
\tfrac{xy}{\sqrt{x^2 + y^2}} & (x,y) \ne (0,0) \\
a & (x,y) = (0,0)
\end{cases}$
2. $f(x,y) =
\begin{cases}
\tfrac{e^{xy} - 1}{x} & x \ne 0 \\
y & x = 0
\end{cases}$
3. $f(x,y) =
\begin{cases}
\tfrac{x^3}{y} & y \ne 0 \\
0 & y = 0
\end{cases}$
4. $f(x,y) =
\begin{cases}
xy \sin(\tfrac{1}{x})\cos(\tfrac{1}{y}) & xy \ne 0 \\
a &xy = 0
\end{cases}$
5. $f(x,y) =
\begin{cases}
x^3 & y \ge 1 \\
x^3 y^2 & y < 1
\end{cases}$

## Resolución

### Función #1

$f(x,y) =
\begin{cases}
\tfrac{xy}{\sqrt{x^2 + y^2}} & (x,y) \ne (0,0) \\
a & (x,y) = (0,0)
\end{cases}$

#### Continuidad

Notemos que tenemos un solo punto problemático, que es $(0,0)$. Evaluemos el límite para este punto y veamos que se corresponda con el valor funcional.

$$
\begin{aligned}
&\lim_{(x,y)\to(0,0)}f(x,y)\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{(x,y)\to(0,0)}\frac{xy}{\sqrt{x^2+y^2}}\\
&=\scriptstyle{(\text{cambio por polares: }x=\rho\cos\theta;y=\rho\sin\theta)}\\
&\lim_{\rho\to0}\frac{\rho^2\cos\theta\sin\theta}{\sqrt{\rho^2}}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{\rho\to0}\rho\cos\theta\sin\theta\\
&=\scriptstyle{(\text{límite de 0 por acotado})}\\
&0
\end{aligned}
$$

Por lo tanto, la función es continua solamente si $a=0$.

#### Derivadas direccionales

Consideremos una dirección genérica $v=(v_1,v_2)$ y separemos dos casos:

##### Punto $(0,0)$

Operando:

$$
\begin{aligned}
&\frac{\partial f}{\partial v}(0,0)\\
&=\scriptstyle{(\text{definición de derivada direccional})}\\
&\lim_{h\to0}\frac{f(hv_1,hv_2)-f(0,0)}{h}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{h\to0}\left(\frac{hv_1hv_2}{\sqrt{h^2v_1^2+h^2v_2^2}}-a\right)\frac{1}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\left(\frac{hv_1hv_2}{|h|\sqrt{v_1^2+v_2^2}}-a\right)\frac{1}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\frac{hv_1hv_2}{|h|h\sqrt{v_1^2+v_2^2}}-\frac{a}{h}\\
\end{aligned}
$$

Para que este límite exista, necesariamente $a=0$, pues sino este será divergente. Con esto podemos hacer la última observación importante:

$$
\begin{aligned}
&\lim_{h\to0}\frac{hv_1hv_2}{|h|h\sqrt{v_1^2+v_2^2}}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\frac{h}{|h|}\cdot\frac{v_1v_2}{\sqrt{v_1^2+v_2^2}}\\
\end{aligned}
$$

Donde se observa que este límite claramente oscila, según por que lado $h$ tiende a cero. Concluimos que las derivadas parciales no existen para ninguna dirección en $(0,0)$

##### Punto $(x,y)\neq(0,0)$

Lo más importante para estos casos, es observar si la función es diferenciable para los puntos que queremos estudiar, pues si es diferenciable, tenemos regalada la existencia de derivadas direccionales.

Por lo tanto, estudiaremos si la función es diferenciable para los puntos $(x,y)\neq(0,0)$ usando el teorema de condición suficiente de diferenciabilidad.
Entonces estudiemos las derivadas parciales, considerando esta definición alternativa de la función para facilitar los cálculos:

- $f(x,y)=xy(x^2+y^2)^{-1/2}$

**Derivada $\frac{\partial f}{\partial x}(x_0,y_0):$**

Operando

$$
\begin{aligned}
&f_x(x_0,y_0)\\
&=\scriptstyle{(\text{derivada del cociente: }f=xy;f'=y;g=\sqrt{x^2+y^2};g'=\frac{2x}{2\sqrt{x^2+y^2}})}\\
&\left(y\sqrt{x^2+y^2}-\frac{xy\cancel{2}x}{\cancel{2}\sqrt{x^2+y^2}}\right)\cdot\frac{1}{x^2+y^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\left(y\sqrt{x^2+y^2}-\frac{yx^2}{\sqrt{x^2+y^2}}\right)\cdot\frac{1}{x^2+y^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\left(\frac{y(x^2+y^2)-yx^2}{\sqrt{x^2+y^2}}\right)\cdot\frac{1}{x^2+y^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{y}{\sqrt{x^2+y^2}}\left(x^2+y^2-x^2\right)\cdot\frac{1}{x^2+y^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{y^3}{(x^2+y^2)^{3/2}}
\end{aligned}
$$

**Derivada $\frac{\partial f}{\partial y}(x_0,y_0)$:**

Por simetría, tenemos que:

$$
\frac{\partial f}{\partial y}(x_0,y_0)=\frac{x^3}{(x^2+y^2)^{3/2}}
$$

A partir de esto, podemos observar que para cualquier punto $(x,y)\neq(0,0)$, ambas derivadas no anulan su denominador, por lo que los puntos problemáticos están fuera del dominio.
Entonces las derivadas parciales son continuas.

Por lo tanto, la función es diferenciable para todo punto distinto de $(0,0)$. Entonces para todo punto distinto de $(0,0)$ existen todas las derivadas direccionales.

##### Conclusión

Por lo que vimos, las derivadas direccionales existen para todo punto distinto de $(0,0)$, y en ese punto no existen.

### Función #2

- $f(x,y) =
\begin{cases}
\tfrac{e^{xy} - 1}{x} & x \ne 0 \\
y & x = 0
\end{cases}$

#### Continuidad

Notemos que los puntos problemáticos de la función son aquellos de la forma $(0,y)\in\mathbb{R}^2$. Entonces tomemos uno genérico y evaluemos el límite:

$$
\begin{aligned}
&\lim_{(x,y)\to(0,y)}f(x,y)\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{x\to0}\frac{e^{xy}-1}{x}\\
&=\scriptstyle{(\text{usando que si: }u\to0\implies e^u-1\sim u)}\\
&\lim_{x\to0}\frac{xy}{x}\\
&=\scriptstyle{(\text{operatoria})}\\
&y
\end{aligned}
$$

Por lo tanto, esta función es continua, pues el valor funcional en el punto $(0,y)$ que tomamos es exactamente $y$.

#### Derivadas direccionales

Consideremos una dirección genérica $v=(v_1,v_2)$ y separemos dos casos:

##### Puntos de la forma $(0,y)\in\mathbb{R}^2$

Operando:

$$
\begin{aligned}
&\frac{\partial f}{\partial v}(0,y)\\
&=\scriptstyle{(\text{definición de derivada direccional})}\\
&\lim_{h\to0}\frac{f(hv_1,y+hv_2) - f(0,y)}{h}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{h\to0}\left(\frac{e^{hv_1(y+hv_2)}-1}{hv_1}-y\right)\cdot\frac{1}{h}\\
&=\scriptstyle{(\text{usando que si: }u\to0\implies e^u-1\sim u)}\\
&\lim_{h\to0}\left(\frac{\cancel{hv_1}(y+hv_2)}{\cancel{hv_1}}-y\right)\cdot\frac{1}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\frac{hv_2}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&v_2
\end{aligned}
$$

Con esto podemos concluir que para estos puntos, la derivada direccional existe y vale $v_2$.

##### Puntos distintos de aquellos de la forma $(0,y)\in\mathbb{R}^2$

Llamamos $(x,y)$ al punto considerado. Operando:

$$
\begin{aligned}
&\frac{\partial f}{\partial v}(x,y)\\
&=\scriptstyle{(\text{definición de derivada direccional})}\\
&\lim_{h\to0}\frac{f(x+hv_1,y+hv_2) - f(x,y)}{h}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{h\to0}\left(\frac{e^{(x+hv_1)(y+hv_2)}-1}{x+hv_1}-\frac{e^{xy}-1}{x}\right)\cdot\frac{1}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\left(\frac{e^{xy+xhv_2+yhv_1+h^2v_1v_2}-1}{x+hv_1}-\frac{e^{xy}-1}{x}\right)\cdot\frac{1}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\left(\frac{e^{xy}e^{h(yv_1+xv_2+hv_1v_2)}-1}{x+hv_1}-\frac{e^{xy}-1}{x}\right)\cdot\frac{1}{h}\\
&=\scriptstyle{(\text{Taylor de }e^u\text{ en }u=0: e^u=1+u)}\\
&\lim_{h\to0}\left(\frac{e^{xy}(1+h(yv_1+xv_2+hv_1v_2))-1}{x+hv_1}-\frac{e^{xy}-1}{x}\right)\cdot\frac{1}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\left(\frac{x(e^{xy}+e^{xy}h(yv_1+xv_2+hv_1v_2)-1)-(x+hv_1)(e^{xy}-1)}{x(x+hv_1)}\right)\cdot\frac{1}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\left(\frac{\cancel{xe^{xy}}+xe^{xy}h(yv_1+xv_2+hv_1v_2)-\cancel{x}-\cancel{xe^{xy}}+\cancel{x}-hv_1e^{xy}+hv_1}{x(x+hv_1)}\right)\cdot\frac{1}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\frac{h(xe^{xy}(yv_1+xv_2+hv_1v_2)-v_1e^{xy}+v_1)}{hx(x+hv_1)}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\frac{xe^{xy}(yv_1+xv_2+hv_1v_2)-v_1e^{xy}+v_1}{x(x+hv_1)}\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{xe^{xy}(yv_1+xv_2+hv_1v_2)-v_1e^{xy}+v_1}{x(x+hv_1)}\\
\end{aligned}
$$

La expresión es compleja, pero al no tener más dependencia de $h$, y depender del punto $(x,y)\in\mathbb{R}$ y los vectores $v_1,v_2$ elegidos nos garantiza que la derivada direccional existe.
Entonces la derivada direccional también existe para todos los puntos distintos a los puntos de la forma $(0,y)\in\mathbb{R}$.

##### Conclusión

Reagrupando los dos casos que evaluamos, podemos concluir que las derivadas direccionales existen para cualquier punto $(x,y)\in\mathbb{R}$ y cualquier dirección.

### Función #3

- $f(x,y) =
\begin{cases}
\tfrac{x^3}{y} & y \ne 0 \\
0 & y = 0
\end{cases}$

#### Continuidad

Estudiemos los puntos problemáticos, es decir aquellos de la forma $(x,0)$. Probaremos que el límite no existe, considerando las direcciones:

- $y=x^3$
- $y=x$

Entonces, desarrollando:

$$
\begin{aligned}
&\lim_{(x,0)\to(0,0)}\frac{x^3}{y}\\
&=\scriptstyle{(\text{considerando la dirección }y=x^3)}\\
&\lim_{x\to0}\frac{x^3}{x^3}\\
&=\scriptstyle{(\text{operatoria})}\\
&1
\end{aligned}
$$

Por otra parte, tenemos que:

$$
\begin{aligned}
&\lim_{(x,0)\to(0,0)}\frac{x^3}{y}\\
&=\scriptstyle{(\text{considerando la dirección }y=x)}\\
&\lim_{x\to0}\frac{x^3}{x}\\
&=\scriptstyle{(\text{operatoria})}\\
&0
\end{aligned}
$$

Concluyendo, la función no es continua para todos los puntos tales que $y=0$.

#### Derivadas direccionales

Para esta parte, separaremos en dos casos. Como $f$ no es continua para los puntos de la forma $(x,0)\in\mathbb{R}^2$, ahí haremos la distinción.

##### Puntos de la forma $(x,0)\in\mathbb{R}^2$

Consideramos la definición para $v=(v_1,v_2)$, entonces:

$$
\begin{aligned}
&\frac{\partial f}{\partial v}(x,0)\\
&=\scriptstyle{(\text{definición de derivada direccional})}\\
&\lim_{h\to0}\frac{f(x+hv_1,hv_2)-f(x,0)}{h}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{h\to0}\frac{1}{h}\left(\frac{(x+hv_1)^3}{hv_2}\right)\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\frac{(x^2+2xhv_1+h^2)(x+hv_1)}{h^2v_2^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\frac{x^3+x^2hv_1+2x^2hv_1+2xh^2v_1^2+h^2x+h^3v_1}{h^2v_2^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\frac{x^3+3x^2hv_1+h^2(2xv_1^2+x+hv_1)}{h^2v_2^2}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{h\to0}\frac{x^3+3x^2hv_1}{h^2v_2^2}+\frac{2xv_1^2+x+hv_1}{v_2^2}\\
\end{aligned}
$$

Este límite solo existe si $x=0$. Además tenemos que verificar que pasa si $v_2=0$, ya que es parte del denominador.

**Caso $v_2=0$**

Considerando $v=(v_1,0)$ y operando:

$$
\begin{aligned}
&\frac{\partial f}{\partial v}(x,0)\\
&=\scriptstyle{(\text{definición de derivada direccional})}\\
&\lim_{h\to0}\frac{f(x+hv_1,0)-f(x,0)}{h}\\
&=\scriptstyle{(\text{definición de la función})}\\
&\lim_{h\to0}\frac{0-0}{h}\\
&=\scriptstyle{(\text{operatoria})}\\
&0
\end{aligned}
$$

Recapitulando lo obtenido para puntos de la forma $(x,0)$:

- Si $(x,0)=(0,0)$, entonces existen todas las derivadas direccionales.
- Para cualquier punto de la forma $(x,0)$, existe la derivada direccional para cualquier dirección de la forma $v=(v_1,0)$

##### Puntos distintos de la forma $(x,0)\in\mathbb{R}^2$

La función es diferenciable para estos puntos, pues $x^3$ es diferenciable para todo punto, $y$ también es diferenciable para todo punto, e $y$ no se anula en ninguno de los puntos que estamos considerando.
Entonces por propiedad de operatoria con funciones diferenciables, la función es diferenciable en este conjunto de puntos.

Y como es diferenciable, existen todos las derivadas direccionales para estos puntos.