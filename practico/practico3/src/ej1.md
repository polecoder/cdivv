# Ejercicio 1

## Consigna

Estudiar monotonía, acotación y convergencia de las siguientes sucesiones $(a_n)_{n \in \mathbb{N}}$, donde:

1. $a_n = 1 + \frac{1}{n}$
2. $a_n = 1 + \frac{(-1)^n}{n}$
3. $a_n = n + \frac{1}{n}$
4. $a_n = \frac{n}{\sqrt{n^2 + 1}}$
5. $a_n = \frac{n^2}{2^n}$

## Resolución

### Sucesión #1

- $a_n = 1 + \frac{1}{n}$

- Monotonía: Estrictamente decreciente.
    - Esto porque la sucesión $a_n=\frac{1}{n}$ es estrictamente decreciente, y se está sumando a una función constante.
- Acotación: Acotada.
    - Pues $a_1=2$ y luego decrece hasta casi llegar a 1.
- Convergencia: $\lim_{n\to\infty}1+\frac{1}{n}=1$
    - Por suma de límites.

### Sucesión #2

- $a_n = 1 + \frac{(-1)^n}{n}$

- Monotonía: No es monótona.
    - Tiene términos cada vez más cercanos al uno, pero por arriba y por abajo.
- Acotación: Acotada.
    - Le sumamos/restamos a 1, términos cada vez más pequeños (y acotados).
- Convergencia: $\lim_{n\to\infty}1+\frac{(-1)^n}{n}=1$
    - Por suma de límites.

### Sucesión #3

- $a_n = n + \frac{1}{n}$

- Monotonía: Estrictamente creciente.
    - Pues $a_n=n$ es estrictamente creciente y le estamos sumando 
- Acotación: No acotada
    - Crece hasta infinito.
- Convergencia: $\lim_{n\to\infty}n+\frac{1}{n}=+\infty$
    - Por suma de límites.

### Sucesión #4

- $a_n = \frac{n}{\sqrt{n^2 + 1}}$

- Monotonía: Monotona decreciente.
    - Pues el denominador crece muy ligeramente más rapido que el numerador, por lo tanto la función va decreciendo.
- Acotación: Acotada.
    - Pues empieza en $a_1=\frac{1}{\sqrt{2}}$ y decrece hasta el límite $1$.
- Convergencia:
    $$
    \lim_{n\to\infty}\frac{n}{\sqrt{n^2+1}}=\lim_{n\to\infty}\frac{n}{\sqrt{n^2}}=1
    $$

### Sucesión #5

- $a_n = \frac{n^2}{2^n}$

- Montonía: Monotona decreciente.
    - Pues el denominador crece más rápido que el numerador, por lo tanto la función va decreciendo.
- Acotación: Acotada.
    - Pues empieza en $a_1=1$ y decrece hasta el límite $0$
- Convergencia: $\lim_{n\to\infty}\frac{n^2}{2^n}=0$
    - Por órdenes de crecimiento.