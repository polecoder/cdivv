# CLASE 6 - 08/08/2025

## Ecuaciones diferenciales lineales de segundo orden a coeficientes constantes homogéneas

### Definición 6.1

Una ecuación diferencial de segundo orden se llama lineal a coeficientes constantes homogénea si es:

- $y''+ay'+by=0$

Donde $a$ y $b$ son constantes dadas independientes de $x$ e $y$

### Teorema 6.2

Todas las funciones soluciones de la ecuación diferencial de segundo orden homogénea forman un espacio vectorial de dimensión 2.
Se puede comprobar fácilmente que dadas $y_1(x)$ e $y_2(x)$ soluciones de la ecuación diferencial, entonces cualquier combinación lineal de ellas $C_1y_1(x)+C_2y_2(x)$ también es solución.

### Corolario 6.3

Si dos funciones solución $y_1(x)$ e $y_2(x)$ de la ecuación diferencial $y''+ay'+by=0$ **son linealmente independientes**, entonces forman una base del espacio vectorial de todas las soluciones. Es decir, la solución general es:

- $y(x)=C_1y_1(x)+C_2y_2(x)$, donde $C_1$ y $C_2$ son constantes reales arbitrarias.

Por lo tanto, para hallar la solución general de una ecuación lineal homogénea de segundo grado, basta con hallar **dos soluciones linealmente independientes**

### Soluciones exponenciales 6.4

A continuación, buscaremos soluciones $y(x)=e^{\lambda x}$, donde $\lambda$ es una constante real a determinar, que sean solución de la ecuación diferencial $y''+ay'+by=0$.
Sustituyendo en la ecuación diferencial $y(x)=e^{\lambda x};y'(x)=\lambda e^{\lambda x};y''(x)=\lambda^2 e^{\lambda x}$, obtenemos:

- $(\lambda^2+a\lambda+b)e^{\lambda x}=0$

Se observa que esto solo ocurre cuando $\lambda$ es raíz del polinomio $\lambda^2+a\lambda+b$; igualando dicho polinomio a 0, obtenemos **la ecuación característica**:

- $\lambda^2+a\lambda+b=0$

Concluyendo, $y(x)=e^{\lambda x}$ es solución de la ecuación diferencial **si y sólo si $\lambda$ es solución de la ecuación característica** $\lambda^2+a\lambda+b=0$

A partir de esto, vamos a generalizar el procedimiento para hallar la solución de una ecuación diferencial de estas características, en función de la naturaleza de las raíces de la ecuación característica.

### Procedimiento para hallar la solución general de estas ecuaciones diferenciales 6.6

Lo primero que haremos es hallar las raíces de la ecuación característica $\lambda^2+a\lambda+b=0$ discutiendo tres casos diferentes según el determinante de la ecuación característica:

- $\Delta=a^2-4b$

#### Caso A: $\Delta>0$

En este caso tenemos dos raíces reales diferentes $\lambda_1,\lambda_2$, esto implica que $e^{\lambda_1x}$ y $e^{\lambda_2x}$ son linealmente independientes  (tomarlo como un resultado teórico aunque es simple de observar), con lo que podemos obtener la solución general:

- $y(x)=C_1e^{\lambda_1 x}+C_2e^{\lambda_2 x}$

Con $C_1$ y $C_2$ dos constantes reales arbitrarias.

#### Caso B: $\Delta=0$

En este caso tenemos una raíz real doble $\lambda_0$, ahora ya no tenemos dos funciones linealmente independientes para para cada raíz (pues son la misma función). Sin embargo, es fácil verificar que si $\lambda_0$ es doble, entonces la función $y_2(x)=xe^{\lambda_0 x}$ también es solución, que es linealmente independiente de $y_1(x)=e^{\lambda_0 x}$. Lo que nos deja con la solución general:

- $y(x)=C_1e^{\lambda_0x}+C_2xe^{\lambda_0x}$

Con $C_1$ y $C_2$ dos constantes reales arbitrarias.

#### Caso C: $\Delta<0$

En este caso tenemos dos raíces complejas diferentes $\lambda_1$ y $\lambda_2$.
Consideramos $\lambda=\alpha\pm\beta$, la solución general para este caso es:

- $y(x)=C_1e^{\alpha x}cos(\beta x)+C_2e^{\alpha x}sen(\beta x)$


**Observación**: Se puede expandir más sobre la forma de las soluciones (que tienen una gran influencia de la exponencial compleja), pero no lo voy a hacer en estas notas ya que considero que no aporta demasiado.

## Ecuaciones diferenciales lineales de segundo orden a coeficientes constantes NO homogéneas

### Definición 7.1

Una ecuación diferencial de segundo órden se llama lineal a coeficientes constantes y NO homogénea si es:

- $y''+ay'+by=r(x)$

Donde $a$ y $b$ son constantes dadas independientes de $x$ e $y$, y $r(x)$ es una función dada.
Ahora recordamos el siguiente teorema que usaremos como método de resolución, de forma muy similar a las ecuaciones de segundo órden.

### Recordatorio: Teorema 5.3

La solución general de una ecuación diferencial lineal no homogénea es igual a la solución general de la ecuación homogénea asociada, más una (y solo una, cualquiera) solución particular de la ecuación diferencial dada NO homogénea:

- $y_G=y_H+y_P$

### Método de resolución

Usaremos la misma estrategia que en las ecuaciones de primer orden, lo único que cambia es la forma en la que hallamos la solución de $(H)$ (que se vió en la parte anterior), y el como hallar una solución particular de $(NH)$.

En las notas, la formalización de esta estrategia es bastante compleja, y a mi criterio bastante innecesaria para los tipos de ejercicios a los que nos vamos a enfrentar. En las notas de Fiori, se propone la idea interesante de basarse en la forma de $r(x)$ para buscar candidatos a solución, veamos algunos ejemplos:

- $y''+ay'+by=cos(bx)$
    - En este caso, está claro que la función solución no va a ser un polinomio, buscaremos alguna solución válida que contenga alguna función trigonométrica. En estos casos conviene considerar una combinación lineal de seno y coseno de la siguiente forma:

        - $y_P(x)=Acos(bx)+Bsen(bx)$

- $y''+ay'+by=3x^2+x$
    - En este caso probaremos con un polinomio, como el grado del mismo es 2, conviene considerar un polinomio genérico del mismo grado como solución. Al sustituir nos quedará despejar para obtener la cara del polinomio solución.

Concluyendo, para el método de resolución de este tipo de ecuaciones diferenciales, lo mejor es mirar ejercicios de práctico para entender mejor como funciona el procedimiento, que de por si es simple.

