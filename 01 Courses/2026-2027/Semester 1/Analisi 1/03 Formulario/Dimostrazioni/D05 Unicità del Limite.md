---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D5
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 5"
  - "73 Unicità del Limite di Successione"
  - "74 Limiti Infiniti e Regolarità delle Successioni"
cssclasses:
  - formulario
---

# D5 — Unicità del Limite

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D5** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Se una successione reale $(a_n)$ ammette limite in $\overline{\mathbb R}=\mathbb R\cup\{-\infty,+\infty\}$, tale limite è unico.

In particolare, se $a_n\to\ell_1\in\mathbb R$ e $a_n\to\ell_2\in\mathbb R$, allora $\ell_1=\ell_2$.

## Idea della dimostrazione

Due limiti diversi avrebbero intorni disgiunti. La successione dovrebbe trovarsi definitivamente in entrambi, cosa impossibile.

## Dimostrazione

### Due limiti finiti: prova del docente

Supponiamo che la stessa successione abbia due limiti distinti $\ell_1$ e $\ell_2$. Senza perdita di generalità, sia

$$
\ell_1>\ell_2.
$$

Scegliamo

$$
\varepsilon=\frac{\ell_1-\ell_2}{3}>0.
$$

Dalla convergenza a $\ell_1$ esiste $N_1$ tale che, per ogni $n\geq N_1$,

$$
a_n\in(\ell_1-\varepsilon,\ell_1+\varepsilon).
$$

Dalla convergenza a $\ell_2$ esiste $N_2$ tale che, per ogni $n\geq N_2$,

$$
a_n\in(\ell_2-\varepsilon,\ell_2+\varepsilon).
$$

Ponendo $N=\max\{N_1,N_2\}$, per ogni $n\geq N$ il termine $a_n$ dovrebbe appartenere contemporaneamente a entrambi gli intervalli.

![[73 Unicita Limite Successione.svg|624]]

Ma gli intervalli sono disgiunti. Infatti

$$
\ell_2+\varepsilon<\ell_1-\varepsilon
$$

perché $2\varepsilon=2(\ell_1-\ell_2)/3<\ell_1-\ell_2$. Si ottiene una contraddizione. Dunque $\ell_1=\ell_2$.

### Estensione ai limiti infiniti

**Un limite finito e $+\infty$.** Se $a_n\to\ell\in\mathbb R$, definitivamente $a_n<\ell+1$. Se anche $a_n\to+\infty$, scegliendo una soglia $M>\max\{0,\ell+1\}$ avremmo definitivamente $a_n>M>\ell+1$. Prendendo il massimo delle due soglie sugli indici si ottiene una contraddizione. Il caso con $-\infty$ si tratta allo stesso modo, usando $a_n>\ell-1$ e una soglia inferiore a $\ell-1$.

**I due infiniti opposti.** Se la stessa successione tendesse sia a $+\infty$ sia a $-\infty$, definitivamente avremmo contemporaneamente $a_n>1$ e $a_n<-1$, impossibile.

Anche nella retta reale estesa il limite, quando esiste, è quindi unico.

## Da ricordare

Il massimo degli indici garantisce che le due condizioni valgano **contemporaneamente**. Il teorema non afferma che ogni successione abbia limite.

## Note di riferimento

[[73 Unicità del Limite di Successione]] · [[74 Limiti Infiniti e Regolarità delle Successioni]]
