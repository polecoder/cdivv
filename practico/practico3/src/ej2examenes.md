# Ejercicio 2 (evaluaciones anteriores)

## Consigna

Consideremos las siguientes sucesiones de números reales:

- $a_n = \frac{\sqrt{n}}{n + 2} \quad (n \geq 2)$
- $b_n = \frac{1}{n \ln(n) (\ln(\ln(n)))^2} \quad (n \geq 3)$

1. Para la sucesión $(a_n)$, estudiar su monotonía y convergencia.  
2. Para la sucesión $(b_n)$, estudiar su monotonía y convergencia.

## Resolución

### Parte 1

- $a_n = \frac{\sqrt{n}}{n+2} \quad (n \geq 2)$

Veremos si la sucesión es monotona estudiando términos consecutivos, consideremos $a_{n+1}$:

- $a_{n+1}=\frac{\sqrt{n+1}}{n+3}$

Comparemos:

$$
\begin{aligned}
&a_n\geq a_{n+1}\\
&\iff\scriptstyle{(\text{reemplazando por la definición})}\\
&\frac{\sqrt{n}}{n+2}\geq\frac{\sqrt{n+1}}{n+3}\\
&\iff\scriptstyle{(\text{operatoria})}\\
&\sqrt{n}(n+3)\geq\sqrt{n+1}(n+2)\\
&\iff\scriptstyle{(\text{operatoria})}\\
&n\sqrt{n}+3\sqrt{n}\geq n\sqrt{n+1}+2\sqrt{n+1}\\
&\iff\scriptstyle{(\text{operatoria})}\\
&3\sqrt{n}\geq 2\sqrt{n+1}\\
&\iff\scriptstyle{(\text{operatoria})}\\
&9n\geq 4(n+1)\\
&\iff\scriptstyle{(\text{operatoria})}\\
&9n\geq 4n+4\\
&\iff\scriptstyle{(\text{operatoria})}\\
&n\geq \frac{4}{5}\\
\end{aligned}
$$

Que es claramente cierto pues estamos considerando $n\geq 2$.

Además es convergente y su límite es cero:

$$
\begin{aligned}
&\lim_{n\to+\infty}\frac{\sqrt{n}}{n+2}\\
&=\scriptstyle{(\text{equivalencia})}\\
&\lim_{n\to+\infty}\frac{\sqrt{n}}{n}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{n\to+\infty}\frac{1}{\sqrt{n}}\\
&=\scriptstyle{(\text{operatoria})}\\
&0
\end{aligned}
$$

### Parte 2

- $b_n = \frac{1}{n \ln(n) (\ln(\ln(n)))^2} \quad (n \geq 3)$

Notemos que para $n\geq 3$:

- $\ln(n)$ es estrictamente creciente y positiva, por lo tanto:
- $\ln(\ln(n))$ también es estrictamente creciente y positiva, por lo tanto:
- $(\ln(\ln(n)))^2$ también es estrictamente creciente y positiva.

Por otra parte, $n\ln(n)$ también es estrictamente creciente y positiva, así que tomando el producto entre estas dos sucesiones, el resultado es otra sucesión estrictamente creciente y positiva.
Por lo tanto tomando el inverso, tenemos que la función es estrictamente decreciente.
Además, la función está acotada inferiormente (por cero), por lo tanto como es monótona y acotada tiene límite.