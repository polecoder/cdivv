# Ejercicio 7

## Consigna

Sea $(a_n)$ una sucesión tal que sus subsucesiones $a_{2n}$, $a_{2n+1}$ y $a_{3n}$ convergen. Probar que $(a_n)$ es convergente.

## Resolución

Por hipótesis tenemos que:

- $a_{2n}\to L_1$
- $a_{2n+1}\to L_2$
- $a_{3n}\to L_3$

Intentaremos afirmar que las tres subsucesiones convergen al mismo punto para poder afirmar que $a_n$ es convergente.

Primero, observemos que $a_{6n}$ es a la vez una subsucesión de $a_{2n}$ y de $a_{3n}$, por lo que:

- $a_{6n}\to L_1$
- $a_{6n}\to L_3$

Y por lo tanto $L_1=L_3$.

En segundo lugar, observemos que $a_{6n+3}$ es a la vez una subsucesión de $a_{3n}$ y de $a_{2n+1}$, por lo que:

- $a_{6n+3}\to L_3$
- $a_{6n+3}\to L_2$

Y por lo tanto $L_2=L_3$.

Esto nos deja con que:

- $L_1=L_2=L_3$, y por lo tanto:
- $a_{2n}\to L$
- $a_{2n+1}\to L$

Podemos establecer la definición de límite para las dos subsucesiones:

- $\forall\varepsilon>0,\exists k_0$ tal que $\forall k>k_0 :|a_{2k}-L|<\varepsilon$
- $\forall\varepsilon>0,\exists k_1$ tal que $\forall k>k_1 :|a_{2k+1}-L|<\varepsilon$

Por lo tanto, tomamos $n_0:=\max\{k_0,k_1\}$, para cualquier $n\in\mathbb{N}$, tenemos que:

- $n=2k$ con $k\in\mathbb{N}$, o
- $n=2k+1$ con $k\in\mathbb{N}$

Entonces en particular $\forall\varepsilon>0, \forall n>n_0: |a_n-L|<\varepsilon$

Finalizando, esto significa que:

- $a_n\to L$