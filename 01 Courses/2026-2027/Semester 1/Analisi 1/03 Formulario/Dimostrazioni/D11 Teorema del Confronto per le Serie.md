---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D11
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 11"
  - "107 Criterio del Confronto per Serie"
cssclasses:
  - formulario
---

# D11 — Teorema del Confronto per le Serie

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D11** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Siano $0\leq a_n\leq b_n$ definitivamente. Allora:

$$
\begin{aligned}
\sum b_n\text{ converge}&\Longrightarrow\sum a_n\text{ converge},\\
\sum a_n=+\infty&\Longrightarrow\sum b_n=+\infty.
\end{aligned}
$$

Nel regolamento D11 è chiamata anche **criterio del confronto**.

## Idea della dimostrazione

Le somme parziali conservano l’ordine dei termini. Una serie non negativa converge quando le sue somme parziali sono limitate superiormente.

## Dimostrazione

Se le disuguaglianze valgono soltanto dopo $n_0$, consideriamo prima le code: per [[105 Code e Resto di una Serie]] il carattere è lo stesso. Possiamo quindi dimostrare il risultato supponendo $0\leq a_n\leq b_n$ per ogni $n\geq1$.

Poniamo

$$
S_N=\sum_{n=1}^{N}a_n,\qquad
\sigma_N=\sum_{n=1}^{N}b_n.
$$

Sommando le disuguaglianze finite,

$$
0\leq S_N\leq\sigma_N\qquad\text{per ogni }N.
$$

Entrambe le successioni sono crescenti per [[106 Serie a Termini Positivi]].

**Divergenza della minore.** Se $S_N\to+\infty$, da $\sigma_N\geq S_N$ e dal [[83 Teorema del confronto per successioni divergenti]] segue $\sigma_N\to+\infty$.

**Convergenza della maggiore.** Se $\sigma_N\to\sigma\in\mathbb R$, la crescita implica $\sigma_N\leq\sigma$. Pertanto $S_N\leq\sigma$ per ogni $N$: $(S_N)$ è crescente e limitata superiormente, quindi converge a un numero reale. La serie minore converge.

## Da ricordare

La convergenza passa alla **minore**; la divergenza positiva alla **maggiore**. Essere minori di una divergente o maggiori di una convergente non decide nulla. Il confronto delle somme totali richiede la disuguaglianza per tutti gli indici.

## Note di riferimento

[[107 Criterio del Confronto per Serie]]
