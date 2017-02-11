---
layout: post
title:  Algunos problemas para combatir el aburrimiento (Cuántica I)
date: 2017-01-03 17:01:00
description: 
---
$$\newcommand{\ket}[1]{\left |#1 \right\rangle}
\newcommand{\bra}[1]{\left\langle#1\right|}
\newcommand{\bracket}[2]{\left\langle#1\right.|\left.#2\right\rangle}
\newcommand{\vev}[1]{\left\langle#1\right\rangle}
\newcommand{\tr}{\mathrm{Tr}}	
\newcommand{\id}{1\!\!1}$$

1. Partiendo del Hamiltoniano 
$$ \mathcal{H} = \frac{P^2}{2m} + \frac{m \omega^2 Q^2}{2} $$
en donde $\omega^2 = k/m$, y definiendo los operadores
$$ a^\pm = \sqrt{\frac{m\omega}{2\hbar}}\left(Q \pm i \frac{P}{m\omega} \right),\quad N = a^+ a^-,   $$
calcule las relaciones de conmutación
$$ [a^-, a^+ ] = 1, \quad [N, a^\pm] = \pm a^\pm $$
y muestre que 
$$\mathcal{H} = \hbar\omega \left(N + \frac{1}{2}\right).$$
2. Usando los resultados del problema anterior, utilice los eigenkets $\ket{n}$ de $N$ para mostrar que 
    - $a^- \ket{n} = \sqrt{n} \ket{n-1}$
    - $a^+ \ket{n} = \sqrt{n+1} \ket{n+1}$
    - $n \geq 0$.  
Argumente que $n$ debe ser un entero no negativo, y su menor valor posible es $n=0$.  
2. Construya los elementos de matriz de $Q$ y $P$ en la base de los eigenkets de $N$. 
3. Usando la notación de Dirac (kets y bras) pruebe las siguientes relaciones:
    * $\tr( \mathcal{O}_1  \mathcal{O}_2 ) =  \tr( \mathcal{O}_2  \mathcal{O}_1 )$
	* $(\mathcal{O}_1 \mathcal{O}_2 )^\dagger = \mathcal{O}_2^\dagger
      \mathcal{O}_1^\dagger$
4. Evalúe $\exp( i f(A) )$ en donde $A$ es un operador Hermítico cuyos eigenvalores conocemos.
5. Evalúe $$\sum \psi^*_a(q') \psi^*_a(q)$$, en donde $\psi_a(q) = \bracket{q}{a}$ es un operador Hermítico cuyos eigenvalores conocemos.
6. Suponga  que $\ket{i}$ y $\ket{j}$ son eigenestados de un mismo operador Hermítico $K$. ¿Bajo que condiciones podemos concluir que $\ket{i}+\ket{j}$ es un eigenvector de $K$?
7. Suponga que los eigenkets $\ket{a}$ de un operador Hermítico $A$ no degenerado forman una base ortonormal.
    * Pruebe que $\mathcal{O}_1 = \prod_a (A -a \id)$ es el operador nulo.
	* Explique cuál es el significado del siguiente operador:
	$$\mathcal{O}_2  = \prod_{a'\neq a} \frac{(A -a' \id)}{a-a'}. $$
	* Ilustre $\mathcal{O}_1 $ y $\mathcal{O}_2$ usando $A$ igual al operador
	$$\sigma_3 = \begin{pmatrix} 1 & 0 \\ 0 & -1 \\ \end{pmatrix}   $$
8. Considere el siguiente experimento: una fuente de electrones emite un electrón en el estado $\ket{\psi}$ que viaja hacia una rejilla con $n$ rendijas. Detrás de esta rejilla hay una rendija con $2m+1$ detectores en las posiciones $q_s = q_0 \pm s \Delta q$, con $s= -m, \dots 0 \dots m$. Considere que el electrón debe pasar por alguna rendija, y denote por $\ket{\varnothing}$ el resultado donde no arriba a ningún detector. 
    * En el caso sencillo donde $n=1$, $m=0$, escriba la descomposición del estado original en la base de rendijas, y secuencialmente en la base de detectores. ¿Cuál es la probabilidad de detectar al electrón en $q_0$?
	* Suponga ahora que $n=2$ y $m=0$. Primero, tapamos la segunda
	rendija, de modo que $\ket{psi} = \ket{1}$. Luego tenemos que 
	$$ \bracket{1}{\psi} = 1 \quad \bracket{2}{\psi} = 0, \quad
	\bracket{q_0}{1} = f(q_0)e^{i \alpha}.$$
	¿Cuál es la probabilidad de detectar al electrón en el detector en $q_0$? 
	* Después, tapamos la primer rendija de manera que
	$$ \bracket{1}{\psi} = 0 \quad \bracket{2}{\psi} = 1, \quad
	\bracket{q_0}{2} = f(q_0)e^{i \alpha}.$$
	Por sencillez, suponemos que $f$ y $\alpha$ son iguales para ambas rendijas. 
	¿Cuál es la probabilidad de detectar al electrón en el detector en $q_0$?  
	* Por último, con ambas rendijas libres, y los valores $$
	\bracket{1}{\psi} = 1/\sqrt{2},\quad \bracket{2}{\psi} =
	1/\sqrt{2}, \quad \bracket{q_0}{1} = \bracket{q_0}{2} =f(q_0)e^{i
	\alpha}, $$ ¿cuál es ahora la probabilidad? ¿Cómo difiere esto de
	sus expectativas?
    * Si tienen en general $n$ rendijas y $m$ detectores, con $$
	\bracket{i}{\psi} = 1/\sqrt{n},\quad  \bracket{q_s}{j} =f_j(q_s)e^{i
	\alpha_j(q_s)}, $$
    ¿cuál es la probabilidad de detección en $q_s$?
