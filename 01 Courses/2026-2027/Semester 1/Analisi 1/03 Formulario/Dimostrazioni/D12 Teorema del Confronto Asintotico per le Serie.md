---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D12
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 12"
  - "109 Criterio del Confronto Asintotico per Serie"
cssclasses:
  - formulario
---

# D12 — Teorema del Confronto Asintotico per le Serie

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D12** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Siano $a_n,b_n>0$ definitivamente e

$$
a_n\sim b_n,\qquad\text{cioè}\qquad\frac{a_n}{b_n}\to1.
$$

Le serie $\sum a_n$ e $\sum b_n$ hanno lo stesso carattere: convergono entrambe oppure divergono entrambe a $+\infty$.

Più in generale vale la stessa conclusione se $a_n/b_n\to c\in(0,+\infty)$.

## Idea della dimostrazione

Un rapporto vicino a uno permette di racchiudere un termine fra due multipli positivi dell’altro. Poi usiamo il teorema del confronto.

## Dimostrazione

Dalla [[72 Limite Finito di una Successione|definizione di limite]], scegliendo la tolleranza $\varepsilon=1/2$, esiste $N_1$ tale che

$$
\frac12<\frac{a_n}{b_n}<\frac32\qquad(n\geq N_1).
$$

Scegliamo anche un indice dopo il quale $a_n,b_n>0$ e prendiamo il massimo dei due indici. Moltiplicando per $b_n>0$ otteniamo definitivamente

$$
\frac12b_n<a_n<\frac32b_n.
$$

![[109 Equivalenza e Confronto con Multipli.svg|900]]

Se $\sum b_n$ converge, il maggiorante $3b_n/2$ ha serie convergente e il confronto dà la convergenza di $\sum a_n$. Viceversa $b_n<2a_n$: se $\sum a_n$ converge, converge anche $\sum b_n$.

Se $\sum b_n$ diverge positivamente, dal minorante $a_n>b_n/2$ segue la divergenza di $\sum a_n$. Viceversa, da $b_n>2a_n/3$ segue la divergenza di $\sum b_n$ quando diverge $\sum a_n$. Le costanti positive non cambiano il carattere, per [[101 Linearità e Algebra delle Serie]]. Tutti i confronti sono sufficienti nella coda.

### Rapporto tendente a $c>0$ finito

Se $a_n/b_n\to c\in(0,+\infty)$, allora $a_n/(cb_n)\to1$. Il caso dimostrato confronta $\sum a_n$ con $\sum cb_n$; moltiplicare per la costante positiva $c$ non cambia il carattere di $\sum b_n$.

## Da ricordare

**Stesso carattere** non significa stessa somma. La positività definitiva è essenziale: l’equivalenza delle ampiezze, da sola, non trasferisce la convergenza di una serie alternata.

## Note di riferimento

[[109 Criterio del Confronto Asintotico per Serie]]
