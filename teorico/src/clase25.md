# CLASE 25 - 04/11/2025

## Límites y continuidad

### Proposición 6.18

Si $f$ y $g$ son dos funciones continuas en $a$, entonces:

1. $f+g$ es continua en $a$
2. $f\cdot g$ es continua en $a$
3. Si $g(a)\neq0$ entonces $f/g$ es continua en $a$

### Demostración

Veremos solo la demostración de la suma, pues las demás son muy similares.
La estrategia será utilizar el teorema 6.9, es decir:

**Recordatorio:**
Sea un conjunto $D\subset\mathbb{R}^n$, una función $f:D\to\mathbb{R}$, y $a\in\mathbb{R}^n$ un punto de $D$. Entonces:

- $f$ es continua $\iff$ para toda sucesión $x_k$ de elementos de $D$ tal que $\lim_{k\to+\infty}x_k=a$, tenemos que $\lim_{k\to+\infty} f(x_k)=f(a)$

**Continuación:**
Como tenemos que $f$ y $g$ son continuas, tomamos una sucesión genérica $x_k\in\mathbb{R}^n$ que cumple que $\lim_{k\to+\infty}x_k=a$, y sabemos que esta cumple que:

- $\lim_{k\to+\infty}f(x_k)=f(a)$
- $\lim_{k\to+\infty}g(x_k)=g(a)$

Entonces podemos usar la suma de límite en sucesiones (que ya probamos en el curso):

- $\lim_{k\to+\infty}(f+g)(x_k)=f(x_k)+g(x_k)=f(a)+g(a)=(f+g)(a)$

Entonces, cómo es cierto que para toda sucesión $x_k\in\mathbb{R}^n$ que tiende a $a$, sus imágenes por la función $f+g$ tienden a $(f+g)(a)$, concluimos que la función es continua (también por el teorema 6.9).

### Proposición 6.19

Sea $f:\mathbb{R}^n\to\mathbb{R}$ continua en $a\in\mathbb{R}^n$, y $g:\mathbb{R}\to\mathbb{R}$ una función continua en $f(a)\in\mathbb{R}$. Entonces la composición $g\circ f$ es continua en $a$.

### Teorema 6.20 (Weierstrass)

Sea $C\subset\mathbb{R}^n$ un conjunto compacto, y $f:C\to\mathbb{R}$ una función continua. Entonces $f$ alcanza mínimo y máximo en $C$. Es decir que existen $x_m,x_M\in\mathbb{C}$, tales que:

- $f(x)\geq f(x_m)\quad\forall x\in C$
- $f(x)\leq f(x_M)\quad\forall x\in C$

#### Demostración

**Primer parte:**
Primero probaremos que $f$ es acotada (superiormente). 
Para esto suponemos que no lo es, es decir que para todo $B\in\mathbb{R}$, existe un punto $x\in C$ tal que $f(x)>B$.

Consideramos entonces una sucesión de valores crecientes de $B$, por ejemplo $B_k=k$. Como estamos suponiendo que $f$ no es acotada, para cada uno de estos $B_k$ podemos conseguir un $x_k\in C$ tal que $f(x_k)> B_k$.

De este modo construimos una sucesión $x_k$ tal que $\lim_{x\to+\infty}f(x_k)=+\infty$. Por otro lado notemos que la sucesión está contenida en $C$ por construcción, y como $C$ es un conjunto compacto (corolario 5.32), tiene una subsucesión convergente. Llamaremos $x_{k_j}$ a esta subsucesión y $\overline{x}\in\mathbb{C}$ a su límite.

Como $f$ es continua en todo el conjunto $C$, en particular en $\overline{x}$, tenemos que para toda sucesión que tienda a $\overline{x}$, entonces sus imágenes por $f$ tienden a $f(\overline{x})$ (teorema 6.9).
Sin embargo $x_{k_j}$ es una sucesión de estas características, pero sus imágenes por $f$ tienden a infinito.
Esto es absurdo, pues contradice un teorema. Por lo tanto $f$ es acotada (superiormente).

**Segunda parte:**
Consideremos el conjunto imagen de la función $Im(f)=\{f(x):x\in C\}$. Como probamos que $f$ es acotada, y no vacía (pues sino estaría mal definida), por el axioma de completitud tenemos que $Im(f)$ tiene supremo, llamemosle $M=sup(Im(f))$.

Usando la propiedad fundamental del supremo, podemos obtener elementos de $Im(f)$ cada vez más cerca de $M$, de forma que podemos construir una sucesión $x_k$ tal que $f(x_k)$ tienda a $M$.
Esto lo podemos hacer por ejemplo tomando $\varepsilon=\frac{1}{k}$, para todo $k\in\mathbb{N}$ y tomando un elemento $x_k\in C$ tal que $f(x_k)\in (M-\frac{1}{k},M]$.

Entonces, como $\{x_k\}\subset C$ (compacto), $x_k$ tiene una subsucesión convergente, llamemosla $x_{k_j}$ y a su límite $\overline{x}$. Y cómo $f$ es continua en $\overline{x}$, $f(x_{k_j})$ tiende a $f(\overline{x})$.
Como además $f(x_k)\to M$, en particular $f(x_{k_j})$ también tiende a $M$, por lo que juntando las últimas dos afirmaciones:

- $f(\overline{x})=M$

Esto concluye la prueba, pues construimos $M$ como el supremo del conjunto imagen de $f$, y probamos que tiene preimagen en $C$.