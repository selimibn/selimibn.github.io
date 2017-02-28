---
layout: post
title:  Primer examen, resuelto (Cuántica I)
date: 2017-02-15 23:40:00
description: 
---
$$\newcommand{\ket}[1]{\left |#1 \right\rangle}
\newcommand{\bra}[1]{\left\langle#1\right|}
\newcommand{\bracket}[2]{\left\langle#1\right.|\left.#2\right\rangle}
\newcommand{\vev}[1]{\left\langle#1\right\rangle}
\newcommand{\tr}{\mathrm{Tr}}
\newcommand{\diag}{\mathrm{diag}}	
\newcommand{\id}{1\!\!1}
\newcommand{\norm}[1]{\left\lVert #1 \right\rVert}$$

**Problema 1**: *Considere un conjunto de matrices hermíticas $\gamma^1, \gamma^2, \gamma^3, \gamma^4$ que satisfacen*

$$\gamma^i \gamma^j + \gamma^j \gamma^i = 2 \delta^{i j}\id. $$

* *Muestre que los eigenvalores de $\gamma^i$ son $\pm1$.*
* *Muestre que las matrices $\gamma^i$ tienen traza nula (usando la ciclicidad de la traza).*
* *Muestre que no pueden ser matrices de dimensión impar.*
	
Primero, consideramos el caso $i=j$. En este caso, tendremos que

$$ (\gamma^i)^2 + (\gamma^i)^2 = 2\id \Rightarrow (\gamma^i)^2 = \id.$$

En la base de los eigenvectores de $\gamma^i$, esto no es sino 

$$ \mathrm{diag}( \omega^2_1, \omega^2_2, \omega^2_3, s\dots ) = \id $$

en donde $\omega_j$ es el $j$-ésimo eigenvalor de $\gamma^i$. Luego $\omega^2_j =1$ y por tanto $\omega_j = \pm 1$.

Ahora, tomemos el caso $i\neq j$ y mulqipliquemos por $\gamma^i$. Obtendremos la siguiente ecuación:

$$\gamma^i\gamma^i \gamma^j + \gamma^i\gamma^j \gamma^i = 0$$

Tomando la traza tendremos 

$$\tr(\gamma^i\gamma^i \gamma^j) = - \tr(\gamma^i\gamma^j \gamma^i ).$$ 

Usando que $(\gamma^i)^2 = \id$, más la ciclicidad de la traza, llegamos a

$$\tr( \gamma^j) = - \tr(\gamma^j ) \Rightarrow \tr( \gamma^j) = 0.$$ 

Pero esa traza no es más que la suma de los eigenvalores $\omega_j$, que además son todos iguales a $\pm 1$. De modo que esto sólo puede satisfacerse si la dimensión de la matriz es par. 



**Problema 2**: *Utilice la representación diferencial del operador de momento $P$ para mostrar que si una función de onda $\psi(q)$ tiene valor esperado de momento $\langle P \rangle$, entonces para la función $\exp(i p_o q /\hbar)\psi(q)$ el  valor esperado del momento  será $\langle P \rangle + p_0$.*

Llamamos $\psi'(q)$ a $\exp(i p_o q /\hbar)\psi(q)$. El valor de expectación será

$$ \langle \psi'(q), P \psi'(q) \rangle = \int dq e^{-i p_o q /\hbar} \psi(q)^* \frac{\hbar}{ i } \partial_q e^{i p_o q /\hbar}\psi(q)  $$

Aplicando la derivada obtenemos

$$ \langle \psi'(q), P \psi'(q) \rangle = \int dq e^{-i p_o q /\hbar} e^{i p_o q /\hbar} \psi(q)^* \frac{\hbar}{ i } \partial_q \psi(q) + \int dq e^{-i p_o q /\hbar} \psi(q)^* \frac{\hbar i p_o}{ i \hbar }   e^{i p_o q /\hbar}  \psi(q)  $$

es decir

$$ \langle \psi'(q), P \psi'(q) \rangle = \int dq \psi(q)^* \frac{\hbar}{ i } \partial_q \psi(q) + \int dq \psi(q)^* {p_o}\psi(q)  $$

ó

$$ \langle \psi'(q), P \psi'(q) \rangle = \langle \psi(q), P \psi(q) \rangle + p_o \langle \psi(q), \psi(q) \rangle  =  \langle  P \rangle + p_o. $$


**Problema 3**: *Sea $U$ una matriz unitaria que escribimos como $U = \exp( i H)$, con $H$ hermítico. Cosidere la base de los eigenestados de $H$, y muestre que 
$$ \det U  = \exp( i \tr H). $$*

Sean $\omega_i$ los eigenvalores de $H$. En la base de sus eigenestados de $H$, entonces, tendremos que

$$ H = \diag(\omega_1, \omega_2, \dots \omega_n). $$

La matriz $U$, en la misma base, tiene la forma 

$$  U  = \exp( i H) = \diag(e^{\omega_1}, e^{\omega_2}, \dots, e^{\omega_n}). $$

El determinante de una matriz diagonal es el producto de sus elementos, de modo que 

$$ \det U  = e^{\omega_1}\cdot e^{\omega_2} \cdots e^{\omega_n} = e^{\omega_1 + \omega_2+ \dots + \omega_n}. $$

Pero la suma de los eigenvalores de $H$ es justo la traza $\tr H$. Así, llegamos a

$$ \det U  = \exp( i \tr H). $$

**Problema 4**: *Calcule los eigenvalores del siguiente Hamiltoniano, que actúa sobre el producto tensorial de dos espacios de Hilbert de dos niveles:*
$$ H = E\sigma_3\otimes\id + E \id \otimes\sigma_3 +  V $$
*en donde*
$$ V = \lambda (\ket{1}\otimes\ket{-1})(\bra{-1}\otimes\bra{1}) + (\ket{-1}\otimes\ket{1})(\bra{1}\otimes\bra{-1}). $$

Vamos a etiquetar los estados de la base en el espacio producto de la siguiente manera: 

$$ \ket{1} = \ket{1}\otimes\ket{1}\quad \ket{2} = \ket{1}\otimes\ket{-1}\quad \ket{3} = \ket{-1}\otimes\ket{1}\quad \ket{4} = \ket{-1}\otimes\ket{-1}.$$

Escribiendo los términos del Hamiltoniano en este lenguaje,

$$ E\sigma_3\otimes\id = E (\ket{1}\bra{1} + \ket{2}\bra{2}- \ket{3}\bra{3} -\ket{4}\bra{4}),$$

mientras que 

$$ E\id\otimes\sigma_3 = E (\ket{1}\bra{1} - \ket{2}\bra{2} +  \ket{3}\bra{3} - \ket{4}\bra{4}),$$

y

$$ V = \lambda (\ket{2}\bra{3} + \ket{3}\bra{2}). $$

Luego 

$$ H =  2E (\ket{1}\bra{1}  -\ket{4}\bra{4}) + \lambda (\ket{2}\bra{3} + \ket{3}\bra{2}). $$

Podemos escribir las componentes de $H$ en una matriz

$$ [\bra{i}H\ket{j} ] = \begin{pmatrix} 
2E &0&0&0\\ 
0 & 0 & \lambda & 0 \\ 
0 & \lambda & 0 & 0\\
0 & 0 & 0 & -2E\end{pmatrix}. $$

La ecuación característica proviene del determinante de $H - \omega\id$:

$$ \det \begin{pmatrix} 
2E-\omega &0&0&0\\ 
0 & -\omega & \lambda & 0 \\ 
0 & \lambda & -\omega & 0\\
0 & 0 & 0 & -2E-\omega\end{pmatrix} =   (2E-\omega)( \omega^2 - \lambda^2)   (-2E-\omega) = 0. $$

Los eigenvalores son:

$$\omega_1 = -2E\quad \omega_2 = -\lambda\quad \omega_3 = \lambda\quad \omega_4 = 2E.$$

**Problema 5**: *Un estado **coherente** del oscilador armónico se define como un
eigenestado del operador $a^-$. Recuerde que $a^- \ket{n} = \sqrt{n}
\ket{n-1}$ y $a^+ \ket{n} = \sqrt{n+1} \ket{n+1}$, y que*

$$ [a^-, a^+] = 1, \quad [N, a^\pm] = \pm a^\pm. $$

1. *Evalúe  $(a^+)^n\ket{0}$.*
2. *Pruebe que $\ket{\lambda} = \exp( - |\lambda|^2/2)\exp( \lambda
   a^+)\ket{0}$ es un estado coherente.*
3. *Escriba $\ket{\lambda}= \sum_{n=0}^\infty f(n) \ket{n}$ y encuentre $f(n)$.* 

Primero, mostremos por inducción que 

$$(a^+)^n\ket{0} = \sqrt{n!} \ket{n}.$$

Sabemos que $(a^+)\ket{n} = \sqrt{n+1} \ket{n+1}$. Luego, para $n=1$, tenemos que en efecto.

$$(a^+)\ket{0} = \sqrt{1} \ket{1} = \sqrt{1!} \ket{1}.$$

Suponemos que en efecto $(a^+)^n\ket{0} = \sqrt{n!} \ket{n}$. Calculamos 

$$(a^+)^{n+1}\ket{0} = a^+ (a^+)^{n}\ket{0} = \sqrt{n!} (a^+) \ket{n}.$$  

Pero esto no es sino 

$$(a^+)^{n+1}\ket{0} =  \sqrt{n!}\sqrt{n+1}  \ket{n+1} = \sqrt{(n+1)!} \ket{n+1},  $$

como esperabamos. 

Ahora, queremos mostrar que $\ket{\lambda}$ es un estado coherente, es decir, que es un eigenestado de $a^-$. Nos interesa entonces calcular

$$a^- \ket{\lambda} = a^- \exp( - |\lambda|^2/2)\exp( \lambda
   a^+)\ket{0} = a^-  \exp(- |\lambda|^2/2) \sum_{n=0}^\infty \frac{ \lambda^n}{n!}
   (a^+)^n\ket{0}. $$

Esto es lo mismo que 

$$ a^- \ket{\lambda} =  \exp(- |\lambda|^2/2) \sum_{n=0}^\infty   \frac{ \lambda^n}{\sqrt{n!}}
   a^- \ket{n} = \exp(- |\lambda|^2/2) \sum_{n=1}^\infty    \frac{ \lambda^n}{\sqrt{n!}}
   \sqrt{n}\ket{n-1}.$$

Con el índice de suma $n' = n-1$, esto corresponde a 

$$ a^- \ket{\lambda} = \lambda  \exp(- |\lambda|^2/2) \sum_{n'=0}^\infty    \frac{ \lambda^{n'}}{\sqrt{(n')!}}
   \ket{n'} = \lambda \ket{\lambda}.$$

Identificamos, en la expansión de $\ket\lambda$, 

$$\lambda =  \sum_{n=0}^\infty f(n) \ket{n} = \sum_{n=0}^\infty   \exp(- |\lambda|^2/2) \frac{ \lambda^n}{\sqrt{n!}} \ket{n} $$

el coeficiente f(n):

$$f(n) = \exp(- |\lambda|^2/2) \frac{ \lambda^n}{\sqrt{n!}} .$$

**Problema 6**: *Considere el  estado inicial de un sistema de dos niveles con hamiltoniano $H= \omega \sigma_3$, $\ket{\psi} = \frac{1}{\sqrt{2}}\left( \ket{1} + \ket{-1} \right)$. Calcule el operador de evolución temporal y evalúe el valor de expectación de $\sigma_1$ para un tiempo $t$ posterior.*    

El operador de evolución temporal es

$$ U(t) = \exp( - i \omega \sigma_3 t/\hbar) = \id \cos \left( \frac{\omega t}{\hbar}\right) - i \sigma_3 \sin \left(\frac{\omega t}{\hbar}\right) = \diag\left( e^{ - i \omega t/\hbar}, e^{  i \omega t/\hbar} \right).$$

En el cuadro de Heisenberg, el operador depende del tiempo, y 

$$\sigma_1(t) =  U^\dagger(t)\sigma_1 U(t) = \begin{pmatrix} e^{  i \omega t/\hbar} & 0 \\ 0 & e^{ -i \omega t/\hbar} \end{pmatrix} \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} e^{ - i \omega t/\hbar} & 0 \\ 0 & e^{ i \omega t/\hbar} \end{pmatrix}  = \begin{pmatrix} 0 & e^{ 2i \omega t/\hbar} 0 \\  e^{ - 2i \omega t/\hbar} & 0 \end{pmatrix}, $$

ó

$$ \sigma_1(t) =  e^{ 2i \omega t/\hbar} \ket{1}\bra{-1} + e^{ -2i \omega t/\hbar}  \ket{-1}\bra{1}.$$

Luego el valor de expectación será

$$\bra{\psi} \sigma_1(t) \ket{\psi} = \frac{1}{2} (\bra{1} + \bra{-1} ) (  e^{ 2i \omega t/\hbar} \ket{1}\bra{-1} + e^{ -2i \omega t/\hbar}  \ket{-1}\bra{1}) (\ket{1} + \ket{-1} ),    $$

es decir, 

$$\bra{\psi} \sigma_1(t) \ket{\psi} =  \frac{1}{2} (  e^{ 2i \omega t/\hbar}  + e^{ -2i \omega t/\hbar} ) =  \cos \left(\frac{2\omega t}{\hbar}\right).$$

Alternativamente, en el cuadro de Schrödinger, el vector de estado depende del tiempo, y 

$$\ket{\psi(t)} = U(t)\ket\psi = \frac{1}{\sqrt{2}}\left( e^{ - i \omega t/\hbar} \ket{1} + e^{  i \omega t/\hbar}\ket{-1} \right).$$

El valor de expectación será en este caso 

$$\bra{\psi(t)} \sigma_1 \ket{\psi(t)} = \frac{1}{2} ( e^{ i \omega t/\hbar} \bra{1} +  e^{ -i \omega t/\hbar} \bra{-1} ) (  \ket{1}\bra{-1} + \ket{-1}\bra{1}) ( e^{ -i \omega t/\hbar}\ket{1} +  e^{ i \omega t/\hbar}\ket{-1} ),    $$

que podemos evaluar a 

$$\bra{\psi(t)} \sigma_1 \ket{\psi(t)} =  \frac{1}{2} (  e^{ 2i \omega t/\hbar}  + e^{ -2i \omega t/\hbar} ) =  \cos \left(\frac{2\omega t}{\hbar}\right).$$
