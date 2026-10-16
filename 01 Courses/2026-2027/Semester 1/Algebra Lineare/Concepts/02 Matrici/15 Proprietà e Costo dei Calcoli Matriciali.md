---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 3, PDF pp. 13-14, pagine stampate 33-34"
---

# Proprietà e costo dei calcoli matriciali

Stato: **da studiare**.

## Perché conoscere le proprietà

La distributività

$$
\lambda(A+B)=\lambda A+\lambda B
$$

consente di ottenere lo stesso risultato con sequenze di operazioni diverse. Il professore usa questo esempio per mostrare l'importanza computazionale delle proprietà algebriche.

## Ipotesi

Siano

$$
A,B\in M_{\mathbb K}(m,n),\qquad \lambda\in\mathbb K.
$$

Le matrici hanno $mn$ entrate ciascuna. Si confrontano due procedure dirette che calcolano tutte le entrate, senza ottimizzazioni particolari per valori speciali dello scalare o delle matrici.

## Procedura 1: prima sommare

Si calcola $S=A+B$, poi si calcola $\lambda S$.

- La somma richiede $mn$ somme nel campo.
- Il prodotto per lo scalare richiede $mn$ prodotti nel campo.

Per la posizione $(i,j)$:

$$
s_{ij}=a_{ij}+b_{ij},\qquad
c_{ij}=\lambda s_{ij}.
$$

## Procedura 2: prima moltiplicare

Si calcolano $U=\lambda A$ e $V=\lambda B$, poi $U+V$.

- I due prodotti per scalare richiedono complessivamente $2mn$ prodotti nel campo.
- La somma finale richiede $mn$ somme nel campo.

Per la posizione $(i,j)$:

$$
u_{ij}=\lambda a_{ij},\quad
v_{ij}=\lambda b_{ij},\quad
c_{ij}=u_{ij}+v_{ij}.
$$

## Confronto

| Procedura | Somme | Prodotti |
|---|---|---|
| $\lambda(A+B)$ | $mn$ | $mn$ |
| $\lambda A+\lambda B$ | $mn$ | $2mn$ |

Il risparmio è di $mn$ prodotti. Non si dimezza automaticamente il tempo complessivo, perché entrambe le procedure eseguono anche somme, accessi alla memoria e altre operazioni.

Nel modello semplificato in cui somme e prodotti hanno lo stesso costo unitario, i totali sono $2mn$ e $3mn$: il loro rapporto è $3/2$. Questa è una stima del numero di operazioni, non una legge universale sui tempi.

### Esempio del tutor

Per matrici $2\times3$, $mn=6$:

- prima sommare: 6 somme e 6 prodotti;
- prima moltiplicare: 6 somme e 12 prodotti.

I valori ottenuti coincidono grazie alla [[14 Prodotto di una Matrice per uno Scalare|distributività]].

## I grafici sperimentali del PDF

A p. 14 sono riportati tempi per matrici di tipo $(1000,1500)$ al variare del numero di ripetizioni.

Nel grafico mostrato, la procedura $\lambda A+\lambda B$ richiede più tempo e il rapporto tra i tempi si avvicina a circa $1{,}5$ per molte ripetizioni.

Il grafico documenta quell'esperimento. Non dimostra che ogni implementazione, per qualunque campo, dimensione o macchina, abbia lo stesso rapporto temporale.

## Da dire all'orale

> Le proprietà algebriche consentono di scegliere procedure equivalenti con costi diversi. Per matrici m per n, calcolare prima la somma in lambda per A più B usa mn prodotti scalari, mentre distribuire lo scalare prima della somma ne usa due mn.

## Collegamenti e fonte

- [[13 Uguaglianza e Somma di Matrici]] e [[14 Prodotto di una Matrice per uno Scalare]].
- Fonte: [[GAL 2026-2027 - 20260930 - LEZIONE 3.pdf#page=13|Lezione 3, pp. 13-14, stampate 33-34]]. Il conteggio delle somme e la distinzione tra modello ed esecuzione sono esplicitati dal tutor.
