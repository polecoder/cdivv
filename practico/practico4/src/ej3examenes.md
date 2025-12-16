# Ejercicio 3 (evaluaciones anteriores)

## Consigna

Sea $(a_n)$ una sucesión de términos positivos tal que $\sum a_n$ es convergente. Considere las siguientes series:

- $\sum_{n=1}^{+\infty} e^{a_n^2}-1$
- $\sum_{n=1}^{+\infty} \cos(a_n)\,\sin(a_n)$

Entonces:

(A) Ambas series son divergentes.  
(B) Ambas series son convergentes.  
(C) Solo la primera serie es convergente.  
(D) Solo la segunda serie es convergente.  
(E) La segunda serie no se puede clasificar a priori, por no ser de signo constante.

## Resolución

Sabemos que $\sum a_n$ es convergente, sea $L$ el valor al que converge la serie.

### Serie #1

- $\sum_{n=1}^{+\infty} e^{a_n^2}-1$

Recordando que si $u\to0$ entonces $e^u-1\sim u$ por Taylor, tenemos entonces que el término general es equivalente a $a_n^2$. Podemos aplicar entonces el criterio de equivalentes:

$$
\begin{aligned}
&\lim_{n\to+\infty}\frac{e^{a_n^2}-1}{a_n}\\
&=\scriptstyle{(\text{por la observación que hicimos})}\\
&\lim_{n\to+\infty}\frac{a_n^2}{a_n}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{n\to+\infty}a_n\\
&\scriptstyle{(\text{como }\sum a_n\text{ es convergente})}\\
&0
\end{aligned}
$$

Por el criterio de equivalentes, tenemos que:

- Como $\sum a_n$ es convergente, entonces $\sum a_n^2$ también es convergente.

Concluimos que entonces la serie original es convergente.

### Serie #2

- $\sum_{n=1}^{+\infty} \cos(a_n)\sin(a_n)$

Notemos que $\cos(a_n)\leq 1$ para cualquier valor de $a_n$, por lo tanto tenemos que:

- $\cos(a_n)\sin(a_n)\leq\sin(a_n)$

Además, por Taylor se tiene que cuando $u\to0$, entonces $\sin u\sim u$, entonces tenemos que:

- $\sum_{n=1}^{+\infty} \cos(a_n)\sin(a_n)\leq\sum_{n=1}^{+\infty} a_n$

Y como la segunda serie converge, la primera también lo hace por el criterio de comparación.