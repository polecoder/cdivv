# CLASE 5 - 07/08/2025

## Ecuaciones diferenciales

### Ecuación diferencial lineal de primer orden homogénea

#### Definición 4.1

Se llama ecuación diferencial lineal de primer orden homogénea a una ecuación del tipo:

- $y'+a(x)y=0$

Donde $a(x)$ es una función dada.

**Observación:** Claramente se ve que la ecuación diferencial mencionada, es de variables separables, pues:

- $y'=-a(x)\cdot y$

Por lo tanto se resuelve como se vió en la sección de variables separables.

### Ecuación diferencial lineal de primer orden NO homogénea

#### Definición 5.1

Se llama ecuación diferencial NO homogénea a una ecuación del tipo:

- $y'+a(x)y=r(x)$

Donde $a(x)$ y $r(x)$ son funciones conocidas, definidas y continuas para todo $x\in\mathbb{R}$, tal que $r(x)$ no es idénticamente nula.

**Observación:** Consideramos la ecuación diferencial homogénea asociada a la siguiente ecuación diferencial:

- $y'+a(x)y=0$

#### Procedimiento de resolución de una ecuación diferencial lineal NO homogénea 5.2

Basaremos nuestro procedimiento de resolución en el siguiente teorema:

##### Teorema 5.3

La solución general de una ecuación diferencial lineal no homogénea es igual a la solución general de la ecuación homogénea asociada, más una (y solo una, cualquiera) solución particular de la ecuación diferencial dada NO homogénea.
Representamos este teorema con la siguiente notación:

- $y_G=y_H+y_P$, donde:
    - $y_G$ es la solución general de la ecuación diferencial **NO homogénea**
    - $y_H$ es la solución general de la ecuación diferencial **homogénea**
    - $y_P$ es una solución particular de la ecuación diferencial **NO homogénea**

**Observación:** La demostración del teorema está hecha en las notas, pero no se hace formalmente en las clases, por esto no voy a reescribirla en los apuntes. De todos modos la intuición que se da en la clase hace entender que no es muy complicado el porque este teorema se cumple.

A continuación, describimos el procedimiento para la resolución de una ecuación diferencial lineal NO homogénea.

1. Hallar la solución general $y_H(x)$ de la ecuación lineal homogénea asociada.
2. Hallar una solución particular $y_P(x)$ de la ecuación diferencial dada NO homogénea. En la siguiente sección veremos como hallar dicha $y_P$ usando el "método de variación de constante".
3. Sumar la solución general de la homogénea $y_H(x)$ con la solución particular $y_P(x)$ para obtener la solución final $y_G(x)$

#### Método de variación de constante 5.4

Este método se usará para hallar (en cualquier caso) una solución particular $y_P$ para poder aplicar el método de resolución descrito anteriormente.

1. En la solución general $y_H(x)$ de la ecuación diferencial homogénea asociada $(H)$ siempre aparecerá una constante $C$ real arbitraria (se verá más claro al hacer un ejemplo).
2. Tomaremos $y_P(x)$ igual a $y_H(x)$, pero reemplazaremos donde tenemos $C$, la constante arbitraria, con $C(x)$ una función genérica que depende de $x$.
3. Sustituyendo la función $y_P(x)$ descrita en el paso anterior, en la ecuación diferencial NO homogénea $(NH)$, haciendo que la verifique, se despeja y se encuentra $C(x)$. De todas las posibles funciones $C(x)$ que se despejen habrá que elegir solo una.
4. La función $C(x)$ se sustituye en la expresión de $y_P(x)$ que teníamos hasta ahora para obtener la solución particular de $(NH)$

#### Ejemplo 5.5

Queremos resolver $y'=cos(x)y+cos(x)$, definimos las siguientes ecuaciones diferenciales con las que vamos a trabajar:

- $y'-cos(x)y=0\quad(H)$
- $y'-cos(x)y=cos(x)\quad(NH)$

Entonces ahora hallamos la solución general para $(H)$.

##### Solución de $(H)$

Desarrollemos:

$$
\begin{aligned}
&y'-cos(x)y=0\\
&\iff\\
&y'=cos(x)y\\
&\iff\\
&\frac{y'}{y}=cos(x)\\
&\iff\\
&\int\frac{y'}{y}dx=\int cos(x)dx\\
&\iff\scriptstyle{(u=y(x),du=y'(x)dx)}\\
&\int\frac{du}{u}dx=sen(x)+C\\
&\iff\\
&ln|u|=sen(x)+C\\
&\iff\\
&|u|=e^Ce^{sen(x)}\\
&\iff\\
&u=ke^{sen(x)}\\
&\iff\scriptstyle{(\text{deshago el cambio de variable})}\\
&y(x)=ke^{sen(x)}\\
\end{aligned}
$$

Por lo tanto concluimos que:

- $y_H(x)=ke^{sen(x)}$

##### Solución particular $(NH)$

Consideramos $y_P(x)=C(x)e^{sen(x)}$ y sustituimos en $(NH)$ para despejar $C(x)$:

$$
\begin{aligned}
&y'-cos(x)y=cos(x)\\
&\iff\\
&(C(x)e^{sen(x)})'=cos(x)+cos(x)C(x)e^{sen(x)}\\
&\iff\scriptstyle{(\text{derivada del producto})}\\
&C'(x)e^{sen(x)}+C(x)e^{sen(x)}cos(x)=cos(x)+cos(x)C(x)e^{sen(x)}\\
&\iff\scriptstyle{(\text{simplificando})}\\
&C'(x)e^{sen(x)}=cos(x)\\
&\iff\\
&C'(x)=cos(x)e^{-sen(x)}\\
&\iff\\
&\int C'(x)dx=\int cos(x)e^{-sen(x)}dx\\
&\iff\scriptstyle{(\text{u=sen(x),du=cos(x)dx})}\\
&C(x)+k_1=\int cos(x)e^{-sen(x)}dx\\
&\iff\\
&C(x)+k_1=\int e^{-u}du\\
&\iff\\
&C(x)+k_1=-e^{-u}+k_2\\
&\iff\\
&C(x)=-e^{-u}+k\\
&\iff\scriptstyle{(\text{deshaciendo el cambio de variable})}\\
&C(x)=-e^{-sen(x)}+k\\
\end{aligned}
$$

Ahora elegimos una sola de estas soluciones, con $k=0$:

- $C(x)=-e^{-sen(x)}$, por lo tanto:
- $y_P(x)=-e^{-sen(x)}e^{sen(x)}=-1$

##### Conclusión del problema

La solución general de la ecuación diferencial dada $(NH)$ es:

- $y(x)=Ce^{sen(x)}-1\quad\forall x\in\mathbb{R}$