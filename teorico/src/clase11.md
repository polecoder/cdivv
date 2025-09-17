# CLASE 11 - 15/09/2025

## Sucesiones

### Teorema 3.2.6

Toda sucesión $a_n$ acotada tiene una subsucesión convergente.

#### Demostración

Llamemos $A$ al recorrido de la sucesión $A=\{a_n:n\in\mathbb{N}\}$. Como la sucesión es acotada, el conjunto $A$ es acotado.
Puede ocurrir que $A$ sea finito o infinito.

- Observemos que si $A$ es finito, entonces la sucesión $a_n$ pasa infinitas veces por alguno de sus puntos. Tomando esos índices, construimos una subsucesión que converge a ese elemento.

Por otra parte, si $A$ es infinito, podemos aplicar el teorema 3.2.4, y por lo tanto $A$ tiene un punto de acumulación $L$.

Como $L$ es de acumulación, en cualquier entorno habrá puntos de $a_n$. Tomamos entonces valores sucesivos de radios $\varepsilon_k=\frac{1}{k}$. 
En cada entorno $E^*(L,\varepsilon_k)$ hay un elemento de la sucesión, al que llamaremos $a_{n_k}$. Por construcción, $|a_{n_k}-L|<\varepsilon_k$, y por lo tanto:

- $a_{n_k}\to L$

## Series

### Definición 3.34

Dada una sucesión real $a_n$, se llama suma parcial o reducida enésima a la sucesión $s_n=\sum_{i=1}^n a_i$, y se denomina serie de término general $a_n$ a la suma infinita $\sum a_n$.
Se dice que la serie converge, diverge u oscila, cuando lo hace la sucesión $s_n$. Además, cuando la serie es convergente, al límite $S\in\mathbb{R}$ de $s_n$ se lo denomina la suma de la serie, y se escribe $S=\sum a_n$.
También utilizaremos la notación $\sum a_n<\infty$ para referirnos a que la serie es convergente.

### Ejemplo 3.35

La serie $\sum_{i=1}^\infty q^n$ se denomina serie geométrica. Tenemos que:

- $s_n=1+q^1+q^2+\ldots+q^n$

Múltiplicando por $q$ y restando podemos llegar a lo siguiente:

$$
\begin{aligned}
s_n&=1+\cancel{q^1}+\cancel{q^2}+\ldots+\cancel{q^n}\\
-qs_n&=\cancel{q^1}+\cancel{q^2}+\cancel{q^3}+\ldots+q^{n+1}\\
\hline
s_n(1-q)&=1+q^{n+1}\\
s_n&=\frac{1+q^{n+1}}{1-q}
\end{aligned}
$$

Ahora queremos evaluar $\lim s_n=\lim \frac{1+q^{n+1}}{1-q}$, y para esto distinguimos dos casos:

- $|q|<1: q^{n+1}\to0$, entonces $\lim s_n=\lim \frac{1+q^{n+1}}{1-q}=\frac{1}{1-q}$
- $|q|>1: q^{n+1}$ diverge. Entonces en este caso no tenemos límite.

Faltaría ver el caso $|q|=1$, en el que la serie se convierte en una de las siguientes:

- $\sum 1^n$
- $\sum (-1)^n$

Donde ambas son divergentes.