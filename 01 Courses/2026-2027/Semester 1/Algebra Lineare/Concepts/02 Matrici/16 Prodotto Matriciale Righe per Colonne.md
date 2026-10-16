---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 4, PDF pp. 2-4, stampate 36-38"
---

# Prodotto matriciale righe per colonne

Stato: **da studiare**.

## Definizione e dimensioni

Siano $A\in M_{\mathbb K}(m,n)$ e $B\in M_{\mathbb K}(n,p)$. Il prodotto $AB$ è la matrice $C\in M_{\mathbb K}(m,p)$ definita da

$$
c_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}
=a_{i1}b_{1j}+\cdots+a_{in}b_{nj}.
$$

Le colonne di $A$ e le righe di $B$ devono essere in ugual numero. Le dimensioni esterne determinano quelle del risultato:

$$
(m\times n)(n\times p)\longrightarrow m\times p.
$$

Per ottenere $c_{ij}$ si usa la riga $i$ di $A$ e la colonna $j$ di $B$. L'indice $k$ percorre le loro posizioni corrispondenti; si moltiplicano i valori e poi si sommano i prodotti nel campo $\mathbb K$.

![[16 Prodotto Righe per Colonne.svg|1000]]

Lo schema del tutor evidenzia la seconda riga e la terza colonna: $c_{23}=3(-1)+4\cdot2=5$. I colori indicano posizioni, non coordinate geometriche.

## Caso riga per colonna

Se $A$ è $1\times n$ e $B$ è $n\times1$, il risultato è $1\times1$:

$$
\begin{pmatrix}a_1&\cdots&a_n\end{pmatrix}
\begin{pmatrix}b_1\\\vdots\\b_n\end{pmatrix}
=\begin{pmatrix}\sum_{k=1}^na_kb_k\end{pmatrix}.
$$

Si può identificare la matrice con una sola entrata con il suo valore nel campo. Non si confonde questa operazione con il prodotto per scalare.

## Esempio del professore svolto interamente

Su $\mathbb R$:

$$
A=\begin{pmatrix}1&2\\3&4\end{pmatrix},
\qquad
B=\begin{pmatrix}0&1&-1\\0&-1&2\end{pmatrix}.
$$

Il prodotto è definito: $(2\times2)(2\times3)$ dà una matrice $2\times3$.

$$
\begin{aligned}
c_{11}&=1\cdot0+2\cdot0=0,\\
c_{12}&=1\cdot1+2(-1)=1-2=-1,\\
c_{13}&=1(-1)+2\cdot2=-1+4=3,\\
c_{21}&=3\cdot0+4\cdot0=0,\\
c_{22}&=3\cdot1+4(-1)=3-4=-1,\\
c_{23}&=3(-1)+4\cdot2=-3+8=5.
\end{aligned}
$$

Quindi

$$
AB=\begin{pmatrix}0&-1&3\\0&-1&5\end{pmatrix}.
$$

$BA$ non è definito per queste due matrici: richiederebbe di moltiplicare una $2\times3$ per una $2\times2$, ma $3\ne2$.

## Colonna per riga

L'ordine inverso del caso riga-colonna dà un oggetto diverso:

$$
\begin{pmatrix}b_1\\\vdots\\b_n\end{pmatrix}
\begin{pmatrix}a_1&\cdots&a_n\end{pmatrix}
=
\begin{pmatrix}
b_1a_1&\cdots&b_1a_n\\
\vdots&&\vdots\\
b_na_1&\cdots&b_na_n
\end{pmatrix}.
$$

Il risultato è $n\times n$ e ha $n^2$ entrate. Questo prodotto è la base della definizione di [[21 Rango e Prodotti Colonna per Riga|rango]] adottata nella Lezione 6.

## Procedimento e controlli

1. Scrivere le dimensioni dei due fattori.
2. Controllare la compatibilità interna.
3. Preparare il risultato con le dimensioni esterne.
4. Calcolare ciascuna entrata con la riga e la colonna appropriate.
5. Controllare separatamente segni, numero di addendi e campo usato.

Il prodotto non è posizione per posizione e l'ordine dei fattori va conservato.

## Da dire all'orale

> Il prodotto di una matrice m per n con una matrice n per p è una matrice m per p. L'entrata i, j è la somma dei prodotti tra gli elementi corrispondenti della riga i del primo fattore e della colonna j del secondo.

## Collegamenti e fonte

- [[11 Matrici come Funzioni e Indici]], [[14 Prodotto di una Matrice per uno Scalare]].
- [[17 Prodotto Matriciale e Composizione]], [[19 Proprietà del Prodotto e Matrice Identità]].
- Fonte: [[GAL 2026-2027 - 20261001 - LEZIONE 4.pdf#page=2|Lezione 4, pp. 2-4, stampate 36-38]].
