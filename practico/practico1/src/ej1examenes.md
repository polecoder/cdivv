# Ejercicio 1 (evaluaciones anteriores)

## Consigna



Considere las soluciones de la siguiente ecuación en los números complejos:

- $z^3 = 4\overline{z}$

Entonces:

(A) La ecuación tiene 5 soluciones, una sola de ellas con parte imaginaria nula.  
(B) La ecuación tiene 4 soluciones, y el producto de ellas es $i$.  
(C) La ecuación tiene 5 soluciones, tres de ellas con parte imaginaria nula.  
(D) La ecuación tiene 3 soluciones, una real pura y dos complejas conjugadas.  
(E) La ecuación tiene 3 soluciones, la suma de ellas da cero.

## Resolución

Usemos notación polar para representar mejor este problema, con esto obtenemos que:

- $z=\rho e^{i\theta}$, entonces:
    - $4\overline{z}=4\rho e^{-i\theta}$
    - $z^3=\rho^3e^{3i\theta}$

Con esto igualamos módulo y ángulo teniendo en cuenta la ecuación original:

- $\rho^3=4\rho$
- $-\theta=3\theta+2k\pi$

Operemos con ambas para ver que se obtiene:

$$
\rho^3=4\rho\implies\rho^2=4\implies\rho=2
$$

$$
-\theta=3\theta+2k\pi\implies-4\theta=2k\pi\implies\theta=-\frac{k\pi}{2}
$$

Entonces veamos que sucede con el ángulo para ver cuando se empieza a repetir:

- $k=0\implies\theta=0$
- $k=1\implies\theta=-\frac{\pi}{2}$
- $k=2\implies\theta=-\pi$
- $k=3\implies\theta=-\frac{3\pi}{2}$
- $k=4\implies\theta=-2\pi=0$

Por lo tanto, tenemos cuatro soluciones diferentes para $\rho=2$, donde dos de ellas son imaginarias puras $(k=1,3)$, mientras que las otras dos $(k=0,2)$ son reales.

Ojo... Podríamos ponernos a revisar soluciones ahora, pero nos estamos olvidando de una solución trivial. Que pasa si el módulo es $0$? De hecho esta es otra solución.

Por lo tanto tenemos cinco soluciones, estamos entre la respuesta A y la respuesta C, pero sabemos que hay dos soluciones con la parte imaginaria nula, si a esto le sumamos la que tiene módulo cero, tenemos que la respuesta correcta es la C.