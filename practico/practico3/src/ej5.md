# Ejercicio 5

## Consigna

Estudiar los límites de las siguientes sucesiones. ¿Existen subsucesiones convergentes? Indicar los límites de dichas subsucesiones.

1. $a_n = \frac{1 + (-1)^n}{2}$
2. $a_n = (-1)^n n$
3. $a_n = 3\cos(n\pi)$
4. $a_n = \frac{n - 1}{n + 1} \cos\left(\frac{2n\pi}{3}\right)$
5. $a_n = n^2(1 + (-1)^n)$
6. $a_n = n^{(-1)^n}$
7. $a_n = \frac{(-1)^n}{n} + \frac{1 + (-1)^n}{2}$

## Resolución

### Sucesión #1

- $a_n = \frac{1 + (-1)^n}{2}$

Veamos los primeros términos de la sucesión para agarrar intuición sobre lo que pasa:

- $\{0,1,0,1,0,\ldots\}$

Claramente $a_n$ no converge, pero tenemos dos subsucesiones convergentes en:

- $a_{2k+1}\to 0$
- $a_{2k}\to 1$

### Sucesión #2

- $a_n = (-1)^n n$

Veamos los primeros términos de la sucesión para agarrar intuición sobre lo que pasa:

- $\{-1,2,-3,4,-5,\ldots\}$

Claramente $a_n$ no converge. Pero en este caso tampoco ninguna subsucesión converge, pues la función va oscilando entre términos cada vez mayores por el lado positivo, y cada vez menores por el lado negativo.

### Sucesión #3

- $a_n = 3\cos(n\pi)$

Veamos los primeros términos de la sucesión para agarrar intuición sobre lo que pasa:

- $\{3,-3,3,-3,3,-3\ldots\}$

Claramente $a_n$ no converge, pero tenemos dos subsucesiones convergentes en:

- $a_{2k+1}\to 3$
- $a_{2k}\to -3$

### Sucesión #4

- $a_n = \frac{n - 1}{n + 1} \cos\left(\frac{2n\pi}{3}\right)$

Veamos los primeros términos de la sucesión para agarrar intuición sobre lo que pasa:

- $a_1=0$
- $a_2=\frac{1}{3}\cos(\frac{4\pi}{3})=\frac{1}{3}\cdot\frac{-1}{2}=-\frac{1}{6}$
- $a_3=\frac{1}{2}\cos(2\pi)=\frac{1}{2}$
- $a_4=\frac{3}{5}\cos(\frac{8\pi}{3})=\frac{3}{5}\cdot\frac{-1}{2}=-\frac{3}{10}$
- $a_5=\frac{2}{3}\cos(\frac{10\pi}{3})=\frac{2}{3}\cdot\frac{-1}{2}=-\frac{1}{3}$
- $a_6=\frac{5}{7}\cos(\frac{12\pi}{3})=\frac{5}{7}$

A partir de estos valores, podemos separar entre los múltiplos de 3, y los que no son múltiplos de 3:

- $a_{3k}=\frac{3k-1}{3k+1}\cos(2k\pi)=\frac{3k-1}{3k+1}$
    - $\lim a_{3k}=1$
- $a_{3k+1}=\frac{3k}{3k+2}\cos(\frac{2(3k+1)\pi}{3})=\frac{3k}{3k+2}\cos(\frac{6k\pi+2\pi}{3})=\frac{3k}{3k+2}\cos(\frac{2\pi}{3})$
    - $\lim a_{3k+1}=\frac{-1}{2}$
- $a_{3k+2}=\frac{3k+1}{3k+3}\cos(\frac{2(3k+2)\pi}{3})=\frac{3k+1}{3k+3}\cos(\frac{6k\pi+4\pi}{3})=\frac{3k+1}{3k+3}\cos(\frac{4\pi}{3})$
    - $\lim a_{3k+2}=\frac{-1}{2}$

Por lo tanto:

- Para toda subsucesión que a partir de un punto tome solo valores de $n$ múltiplos de $3$ converge a 1.
- Para toda subsucesión que a partir de un punto tome solo valores de $n$ NO múltiples de $3$ converge a $\frac{-1}{2}$

### Sucesión #5

- $a_n = n^2(1 + (-1)^n)$

Veamos los primeros términos de la sucesión para agarrar intuición sobre lo que pasa:

- $\{0,8,0,32,0,72\}$

Claramente $a_n$ no converge, pero el comportamiento que tiene nos hace separar por múltiplos de 2:

- $a_{2k}=8k^2$
    - $\lim a_{2k}=+\infty$
- $a_{2k+1}=0$
    - $\lim a_{2k+1}=0$

Por lo tanto:

- Para toda subsucesión que a partir de un punto tome solo valores de $n$ tales que: $n=2k+1$, converge a 0.

### Sucesión #6

- $a_n = n^{(-1)^n}$

Veamos los primeros términos de la sucesión para agarrar intuición sobre lo que pasa:

- $\{1,2,\frac{1}{3},4,\frac{1}{5},6\}$

Claramente $a_n$ no converge, pero el comportamiento que tiene nos hace separar por múltiplos de 2:

- $a_{2k}=2k^{(-1)^{2k}}=2k$
    - $\lim a_{2k}=+\infty$
- $a_{2k+1}=(2k+1)^{(-1)^{2k+1}}=\frac{1}{2k+1}$
    - $\lim a_{2k+1}=0$

Por lo tanto:

- Para toda subsucesión que a partir de un punto tome solo valores de $n$ tales que: $n=2k+1$, converge a 0.

### Sucesión #5

- $a_n = \frac{(-1)^n}{n} + \frac{1 + (-1)^n}{2}$

Veamos los primeros términos de la sucesión para agarrar intuición sobre lo que pasa:

- $\{-1,\frac{3}{2},\frac{-1}{3},\frac{5}{4},\frac{-1}{5}\}$

Claramente $a_n$ no converge, pero el comportamiento que tiene nos hace separar por múltiplos de 2:

- $a_{2k}=\frac{1}{2k}+1$
    - $\lim a_{2k}=1$
- $a_{2k+1}=\frac{-1}{2k+1}$
    - $\lim a_{2k+1}=0$

Por lo tanto:

- Para toda subsucesión que a partir de un punto tome solo valores de $n$ tales que $n=2k$, converge a 1.
- Para toda subsucesión que a partir de un punto tome solo valores de $n$ tales que: $n=2k+1$, converge a 0.
