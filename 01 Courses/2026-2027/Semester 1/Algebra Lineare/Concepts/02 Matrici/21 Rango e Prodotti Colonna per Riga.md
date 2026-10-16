---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 6, PDF pp. 4-6, stampate 48-50"
---

# Rango e prodotti colonna per riga

Stato: **da studiare**.

## La definizione adottata dal professore

Il prodotto di una colonna $C\in M_{\mathbb K}(m,1)$ per una riga $R\in M_{\mathbb K}(1,n)$ è una matrice $m\times n$ con entrate

$$
(CR)_{ij}=c_ir_j.
$$

Tutte le righe sono multipli della stessa riga $R$; tutte le colonne sono multipli della stessa colonna $C$.

### Definizione 6.3

Il rango di $A\in M_{\mathbb K}(m,n)$ è il minimo numero di prodotti colonna-riga necessari per ottenere $A$ come somma:

$$
r(A)=\min\left\{
q\in\mathbb N_0:
A=\sum_{\ell=1}^{q}C_\ell R_\ell,\
C_\ell\in M_{\mathbb K}(m,1),\
R_\ell\in M_{\mathbb K}(1,n)
\right\}.
$$

Si ammette $q=0$: la somma senza addendi è la matrice nulla. Questa convenzione rende esplicita la proprietà $r(A)=0\iff A=0$.

Il rango misura qui una complessità algebrica della rappresentazione. Non viene definito come numero di entrate non nulle.

## Perché una decomposizione esiste

Indichiamo con $e_i$ la colonna che ha 1 nella posizione $i$ e 0 nelle altre. Se $R_i(A)$ è la riga $i$ di $A$:

$$
A=\sum_{i=1}^{m}e_iR_i(A).
$$

Ogni addendo ricostruisce una sola riga e lascia nulle le altre.

Analogamente, usando le colonne $C_j(A)$ e le righe canoniche:

$$
A=\sum_{j=1}^{n}C_j(A)e_j^{\mathrm{riga}}.
$$

Quindi

$$
0\le r(A)\le\min(m,n).
$$

Se $r(A)=0$, $A$ è la somma vuota e dunque nulla. La matrice nulla ammette la somma vuota, quindi ha rango 0.

## Esempio del professore

$$
A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}
=
\begin{pmatrix}1\\0\end{pmatrix}
\begin{pmatrix}1&2&3\end{pmatrix}
+
\begin{pmatrix}0\\1\end{pmatrix}
\begin{pmatrix}4&5&6\end{pmatrix}.
$$

La decomposizione dimostra $r(A)\le2$. Una decomposizione sulle tre colonne dimostrerebbe soltanto $r(A)\le3$.

Per ottenere l'uguaglianza si deve escludere un solo addendo. Se $A=CR$, la seconda riga dovrebbe essere quattro volte la prima, perché nella prima colonna compaiono 1 e 4. Ma $4(1,2,3)=(4,8,12)\ne(4,5,6)$. Dunque $r(A)\ne1$; essendo $A\ne0$, si conclude $r(A)=2$.

Quest'ultimo controllo del minimo è esplicitato dal tutor.

## Probabilità congiunte

La matrice $2\times6$ con tutte le entrate $1/12$ si scrive

$$
P=
\begin{pmatrix}\frac12\\\frac12\end{pmatrix}
\begin{pmatrix}\frac16&\frac16&\frac16&\frac16&\frac16&\frac16\end{pmatrix}.
$$

Poiché $P\ne0$, la presenza di un solo prodotto implica $r(P)=1$.

Per una tabella di probabilità congiunte, l'indipendenza delle due variabili significa

$$
p_{ij}=p_iq_j,
$$

dove $p_i$ e $q_j$ sono le probabilità marginali. La tabella diventa il prodotto della colonna delle prime marginali per la riga delle seconde.

Viceversa, una tabella di probabilità di rango 1 fattorizza nelle proprie marginali. Se $P=uv$, ponendo $\alpha=\sum_i u_i$ e $\beta=\sum_jv_j$ si ha $\alpha\beta=\sum_{ij}p_{ij}=1$. Le marginali sono $p_i=u_i\beta$, $q_j=\alpha v_j$, quindi $p_iq_j=u_iv_j=p_{ij}$.

Questa verifica esplicita il criterio del PDF. Si applica a una tabella reale non negativa con somma totale 1, non a una matrice arbitraria.

## Il problema dei due dadi

A p. 6 il professore propone di confrontare la parità del primo dado con la parità della somma dei due dadi. La tabella e la soluzione completa, assumendo dadi equi e indipendenti, sono in [[05 Rango Laplace e Matrici Triangolari]].

## Da dire all'orale

> Il rango di una matrice è il minimo numero di prodotti di una colonna per una riga la cui somma ricostruisce la matrice. È compreso tra zero e il minimo tra numero di righe e numero di colonne.

## Collegamenti e fonte

- [[16 Prodotto Matriciale Righe per Colonne]].
- [[27 Calcolo del Rango con Gauss]]: il minimo si calcola contando i pivot dopo eliminazione.
- Fonte: [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=4|Lezione 6, pp. 4-6, stampate 48-50]].
