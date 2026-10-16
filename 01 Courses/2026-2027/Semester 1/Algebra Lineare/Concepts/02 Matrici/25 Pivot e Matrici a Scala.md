---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 6, PDF pp. 16-17, stampate 60-61"
---

# Pivot e matrici a scala

Stato: **da studiare**.

## Definizione 6.6

Il **pivot** di una riga non nulla è il suo primo elemento non nullo, leggendo da sinistra. Una riga nulla non ha pivot.

Una matrice è **a scala** se:

1. il pivot di ogni riga non nulla è in una colonna strettamente a destra di quello della riga non nulla precedente;
2. tutte le righe nulle, se presenti, sono dopo le righe non nulle.

Se le colonne dei pivot sono $j_1,\ldots,j_r$, allora

$$
j_1<j_2<\cdots<j_r.
$$

## Esempio della Lezione 6

$$
U=\begin{pmatrix}
1&0&1&-1\\
0&0&-1&6\\
0&0&0&12
\end{pmatrix}.
$$

I pivot sono:

- $1$ nella posizione $(1,1)$;
- $-1$ nella posizione $(2,3)$;
- $12$ nella posizione $(3,4)$.

![[25 Pivot e Forma a Scala.svg|940]]

Lo schema del tutor evidenzia i tre pivot. La seconda colonna non contiene un pivot: non bisogna contare le colonne attraversate dalla scala.

Nel campo reale i tre pivot sono non nulli. Riducendo le stesse entrate in un altro campo, il conto va rifatto con le sue operazioni.

## Che cosa non è richiesto

I pivot non devono necessariamente essere 1 e sopra i pivot possono esserci entrate non nulle.

La forma a scala ridotta aggiunge condizioni ulteriori, fra cui pivot unitari e zeri anche sopra ciascun pivot. Questa distinzione è un richiamo del tutor; il MEG del PDF richiede la forma a scala ordinaria.

## Controesempi del tutor

$$
\begin{pmatrix}1&2\\0&0\\0&3\end{pmatrix}
$$

non è a scala, perché una riga nulla precede una non nulla.

$$
\begin{pmatrix}0&1\\0&2\end{pmatrix}
$$

non è a scala, perché i due pivot sono nella stessa colonna.

## Collegamento con le triangolari

In una matrice quadrata a scala, il pivot della riga $i$, quando esiste, è in una colonna $j_i\ge i$. Tutte le entrate sotto la diagonale sono quindi nulle: la matrice è triangolare superiore.

Una triangolare superiore può invece avere pivot non correttamente disposti, come mostra il secondo controesempio.

## Rango

Per una matrice a scala:

$$
r(U)=\text{numero di righe non nulle}
=\text{numero di pivot}.
$$

Il risultato e la sua relazione con la definizione mediante prodotti colonna-riga sono in [[27 Calcolo del Rango con Gauss]].

## Da dire all'orale

> Il pivot è il primo elemento non nullo di una riga. Una matrice è a scala se i pivot si spostano strettamente verso destra scendendo fra le righe non nulle e tutte le righe nulle sono in fondo.

## Collegamenti e fonte

- [[23 Matrici Diagonali e Triangolari]], [[24 Operazioni Elementari e Metodo di Gauss]].
- Fonte: [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=16|Lezione 6, pp. 16-17, stampate 60-61]].
