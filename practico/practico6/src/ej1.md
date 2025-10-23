# Ejercicio 1

## Consigna

1. Investigar si las siguientes funciones de $\mathbb{R}^2$ en $\mathbb{R}$ son normas:

    1. $N(x, y) = |x| + |y|$  
    2. $N(x, y) = \sqrt{x^2 + y^2}$  
    3. $N(x, y) = \max\{|x|, |y|\}$  
    4. $N(x, y) = |x + y|$

2. Para aquellas que sean normas, dibujar la bola de centro en el origen y radio 1. Indicar cuáles de los siguientes puntos pertenecen a la bola de centro $(3, 4)$ y radio 2: $(3, 4)$, $(4, 5)$, $(0, 1)$.

3. Decimos que dos normas $N_1, N_2$ son equivalentes si existen constantes $\alpha, \beta > 0$ tales que:

    - $\alpha N_1(u) \le N_2(u) \le \beta N_1(u)$.

    Probar que aquellas funciones que son normas de este ejercicio son equivalentes dos a dos.

## Resolución

### Recordatorio

Decimos que una función $\|\cdot\|:\mathbb{R}^n\to\mathbb{R}$ es una *norma* si verifica las siguientes tres propiedades:

1. $\|x\|\geq0$, y $\|x\|=0$ solamente si $x=0$.
2. $\|\lambda x\|=|\lambda|\|x\|$, para todo $\lambda\in\mathbb{R}$
3. $\|x+y\|\leq\|x\|+\|y\|$ que se denomina la desigualdad triangular

### Parte 1

#### Norma #1

- $N(x,y)=|x|+|y|$

1. Cumple con esta propiedad pues se están sumando dos valores siempre positivos. La única forma de que sea 0 es que ambos sean 0.
2. Queremos verificar que $N(\lambda x,\lambda y)=|\lambda|N(x,y)$, es decir:
    - $|\lambda x| + |\lambda y|=|\lambda|(|x|+|y|)$
    
    Esto también se cumple, pues es el resultado de sacar factor común $|\lambda|$
3. Queremos verificar que $N(x_1+x_2,y_1+y_2)\leq N(x_1,y_1)+N(x_2,y_2)$, es decir:
    - $|x_1+x_2| + |y_1+y_2| \leq |x_1|+|y_1|+|x_2|+|y_2|$

Concluyendo, la función es una norma.

#### Norma #2

- $N(x, y) = \sqrt{x^2 + y^2}$

Es claramente una norma, es la norma euclidea en $\mathbb{R}^2$.

#### Norma #3

- $N(x, y) = \max\{|x|, |y|\}$

Es claramente una normal, es la norma infinito en $\mathbb{R}^2$

#### Norma #4

- $N(x, y) = |x + y|$

1. Esta propiedad no se cumple, veamos un contraejemplo:
    - $(x,y)=(1,-1)$

    Por lo tanto $N(1,-1)=0$, sin embargo $(1,-1)\neq(0,0)$

Concluyendo, la función NO es una norma.

### Parte 2

Esta parte consiste en gráficar, por lo que se va a saltear. De todos modos en el teórico se ve en detalle la bola abierta para cada una de las normas vistas.

### Parte 3

Decimos que dos normas $N_1, N_2$ son equivalentes si existen constantes $\alpha, \beta > 0$ tales que:

- $\alpha N_1(u) \le N_2(u) \le \beta N_1(u)$.

Trabajaremos con estas normas:

1. $N_1(x, y) = |x| + |y|$  
2. $N_2(x, y) = \sqrt{x^2 + y^2}$  
3. $N_3(x, y) = \max\{|x|, |y|\}$

Como la efectivamente la relación es de equivalencia, bastará con probar que:

- $N_1\sim N_3$
- $N_2\sim N_3$

Consideremos $(x,y)\in\mathbb{R}^2$ cualquiera, y supongamos que $x\geq y$ (sin perder generalidad). Entonces $N_3(x,y)=|x|$.

**Caso $N_1\sim N_3$**:

Queremos probar que:

- $\alpha(|x|+|y|)\leq |x|\leq\beta(|x|+|y|)$

Notemos que con $\alpha=\frac{1}{2};\beta=1$ se cumple la desigualdad.

**Caso $N_2\sim N_3$**:

Queremos probar que:

- $\alpha\sqrt{x^2+y^2}\leq|x|\leq\beta\sqrt{x^2+y^2}$

Operemos un poco:

$$
\alpha\sqrt{x^2+y^2}\leq\alpha\sqrt{x^2+x^2}\leq\sqrt{2}\alpha|x|\leq^?|x|\leq^?\beta\sqrt{x^2+y^2}
$$

Entonces, esto último se cumple para:

- $\alpha=\frac{1}{\sqrt{2}}$
- $\beta=1$

**Conclusión:** Las normas son equivalentes dos a dos.