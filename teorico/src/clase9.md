# CLASE 9 - 27/08/2025

## Sucesiones

### Ejercicio 3.10

1. Demostrar que si $a_n\leq b_n,\forall n\in\mathbb{N}$ y ambas tienen límite, entonces $\lim a_n\leq \lim b_n$
2. Si $a_n$ es acotada y $\lim b_n=0$, demostrar que $\lim a_nb_n=0$

#### Parte 1

Llamemos:

- $A=\lim a_n$, y
- $B=\lim b_n$

Probaremos esta propiedad por absurdo, entonces supongamos que $B<A$:

Como sabemos que ambas sucesiones tienen límite, tenemos que:

- $\forall\varepsilon>0,\exists n_1\in\mathbb{N}$ tal que $\forall n>n_1:a_n\in E(A,\varepsilon)$
- $\forall\varepsilon>0,\exists n_2\in\mathbb{N}$ tal que $\forall n>n_2:b_n\in E(B,\varepsilon)$

Esto nos permite considerar:

- $n_0=\max\{n_1,n_2\}$, y
- $\varepsilon= \frac{|A-B|}{2}$

De forma que $E(B,\varepsilon)\cap E(A,\varepsilon)=\emptyset$.
Gráficamente la situación se ve algo así:

![Figura 1](../img/clase9fig1.png)

Entonces ahora consideremos cualquier $n>n_0$, para este se tiene que cumplir que:

- $a_n\in E(A,\varepsilon)$
- $b_n\in E(B,\varepsilon)$

Pero como son disjuntos y el entorno $E(A,\varepsilon)$ está más adelante en la recta que $E(B,\varepsilon)$, necesariamente vamos a tener que:

- $b_n<a_n$ para todo $n>n_0$

Pero esto es absurdo pues estamos contradiciendo la hipótesis que nos dice que:

- $a_n\leq b_n,\forall n\in\mathbb{N}$

Por lo que queda probada la propiedad.

#### Parte 2

Como $\lim b_n=0$, tenemos que:

- $\forall\varepsilon>0,\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0: |b_n-0| < \varepsilon$

Como $a_n$ es acotada, tenemos que:

- $\exists K\in\mathbb{R}$ tal que $\forall n\in\mathbb{N}:|a_n|< K$

Tomamos $\varepsilon_1=\frac{\varepsilon}{K}>0$ y como $\lim b_n=0$ tenemos que:

- $\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0:|b_n|<\frac{\varepsilon}{K}$

Operando a partir de este punto, $\forall n>n_0$ tenemos que:

$$
\begin{aligned}
&|b_n|<\frac{\varepsilon}{K}\\
&\iff\scriptstyle{(\text{operando})}\\
&K|b_n|<\varepsilon\\
&\iff\scriptstyle{(a_n\text{ acotada})}\\
&|a_n||b_n|<K|b_n|<\varepsilon\\
&\iff\scriptstyle{(\text{operando})}\\
&|a_nb_n|<K|b_n|<\varepsilon\\
&\iff\scriptstyle{(\text{simplificando})}\\
&|a_nb_n|<\varepsilon\\
\end{aligned}
$$

Como demostramos esto para todo $n>n_0$, probamos que efectivamente:

- $\forall\varepsilon>0,\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0: |a_nb_n|<\varepsilon$

Lo que es equivalente a decir que:

- $\lim a_nb_n=0$

### Teorema 3.11 (propiedades de límite)

Sean $a_n,b_n$ dos sucesiones tales que $\lim a_n=A$ y $\lim b_n=B$. Entonces:

1. $\lim a_n+b_n=A+B$
2. $\lim a_nb_n=AB$
3. Si $B\neq0$, entonces $\lim \frac{a_n}{b_n}=\frac{A}{B}$

En todos los casos, por hipótesis tenemos que:

- $\forall\varepsilon>0,\exists n_1$ tal que $\forall n>n_0: |a_n-A|<\varepsilon\quad(*_1)$
- $\forall\varepsilon>0,\exists n_2$ tal que $\forall n>n_0: |b_n-B|<\varepsilon\quad(*_2)$

#### Demostración 1

- $\lim a_n+b_n=A+B$

Por definición de límite, queremos probar que:

- $\forall\varepsilon>0,\exists n_0$ tal que $\forall n>n_0: |a_n+b_n-A-B|<\varepsilon$

Consideremos $\varepsilon=\frac{\varepsilon}{2}$ y $n_0=\max\{n_1,n_2\}$ y el siguiente razonamiento $\forall n>n_0$:

$$
\begin{aligned}
&|a_n+b_n-A-B|\\
&=\scriptstyle{(\text{reordenando})}\\
&|a_n-A+b_n-B|\\
&\leq\scriptstyle{(\text{desigualdad triangular})}\\
&|a_n-A|+|b_n-B|\\
&<\scriptstyle{(\text{def. de límite})}\\
&\frac{\varepsilon}{2}+\frac{\varepsilon}{2}\\
&=\\
&\varepsilon
\end{aligned}
$$

Por lo tanto, probamos lo que queríamos verificar, y eso implica que:

- $\lim a_n+b_n=A+B$

**Observación:** Esta propiedad es válida también cuando hay una resta, y su prueba es análoga.

#### Demostración 2

- $\lim a_nb_n=AB$

Por definición de límite, queremos probar que:

- $\forall\varepsilon>0,\exists n_0\in\mathbb{N}$ tal que $\forall n>n_0: |a_nb_n-AB|<\varepsilon$

Consideremos $\varepsilon=$ y $n_0=\max\{n_1,n_2\}$ y el siguiente razonamiento $\forall n>n_0$:

$$
\begin{aligned}
&|a_nb_n-AB|\\
&=\\
&|a_nb_n+Ab_n-Ab_n-AB|\\
&=\\
&|A(b_n-B)+b_n(a_n-A)|\\
&\leq\scriptstyle{(\text{desigualdad triangular})}\\
&|A||b_n-B|+|b_n||a_n-A|\\
\end{aligned}
$$

Observemos los sumados por separado por  $a_n$ y $b_n$:

- $|A||b_n-B|<\frac{\varepsilon}{2|A|}$, por definición de límite. $(*_1)$

**Atención:** Si $A=0$ entonces la propiedad cae en las hipótesis de la vista en la parte 3.10, por lo que consideramos $A\neq0$

Por otra parte tenemos que, como $\lim b_n=B$, tenemos que $b_n$ es acotada (propiedad vista anteriormente), por lo tanto:

- $\exists K\in\mathbb{R}$ tal que $\forall n\in\mathbb{N}: |b_n|<K$

Con esto, veamos que:

- $|b_n||a_n-A|< K|a_n-A|<\frac{\varepsilon}{2K}$, por definición de límite. $(*_2)$

**Atención:** En ambos puntos $(*_1)$ y $(*_2)$ estamos considerando $n>n_0$ para usar la definición de límite.

Ahora podemos redondear el ejercicio retomando el primer razonamiento que hicimos:

$$
\begin{aligned}
&|A||b_n-B|+|b_n||a_n-A|\\
&<\scriptstyle{(\text{por }(*_1),(*_2))}\\
&|A|\cdot\frac{\varepsilon}{2|A|}+|b_n|\frac{\varepsilon}{2K}\\
&=\scriptstyle{(\text{simplificando})}\\
&\frac{\varepsilon}{2}+\frac{\varepsilon}{2}\\
&=\\
&\varepsilon
\end{aligned}
$$

Por lo tanto, probamos lo que queríamos verificar, y eso implica que:

- $\lim a_nb_n=AB$

#### Demostración 3