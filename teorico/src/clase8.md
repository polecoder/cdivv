# CLASE 8 - 26/08/2025

## Sucesiones

### Definición 3.5

Decimos que una sucesión $a_n$ está acotada si $\exists K\in\mathbb{R}$ tal que $|a_n|\leq K$ para todo $n\in\mathbb{N}$.
También decimos que la sucesión está acotada superiormente cuando existe un $K\in\mathbb{R}$ tal que $a_n<K$ para todo $n\in\mathbb{N}$, y de manera similar se define la acotación inferior.

### Proposición 3.6

Si $a_n$ tiene límite, entonces está acotada.

#### Demostración

Tomemos $\varepsilon>0$ cualquiera, por ejemplo $\varepsilon=1$. Como $a_n$ converge, tenemos que:

- $\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0:a_n\in E(L,1)$

A partir de esto podemos deducir que:

- $|a_n|<|L|+1$

Por lo tanto esta cota nos vale para todos los $n>n_0$. Veamos que podemos hacer con todos los elementos anteriores a $n_0$:

- $\{a_1,a_2,\ldots,a_{n_0}\}$

Como es un conjunto finito, podemos tomar:

- $k=\max\{|a_1|,|a_2|,\ldots,|a_{n_0}|\}$

Y con esto podemos finalizar tomando:

- $K=\max\{k, |L|+1\}$

Esto concluye la prueba, pues con esto se tiene que:

- $|a_n|<K$ para todo $n\in\mathbb{N}$

Que significa que la sucesión $a_n$ está acotada.

**Observación:** Para recordar mejor esta prueba, siempre lo ideal es pensar en el caso de una sucesión con todo positivo, a partir de la misma se puede derivar todo lo equivalente a ese razonamiento cuando la sucesión tiene términos negativos y hasta un límite negativo.

### Definición 3.7

Decimos que el límite de $a_n$ es infinito, $\lim_{n\to\infty}=+\infty$ sii:

- $\forall K>0,\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0: a_n>K$

De forma equivalente, definimos que el límite de $a_n$ es menos infinito, $\lim_{n\to\infty}=-\infty$ sii:

- $\forall K<0,\exists n_0\in\mathbb{N}$ tal que $\forall n<n_0: a_n<K$

**Observación:** Entonces tenemos que las sucesiones acotadas pueden ser convergentes o no. Qué pasa con las sucesiones no acotadas?
La respuesta es que no necesariamente tienen límite más o menos infinito, por ejemplo, considerar el ejemplo de $a_n=(-1)^n$

### Definición 3.8

Decimos que una sucesión $a_n$ es:

- Mónotona creciente sii $a_{n+1}\geq a_n\quad\forall n\in\mathbb{N}$, o
- Mónotona decreciente sii $a_{n+1}\leq a_n\quad\forall n\in\mathbb{N}$

Cuando la desigualdad es estricta, decimos que la sucesión es estrictamente mónotona.

### Teorema 3.9

Si $a_n$ es una sucesión mónotona creciente y acotada superiormente, entonces tiene límite.

#### Demostración

Sea $L=\sup\{a_n:n\in\mathbb{N}\}$, es decir, el supremo del conjunto imagen de la sucesión. Sabemos que existe por el Axioma de Completitud en los reales (ya que el conjunto es no vacío y acotado). Ahora consideremos $\varepsilon > 0$, queremos probar que:

- $\exists n_0\in\mathbb{N}$ tal que $\forall n>0: a_n\in (L-\varepsilon,L]$ (pues no es necesario considerar lo que está "a la derecha" de L ya que es supremo)

Observemos que si no existe ningún elemento $a_n$ en el intervalo dado, entonces tendríamos que:

- $L-\frac{\varepsilon}{2}$ es cota superior, además:
- $L-\frac{\varepsilon}{2}<L$

Por lo tanto, $L-\frac{\varepsilon}{2}$ es supremo, lo cual es absurdo pues $L$ es el supremo. Entonces necesariamente tiene que existir un elemento $a_{n_0}\in E(L-\varepsilon, L]$.

Cómo $a_n$ es monótona creciente, tenemos que todos los elementos "posteriores" a $a_{n_0}$ cumplen con lo siguiente:

- $\forall a_n>a_{n_0}: a_n\in [a_{n_0}, L]$

Por lo tanto, a partir de $n_0$, se cumple que $a_n\in(L-\varepsilon, L]$, como queríamos probar.

**Observación:** De forma análoga tenemos que toda sucesión mónotona decreciente acotada inferiormente tiene límite.