---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 13, PDF pp. 2-4
  - Libro, §5.1, pp. 131-132
---

# Punti di accumulazione

## Definizione del docente

Siano $I\subseteq\mathbb R$ e $x_0\in\overline{\mathbb R}=\mathbb R\cup\{-\infty,+\infty\}$. Il punto $x_0$ è un **punto di accumulazione per $I$** se e solo se ogni suo [[119 Intorni Finiti e Infiniti|intorno]] soddisfa

$$
\boxed{(\mathcal U(x_0)\cap I)\setminus\{x_0\}\neq\varnothing.}
$$

Esistono quindi elementi di $I$ diversi da $x_0$ in ogni intorno di $x_0$. Il docente precisa che **$x_0$ può appartenere a $I$ oppure no**.

## Esempi del docente, nello stesso ordine

### Intervalli fra $1$ e $2$

Per ciascuno degli insiemi $(1,2)$, $[1,2)$, $[1,2]$, $(1,2]$, l'insieme dei punti di accumulazione è $[1,2]$. Anche gli estremi esclusi sono avvicinabili con punti dell'intervallo: per esempio $1+1/n\to1$ e $2-1/n\to2$, prendendo gli indici sufficientemente grandi.

### Semirette da $3$

Per $I=(3,+\infty)$ oppure $I=[3,+\infty)$, i punti di accumulazione nella retta estesa sono

$$
[3,+\infty)\cup\{+\infty\}.
$$

Il punto $3$ è avvicinabile da destra; ogni reale maggiore di $3$ è avvicinabile dall'interno; ogni intorno di $+\infty$ contiene elementi di $I$. Nessun punto minore di $3$, e nemmeno $-\infty$, soddisfa la definizione.

### Naturali

Per $I=\mathbb N$, l'unico punto di accumulazione nella retta estesa è $+\infty$. Ogni naturale è separabile dagli altri con un intervallo di raggio minore di $1/2$. Anche per un reale non naturale possiamo scegliere un intervallo che non contiene naturali. Invece ogni semiretta superiore contiene naturali arbitrariamente grandi.

### Razionali

Per $I=\mathbb Q$, l'insieme dei punti di accumulazione è tutta $\overline{\mathbb R}$. Ogni intervallo reale contiene razionali diversi dal centro, per la [[32 Densità dei Razionali nei Reali|densità]]; inoltre i razionali sono illimitati sia superiormente sia inferiormente.

## Commenti: leggere la definizione negli esercizi

Per $x_0\in\mathbb R$, la definizione equivale a

$$
\forall\delta>0\ \exists x\in I:\quad0<|x-x_0|<\delta.
$$

Per $x_0=+\infty$ significa $\forall M\in\mathbb R\ \exists x\in I$ con $x>M$: è l'illimitatezza superiore. Per $x_0=-\infty$ significa illimitatezza inferiore.

![[120 Punti di Accumulazione.svg|900]]

Un punto appartenente all'insieme ma isolato dagli altri non è di accumulazione. Per esempio, per $I=\{0\}\cup(1,2)$, l'intorno $(-1/2,1/2)$ contiene di $I$ soltanto $0$; tolto il centro, l'intersezione è vuota.

## Perché è un'ipotesi necessaria per il limite

Nel [[121 Limite di Funzione e Definizione Successionale|limite di funzione]] dobbiamo poter avvicinare $x_0$ attraverso punti del dominio diversi da $x_0$. Senza accumulazione, una condizione su un intorno privato del centro potrebbe essere soddisfatta senza controllare alcun valore della funzione, e non determinerebbe un limite unico.

### Da dire all'orale

> Un punto, finito o infinito nella retta estesa, è di accumulazione per un insieme se ogni suo intorno contiene almeno un punto dell'insieme diverso dal punto considerato. L'appartenenza all'insieme e l'essere punto di accumulazione sono proprietà distinte.
