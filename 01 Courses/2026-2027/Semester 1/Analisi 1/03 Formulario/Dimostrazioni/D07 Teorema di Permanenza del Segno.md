---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D7
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 7"
  - "79 Teorema di Permanenza del Segno"
cssclasses:
  - formulario
---

# D7 — Teorema di Permanenza del Segno

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D7** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Sia $a_n\to\ell\in\overline{\mathbb R}$.

- Se $\ell>0$, incluso $+\infty$, allora $a_n>0$ definitivamente.
- Se $\ell<0$, incluso $-\infty$, allora $a_n<0$ definitivamente.

Inoltre, **se il limite esiste**, $a_n\geq0$ definitivamente implica $\ell\geq0$; analogamente $a_n\leq0$ definitivamente implica $\ell\leq0$.

## Idea della dimostrazione

Se il limite è diverso da zero, scegliamo una fascia attorno a esso che non attraversi lo zero.

## Dimostrazione

### 1. Limite finito positivo

Sia $0<\ell<+\infty$. Nella definizione di limite scegliamo

$$
\varepsilon=\frac\ell2>0.
$$

Esiste $N$ tale che, per ogni $n\geq N$,

$$
a_n>\ell-\varepsilon=\frac\ell2>0.
$$

Quindi $a_n>0$ definitivamente.

### 2. Limite finito negativo

Se $-\infty<\ell<0$, scegliamo $\varepsilon=-\ell/2>0$. Per tutti gli indici abbastanza grandi,

$$
a_n<\ell+\varepsilon=\frac\ell2<0.
$$

### 3. Limiti infiniti

Se $a_n\to+\infty$, la definizione con $M=1$ dà definitivamente $a_n>1>0$. Se $a_n\to-\infty$, dà definitivamente $a_n<-1<0$.

### 4. Dai termini al limite

Supponiamo $a_n\geq0$ per $n\geq N_0$ e che il limite esista. Per assurdo, se fosse $\ell<0$, la parte appena dimostrata darebbe $a_n<0$ per $n\geq N_1$.

Per $n\geq\max\{N_0,N_1\}$ avremmo insieme $a_n\geq0$ e $a_n<0$: impossibile. Dunque $\ell\geq0$. Il caso non positivo si ottiene invertendo i segni.

## Da ricordare

Termini strettamente positivi possono avere limite **zero**, come $1/n$. Il segno dei termini da solo non garantisce l’esistenza del limite.

## Note di riferimento

[[79 Teorema di Permanenza del Segno]]
