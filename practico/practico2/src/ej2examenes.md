# Ejercicio 2 - Evaluaciones anteriores

## Consigna

Consideremos la siguiente ecuación diferencial (E) dependiendo de una función $r(x)$:

$$
y''+4y'+4y=r(x)
$$

y las siguientes afirmaciones:

**(I)** Si $e^{-2x} + x^2$ es solución de (E) entonces $r(x) = 4x^2 + 8x + 2$.

**(II)** Si $r(x) = x^2$ entonces $y(x) = e^{-2x} + 3xe^{-2x} + x^2$ es la única solución de (E) que verifica que $y(0) = y'(0) = 1$.

**(III)** Si $r(x) = 0$ entonces todas las soluciones son de la forma $y(x) = ae^{-2x} + be^{-2x}x$ con $a,b \in \mathbb{R}$.

Entonces:

(A) Todas las afirmaciones son verdaderas.  
(B) Solamente (III) es verdadera.  
(C) Solamente (I) es verdadera.  
(D) Solamente (I) y (III) son verdaderas.

## Resolución

La estrategia es simple, vayamos afirmación por afirmación y notemos sus implicancias:

### Afirmación #1

- Si $e^{-2x}+x^2$ es solución de (E) entonces $r(x)=4x^2+8x+2$.

Para esta afirmación tenemos que reemplazar en la ecuación la función y sus derivadas, por lo tanto:

- $y(x)=e^{-2x}+x^2$
- $y'(x)=-2e^{-2x}+2x$
- $y''(x)=4e^{-2x}+2$

$$
\begin{aligned}
&y''+4y'+4y\\
&=\scriptstyle{(\text{reemplazando lo conocido})}\\
&4e^{-2x}+2+4(-2e^{-2x}+2x)+4(e^{-2x}+x^2)\\
&=\scriptstyle{(\text{operatoria})}\\
&\cancel{4e^{-2x}}+2-\cancel{8e^{-2x}}+8x+\cancel{4e^{-2x}}+4x^2\\
&=\scriptstyle{(\text{operatoria})}\\
&4x^2+8x+2
\end{aligned}
$$

Por lo tanto $r(x)=4x^2+8x+2$, esto significa que la afirmación es **VERDADERA**.

### Afirmación #2

- Si $r(x) = x^2$ entonces $y(x) = e^{-2x} + 3xe^{-2x} + x^2$ es la única solución de (E) que verifica que $y(0) = y'(0) = 1$.

Esta afirmación nos va a costar un poco más de trabajo, ya que no hay forma de saber si esa es la única solución que no sea encontrando nosotros la solución...

Por lo tanto el problema que se nos plantea es hallar la solución general de:

- $y''+4y'+4y=x^2$

Separamos en homogénea y no homogénea:

- $(H)\quad y''+4y'+4y=0$
- $(NH)\quad y''+4y'+4y=x^2$

#### Homogénea

- $y''+4y'+4y=0$

Planteamos el polinomio característico y hallamos sus raíces con Bháskara:

- $\lambda^2+4\lambda+4=0$

$$
\begin{aligned}
&\lambda=\frac{-4\pm\sqrt{16-16}}{2}\\
&\iff\scriptstyle{(\text{operatoria})}\\
&\lambda=-2
\end{aligned}
$$

Concluimos que tenemos raíz doble en $\lambda=-2$, por lo que la forma general de la solución de la homogénea es:

- $y_H(x)=K_1e^{-2x}+K_2xe^{-2x}$

#### No homogénea

- $y''+4y'+4y=x^2$

Buscamos una solución polinómica, de la siguiente forma:

- $y(x)=Ax^2+Bx+C$
- $y'(x)=2Ax+B$
- $y''(x)=2A$

Con esto podemos reemplazar en la ecuación y obtener un sistema de ecuaciones:

$$
\begin{aligned}
&2A+4(2Ax+B)+4(Ax^2+Bx+C)=x^2\\
&\scriptstyle{(\text{separando por órdenes})}\\
&4Ax^2+(8A+4B)x+(2A+4B+4C)=x^2
\end{aligned}
$$

De esto se desprende el siguiente sistema:

$$
\left(
\begin{array}{ccc|c}
4&0&0&1\\
8&4&0&0\\
2&4&4&0\\
\end{array}
\right)
$$

De esto se obtiene que:

- $A=\frac{1}{4}$
- $B=-\frac{1}{2}$
- $\frac{1}{2}-2=-4C\implies C=\frac{3}{8}$

Esto nos da la siguiente solución particular:

- $y_P(x)=\frac{1}{4}x^2-\frac{1}{2}x+\frac{3}{8}$

Que es claramente diferente a $x^2$, por lo tanto, la solución $y(x) = e^{-2x} + 3xe^{-2x} + x^2$ no puede ser la única función que cumple con las condiciones indicadas... De hecho, es posible que ni siquiera sea una solución. Verifiquemos esto último para quedarnos tranquilos.

- $y(x) = e^{-2x} + 3xe^{-2x} + x^2$
- $y'(x)=-2e^{-2x}-6xe^{-2x}+2x$

Ojo, miremos la derivada primera, claramente cuando $x=0$, $y(0)=-2$ que es claramente distinto a $y(0)=1$ que es la condición que queremos verificar.

Con esto podemos concluir que esta afirmación es **FALSA**.

### Afirmación #3

- Si $r(x) = 0$ entonces todas las soluciones son de la forma $y(x) = ae^{-2x} + be^{-2x}x$ con $a,b \in \mathbb{R}$.

Esta afirmación ya la podíamos responder mientras trabajabamos en la segunda, ya que corresponde a la solución general de la homogénea que hallamos:

- $y_H(x)=K_1e^{-2x}+K_2xe^{-2x}$

Como estas coinciden, concluimos que esta afirmación es **VERDADERA**.

### Conclusión

La respuesta correcta es:

- (D) Solamente (I) y (III) son verdaderas.