---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 13, PDF pp. 6-7
---

# Unicità del limite di funzione

## Teorema del docente

Data $f:I\subseteq\mathbb R\to\mathbb R$, sia $x_0\in\overline{\mathbb R}$ punto di accumulazione per $I$. Se esiste

$$
\lim_{x\to x_0}f(x)=\ell\in\overline{\mathbb R},
$$

allora tale limite è unico.

## Dimostrazione del professore

Per assurdo esistano $\ell_1,\ell_2\in\overline{\mathbb R}$, con $\ell_1\neq\ell_2$, e

$$
\lim_{x\to x_0}f(x)=\ell_1,\qquad
\lim_{x\to x_0}f(x)=\ell_2.
$$

Allora, per ogni successione $(x_n)\subset I$ tale che $x_n\neq x_0$ per ogni $n\geq1$ e con

$$
\lim_{n\to+\infty}x_n=x_0,
$$

deve essere contemporaneamente

$$
\lim_{n\to+\infty}f(x_n)=\ell_1
\qquad\text{e}\qquad
\lim_{n\to+\infty}f(x_n)=\ell_2,
$$

con $\ell_1\neq\ell_2$.

Assurdo per l'unicità del limite per successioni. $\square$

## Commenti alla dimostrazione

La prova segue l'ordine del PDF L13, pp. 6-7: assurdo, [[121 Limite di Funzione e Definizione Successionale|definizione successionale]], contraddizione con [[73 Unicità del Limite di Successione]] e la sua estensione ai limiti infiniti in [[74 Limiti Infiniti e Regolarità delle Successioni]]. Non serve una nuova scelta di $\varepsilon$: il risultato già dimostrato per le successioni è sufficiente.

È essenziale che esista almeno una successione ammissibile. Per $x_0$ finito, l'accumulazione consente di scegliere $x_n\in I$ con $0<|x_n-x_0|<1/n$. Per $x_0=+\infty$ si scelgono punti di $I$ maggiori di $n$; per $x_0=-\infty$ minori di $-n$. Queste scelte rendono esplicito un passaggio sottinteso dal docente.

## Conseguenze e uso negli esercizi

Il teorema garantisce che due calcoli corretti dello stesso limite, sullo stesso dominio e con lo stesso avvicinamento, non possono dare risultati diversi. Non garantisce l'esistenza del limite: $\sin x$ per $x\to+\infty$ ne è già un controesempio.

Limiti da destra e da sinistra sono problemi diversi e possono avere esiti diversi; per questo non contraddicono l'unicità. Il collegamento è precisato in [[128 Limiti Laterali e Asintoti Verticali]].

### Da dire all'orale

> Se il limite di una funzione in un punto di accumulazione del dominio esiste nella retta reale estesa, è unico. Supponendo due limiti distinti, la definizione successionale imporrebbe alla stessa successione di valori della funzione due limiti diversi, contro l'unicità del limite delle successioni.
