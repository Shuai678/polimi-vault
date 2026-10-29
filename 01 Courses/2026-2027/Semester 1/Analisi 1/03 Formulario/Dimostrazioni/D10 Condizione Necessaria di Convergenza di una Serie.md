---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D10
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 10"
  - "103 Condizione Necessaria di Convergenza di una Serie"
cssclasses:
  - formulario
---

# D10 — Condizione Necessaria di Convergenza di una Serie

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D10** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Se la serie $\sum_{n=0}^{+\infty}a_n$ converge a un numero reale, allora

$$
a_n\longrightarrow0.
$$

Equivalentemente: se $a_n$ non tende a zero, la serie non converge.

## Idea della dimostrazione

Un termine è la differenza fra due somme parziali consecutive. Se entrambe si avvicinano allo stesso numero finito, la differenza tende a zero.

## Dimostrazione

Per ogni $N\geq1$,

$$
S_N=\sum_{n=0}^{N-1}a_n+a_N=S_{N-1}+a_N,
\qquad a_N=S_N-S_{N-1}.
$$

Per ipotesi $S_N\to S\in\mathbb R$. Anche $S_{N-1}\to S$: togliere o spostare un numero finito di indici non cambia il limite. L'[[80 Algebra dei Limiti di Successioni|algebra dei limiti finiti]] dà

$$
\lim_{N\to+\infty}a_N
=\lim_{N\to+\infty}(S_N-S_{N-1})
=S-S=0.
$$

Non possiamo ripetere lo stesso ragionamento con $S=+\infty$ o $S=-\infty$, perché la differenza degli infiniti è una forma indeterminata.

## Da ricordare

Il viceversa è falso: $1/n	o0$, ma la serie armonica diverge. Se il termine non tende a zero puoi dire **non converge**; per distinguere divergenza e irregolarità occorre un ulteriore argomento.

## Note di riferimento

[[103 Condizione Necessaria di Convergenza di una Serie]]
