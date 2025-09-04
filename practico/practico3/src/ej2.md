# Ejercicio 2

## Consigna

Sean $a_n$ y $b_n$ dos sucesiones reales convergentes tales que $\lim_{n \to +\infty} a_n = A$ y $\lim_{n \to +\infty} b_n = B$.

1. Probar que la sucesión $c_n = a_n + b_n$ es convergente y $\lim_{n \to +\infty} c_n = A + B$.
2. Sea $\lambda \in \mathbb{R}$, probar que la sucesión $\tilde{a}_n = \lambda a_n$ converge y $\lim_{n \to +\infty} \tilde{a}_n = \lambda A$.
3. Probar que la sucesión $d_n = a_n b_n$ converge y $\lim_{n \to +\infty} d_n = AB$.
4. Sea $(e_n)$ una sucesión acotada y suponga que $A = 0$. Probar que $\lim_{n \to +\infty} e_n a_n = 0$.

### Parte 1

Hecho en el teórico, clase 9, sección 3.11

### Parte 2

- Sea $\lambda \in \mathbb{R}$, probar que la sucesión $\tilde{a}_n = \lambda a_n$ converge y $\lim_{n \to +\infty} \tilde{a}_n = \lambda A$.

Como $\lim_{n\to\infty}a_n=A$, tenemos que:

- $\forall\varepsilon>0,\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0:|a_n-A|<\varepsilon$

Tomamos $\varepsilon=\frac{\varepsilon}{|\lambda|}$, entonces a partir de un $n_0\in\mathbb{N}$ se cumple el siguiente razonamiento:

$$
\begin{aligned}
&|a_n-A|<\frac{\varepsilon}{|\lambda|}\\
&\iff\scriptstyle{(\text{operando})}\\
&|\lambda||a_n-A|<\varepsilon\\
&\iff\scriptstyle{(\text{operando})}\\
&|\lambda(a_n-A)|<\varepsilon\\
&\iff\scriptstyle{(\text{operando})}\\
&|\lambda a_n-\lambda A|<\varepsilon\\
&\iff\scriptstyle{(\tilde{a}_n=\lambda a_n)}\\
&|\tilde{a}_n-\lambda A|<\varepsilon\\
\end{aligned}
$$

Por lo tanto demostramos lo que queríamos verificar, es decir que:

- $\lim_{n\to\infty}\tilde{a}_n=\lambda A$

### Parte 3

Hecho en el teórico, clase 9, sección 3.11

### Parte 4

Hecho en el teórico, clase 9, sección 3.10