---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D14
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 14"
  - "114 Convergenza Assoluta e Semplice delle Serie"
cssclasses:
  - formulario
---

# D14 — Convergenza Assoluta Implica Convergenza Semplice

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D14** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Sia $(a_n)$ una successione reale. Se la serie dei valori assoluti converge,

$$
\sum_{n=n_0}^{+\infty}|a_n|<+\infty,
$$

allora converge anche $\sum_{n=n_0}^{+\infty}a_n$. Inoltre

$$
\left|\sum_{n=n_0}^{+\infty}a_n\right|
\leq\sum_{n=n_0}^{+\infty}|a_n|.
$$

## Idea della dimostrazione

Aggiungiamo $|a_n|$ per ottenere termini non negativi e usiamo il [[107 Criterio del Confronto per Serie|criterio del confronto]]. Poi sottraiamo due successioni di somme parziali con limite finito.

## Dimostrazione

### 1. Un confronto fra termini non negativi

Da $-|a_n|\leq a_n\leq|a_n|$, sommando $|a_n|$, otteniamo

$$
0\leq a_n+|a_n|\leq2|a_n|.
$$

La serie $\sum2|a_n|$ converge per ipotesi e [[101 Linearità e Algebra delle Serie|linearità]]. Per il [[107 Criterio del Confronto per Serie]] converge dunque anche $\sum(a_n+|a_n|)$.

### 2. Recuperare le somme parziali originarie

Poniamo

$$
P_N=\sum_{n=n_0}^{N}(a_n+|a_n|),
\qquad Q_N=\sum_{n=n_0}^{N}|a_n|.
$$

Esistono $P,Q\in\mathbb R$ tali che $P_N\to P$, $Q_N\to Q$. Per ogni indice finito $N$,

$$
S_N=\sum_{n=n_0}^{N}a_n=P_N-Q_N.
$$

L'[[80 Algebra dei Limiti di Successioni|algebra dei limiti finiti]] dà $S_N\to P-Q\in\mathbb R$. La serie originaria converge semplicemente. Non abbiamo separato serie di carattere ancora ignoto: abbiamo prima lavorato con somme finite e provato i limiti necessari.

### 3. La stima del modulo della somma

Per la [[30 Disuguaglianza Triangolare|disuguaglianza triangolare]], applicata ripetutamente a una somma finita,

$$
|S_N|=\left|\sum_{n=n_0}^{N}a_n\right|
\leq\sum_{n=n_0}^{N}|a_n|=Q_N.
$$

Se $S_N\to S$, anche $|S_N|\to|S|$, perché

$$
\bigl||S_N|-|S|\bigr|\leq|S_N-S|\to0.
$$

Passando al limite nella disuguaglianza otteniamo $|S|\leq Q$, cioè la stima del teorema.

Usando direttamente la continuità del valore assoluto e la [[79 Teorema di Permanenza del Segno|permanenza del segno]], da $|S_N|\leq Q_N$ per ogni $N$ otteniamo

$$
|S|=\lim_{N\to+\infty}|S_N|
\leq\lim_{N\to+\infty}Q_N=Q,
$$

ossia

$$
\left|\sum_{n=n_0}^{+\infty}a_n\right|
\leq\sum_{n=n_0}^{+\infty}|a_n|.
$$

## Da ricordare

Il viceversa è falso: $\sum_{n=1}^{\infty}(-1)^{n+1}/n$ converge per Leibniz, ma la serie dei moduli è l’armonica e diverge. **Semplice** da solo non esclude **assoluta**; **solo semplice** significa convergente ma non assolutamente.

## Note di riferimento

[[114 Convergenza Assoluta e Semplice delle Serie]]
