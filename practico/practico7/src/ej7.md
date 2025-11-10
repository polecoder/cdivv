# Ejercicio 7

## Consigna

Decidir si los siguientes límites existen y en caso afirmativo calcularlos:

1. $\lim_{(x,y,z)\to(2,2,6)} \tfrac{x - y}{x^2 + y - z}$
2. $\lim_{(x,y,z)\to(1,0,1)} \tfrac{\sin(x^2 + e^y - z)}{x^2 + \tan\left(\tfrac{1}{\cos(xyz)}\right)}$
3. $\lim_{(x,y,z)\to(0,0,0)} \tfrac{x^2yz - z^4}{x^4 + y^4 + z^4}$


## Resolución

### Límite #1

- $\lim_{(x,y,z)\to(2,2,6)} \frac{x-y}{x^2+y-z}$

Evaluemos algunos límites direccionales, por ejemplo cuando:

- $y=x$
- $z=6$

Por lo tanto, el límite se convierte en el siguiente:

- $\lim_{x\to 2} \frac{0}{x^2+x-6}$

Esto tiende a 0, teniendo muy en cuenta que NO estamos evaluando la función en el punto $x=2$, sino en los puntos arbitrariamente cercanos a él.

Ahora veamos otra dirección:

- $y=2$
- $z=6$

Por lo tanto, el límite se convierte en el siguiente:

- $\lim_{x\to2}\frac{x-2}{x^2-4}=\lim_{x\to2}\frac{x-2}{(x+2)(x-2)}=\frac{1}{4}$

Con esto podemos concluir que el límite no existe, ya que hallamos dos direcciones en que el límite nos da un valor numérico diferente.

### Límite #2

- $\lim_{(x,y,z)\to(1,0,1)} \tfrac{\sin(x^2 + e^y - z)}{x^2 + \tan\left(\tfrac{1}{\cos(xyz)}\right)}$

Probemos sustituyendo:

- $\tfrac{\sin(x^2+e^y-z)}{x^2+\tan\left(\tfrac{1}{\cos(xyz)}\right)}=\frac{\sin(1)}{1+\tan\left(\frac{1}{\cos(0)}\right)}=\frac{\sin(1)}{1+\tan(1)}$

Por lo tanto el límite existe, y tiende a $\frac{\sin(1)}{1+\tan(1)}$

### Límite #3

- $\lim_{(x,y,z)\to(0,0,0)} \tfrac{x^2yz - z^4}{x^4 + y^4 + z^4}$

Evaluemos algunos límites direccionales, por ejemplo cuando:

- $y=z$
- $x=0$

Por lo tanto el límite se convierte en:

- $\lim_{z\to0}\frac{-z^4}{2z^4}=\frac{-1}{2}$

Ahora, veamos otra dirección:

- $y=z$
- $x=z$

Por lo tanto el límite se convierte en:

- $\lim_{z\to0}\frac{z^4-z^4}{3z^4}=\lim_{z\to0}\frac{0}{3z^4}=0$

Por el mismo razonamiento que el que usamos para el límite de la parte 1, tenemos que este también tiende a 0.

Con esto podemos concluir que el límite no existe, ya que hallamos dos direcciones en que el límite nos da un valor numérico diferente.