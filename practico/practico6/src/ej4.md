# Ejercicio 4

## Consigna

Sean $A$ un conjunto abierto de $\mathbb{R}^2$ y $C = A \cap (\mathbb{Q} \times \mathbb{Q})$.  
Hallar $\mathring{C}$, $\overline{C}$ y $\partial C$.

## Resolución

Tengamos presente la siguiente afirmación que vale para $x_1,x_2\in\mathbb{R}$ tales que $x_1<x_2$:

- $\exists q\in\mathbb{Q}: x_1\leq q\leq x_2$
- $\exists i\in\mathbb{R\setminus Q}: x_1\leq i\leq x_2$

Que significa que ambos $\mathbb{Q}$ y $\mathbb{R\setminus Q}$ son densos en $\mathbb{R}$.

### Puntos interiores

Trabajemos primero con el conjunto de puntos interiores. Consideremos $p=(p_1,p_2)\in C$ un punto cualquiera de $C$. Queremos verificar si este punto $p$ es interior a $C$, entonces queremos probar que existe un $\delta>0$ tal que:

- $B(p,\delta)\subset A\cap\mathbb{Q}^2$

Pero esto no es posible, ya que para cualquier $\delta>0$ se cumple que:

- $\exists r_1\in\mathbb{R\setminus Q}:p_1-\delta\leq r_1\leq p_1+\delta$
- $\exists r_2\in\mathbb{R\setminus Q}:p_2-\delta\leq r_2\leq p_2+\delta$

Entonces considerando el punto $r=(r_1,r_2)$, tendríamos un punto conformado por coordenadas irracionales dentro de la bola abierta $B(p,\delta)$, lo que nos dice que $p$ no puede ser interior.

**Conclusión:** $\mathring{C}=\emptyset$

### Puntos frontera

Nuevamente consideremos $p=(p_1,p_2)\in A$. Queremos ver si el punto $p$ es frontera de $C$, para esto queremos probar:

- $\forall\delta>0:B(p,\delta)\cap C\neq\emptyset\land B(p,\delta)\cap C^C\neq\emptyset$

Esto es bastante trivial, pues usando la densidad de $\mathbb{Q}$ y $\mathbb{R\setminus Q}$ en $\mathbb{R}$, obtenemos:

- $\exists q_1\in\mathbb{Q}:p_1-\delta\leq q_1\leq p_1+\delta$
- $\exists q_2\in\mathbb{Q}:p_2-\delta\leq q_2\leq p_2+\delta$
- $\exists r_1\in\mathbb{R\setminus Q}:p_1-\delta\leq r_1\leq p_1+\delta$
- $\exists r_2\in\mathbb{R\setminus Q}:p_2-\delta\leq r_2\leq p_2+\delta$

Por lo que considerando $q=(q_1,q_2)$ y $r=(r_1,r_2)$, tenemos que:

- $q\in C$ y $r\in C^C$
- Por construcción, ambos $q,r$ pertenecen a la bola abierta $B(p,\delta)$

**Conclusión:** $p\in A$ es un punto frontera, y como consideramos uno genérico, este razonamiento vale para todo $p\in A$, es decir que $\partial C=A\cup \partial A$

### Clausura de $C$

La clasura de $C$ es por definición:

- $\overline{C}=A\cup\partial C=A\cup\partial A=\overline{A}$
