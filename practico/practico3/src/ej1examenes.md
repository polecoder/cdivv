# Ejercicio 1 (evaluaciones anteriores)

## Consigna

### Parte 1

1) Definir límite finito de una sucesión:
$$
\lim_{n \to \infty} a_n = L \in \mathbb{R} \;\; \text{sii} \; \dots
$$

2) Definir sucesión acotada. Se dice que una sucesión $a_n$ es acotada sii $\dots$

### Parte 2

Sean $a_n$ y $b_n$ sucesiones tales que $\lim_{n \to \infty} a_n = 0$ y $b_n$ es acotada. Demostrar que:

- $\lim_{n \to \infty} a_n b_n = 0$

### Parte 3

1) Dar un ejemplo de un par de sucesiones $a_n$ y $b_n$, con $\lim_{n \to \infty} a_n = 0$ y $b_n$ no acotada, tales que $\lim_{n \to \infty} a_n b_n = 0$.

2) Dar un ejemplo de un par de sucesiones $a_n$ y $b_n$, con $\lim_{n \to \infty} a_n = 0$ y $b_n$ no acotada, tales que el límite de $a_n b_n$ no sea cero (infinito u otro límite real no nulo).

## Resolución

### Parte 1

1. Definir límite finito de una sucesión.

Decimos que $\lim_{n\to+\infty}a_n=L\in\mathbb{R}$ sii:

- $\forall\varepsilon>0,\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0: a_n\in E(L,\varepsilon)$, o alternativamente:
- $\forall\varepsilon>0,\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0: |a_n-L|<\varepsilon$

2. Definir sucesión acotada.

Decimos que una sucesión $a_n$ es acotada sii:

- $\exists K\in\mathbb{R}$ tal que $\forall n\in\mathbb{N}: |a_n|\leq K$

### Parte 2

Sean $a_n$ y $b_n$ sucesiones tales que $\lim_{n \to \infty} a_n = 0$ y $b_n$ es acotada. Demostrar que:

- $\lim_{n \to \infty} a_nb_n = 0$

Planteemos la definición de lo que queremos probar:

- $\forall\varepsilon>0,\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0:|a_nb_n|<\varepsilon$

Por otra parte, lo que sabemos es que para cualquier $\varepsilon>0$:


- $(*_1)\quad\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0: |a_n|<\varepsilon$
Además, como $b_n$ es acotada, tenemos que:

- $(*_2)\quad\exists K\in\mathbb{R}$ tal que $\forall n\in\mathbb{N}:|b_n|< K$

Ahora, consideremos la afirmación $(*_1)$ con $\varepsilon:=\frac{\varepsilon}{K}$, entonces a partir de un cierto $n_0$ tenemos que:

$$
\begin{aligned}
&|a_n|<\frac{\varepsilon}{K}\\
&\iff\scriptstyle{(\text{considerando que }|b_n|< K)}\\
&|a_n||b_n|<\frac{\varepsilon}{K}\cdot K\\
&\iff\scriptstyle{(\text{operatoria})}\\
&|a_nb_n|<\varepsilon\\
\end{aligned}
$$

Que es exactamente lo que queríamos probar para cualquier $\varepsilon>0$.

### Parte 3

1) Dar un ejemplo de un par de sucesiones $a_n$ y $b_n$, con $\lim_{n \to \infty} a_n = 0$ y $b_n$ no acotada, tales que $\lim_{n \to \infty} a_n b_n = 0$.
    - Consideremos $a_n=\frac{1}{n^2}$ y $b_n=n$, entonces $a_nb_n=\frac{1}{n}$ que claramente converge a cero.

2) Dar un ejemplo de un par de sucesiones $a_n$ y $b_n$, con $\lim_{n \to \infty} a_n = 0$ y $b_n$ no acotada, tales que el límite de $a_n b_n$ no sea cero (infinito u otro límite real no nulo).
    - Consideremos $a_n=\frac{1}{n}$ y $b_n=n^2$ entonces $a_nb_n=n$, que claramente es divergente.