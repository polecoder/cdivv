# CLASE 4 - 06/08/2025

## Ecuaciones diferenciales

### Intuición

Una ecuación diferencial es una igualdad en la cual:

- La incógnita es una función desconocida $y=f(x)$ definida y derivable hasta orden $k$ para todo $x\in\mathbb{R}$ (casos que vamos a trabajar en general) o para todo $x$ en un intervalo de reales.
- Aparece en la ecuación alguna de las derivadas de la función desconocida $y=f(x)$, puede ser cualquiera de ellas hasta la derivada de orden $k$.
- La derivada de mayor orden es la que determina el orden de la ecuación diferencial, es decir: si la derivada de mayor orden que aparece en la ecuación es la derivada segunda $y''=f''(x)$, entonces es una ecuación diferencial de grado 2.

En este tema nos vamos a centrar en una clase muy particular de ecuaciones diferenciales, y vamos a trabajar solamente en esas clases. Hay otros cursos que expanden sobre este tópico.
Vayamos ahora a uno de los tipos que vamos a estar trabajando.

### Ecuación diferencial de primer orden de variables separables.

#### Definición 2.1

Una ecuación diferencial ordinaria de primer orden se llama de variables separadas si es de la forma:

- $y'=A(y)B(x)$

Donde: 

- $A(y)$ es una función dada, que depende solo de $y$ y,
- $B(x)$ es una función dada, que depende solo de $x$

**ATENCIÓN:** $y$ es una función, pero $x$ es una variable, este punto es muy importante, ya que la costumbre tiende a indicarnos que $y$ es una variable numerica.

##### Ejemplos:

1. $y'=(sen (x))(1+y^2)$ es de variables separables, donde $A(y)=1+y^2$ y $B(x)=sen(x)$.
2. $y'=sen(x+y)$ claramente no es de variables separables.

#### Solución general 2.2

Distingamos dos casos:

1. Si existen algunos valores reales $\alpha$ tales que $A(\alpha)=0$ entonces la función $y(x)=\alpha$ constante, independiente de $x$, definida para todo $x\in\mathbb{R}$, es solución de la ecuación diferencial $y'=A(y)B(x)$.
    Esto lo podemos ver sustituyendo $y(x)=\alpha\Rightarrow0=A(\alpha)B(x)$, que trivialmente se cumple pues $A(\alpha)=0$.
2. Ahora, podemos buscar las restantes soluciones $y(x)$ tales que $A(y(x))\neq0$; entonces, dividiendo la ecuación diferencial dada entre $A(y)$ se obtiene:

    $$
    \frac{y'(x)}{A(y(x))}=B(x)
    $$

    Primitivando respecto de $x$ (atención, para mantener la igualdad tenemos que considerar la misma variable de ambos lados) obtenemos lo siguiente:

    $$
    \int\frac{y'(x)}{A(y(x))}dx=C+\int B(x)dx
    $$

    Donde $C$ es una constante real arbitraria. En la primer primitiva hacemos el cambio de variable:

    - $u=y(x)$
    - $du=y'(x)dx$
    
    Esto resulta en:

    $$
    \int\frac{du}{A(u)}=C+\int B(x)dx
    $$

    Como $A(y)$ y $B(x)$ son funciones conocidas al dar la ecuación diferencial, calculando las primitivas obtenemos funciones conocidas:

    $$
    P(y)=C+Q(x)
    $$

    Donde $C$ es una constante real arbitraria, $P(y)$ es una primitiva respecto de $y$ de la función $\frac{1}{A(u)}$, y $Q(x)$ es una primitiva de la función continua dada $B(x)$.
    A partir de este punto se despeja y se obtiene una (o en general varias) expresión de $y$

**Observación:** El caso 1 se puede ignorar ya que se obtiene directamente de la expresión general de $y$ obtenida.

#### Ejemplo 2.3

Encontrar todas las soluciones de la ecuación diferencial:

- $y'=cos(x)y$

Realicemos el procedimiento mencionado en la parte que vimos anteriormente:

$$
\begin{aligned}
&\frac{y'}{y}=cos(x)\\
&\iff\\
&\int\frac{y'}{y}dx=\int cos(x)dx\\
&\iff\scriptstyle{(u=y(x),du=y'(x)dx)}\\
&\int\frac{1}{u}du=sen(x)+C\\
&\iff\\
&ln|u|=sen(x)+C\\
&\iff\scriptstyle{(\text{deshago el cambio de variable})}\\
&ln|y(x)|=sen(x)+C\\
&\iff\\
&e^{ln|y(x)|}=e^{sen(x)+C}\\
&\iff\\
&|y(x)|=e^{sen(x)+C}\\
&\iff\\
&y(x)=\pm e^Ce^{sen(x)}\\
&\iff\\
&y(x)=\pm e^Ce^{sen(x)}\\
\end{aligned}
$$

Llamo $k=\pm e^C$, que es una constante real arbitraria. Por lo tanto la solución a la ecuación diferencial es la siguiente:

- $y=ke^{sen(x)}$ con $k\in\mathbb{R}$

##### Verificación

Por lo general, verificar que la solución de una ecuación diferencial que hallamos es correcta, es sencillo, veamos como verificar:

Quiero ver que $y(x)=ke^{sen(x)}$ cumple lo siguiente:

- $y'=cos(x)y$

Entonces primero hallemos $y'$:

$$
\begin{aligned}
&y'(x)=(ke^{sen(x)})'\\
&\iff\scriptstyle{(\text{regla de la cadena: }f(x)=e^x;g(x)=sen(x))}\\
&y'(x)=ke^{sen(x)}cos(x)\\
\end{aligned}
$$

Ahora si, sustituyamos $y$ e $y'$ en la ecuación diferencial a ver tenemos igualdad:

$$
\begin{aligned}
&y'=cos(x)y\\
&\iff\\
&ke^{sen(x)}cos(x)=cos(x)ke^{sen(x)}\\
\end{aligned}
$$

Listo! Verificamos que efectivamente la solución que hallamos cumple la ecuación diferencial.

### Datos iniciales

Como vimos en la sección anterior, por lo general llegamos a infinitas soluciones para una ecuación diferencial. En algunos casos, además de hallar una función $y$ y que cumpla con la ecuación diferencias, también es de interés hallar una función $y$ de estas mismas características pero que además cumpla con lo que se llama una condición inicial.

Por lo general estas son del tipo:

- $y(x_0)=y_0$ con $x_0,y_0\in\mathbb{R}$

Cuando nos dan datos iniciales, procedemos exactamente de la misma forma que venimos trabajando hasta ahora, para hallar lo que llamaremos **la solución general** que básicamente es la forma general que tiene una función solución $y$. Luego para que cumpla con los datos iniciales, sustituimos los valores reales que nos fueron dados en la solución general, para hallar la solución "particular" despejando.
Veamos un ejemplo:

#### Ejemplo 3.1

Sabiendo que todas las soluciones de la ecuación diferencial $y'=(cos x)y$ son de la forma $y(x)=Ce^{sen(x)}$, hallar la única solución que cumple que:

- $y(0)=3$

Sustiyuendo en la forma general de la solución tenemos que:

$$
\begin{aligned}
&y(x)=Ce^{sen(x)}\\
&\iff\\
&3=Ce^{sen(0)}\\
&\iff\\
&3=C\\
\end{aligned}
$$

Por lo que entonces la solución al problema con datos iniciales es:

- $y(x)=3e^{sen(x)}$