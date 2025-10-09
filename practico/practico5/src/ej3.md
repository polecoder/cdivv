# Ejercicio 3

## Consigna

Sea $k > 0$. Hallar el valor de $k$ para que la integral

$$
\int_1^{+\infty} \left( \frac{x}{2x^2 + 2k} - \frac{k}{x + 1} \right)dx
$$

sea convergente y calcularla.

## Resolución

Operemos un poco con la integral para simplificar la expresión:

$$
\begin{aligned}
&\int_1^{+\infty} \left( \frac{x}{2x^2 + 2k} - \frac{k}{x + 1} \right)dx\\
&=\\
&\int_1^{+\infty} \left(\frac{x^2+x-2kx^2-2k^2}{2x^3+2kx+2x^2+2k}\right)dx\\
&=\\
&\int_1^{+\infty} \left(\frac{(1-2k)x^2+x-2k^2}{2x^3+2kx+2x^2+2k}\right)dx\\
\end{aligned}
$$

Observemos que $1-2k$ determina si la integral converge o no.

- Si $1-2k=0$, entonces la impropia equivale a $\frac{1}{x^2}$, por lo que convergería
- Si $1-2k\neq0$, entonces la impropia equivale a $\frac{1}{x}$, por lo que divergería

De esto concluimos que la integral impropia converge sii $k=\frac{1}{2}$.

Por lo tanto queremos trabajar con la siguiente integral:

$$
\begin{aligned}
&\int_1^{+\infty} \left( \frac{x}{2x^2 + 1} - \frac{1}{2(x+1)} \right)dx
\end{aligned}
$$

Entonces, tenemos dos primitivas que calcular, vamos paso a paso para cada una:

### Primitiva #1

$$
\begin{aligned}
&\int \frac{x}{2x^2+1}dx\\
&=\\
&\frac{1}{2}\int \frac{2x}{2x^2+1}dx\\
&=\scriptstyle{(\text{cambio de variable }u=x^2;du=2xdx)}\\
&\frac{1}{2}\int \frac{du}{2u+1}\\
&=\scriptstyle{(*_1)}\\
&\frac{1}{4}log(2u+1)\\
&=\scriptstyle{(\text{deshaciendo cambio de variable})}\\
&\frac{1}{4}log(2x^2+1)\\
\end{aligned}
$$

**Observación $(*_1)$:** En este paso usamos la regla de la cadena con las siguientes funciones:

- $f(x)=log(x)$
- $g(x)=2u+1$

Entonces: $(f\circ g)'=\frac{1}{2u+1}\cdot 2=\frac{2}{2u+1}$.

Esto es casi lo que buscabamos, pero multiplicado por dos. Fácilmente vemos que si consideramos la función

- $\frac{1}{2}\log(2u+1)$

La regla de la cadena devuelve lo que estamos necesitando.

### Primitiva #2

$$
\begin{aligned}
&\int\frac{1}{2(x+1)}dx\\
&=\\
&\frac{1}{2}\int\frac{1}{x+1}dx\\
&=\\
&\frac{1}{2}\log(x+1)
\end{aligned}
$$

### Primitiva original

Entonces la primitiva que queríamos calcular queda de la siguiente forma:

$$
\begin{aligned}
&\int\left( \frac{x}{2x^2 + 1} - \frac{1}{2(x+1)} \right)dx\\
&=\\
&\frac{1}{4}\log(2x^2+1)-\frac{1}{2}\log(x+1)\\
&=\\
&\frac{\log(2x^2+1)-2\log(x+1)}{4}\\
&=\\
&\frac{\log(2x^2+1)-\log((x+1)^2)}{4}\\
&=\\
&\frac{1}{4}\log\left(\frac{2x^2+1}{(x+1)^2}\right)\\
\end{aligned}
$$

Y ahora tendríamos que evaluarla en los extremos:

$$
\begin{aligned}
&\frac{1}{4}\log\left(\frac{2x^2+1}{(x+1)^2}\right)\Big|_1^{+\infty}\\
&=\\
&\frac{1}{4}\left(\lim_{x\to+\infty}\log\left(\frac{2x^2+1}{(x+1)^2}\right)-\log\left(\frac{3}{4}\right)\right)\\
&=\\
&\frac{1}{4}\left(\lim_{x\to+\infty}\log\left(\frac{2x^2}{x^2}\right)-\log\left(\frac{3}{4}\right)\right)\\
&=\\
&\frac{1}{4}\left(\log(2)-\log\left(\frac{3}{4}\right)\right)\\
&=\\
&\frac{1}{4}\log\left(\frac{8}{3}\right)
\end{aligned}
$$

### Conclusión

La integral impropia $\int_1^{+\infty} \left( \frac{x}{2x^2 + 2k} - \frac{k}{x + 1} \right)dx$ converge a $\frac{1}{4}\log\left(\frac{8}{3}\right)$ sii $k=\frac{1}{2}$.
En cualquier otro caso la integral diverge.