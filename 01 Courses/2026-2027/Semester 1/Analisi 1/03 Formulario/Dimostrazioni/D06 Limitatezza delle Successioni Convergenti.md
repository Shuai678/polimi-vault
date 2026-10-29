---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D6
status: Da studiare
updated: 2026-10-29
source:
  - AM1-regolamento26-27.pdf, p. 2, voce 6
  - 77 Limitatezza delle Successioni Convergenti
cssclasses:
  - formulario
---

# D6 — Limitatezza delle Successioni Convergenti

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D6** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Se $a_n\to\ell\in\mathbb R$, allora la successione è limitata: esiste $K>0$ tale che

$$
|a_n|\leq K\qquad\text{per ogni indice ammesso}.
$$

L’ipotesi richiede un limite **finito**.

## Idea della dimostrazione

Il limite controlla la coda dentro una fascia fissa. I termini iniziali sono un insieme finito, quindi possiamo controllare anche quelli.

## Dimostrazione

Supponiamo che la successione inizi dall'indice $n_0$. Poiché $\ell=\lim_{n\to\infty}a_n$ esiste ed è finito, dalla **definizione di convergenza** segue che

$$
\forall\varepsilon>0\;\exists N\in\mathbb N,\ N\geq n_0:\quad
\forall n\geq N,\quad \ell-\varepsilon<a_n<\ell+\varepsilon.
$$

La disuguaglianza $\ell-\varepsilon<a_n<\ell+\varepsilon$ equivale a

$$
|a_n-\ell|<\varepsilon.
$$

In parole semplici: scelta una precisione $\varepsilon>0$, esiste un indice $N$ dopo il quale **tutti i termini** distano da $\ell$ meno di $\varepsilon$. L'indice $N$ può dipendere dalla precisione scelta.

Scegliendo in particolare $\varepsilon=1$, esiste quindi $N\geq n_0$ tale che

$$
\ell-1<a_n<\ell+1\qquad\text{per ogni }n\geq N.
$$

Il valore $1$ non ha nulla di speciale: basta una fascia di ampiezza fissa. Consideriamo ora l'insieme iniziale

$$
\{a_{n_0},a_{n_0+1},\ldots,a_N\}.
$$

È finito e non vuoto, perciò possiede un massimo $M$ e un minimo $m$, entrambi reali. Poniamo

$$
L=\max\{M,\ell+1\},\qquad P=\min\{m,\ell-1\}.
$$

Se $n_0\leq n\leq N$, allora $P\leq m\leq a_n\leq M\leq L$. Se $n\geq N$, allora $P\leq\ell-1<a_n<\ell+1\leq L$. Quindi

$$
P\leq a_n\leq L\qquad\forall n\geq n_0.
$$

Questo dimostra la tesi. Volendo una stima in valore assoluto, basta prendere $K=\max\{|P|,|L|\}+1>0$: allora $|a_n|\leq K$ per tutti gli indici.

## Da ricordare

Scegliere $arepsilon=1$ controlla soltanto la coda: devi includere i **termini iniziali**. Il viceversa è falso: $(-1)^n$ è limitata e non converge.

## Note di riferimento

[[77 Limitatezza delle Successioni Convergenti]]
