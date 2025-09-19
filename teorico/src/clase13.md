# CLASE 13 - 18/09/2025

## Series

### Proposición 3.40 (criterio de equivalentes)

Sean $\sum a_n,\sum b_n$ dos series de términos positivos.

- Si $\lim\frac{a_n}{b_n}=L>0$, entonces las dos series son de la misma clase (es decir que o ambas son convergentes, o ambas divergentes).
- Si $\lim\frac{a_n}{b_n}=0$, entonces si $\sum b_n$ converge, $\sum a_n$ converge también

#### Demostración

**Primera parte:**

Supongamos que $\lim \frac{a_n}{b_n}=L>0$. Entonces, tomando $\varepsilon:=\frac{L}{2}$, a partir de un $n_0$, tenemos que:

$$
\begin{aligned}
&\frac{L}{2}\leq\frac{a_n}{b_n}\leq\frac{3L}{2}\\
&\iff\scriptstyle{(\text{multiplico por }b_n\geq0)}\\
&\frac{L}{2}b_n\leq a_n\leq\frac{3L}{2}b_n\\
\end{aligned}
$$

A partir de esto nomenclamos las desigualdades de la siguiente forma:

- $\frac{L}{2}b_n\leq a_n\quad(*_1)$
- $a_n\leq\frac{3L}{2}b_n\quad(*_2)$

Tengamos presente lo siguiente:

- Si $b_n$ converge, también lo hace $\frac{L}{2}b_n$
- Si $b_n$ converge, también lo hace $\frac{3L}{2}b_n$

Entonces usando el criterio de comparación, podemos llegar a:

- Si $b_n$ converge, entonces $a_n$ converge, utilizando $(*_2)$
- Si $b_n$ diverge, entonces $a_n$ diverge, utilizando $(*_1)$

**Segunda parte:**

Es análoga a la primera, pero sin considerar la primera igualdad $(*_1)$

#### Conclusión

Con este resultado entonces, para estudiar la convergencia de una serie, basta estudiar una serie cuyo término general sea equivalente. Así, cualquier serie cuyo término general $a_n$ sea un cociente de polinomios será muy fácil de calcular.

### Ejemplos

#### Ejemplo 1

Como $\frac{1}{n^2}\sim\frac{1}{n(n+1)}$, y sabemos que la serie $\sum\frac{1}{n(n+1)}$ converge.

#### Ejemplo 2

Si $\alpha>2$, entonces $\frac{1}{n^{\alpha}}\leq\frac{1}{n^2}$, y como vimos que la serie $\sum\frac{1}{n^2}$ converge, por el criterio de comparación podemos concluir que $\sum\frac{1}{n^{\alpha}}$ también converge.
De esta forma, solo nos queda el sector con $\alpha\in(1,2)$ sin clasificar para esta serie.

#### Ejemplo 3

La serie $\sum\sin(\frac{1}{n})$ es divergente pues $\sin(\frac{1}{n})\sim\frac{1}{n}$ y tenemos que $\sum\frac{1}{n}$ es divergente.

#### Ejemplo 4

La serie $\sum\frac{1}{\sqrt{n(n+2)}}$ es divergente pues el término general es equivalente a $\frac{1}{n}$

#### Ejemplo 5

La serie $\sum\frac{1}{\sqrt{n(n+1)(n+2)(n+3)}}$ es convergente pues el término general es equivalente a $\frac{1}{n^2}$

### Criterio del cociente (o criterio de D'Alambert)

Sea $\sum a_n$ una serie de términos positivos, tal que existe $\lim_{n\to\infty}\frac{a_{n+1}}{a_n}=L$. Entonces:

- Si $L<1$ entonces $a_n$ converge.
- Si $L>1$ entonces $a_n$ diverge.

#### Demostración

**CASO 1 $(L<1)$:**

Observemos que por definición de límite, podemos llegar a la siguiente desigualdad a partir de un cierto $n_0\in\mathbb{N}$:

$$
\frac{a_{n+1}}{a_n}<k<1
$$

**Observación:** Esto lo hacemos tomando $\varepsilon:=\frac{1-L}{2}>0$ por ejemplo.

Entonces, tenemos este resultado $\forall n>n_0$, que se puede simplificar en:

- $a_n<ka_{n-1}$

Y esto se puede usar recursivamente hasta $n_0$:

$$
a_n<ka_{n-1}<k^2a_{n-2}<k^3a_{n-3}<\ldots<k^{n-n_0}a_{n_0}
$$

Y ahora podemos simplificar en:

$$
\begin{aligned}
&k^{n-n_0}a_{n_0}\\
&=\\
&\frac{k^n}{k^{n_0}}a_{n_0}\\
&=\\
&\frac{a_{n_0}}{k^{n_0}}k^n\\
\end{aligned}
$$

Como tenemos que $0<k<1$, tenemos que $\sum k^n$ es convergente, y por el criterio de comparación, también lo hace $\sum a_n$.

**CASO 2 $(L>1)$:**

Observemos que por definición de límite, podemos llegar a la siguiente desigualdad a partir de un cierto $n_0\in\mathbb{N}$:

$$
\frac{a_{n+1}}{a_n}>k>1
$$

**Observación:** Esto lo hacemos tomando $\varepsilon:=\frac{L-1}{2}>0$ por ejemplo.

Entonces, tenemos este resultado $\forall n>n_0$, que se puede simplificar en:

- $a_{n+1}>ka_n$

Y además como $k>1$, tenemos que:

- $a_{n+1}>ka_n>a_n$

Y como este resultado vale $\forall n>n_0$, la serie $\sum a_n$ diverge, pues a partir de $n_0$ su término general es estrictamente creciente.

### Ejemplos 3.43

#### Ejemplo 1

Estudiemos la serie $\sum \frac{n!}{n^n}$. Utilicemos el criterio del cociente:

$$
\begin{aligned}
&\lim_{n\to\infty}\frac{(n+1)!}{(n+1)^{n+1}}\cdot \frac{n^n}{n!}\\
&=\\
&\lim_{n\to\infty}\frac{\bcancel{(n+1)}\cancel{n!}}{(n+1)^{n+\bcancel{1}}}\cdot \frac{n^n}{\cancel{n!}}\\
&=\\
&\lim_{n\to\infty}\frac{n^n}{(n+1)^n}\\
&=\\
&\lim_{n\to\infty}\left(\frac{n}{n+1}\right)^n\\
&=\\
&\lim_{n\to\infty}\left(\frac{n}{n(1+\frac{1}{n})}\right)^n\\
&=\\
&\lim_{n\to\infty}\frac{1}{(1+\frac{1}{n})^n}\\
&=\\
&\frac{1}{e}
\end{aligned}
$$

La última igualdad es un resultado teórico de sucesiones.

#### Ejemplo 2

Estudiemos la serie $\sum \frac{2^n}{n!}$. Utilicemos el criterio del cociente:

$$
\begin{aligned}
&\lim_{n\to\infty} \frac{2^{n+1}}{(n+1)!}\cdot\frac{n!}{2^n}\\
&=\\
&\lim_{n\to\infty} \frac{\bcancel{2^n}2}{(n+1)\cancel{n!}}\cdot\frac{\cancel{n!}}{\bcancel{2^n}}\\
&=\\
&\lim_{n\to\infty} \frac{2}{n+1}\\
&=\\
&0
\end{aligned}
$$