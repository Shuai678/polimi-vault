---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 15-16
  - Libro, §6.2, p. 187
---

# Discontinuità a salto

## Secondo caso della classificazione del docente

Sia $x_0\in I$ punto del dominio di accumulazione da entrambi i lati. Se esistono **finiti**

$$
\lim_{x\to x_0^-}f(x)=\ell_1\in\mathbb R,
\qquad
\lim_{x\to x_0^+}f(x)=\ell_2\in\mathbb R,
$$

ma $\ell_1\neq\ell_2$, allora $x_0$ è punto di **discontinuità di prima specie**, o **a salto**. Il salto, con la convenzione del professore, è

$$
\boxed{s(x_0)=\ell_2-\ell_1
=\text{limite destro}-\text{limite sinistro}.}
$$

Il salto è un numero con segno, non necessariamente positivo.

## Continuità da destra e da sinistra

Se $f(x_0)=\ell_2$, la funzione è **continua da destra** in $x_0$. Se $f(x_0)=\ell_1$, è **continua da sinistra**. Poiché i due limiti sono diversi, non può essere continua da entrambi i lati nello stesso punto.

Il valore nel punto decide l'eventuale continuità laterale, ma non modifica il salto, che dipende dai limiti laterali.

## Primo esempio del docente: la funzione segno

Per $f(x)=\operatorname{sign}x$,

$$
\lim_{x\to0^-}f(x)=-1,\qquad
\lim_{x\to0^+}f(x)=1.
$$

La discontinuità in zero è a salto, con

$$
s(0)=1-(-1)=+2.
$$

Con la definizione usuale del docente $f(0)=0$, la funzione non è continua né da destra né da sinistra. Cambiare il solo valore in zero non può eliminare il salto.

## Secondo esempio del docente: indicatrice di un intervallo

Per $a<b$, sia

$$
f(x)=\begin{cases}
1,&x\in(a,b),\\
0,&x\notin(a,b).
\end{cases}
$$

In $a$ il limite sinistro è $0$ e quello destro è $1$, quindi $s(a)=1-0=+1$. In $b$ il limite sinistro è $1$ e quello destro è $0$, quindi $s(b)=0-1=-1$.

Poiché gli estremi non appartengono all'intervallo aperto, $f(a)=f(b)=0$: la funzione è continua da sinistra in $a$ e da destra in $b$.

![[133 Discontinuita a Salto.svg|900]]

## Commenti: come riconoscere il caso

Calcolare i due limiti separatamente usando la formula valida sul rispettivo lato. Se entrambi sono reali e diversi, si classifica subito il salto; non occorre conoscere $f(x_0)$ per stabilirne il valore.

Per una [[132 Discontinuità Eliminabili ed Estensione per Continuità|discontinuità eliminabile]], invece, i due limiti finiti coincidono e il problema è il valore nel punto. Se almeno un limite laterale è infinito, si passa al caso di [[134 Discontinuità di Seconda Specie|seconda specie]].

### Da dire all'orale

> Una discontinuità è a salto quando i due limiti laterali esistono finiti e sono diversi. Il salto è il limite destro meno quello sinistro. La funzione è continua da un lato se il limite da quel lato coincide con il valore assegnato nel punto; modificare quel valore non elimina un salto fra i due limiti.
