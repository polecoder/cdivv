# Ejercicio 2 (evaluaciones anteriores)

## Consigna

La serie $\sum_{n=0}^{+\infty}\left(\frac{1}{3^n}+e^{-(n+1)^2}-e^{-n^2}\right)$

(A) converge a $\tfrac{3}{2}$.
(B) converge a $\tfrac{1}{2}$.
(C) converge a $1$.
(D) converge a $3 - e$.
(E) diverge.

## Resolución

- $\sum_{n=0}^{+\infty}\left(\frac{1}{3^n}+e^{-(n+1)^2}-e^{-n^2}\right)$

Notemos que podemos separar la serie en:

- $\sum_{n=0}^{+\infty}\frac{1}{3^n}+\sum_{n=0}^{+\infty}e^{-(n+1)^2}-e^{-n^2}$

Entonces para calcular el límite tenemos en cuenta que:

- La primera serie es geométrica, por lo tanto converge a $\frac{3}{2}$.
- Por otra parte la segunda es telescópica, al desarrollarse obtenemos que su reducida enésima es:

    - $s_n=e^{-(n+1)^2}-e^{0}$

Por lo tanto el límite de esta es $-1$.

Por álgebra de límites, concluimos que la serie original converge a $\frac{3}{2}-1=\frac{1}{2}$.
Entonces la respuesta correcta es:

(B) converge a $\tfrac{1}{2}$.