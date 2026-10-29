---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D8
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 8"
  - "82 Teorema dei Due Carabinieri"
cssclasses:
  - formulario
---

# D8 — Teorema dei Due Carabinieri

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D8** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Siano $a_n\leq b_n\leq c_n$ definitivamente. Se

$$
a_n\to\ell,\qquad c_n\to\ell,\qquad\ell\in\mathbb R,
$$

allora anche $b_n\to\ell$.

I due limiti esterni devono essere **lo stesso numero**; non si assume che il limite di $b_n$ esista già.

## Idea della dimostrazione

Se due barriere si avvicinano allo stesso numero, una successione che resta fra esse deve avvicinarsi a quel numero. I termini intermedi possono oscillare: ciò che conta è il controllo fra le barriere.

![[82 Due Carabinieri.svg|740]]

## Dimostrazione

Fissiamo $\varepsilon>0$. Dalla convergenza di $a_n$ esiste $N_1$ tale che

$$
\ell-\varepsilon<a_n<\ell+\varepsilon\qquad(n\geq N_1).
$$

Dalla convergenza di $c_n$ esiste $N_2$ tale che

$$
\ell-\varepsilon<c_n<\ell+\varepsilon\qquad(n\geq N_2).
$$

Il confronto definitivo fornisce un terzo indice $N_3$ tale che $a_n\leq b_n\leq c_n$ per $n\geq N_3$. Poniamo

$$
N=\max\{N_1,N_2,N_3\}.
$$

Per ogni $n\geq N$ tutte le condizioni valgono insieme, quindi

$$
\ell-\varepsilon<a_n\leq b_n\leq c_n<\ell+\varepsilon.
$$

Ne segue $|b_n-\ell|<\varepsilon$, esattamente la definizione di $b_n\to\ell$.

## Da ricordare

Si prende il massimo di **tre soglie**: quelle dei due limiti e quella del confronto definitivo.

## Note di riferimento

[[82 Teorema dei Due Carabinieri]]
