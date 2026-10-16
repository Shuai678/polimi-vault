---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 4, PDF p. 10, stampata 44"
  - "Lezione 6, PDF pp. 10-11, stampate 54-55"
---

# Matrici diagonali e triangolari

Stato: **da studiare**.

## Diagonale principale e matrici diagonali

In una matrice quadrata, la diagonale principale contiene le posizioni $(i,i)$. Una matrice è **diagonale** se tutte le entrate fuori da questa diagonale sono nulle.

Gli elementi diagonali possono essere zero. Sono diagonali sia $I_n$ sia $0_{n,n}$.

La matrice

$$
\begin{pmatrix}0&1\\1&0\end{pmatrix}
$$

non è diagonale: i due 1 sono fuori dalla diagonale principale.

## Definizione 6.5

Una matrice quadrata $T=(t_{ij})$ è:

- **triangolare superiore** se $t_{ij}=0$ per ogni $i>j$;
- **triangolare inferiore** se $t_{ij}=0$ per ogni $i<j$.

Nel primo caso gli zeri obbligatori stanno sotto la diagonale, nel secondo sopra.

$$
T_{\mathrm{sup}}=
\begin{pmatrix}
t_{11}&t_{12}&t_{13}\\
0&t_{22}&t_{23}\\
0&0&t_{33}
\end{pmatrix},
\qquad
T_{\mathrm{inf}}=
\begin{pmatrix}
t_{11}&0&0\\
t_{21}&t_{22}&0\\
t_{31}&t_{32}&t_{33}
\end{pmatrix}.
$$

Una matrice è diagonale esattamente quando è sia triangolare superiore sia triangolare inferiore.

## Determinante di una triangolare

Il risultato del professore è

$$
\boxed{\det T=t_{11}t_{22}\cdots t_{nn}.}
$$

### Dimostrazione per la triangolare superiore

Per $n=1$ coincide con la definizione.

Per $n>1$ si sviluppa sulla prima colonna. Sotto $t_{11}$ ci sono soltanto zeri:

$$
\det T=t_{11}\det\widehat T_{11}.
$$

La matrice $\widehat T_{11}$ è ancora triangolare superiore, con diagonale $t_{22},\ldots,t_{nn}$. Applicando lo stesso ragionamento o l'ipotesi induttiva:

$$
\det T=t_{11}(t_{22}\cdots t_{nn}).
$$

Per una triangolare inferiore si sviluppa invece sulla prima riga. La dimostrazione non richiede che gli elementi diagonali siano non nulli.

## Esempi del tutor

$$
\det\begin{pmatrix}2&5&-1\\0&3&4\\0&0&-2\end{pmatrix}
=2\cdot3\cdot(-2)=-12.
$$

Se una delle entrate diagonali è zero, il determinante è zero anche se le altre entrate sono non nulle.

Per una matrice generica non si può usare il solo prodotto della diagonale: la formula è giustificata dalla struttura triangolare.

## Collegamento con Gauss

Una matrice quadrata [[25 Pivot e Matrici a Scala|a scala]] è triangolare superiore. Il viceversa non vale sempre:

$$
\begin{pmatrix}0&1\\0&1\end{pmatrix}
$$

è triangolare superiore, ma i pivot delle due righe stanno nella stessa colonna, quindi non è a scala.

La formula del determinante resta valida per tutte le triangolari, anche per quelle non a scala.

## Da dire all'orale

> Una matrice triangolare superiore ha entrate nulle sotto la diagonale principale; una inferiore sopra. Il determinante di una triangolare è il prodotto delle entrate della diagonale principale.

## Collegamenti e fonti

- [[19 Proprietà del Prodotto e Matrice Identità]], [[22 Determinante e Sviluppo di Laplace]].
- [[24 Operazioni Elementari e Metodo di Gauss]], [[29 Calcolo del Determinante con Gauss]].
- [[GAL 2026-2027 - 20261001 - LEZIONE 4.pdf#page=10|Lezione 4, p. 10, stampata 44]].
- [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=10|Lezione 6, pp. 10-11, stampate 54-55]].
