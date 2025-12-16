# Ejercicio 2 (evaluaciones anteriores)

## Consigna

Considere la siguiente integral impropia:

$$
\int_{2}^{+\infty}
\frac{1+e^{-x}}{\log(x)\bigl(1+x\log^{\alpha}(x)\bigr)} dx
$$

Entonces:

(A) La integral es divergente para todo $\alpha \in \mathbb{R}$.
(B) La integral es convergente si y solo si $\alpha < 1$.
(C) La integral es convergente para todo $\alpha \in \mathbb{R}$.
(D) La integral es convergente si y solo si $\alpha > 0$.
(E) La integral es convergente si y solo si $\alpha > 1$.

## Resolución

Notemos que no tenemos impropiedades de segunda especie en esta integral, pues no hay ningún valor de $x$ para el cual se genere una indeterminación, por lo tanto tenemos que poner nuestro foco en que pasa en el infinito.

Notemos que para el infinito, tenemos una equivalencia para la función $f(x)$:

$$
\begin{aligned}
&\lim_{n\to+\infty}\frac{1+e^{-x}}{\log(x)\bigl(1+x\log^{\alpha}(x)\bigr)}\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{n\to+\infty}\frac{1}{x\log^{\alpha+1}(x)}\\
\end{aligned}
$$

Por lo tanto, podemos calcular una primitiva para esta integral para resolver el problema:

$$
\begin{aligned}
&\int_2^{+\infty}\frac{1+e^{-x}}{\log(x)\bigl(1+x\log^{\alpha}(x)\bigr)}dx\\
&=\scriptstyle{(\text{por la observación anterior})}\\
&\int_2^{+\infty}\frac{1}{x\log^{\alpha+1}(x)}dx\\
&=\scriptstyle{(\text{cambio de variable: }u=\log(x);du=\frac{1}{x}dx)}\\
&\int_2^{+\infty}\frac{1}{u^{\alpha+1}}du\\
&=\scriptstyle{(\text{operatoria})}\\
&\frac{u^{-\alpha}}{-\alpha}\Big|^{+\infty}_2\\
&=\scriptstyle{(\text{deshaciendo el cambio de variable})}\\
&\frac{\log^{-\alpha}(x)}{-\alpha}\Big|^{+\infty}_2\\
&=\scriptstyle{(\text{operatoria})}\\
&\lim_{x\to+\infty}\frac{\log^{-\alpha}(x)}{-\alpha}-\frac{\log^{-\alpha}(2)}{-\alpha}\\
\end{aligned}
$$

Donde el término que determina la convergencia es el límite, el cual existe sii $\alpha>0$.

Por otro lado, si $\alpha<0$ el límite claramente diverge, mientras que si $\alpha=0$ la primitiva es diferente, exactamente $\log(x)$ (que también es divergente).

Concluyendo, la respuesta correcta es:

(D) La integral es convergente si y solo si $\alpha > 0$.