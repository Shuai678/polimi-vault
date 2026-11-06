---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 13, PDF pp. 2
  - Libro, §5.1, p. 131
---

# Intorni finiti e infiniti

## Definizioni del docente

Per $x_0\in\mathbb R$, un **intorno simmetrico** di $x_0$ è un insieme della forma

$$
\mathcal U(x_0)=(x_0-\varepsilon,x_0+\varepsilon),\qquad\varepsilon>0.
$$

Un **intorno di $+\infty$** è un insieme della forma

$$
\mathcal U(+\infty)=(M,+\infty),\qquad M\in\mathbb R.
$$

Un **intorno di $-\infty$** è un insieme della forma

$$
\mathcal U(-\infty)=(-\infty,M),\qquad M\in\mathbb R.
$$

Tutti questi intorni sono sottoinsiemi di $\mathbb R$. Come osserva il professore, il punto finito $x_0$ appartiene a ogni suo intorno simmetrico, mentre $+\infty\notin\mathcal U(+\infty)$ e $-\infty\notin\mathcal U(-\infty)$: gli infiniti non sono numeri reali.

## Commenti: perché introdurre gli intorni

Un intorno descrive una zona nella quale imponiamo una condizione. Vicino a un punto finito restringiamo un intervallo; vicino a $+\infty$ superiamo una soglia; vicino a $-\infty$ scendiamo sotto una soglia. Questo permette di scrivere una sola [[123 Definizione Topologica di Limite e Teorema Ponte|definizione di limite]] che comprende tutti i casi.

Per il punto finito, usando [[29 Valore Assoluto|valore assoluto e distanza]],

$$
x\in(x_0-\varepsilon,x_0+\varepsilon)
\iff |x-x_0|<\varepsilon.
$$

Se vogliamo escludere il centro, usiamo l'**intorno privato del punto**:

$$
\mathcal U(x_0)\setminus\{x_0\},
\qquad 0<|x-x_0|<\varepsilon.
$$

![[119 Intorni Finiti e Infiniti.svg|900]]

## Esempi e uso della notazione

Per $x_0=2$ ed $\varepsilon=1/4$, l'intorno è $(7/4,9/4)$. Il punto $2$ è incluso, i due estremi sono esclusi. Per $+\infty$, $(100,+\infty)$ è un intorno; $(1000,+\infty)$ ne è uno più ristretto. Per $-\infty$, $(-\infty,-1000)$ è più ristretto di $(-\infty,-100)$.

La lettera $\mathcal U(x_0)$ indica **un** intorno, non un intervallo unico fissato una volta per tutte. Quando leggiamo “per ogni intorno”, la proprietà deve valere anche restringendolo arbitrariamente.

## Errori comuni e connessioni

Non includere gli infiniti negli intervalli. Non confondere “$x$ è in un intorno” con “$x=x_0$”: il primo descrive vicinanza. Nelle definizioni di limite useremo i punti del **dominio** che stanno nell'intorno; non occorre che l'intero intorno sia contenuto nel dominio.

Questa è la base dei [[120 Punti di Accumulazione]] e generalizza gli intervalli già studiati in [[31 Retta Reale e Intervalli]].

### Da dire all'orale

> Un intorno simmetrico di un punto reale è un intervallo aperto centrato nel punto e di raggio positivo. Un intorno di più infinito è una semiretta aperta superiore; un intorno di meno infinito è una semiretta aperta inferiore. Gli intorni degli infiniti sono comunque insiemi di numeri reali.
