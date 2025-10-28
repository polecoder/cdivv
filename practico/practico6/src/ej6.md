# Ejercicio 6

## Consigna

Probar los siguientes resultados:

1. $A$ es abierto si y sólo si $A \cap \partial A = \emptyset$.
2. $\mathring{A} = \overline{A} - \partial A$ es un conjunto abierto; más aún, es la unión de los subconjuntos abiertos contenidos en $A$.
3. $A$ es cerrado si y sólo si $\partial A \subseteq A$ si y sólo si $A' \subseteq A$.
4. $\overline{A} = A \cup \partial A$ es un conjunto cerrado; más aún, es la intersección de todos los conjuntos cerrados que contienen a $A$.
5. $A'$ es un conjunto cerrado.

## Resolución

### Parte 1

- $A$ es abierto si y sólo si $A \cap \partial A = \emptyset$.

#### Directo $(\rightarrow)$

(H) $A$ es abierto
(T) $A\cap\partial A=\emptyset$

Supongamos que $A\cap\partial A\neq\emptyset$, consideremos $p\in A\cap\partial A$, esto signfica que $p\in A$ y además $p\in\partial A$.
Por lo tanto:

- $(p\in \partial A):\forall\delta>0: B(p,\delta)\cap A\neq \emptyset\land B(p,\delta)\cap A^C\neq \emptyset$
- $(p\in A):\exists\delta>0: B(p,\delta)\subset A$ ($A$ es abierto)

Por lo que esto es absurdo, pues $B(p,\delta)$ tiene que estar incluido en $A$ y a la vez tener al menos un punto en $A^C$

#### Recíproco $(\leftarrow)$

(H) $A\cap\partial A=\emptyset$
(T) $A$ es abierto

Supongamos que $A$ no es abierto, es decir que existe $p\in A$ tal que $A$ es frontera (pues no puede ser interior).

Esto es directamente absurdo pues por hipótesis $A\cap\partial A=\emptyset$

### Parte 2

- $\mathring{A} = \overline{A} - \partial A$ es un conjunto abierto; más aún, es la unión de los subconjuntos abiertos contenidos en $A$.

Para probar esta parte, verificaremos las siguientes expresiones:

- $\mathring{A}\subseteq \overline{A}-\partial A$
- $\overline{A}-\partial A\subseteq\mathring{A}$

#### Expresión #1

- $\mathring{A}\subseteq \overline{A}-\partial A$

Sea $p\in\mathring{A}$, queremos verificar que $p\in\overline{A}-\partial A$, es decir:

- $p\in\overline{A}$, y
- $p\notin\partial A$

Probemos ambas expresiones:

- $p\in \mathring{A}\to p\in A\to p\in A\cup\partial A\to p\in\overline{A}$
- $p\in\mathring{A}\to p\notin\partial A$ (definición de punto interior)

#### Expresión #2

- $\overline{A}-\partial A\subseteq\mathring{A}$

Sea $p\in \overline{A}-\partial A$, queremos verificar que $p\in\mathring{A}$ es decir:

- $p$ es interior de $A$

Recordemos que como $p\in \overline{A}-\partial A$ se cumple que:

- $p\in\overline{A}$, y
- $p\notin\partial A$

Como $p\notin\partial A$, tenemos que existe algún $\delta_0>0$ tal que $B(p,\delta_0)\cap A^C=\emptyset$.
Por lo tanto, necesariamente $B(p,\delta_0)\subset A$.

Concluimos que $p$ es interior pues se cumple la definición para $\delta_0$.

**Conclusión:** $\overline{A}-\partial A$ es un conjunto abierto pues verificamos que es igual a $\mathring{A}$

### Parte 3

- $A$ es cerrado si y sólo si $\partial A \subseteq A$ si y sólo si $A' \subseteq A$.

Separamos las pruebas en:

- $A$ es cerrado $\leftrightarrow\partial A \subseteq A$
- $A$ es cerrado $\leftrightarrow A' \subseteq A$

Si probamos estas dos, habriamos probado todas las equivalencias.

#### Equivalencia #1

- $A$ es cerrado $\leftrightarrow\partial A \subseteq A$

##### Directo $(\rightarrow)$

(H) $A$ es cerrado
(T) $\partial A \subseteq A$

Supongamos que $\partial A \not\subseteq A$, es decir que existe $p\in\partial A$ tal que $p\notin A$.
Esto significa que $p\in A^C$, por lo tanto esto contradice que $A$ sea cerrado, pues $A^C$ no es abierto (contiene un punto frontera)

Queda probado el directo por absurdo.

##### Recíproco $(\leftarrow)$

(H) $\partial A \subseteq A$
(T) $A$ es cerrado

Suspongamos que $A$ no es cerrado, es decir que $A^C$ no es abierto. Esto significa que existe $p\in A^C$ tal que $p$ es frontera.
Pero esto no puede pasar pues $\forall p\in\partial A, p\in A$ por hipótesis.

Queda probado el recíproco por absurdo.

#### Equivalencia #2

- $A$ es cerrado $\leftrightarrow A' \subseteq A$

Hecho en la clase 20 del teórico.

**Conclusión:** Las tres expresiones son equivalentes.