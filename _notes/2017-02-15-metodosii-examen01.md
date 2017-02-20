---
layout: post
title:  Primer examen, resuelto
date: 2017-02-15 23:40:00
description: 
---
$$\newcommand{\ket}[1]{\left |#1 \right\rangle}
\newcommand{\bra}[1]{\left\langle#1\right|}
\newcommand{\bracket}[2]{\left\langle#1\right.|\left.#2\right\rangle}
\newcommand{\vev}[1]{\left\langle#1\right\rangle}
\newcommand{\tr}{\mathrm{Tr}}	
\newcommand{\id}{1\!\!1}
\newcommand{\norm}[1]{\left\lVert #1 \right\rVert}$$

**Problema 1**: *Muestre que un operador lineal que actúa sobre un espacio de
Hilbert es unitario sí y sólo si manda una base del espacio de Hilbert
a otra.*

El problema tiene dos partes. Primero queremos mostrar que, dado el operador $U$ y la base $\phi_n$, si $\psi_n = U \phi_n$ es una base, entonces $U$ es unitario. 

¿Qué significa que $\psi_n$ sea una base? Pues que cualquier vector $\zeta$ del espacio de Hilbert puede escribirse como 

$$\zeta = \sum_n \langle\psi_n, \zeta \rangle \psi_n .$$

Esto es lo mismo que 

$$\zeta = \sum_n \langle U \phi_n, \zeta \rangle U \phi_n .$$

Si sacamos el operador $U$ de la integral, y usamos la definición de la adjunta, vemos que 

$$\zeta = U \sum_n \langle \phi_n, U^\dagger \zeta \rangle \phi_n .$$

Pero esto no es más que $U$ actuándo sobre la expansión de $U^\dagger \zeta$ en la base $\phi_n$. Luego 

$$\zeta = U  U^\dagger \zeta \Rightarrow U U^\dagger = 1.$$

El converso es que si $U$ es un operador unitario, entonces $\psi_n = U \phi_n$ será una base si $\phi_n$ lo es. Tomemos un vector general $\zeta$, multipliquémoslo por $U U^\dagger$, y expandamos $U^\dagger \zeta$ en la base $\phi_n$: 

$$\zeta =  U U^\dagger \zeta = U \sum_n \langle\phi_n, U^\dagger\zeta \rangle \phi_n  =  \sum_n \langle U\phi_n, \zeta \rangle U \phi_n .$$

Esto es lo mismo que 

$$\zeta =   \sum_n \langle \psi_n, \zeta \rangle \psi_n,$$

de modo que también $\psi_n$ es una base. 


**Problema 2**: *Muestre que los eigenvalores $\omega$ de un operador unitario deben cumplir que $\|\omega\|^2=1.$*

Sea $\phi_\omega$ el eigenvector del operador unitario $U$ con eigenvalor $\omega$. Luego

$$ O\phi_\omega = \omega \phi_\omega.$$

Tomando la norma al cuadrado del lado izquierdo de esta ecuación encontramos que

$$ \langle O\phi_\omega, O\phi_\omega \rangle = \langle \phi_\omega, O^\dagger O \phi_\omega \rangle = \langle \phi_\omega \phi_\omega \rangle = \norm{\phi_\omega}^2.$$

Haciendo lo mismo con el lado izquierdo, tendremos que

$$ \langle \omega \phi_\omega, \omega \phi_\omega \rangle = |\omega|^2 \langle \phi_\omega, \phi_\omega \rangle = |\omega|^2\norm{\phi_\omega}^2.$$

Luego 

$$ \norm{\phi_\omega}^2 = |\omega|^2 \norm{\phi_\omega}^2 \Rightarrow  |\omega|^2 = 1.$$

**Problema 3**: *Pruebe que dos elementos $\phi$ y $\psi$ del espacio
de Hilbert $H$ sobre los complejos son ortogonales si y sólo si se
cumple que $\norm{\phi + a\psi} \geq \norm{\phi}$ para cualquier $a$
complejo.*

Calculemos

$$\norm{\phi + a\psi}^2 = \langle \phi + a\psi, \phi + a\psi \rangle = \langle \phi, \phi \rangle + a \langle \phi,\psi \rangle + a^* \langle \psi, \phi \rangle + |a|^2 \langle\psi, \psi \rangle.  $$

Si $\psi$ y $\phi$ son ortogonales, $\langle \phi, \psi\rangle=0$, y

$$\norm{\phi + a\psi}^2 = \langle \phi, \phi \rangle + \|a\|^2 \langle\psi, \psi \rangle \geq  \langle \phi, \phi \rangle = \norm{\phi}^2,$$

puesto que el segundo término es siempre positivo. 

Por otra parte, si la desigualdad se cumple para todo $a$ complejo, vemos que esto requiere que 

$$ a \langle \phi,\psi \rangle + a^* \langle \psi, \phi \rangle + |a|^2 \langle\psi, \psi \rangle \geq 0.  $$

Definimos $z = \langle \phi,\psi \rangle / \langle \psi,\psi \rangle$ para reescribir esto como 

$$ a z + a^* z^* + |a|^2 \geq 0.$$

Si $z\neq 0$, podemos encontrar valores de $a$ que violan esta desigualdad. Por ejemplo, si $a = -z^*$, tendremos que 

$$a z + a^* z^* + |a|^2 = - |z|^2, $$

que claramente es negativo. De modo que la única posibilidad es

$$ z = 0\Rightarrow  \langle \phi,\psi \rangle = 0. $$



**Problema 4**: *Considere los polinomios $$p_1 = 1-x^2\quad p_2 =
x(1-x), \quad p_3= x(1+x).$$ Muestre que $\{p_1,p_2,p_3\}$ son una
base para el espacio pre-Hilbert de polinomios de segundo grado, y
exprese la función $q =1+3x$ en términos de esta base.*  

El espacio de polinomios de segundo grado es generado por los monomios $\{1,x,x^2\}$; es un espacio vectorial de dimensión tres. Cualquier conjunto linealmente independiente de tres vectores será una base. Para mostrar la independencia lineal de $\{p_1,p_2,p_3\}$ escribimos

$$a_1 p_1 + a_2 p_2 + a_3 p_3 = a_1 (1-x^2) + a_2 x(1-x) + a_3 x(1+x) =0. $$

Reuniendo términos, esto equivale a 

$$ a_1 + (a_2+a_3)x + (-a_1-a_2 + a_3)x^2 =0. $$

Por independencia lineal de $\{1,x,x^2\}$, esto solo puede ser nulo si 

$$ a_1 =0, \qquad  (a_2+a_3) =0, \qquad (-a_1-a_2 + a_3) =0. $$

Estas ecuaciones implican que $a_1 = a_2 = a_3 = 0$. Luego, $\{p_1,p_2,p_3\}$ son tres vectores linealmente indendientes; luego, forman una base. 

Ahora, queremos reescribir $q = 1 + 3x$ en esta base. Si pedimos que 

$$ a_1 + (a_2+a_3)x + (-a_1-a_2 + a_3)x^2 = 1 + 3x, $$

podemos leer los coeficientes

$$ a_1 = 1, \qquad  (a_2+a_3) = 3, \qquad (-a_1-a_2 + a_3) = 0, $$

de donde tenemos que 

$$ a_1 = 1, \qquad  a_2 = 1, \qquad a_3 = 2. $$

Entonces, 

$$ q = p_1 + p_2 + 2 p_3.$$

**Problema 5**: *Los polinomios de Bessel (así llamados porque pueden
expresarse en términos de las funciones de Bessel con argumento
$x^{-1}$) son soluciones de la ecuación de eigenvalores del siguiente
operador:*  

$$\mathcal{O}\phi_n = - \partial_x^2\phi_n -
\frac{1}{x}\partial_x
\phi_n + \frac{n^2}{x^2} \phi_n = k^2 \phi_n.$$  

*Reescriba esta ecuación en términos de los operadores de escalera*

$$A^+ = -\partial_x + \frac{n}{x},\qquad A^- = \partial_x +
\frac{n+1}{x}.$$   

*Suponiendo que los términos de frontera se anulan,
encuentre el peso $w(x)$ que hace que los operadores $A^\pm$ sean
adjuntos uno del otro.*


Calculamos

$$A^+ A^- \phi = \left(-\partial_x + \frac{n}{x} \right) \left( \partial_x \phi + \frac{n+1}{x} \phi \right), $$

de donde obtenemos que 

$$A^+ A^- \phi =   - \partial_x^2 \phi - \frac{n+1}{x} \partial_x \phi  + \frac{n+1}{x^2}  \phi +  \frac{n}{x} \partial_x \phi + \frac{n}{x} \frac{n+1}{x} \phi,  $$

y cancelando términos, 

$$A^+ A^- \phi =   - \partial_x^2 \phi - \frac{1}{x} \partial_x \phi  +  \frac{(n+1)^2}{x^2} \phi.  $$

De forma similar, 

$$A^- A^+ \phi = - \partial_x^2 \phi - \frac{1}{x} \partial_x \phi  +  \frac{n^2}{x^2} \phi.  $$

En cuanto a la función de peso, escribimos

$$\langle \phi, A^+ \psi\rangle = \int dx w\ \phi A^+ \psi =  \int dx w\ \phi A^+ \psi = -\int dx w\ \phi \left( \partial_x \psi - \frac{n}{x}\psi \right). $$ 

Tomamos el primer término

$$-\int dx w\ \phi \partial_x \psi = -\int dx \partial_x( w\ \phi  \psi) + \int dx \partial_x( w\ \phi)\psi.$$

La primera parte es un término de frontera que suponemos se anula. Entonces


$$\langle \phi, A^+ \psi\rangle = \langle (A^+)^\dagger \phi, \psi\rangle =\int dx \left(\partial_x(w ) \phi + w \partial_x \phi  + w \frac{n}{x}\phi \right)  \psi. $$ 


Si pedimos que $(A^+)^\dagger = (A^-)$ entonces 


$$\int dx \left(\partial_x(w ) \phi + w \partial_x \phi  + w \frac{n}{x}\phi \right)  \psi = \int dx w\  \left(\partial_x \phi  + \frac{n+1}{x}\phi \right)  \psi    $$ 

lo cuál requiere, para toda $\phi$ y $\psi$, 

$$\int dx \partial_x(w ) \phi   \psi = \int dx w  \frac{1}{x}\phi \psi \Rightarrow \partial_x(w ) =    \frac{w}{x} \Rightarrow w = x.  $$ 


