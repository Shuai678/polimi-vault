---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 4, PDF pp. 8-10, stampate 42-44"
  - "Lezione 6, PDF p. 4, stampata 48"
---

# Proprietà del prodotto e matrice identità

Il prodotto righe per colonne è l'operazione

$$
M_{\mathbb K}(m,n)\times M_{\mathbb K}(n,p)
\longrightarrow M_{\mathbb K}(m,p),
\qquad (A,B)\longmapsto AB.
$$

## Proprietà distributiva a destra

Per ogni $A\in M_{\mathbb K}(m,n)$ e $B,C\in M_{\mathbb K}(n,p)$:

$$
A\underbrace{(B+C)}_{\color{#1E6FFF}{\in M_{\mathbb K}(n,p)}}
=
\underbrace{AB+AC}_{\color{#388E3C}{\in M_{\mathbb K}(m,p)}}.
$$

Infatti, per ogni $i,j$:

$$
\sum_k a_{ik}(b_{kj}+c_{kj})
=\sum_k a_{ik}b_{kj}+\sum_k a_{ik}c_{kj}.
$$

La somma $B+C$ riguarda il fattore a destra e appartiene a $M_{\mathbb K}(n,p)$: a questa somma si riferisce l'**annotazione blu**.

Dopo la moltiplicazione per $A$, il risultato $A(B+C)$ appartiene a $M_{\mathbb K}(m,p)$. Anche $AB+AC$ appartiene a questo insieme, come indicato dall'**annotazione verde**. Entrambi i membri dell'uguaglianza hanno quindi dimensioni $m\times p$.

### Attenzione all'efficienza computazionale

Nella p. 8 del PDF si confrontano sperimentalmente $A(B+C)$ e $AB+AC$. Nel calcolo diretto del primo si usa un solo prodotto matriciale; nel secondo due, con gli stessi tipi compatibili.

Il costo totale comprende anche somme e memoria: il rapporto fra i tempi del grafico non è una costante universale.

## Proprietà distributiva a sinistra

Per ogni $A,B\in M_{\mathbb K}(m,n)$ e $C\in M_{\mathbb K}(n,p)$:

$$
(A+B)C=AC+BC,
$$

perché $\sum_k(a_{ik}+b_{ik})c_{kj}$ si separa nelle due somme.

La somma $A+B$ riguarda il fattore a sinistra. Entrambi i membri appartengono a $M_{\mathbb K}(m,p)$.

## Proprietà associativa

Per ogni $A\in M_{\mathbb K}(m,n)$, $B\in M_{\mathbb K}(n,p)$ e $C\in M_{\mathbb K}(p,q)$:

$$
(AB)C=A(BC)=ABC.
$$

Per ogni posizione $(i,j)$ si ha:

$$
\begin{aligned}
((AB)C)_{ij}
&=\sum_{\ell=1}^p\left(\sum_{k=1}^n a_{ik}b_{k\ell}\right)c_{\ell j}\\
&=\sum_{k=1}^n a_{ik}\left(\sum_{\ell=1}^p b_{k\ell}c_{\ell j}\right)\\
&=(A(BC))_{ij}.
\end{aligned}
$$

Si usano associatività e distributività nel campo e si riordinano somme finite. Il risultato ha tipo $(m,q)$.

I due prodotti intermedi hanno tipi diversi: $AB$ è $m\times p$, mentre $BC$ è $n\times q$. L'uguaglianza riguarda i risultati finali.

## Proprietà di omogeneità

Per ogni $\lambda\in\mathbb K$, $A\in M_{\mathbb K}(m,n)$ e $B\in M_{\mathbb K}(n,p)$:

$$
\lambda(AB)=(\lambda A)B=A(\lambda B).
$$

Ogni entrata vale $\lambda\sum_k a_{ik}b_{kj}=\sum_k(\lambda a_{ik})b_{kj}=\sum_k a_{ik}(\lambda b_{kj})$.

## Esistenza dell'elemento neutro (rispetto al prodotto)

Per le matrici di tipo $(m,n)$ si distinguono un elemento neutro a destra e uno a sinistra.

### A destra

Esiste una matrice $N_D\in M_{\mathbb K}(n,n)$ tale che

$$
AN_D=A
\qquad
\forall A\in M_{\mathbb K}(m,n).
$$

### A sinistra

Esiste una matrice $N_S\in M_{\mathbb K}(m,m)$ tale che

$$
N_SA=A
\qquad
\forall A\in M_{\mathbb K}(m,n).
$$

## Definizione: matrice identità

La matrice identità di tipo $(k,k)$ si indica con $\operatorname{Id}_k$ ed è

$$
\operatorname{Id}_k=
\begin{bmatrix}
1&0&\cdots&0\\
0&1&\ddots&\vdots\\
\vdots&\ddots&\ddots&0\\
0&\cdots&0&1
\end{bmatrix}
\in M_{\mathbb K}(k,k).
$$

Le sue entrate sono:

$$
(\operatorname{Id}_k)_{ij}=
\begin{cases}1,&i=j,\\0,&i\ne j.\end{cases}
$$

Gli elementi neutri sono quindi

$$
N_D=\operatorname{Id}_n,
\qquad
N_S=\operatorname{Id}_m.
$$

Per ogni $A\in M_{\mathbb K}(m,n)$:

$$
\operatorname{Id}_mA=A,
\qquad
A\operatorname{Id}_n=A.
$$

Nel primo prodotto, nella somma $\sum_k(\operatorname{Id}_m)_{ik}a_{kj}$ sopravvive solo $k=i$. Nel secondo, in $\sum_ka_{ik}(\operatorname{Id}_n)_{kj}$ sopravvive solo $k=j$.

L'identità a sinistra ha ordine pari al numero di righe di $A$; quella a destra ha ordine pari al numero di colonne.

## Definizione: diagonale principale e matrici diagonali

Le entrate nelle posizioni $(i,i)$ formano la **diagonale principale** di una matrice.

Una matrice quadrata si dice **diagonale** quando tutte le entrate fuori dalla diagonale principale sono nulle. Le entrate sulla diagonale possono anche essere nulle.

La matrice identità $\operatorname{Id}_n$ e la matrice nulla quadrata sono esempi di [[23 Matrici Diagonali e Triangolari|matrici diagonali]].

![[19 Diagonale Principale e Matrici Diagonali - Diagrammi del Professore.png|1000]]

Il **verde** evidenzia la diagonale principale. Gli asterischi indicano entrate qualsiasi del campo $\mathbb K$, anche nulle. Nell'ultimo esempio, evidenziato in **rosso**, i due $1$ sono fuori dalla diagonale principale: la matrice non è quindi diagonale.

Fonte dei diagrammi: [[GAL 2026-2027 - 20261001 - LEZIONE 4.pdf#page=10|Lezione 4, PDF p. 10, pagina stampata 44]].

## Il prodotto non è commutativo

Non sempre entrambi i prodotti sono definiti. Anche quando lo sono, possono avere dimensioni o valori diversi.

Si considerano due matrici quadrate reali:

$$
A=\begin{bmatrix}1&1\\0&1\end{bmatrix},
\quad B=\begin{bmatrix}1&0\\1&1\end{bmatrix}.
$$

$$
AB=\begin{bmatrix}2&1\\1&1\end{bmatrix},
\qquad
BA=\begin{bmatrix}1&1\\1&2\end{bmatrix}.
$$

L'associatività permette di spostare parentesi, non di scambiare i fattori.

## Prodotti nulli e cancellazione

Si considerano le matrici:

$$
P=\begin{bmatrix}1&0\\0&0\end{bmatrix},
\qquad Q=\begin{bmatrix}0&0\\0&1\end{bmatrix}.
$$

Entrambe sono non nulle, ma $PQ=0_{2,2}$. Quindi $AB=0$ non implica che uno dei due fattori sia nullo.

Da $AB=AC$ non si può in generale cancellare $A$. Se $A$ ha un'inversa sinistra, invece, la moltiplicazione per quell'inversa dà $B=C$. Le condizioni sono in [[20 Matrici Invertibili]].

## Da dire all'orale

> Il prodotto matriciale soddisfa le proprietà distributive a destra e a sinistra, la proprietà associativa e la proprietà di omogeneità. Per ogni $A\in M_{\mathbb K}(m,n)$, l'elemento neutro a destra è $N_D=\operatorname{Id}_n$ e quello a sinistra è $N_S=\operatorname{Id}_m$. In generale il prodotto non è commutativo.

## Collegamenti e fonti

- [[16 Prodotto Matriciale Righe per Colonne]], [[20 Matrici Invertibili]].
- [[15 Proprietà e Costo dei Calcoli Matriciali]].
- [[GAL 2026-2027 - 20261001 - LEZIONE 4.pdf#page=8|Lezione 4, pp. 8-10, stampate 42-44]].
- [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=4|Lezione 6, p. 4, stampata 48]].
