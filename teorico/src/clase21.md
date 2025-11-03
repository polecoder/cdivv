# CLASE 21 - 28/10/2025

## Sucesiones en $\mathbb{R}^n$

### Definición 5.23

Una sucesión es una función $a:\mathbb{N}\to\mathbb{R}^n$

Es decir, ahora una sucesión es una lista ordenada de puntos en $\mathbb{R}^n$.
Como antes, denotamos por $a_k$ a la sucesión o al término $k$-ésimo de la sucesión. Podemos describir dicho término por:

- $a_k=(a_{k,1},a_{k,2},\ldots, a_{k,n})$

### Definición 5.24 (límite)

Decimos que la sucesión $a_n$ tiene límite $L\in\mathbb{R}^n$, y lo denotamos $\lim_{k\to\infty}=L$ sii:

- $\forall\varepsilon>0,\exists k_0\in\mathbb{N}$ tal que $\forall k>k_0: a_k\in B(L,\varepsilon)$

#### Observación

Notemos que esta definición es equivalente a pedir que la sucesión (de números reales) $d(a_k, L)$ tienda a cero.
Esto puede parecer extraño pero tiene todo el sentido geométrico, pues queremos que $a_k$ sea lo más cercano a $L$ posible.

### Proposición 5.26

Sea $a_k$ una sucesión en $\mathbb{R}^n$ y $L=(L_1, L_2,\ldots, L_n)$. Entonces:

$$
\begin{aligned}
&\lim_{k\to\infty}a_k=L\\
&\iff\\
&\lim_{k\to\infty}a_{k,i}=L_i\quad\forall i=1,2\ldots,n
\end{aligned}
$$

Es decir, una sucesión de $\mathbb{R}^n$ converge a $L$ si y sólo si cada una de sus coordenadas converge a la coordenada correspondiente de $L$.

#### Demostración

Hagamos la demostración para la norma $\|.\|_2$

##### Directo $(\rightarrow)$

(H) $\lim_{k\to\infty}a_k=L$
(T) $\lim_{k\to\infty}a_{k,i}=L_i\quad\forall i=1,2\ldots,n$

Desarrollando la norma, podemos fácilmente encontrarnos con esta desigualdad:

- $0\leq|a_{k,i}-L_i|\leq\|a_k-L\|$ para todo $i=1,2,\ldots, n$

Como $\|a_k-L\|$ tiende a 0, entonces también lo hace $|a_{k,i}-L_i|$, de donde obtenemos la definición de límite para cualquier $i=1,2,\ldots,n$

##### Recíproco $(\leftarrow)$

(H) $\lim_{k\to\infty}a_{k,i}=L_i\quad\forall i=1,2\ldots,n$
(T) $\lim_{k\to\infty}a_k=L$

Por hipótesis, tenemos que:

- $\forall\varepsilon>0,\exists k_i\in\mathbb{N}$ tal que $\forall k>k_i:|a_{k,i}-L_i|<\varepsilon$ para todo $i=1,2,\ldots,n$

Entonces, elegimos un $\varepsilon>0$ conveniente para las cuentas de lo que sigue, por ejemplo: $\varepsilon:=\frac{\varepsilon}{\sqrt{n}}$. Consideramos también un $k_0$ conveniente de la siguiente forma: $k_0:=\max\{k_1,k_2,\ldots, k_n\}$.
Ahora si, podemos avanzar con el razonamiento:

$$
\begin{aligned}
&\|a_k-L\|\\
&=\\
&\sqrt{(a_{k,1}-L_1)^2+(a_{k,2}-L_2)^2+\ldots+(a_{k,n}-L_n)^2}\\
&<\scriptstyle{(\text{para }k>k_0)}\\
&\sqrt{\left(\frac{\varepsilon}{\sqrt{n}}\right)^2+\left(\frac{\varepsilon}{\sqrt{n}}\right)^2+\ldots+\left(\frac{\varepsilon}{\sqrt{n}}\right)^2}\\
&=\\
&\sqrt{\frac{\varepsilon^2}{n}+\frac{\varepsilon^2}{n}+\ldots+\frac{\varepsilon^2}{n}}\\
&=\\
&\sqrt{\frac{n\varepsilon^2}{n}}\\
&=\\
&\sqrt{\varepsilon^2}\\
&=\\
&\varepsilon\\
\end{aligned}
$$

Por lo tanto, podemos concluir que $\|a_k-L\|<\varepsilon$, por lo que probamos que $\lim_{k\to\infty}a_k=L$.

Esto concluye la prueba.

### Ejemplos 5.27

1. La sucesión de $\mathbb{R}^2$ definida como $a_k=(\frac{1}{k},k^2)$ no es convergente, ya que su segunda componente no lo es.

2. La sucesión de $\mathbb{R}^3$ definida como $a_k=(\sqrt{k},1,\frac{1}{k})$ no es convergente, ya que su primera componente no lo es

3. La sucesión de $\mathbb{R}^3$ definida como $a_k=(2,\frac{(-1)^k}{k},1+e^{-k})$ converge al punto $(2,0,1)$

### Proposición 5.28

Sean $a_k$ y $b_k$ sucesiones de $\mathbb{R}^n$ tales que $\lim a_k=a$ y $\lim b_k=b$ y $\lambda_k$ una sucesión de números reales convergente a $\lambda\in\mathbb{R}$. Entonces:

1. $\lim a_k+b_k=a+b$
2. $\lim\lambda_k a_k=\lambda a$
3. $\lim\|a_k\|=\|a\|$

### Definición

Decimos que un conjunto $A$ es cerrado por sucesiones cuando cumple con la siguiente propiedad:

Si una sucesión de elementos del conjunto $\{a_k\}\subset A$ es convergente a $\lim a_k=a$, entonces $a\in A$.
Es decir un conjunto que contiene todos los límites de las sucesiones de elementos del conjunto.

### Proposición 5.29

Un conjunto $C$ es cerrado sii es cerrado por sucesiones.

#### Demostración

##### Directo $(\rightarrow)$

(H) $C$ es cerrado
(T) $C$ es cerrado por sucesiones

Sea una sucesión de elementos del conjunto $\{a_k\}\subset C$, convergente a $\lim a_k=a$ cualesquiera, queremos probar que $a\in C$.

Supongamos por absurdo, que esto no es cierto. Es decir que $a\in C^C$. Viendo que $C$ es cerrado por hipótesis, tenemos que $C^C$ es abierto, entonces $a$ es interior de $C^C$.

Por esto podemos decir que existe $\delta>0$ tal que $B(a,\delta)\subset C^C$. Esto ya es absurdo, pues contradice que $\lim a_k = a$, porque no "me puedo acercar tanto como quiera" al punto $a$ mediante puntos de la sucesión $a_k$.

##### Recíproco $(\leftarrow)$

(H) $C$ es cerrado por sucesiones
(T) $C$ es cerrado

Probaremos que $C$ es cerrado, tomando un punto frontera de $C$ y verificar que efectivamente pertenece al conjunto.
Sea entonces $x_0$ un punto frontera de $C$, buscamos construir una sucesión que tienda a $x_0$, pues con eso podremos garantizar que $x_0\in C$ por hipótesis.
Consideremos $\varepsilon_k=\frac{1}{k}$, entonces si miramos en la bola abierta $B_k=(x_0,\varepsilon_k)$, tendremos un punto $a_k\in C$ (pues $x_0$ es frontera). Si hacemos esto para infinitos $k\in\mathbb{N}$ habremos conseguido una sucesión $a_k$ que por construcción converge a $x_0$.
Y cómo $C$ es cerrado por sucesiones, tenemos que $\lim a_k=x_0$ pertenece al conjunto $C$.
Como consideramos este razonamiento para un $x_0$ frontera cualquiera de $C$, esto vale para todos ellos, con lo que probamos la propiedad.

### Definición 5.30

Sea $a_k$ una sucesión de $\mathbb{R}^n$, y $k_j$ una sucesión estrictamente creciente de números naturales. Entonces la sucesión $a_{k_j}$ es una subsucesión de $a_k$.

Es fácil de corroborar que si $a_k$ es una sucesión convergente, entonces toda subsucesión $a_{k_j}$ también lo es, y además converge al mismo límite. También es cierto que toda sucesión acotada tiene una subsucesión convergente, pero la demostración no se desprende trivialmente del resultado que teníamos para las sucesiones en $\mathbb{R}$.

### Teorema 5.31

Toda sucesión acotada de $\mathbb{R}^n$ tiene una subsucesión convergente.

#### Demostración

Sea $a_k=(a_{k,1}, a_{k,2},\ldots,a_{k,n})$ una sucesión acotada.

Consideremos primero $a_{k,1}$ que es acotada, pues $a_k$ es acotada por hipótesis.
Entonces podemos usar el resultado de sucesiones reales para obtener una subsucesión convergente, notando el conjunto de los índices como $N_1\subset\mathbb{N}$. Vamos a notar la subsucesión convergente como:

- $(a_{k,1})_{N_1\subset\mathbb{N}}$

Ahora vayamos con $a_{k,2}$, para buscar una subsucesión acotada empezamos directamente a buscar en los índices $N_1$ (donde la sucesión también es acotada), por lo que es válido el resultado de sucesiones reales.
De esta forma obtenemos la subsucesión convergente:

- $(a_{k,2})_{N_2\subset N_1\subset\mathbb{N}}$

Podemos seguir este razonamiento $n$ veces, y cuando lleguemos a ese punto podremos tomar los índices $N_n$ para obtener la subsucesión de $a_k$.

### Corolario 5.32

Si $K\subset\mathbb{R}^n$ es un conjunto compacto, y $a_k$ es una sucesión de elementos de $K$, entonces $a_k$ posee una subsucesión convergente, y además su límite es un elemento de $K$.

#### Demostración

Como $K$ es compacto, en particular es acotado. Por lo que usando el teorema anterior tenemos que $a_k$ tiene una subsucesión convergente, llamemosla:

- $(a_k)_{k\in N_1}$

Por otra parte, como $K$ es compacto, en particular es cerrado. Entonces usando la otra proposición de esta clase (5.29), tenemos que es cerrado por sucesiones.
Por lo tanto $\lim(a_k)_{k\in N_1}$ está en el conjunto.