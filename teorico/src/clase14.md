# CLASE 14 - 22/09/2025

## Series de términos positivos

### Criterio de la raíz enésima (de Cauchy)

Sea $\sum a_n$ una serie de términos positivos, tal que existe $\lim_{n\to\infty} \sqrt[n]{a_n}=L$. Entonces:

- Si $L<1$, entonces $a_n$ converge.
- Si $L>1$, entonces $a_n$ diverge.

#### Demostración

**CASO 1 $(L<1)$:**

Observemos que por definición de límite, podemos llegar a la siguiente desigualdad a partir de un cierto $n_0\in\mathbb{N}$:

$$
\sqrt[n]{a_n}<k<1
$$

**Observación:** Esto lo hacemos tomando $\varepsilon:=\frac{1-L}{2}>0$ por ejemplo.

Despejando, llegamos a:

- $a_n<k^n$

Observando que $k^n$ converge pues es una serie geométrica y $k<1$, por el criterio de comparación tenemos que:

- $a_n$ converge.

**CASO 2 $(L>1)$:**

Observemos que por definición de límite, podemos llegar a la siguiente desigualdad a partir de un cierto $n_0\in\mathbb{N}$:

$$
\sqrt[n]{a_n}>k>1
$$

**Observación:** Esto lo hacemos tomando $\varepsilon:=\frac{L-1}{2}>0$ por ejemplo.

Despejando, llegamos a:

- $a_n>k^n$

Observando que $k^n$ diverge pues es una serie geométrica y $k>1$, por el criterio de comparación tenemos que:

- $a_n$ diverge.

#### Ejemplos 3.45

##### Ejemplo 1

- $\sum (\frac{\log(n)}{n})^n$ es convergente pues:
    - $\lim\sqrt[n]{a_n}=(\frac{\log(n)}{n})^n=\lim\frac{log(n)}{n}=0$

##### Ejemplo 2

- $\sum\frac{n^5}{2^n}$ es convergente pues:
    - $\lim\sqrt[n]{a_n}=\lim\sqrt[n]{\frac{n^5}{2^n}}=\frac{1}{2}$

**Observación:** Podemos expandir sobre este último límite:

$$
\begin{aligned}
&\lim\sqrt[n]{\frac{n^5}{2^n}}\\
&=\\
&\lim\frac{n^{\frac{5}{n}}}{2}\\
&=\\
&\frac{1}{2}\lim n^{\frac{5}{n}}\\
&=\\
&\frac{1}{2}\lim e^{\log(n^{\frac{5}{n}})}\\
&=\\
&\frac{1}{2}\lim e^{\frac{5}{n}\log(n)}\\
&=\\
&\frac{1}{2}\lim e^{\frac{5\log(n)}{n}}\\
&=\\
&\frac{1}{2}e^0\\
&=\\
&\frac{1}{2}\\
\end{aligned}
$$

## Series alternadas

En esta breve sección estudiaremos funciones que no necesariamente son de signos constantes.

### Definición 3.46

Decimos que una serie $\sum a_n$ es absolutamente convergente sii $\sum |a_n|$ es convergente.

Intuitivamente, si una serie es absolutamente convergente, debería ser convergente también $\sum a_n$, pues sumar el valor absoluto de los términos es de alguna forma el "peor caso". Veamos de formalizar este resultado.

### Teorema 3.47

Toda serie absolutamente convergente es convergente.

#### Demostración

Sea $\sum a_n$ la serie absolutamente convergente, y separemos los términos $a_n$ en los positivos y negativos, formando así dos nuevas sucesiones:

$$
a_n^+=\begin{cases}a_n\quad\text{si }a_n\geq0\\0\quad\text{si }a_n<0\end{cases}
\text{ y }
a_n^-\begin{cases}0\quad\text{si }a_n\geq0\\-a_n\quad\text{si }a_n<0\end{cases}
$$

Es decir, en $a_n^+$ ponemos los términos positivos de $a_n$, y los negativos los cambiamos por 0. Mientras que en $a_n^-$ cambiamos los términos positivos por 0, y ponemos los términos negativos de $a_n$ cambiados de signo.
De esta forma ambas las nuevas sucesiones son de términos positivos.

Observemos que:

- $a_n=a_n^+-a_n^-$
- $|a_n|= a_n^++a_n^-$
- $0\leq a_n^+\leq |a_n|$
- $0\leq a_n^-\leq |a_n|$

Por hipótesis, tenemos que $\sum |a_n|$ converge, y por lo tanto usando el criterio de comparación:

- $\sum a_n^+$ es convergente.
- $\sum a_n^-$ es convergente.

Con esto podemos concluir que:

- $\sum (a_n^+-a_n^-)=\sum a_n$ es convergente

### Ejemplo 3.48

- $\sum \frac{\sin(n)}{n^2}$

Queremos estudiar si es absolutamente convergente, por lo tanto queremos estudiar:

- $\sum |\frac{\sin(n)}{n^2}|$

Veamos lo siguiente:

- $\frac{|\sin(n)|}{n^2} \leq \frac{1}{n^2}$

Y como $\sum\frac{1}{n^2}$ es convergente, por criterio de comparación también lo es $\sum\frac{|\sin(n)|}{n^2}$.

Veremos a continuación el único criterio de convergencia para series alternadas, el cual no vamos a demostrar.

### Proposición 3.49 (criterio de Leibnitz)

Si $a_n$ es una sucesión monótona decreciente que tiende a 0, entonces la serie alternada $\sum(-1)^na_n$ es convergente.

#### Ejemplo 3.50

##### Ejemplo 1

- $\sum(-1)^n\frac{1}{n}$

Es convergente por el criterio de Leibnitz, pero no es absolutamente convergente, pues:

- $\sum|(-1)^n\frac{1}{n}|=\sum\frac{1}{n}$

Que ya vemos que es divergente.

##### Ejemplo 2

- $\sum(-1)^n\log(1+\frac{1}{n})$

Es convergente por el criterio de Leibnitz.