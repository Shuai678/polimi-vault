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

Stato: **da studiare**.

## Distributività

Per $A$ di tipo $(m,n)$ e $B,C$ di tipo $(n,p)$:

$$
A(B+C)=AB+AC.
$$

Infatti, per ogni $i,j$:

$$
\sum_k a_{ik}(b_{kj}+c_{kj})
=\sum_k a_{ik}b_{kj}+\sum_k a_{ik}c_{kj}.
$$

Per $A,B$ di tipo $(m,n)$ e $C$ di tipo $(n,p)$:

$$
(A+B)C=AC+BC,
$$

perché $\sum_k(a_{ik}+b_{ik})c_{kj}$ si separa nelle due somme.

## Associatività

Per $A:m\times n$, $B:n\times p$, $C:p\times q$:

$$
(AB)C=A(BC).
$$

La dimostrazione per componenti esplicitata dal tutor è:

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

## Compatibilità con gli scalari

Per $\lambda\in\mathbb K$:

$$
\lambda(AB)=(\lambda A)B=A(\lambda B).
$$

Ogni entrata vale $\lambda\sum_k a_{ik}b_{kj}=\sum_k(\lambda a_{ik})b_{kj}=\sum_k a_{ik}(\lambda b_{kj})$.

## Matrice identità

La matrice identità di ordine $n$, indicata nel PDF con $\operatorname{Id}_n$ e qui anche con $I_n$, è

$$
(I_n)_{ij}=
\begin{cases}1,&i=j,\\0,&i\ne j.\end{cases}
$$

Per ogni $A\in M_{\mathbb K}(m,n)$:

$$
I_mA=A,\qquad AI_n=A.
$$

Nel primo prodotto, nella somma $\sum_k(I_m)_{ik}a_{kj}$ sopravvive solo $k=i$. Nel secondo, in $\sum_ka_{ik}(I_n)_{kj}$ sopravvive solo $k=j$.

L'identità a sinistra ha ordine pari al numero di righe di $A$; quella a destra ha ordine pari al numero di colonne.

L'identità è un esempio di [[23 Matrici Diagonali e Triangolari|matrice diagonale]].

## Il prodotto non è commutativo

Non sempre entrambi i prodotti sono definiti. Anche quando lo sono, possono avere dimensioni o valori diversi.

Esempio del tutor con due matrici quadrate reali:

$$
A=\begin{pmatrix}1&1\\0&1\end{pmatrix},
\quad B=\begin{pmatrix}1&0\\1&1\end{pmatrix}.
$$

$$
AB=\begin{pmatrix}2&1\\1&1\end{pmatrix},
\qquad
BA=\begin{pmatrix}1&1\\1&2\end{pmatrix}.
$$

L'associatività permette di spostare parentesi, non di scambiare i fattori.

## Prodotti nulli e cancellazione

Integrazione del tutor:

$$
P=\begin{pmatrix}1&0\\0&0\end{pmatrix},
\qquad Q=\begin{pmatrix}0&0\\0&1\end{pmatrix}
$$

sono entrambe non nulle, ma $PQ=0_{2,2}$. Quindi $AB=0$ non implica che uno dei due fattori sia nullo.

Da $AB=AC$ non si può in generale cancellare $A$. Se $A$ ha un'inversa sinistra, invece, la moltiplicazione per quell'inversa dà $B=C$. Le condizioni sono in [[20 Matrici Invertibili]].

## Costo e proprietà

La p. 8 confronta sperimentalmente $A(B+C)$ e $AB+AC$. Nel calcolo diretto del primo si usa un solo prodotto matriciale; nel secondo due, con gli stessi tipi compatibili.

Il costo totale comprende anche somme e memoria: il rapporto fra i tempi del grafico non è una costante universale.

## Da dire all'orale

> Il prodotto matriciale è associativo e distributivo rispetto alla somma ed è compatibile con il prodotto per scalari. Le matrici identità sono gli elementi neutri delle dimensioni appropriate. In generale il prodotto non è commutativo.

## Collegamenti e fonti

- [[16 Prodotto Matriciale Righe per Colonne]], [[20 Matrici Invertibili]].
- [[15 Proprietà e Costo dei Calcoli Matriciali]].
- [[GAL 2026-2027 - 20261001 - LEZIONE 4.pdf#page=8|Lezione 4, pp. 8-10, stampate 42-44]].
- [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=4|Lezione 6, p. 4, stampata 48]].
