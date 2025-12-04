# Ejercicio 8

## Consigna

Existe alguna función $f:\mathbb{R}^2\to\mathbb{R}$ de clase $C^2$ tal que $f_x(x,y)=e^{x+y}$ y $f_y(x,y)=\cos(xy)$?

## Resolución

Notemos que la función es de clase $C^2$. Esto significa que es dos veces diferenciable, y hasta sus derivadas segundas son todas funciones continuas.

Entonces estamos en las hipótesis de Schwarz, por lo que se tiene que cumplir que $f_{xy}(x,y)=f_{yx}(x,y)$. Verifiquemos:

- $f_{xy}=e^{x+y}$
- $f_{yx}=-y\sin(xy)$

Claramente son funciones diferentes, por lo tanto es imposible que exista una función $f$ con tales características.