---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 6, PDF pp. 6 e 15-16"
  - esempi aggiuntivi del tutor
---

# Esempi svolti su rango Laplace e matrici triangolari

Stato: **da studiare**. Soluzioni preparate dal tutor; nessun esercizio autonomo dello studente registrato.

## 1 Il problema dei due dadi

### Dati del professore

La [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=6|Lezione 6, p. 6, stampata 50]] propone di confrontare la parità del primo dado $D_1$ con la parità della somma $D_1+D_2$.

Assumiamo dadi a sei facce equi e indipendenti. I 36 esiti ordinati sono equiprobabili.

### Soluzione del tutor

Una somma è pari quando i due risultati hanno la stessa parità.

- $D_1$ pari e somma pari: entrambi pari, $3\cdot3=9$ esiti.
- $D_1$ pari e somma dispari: primo pari e secondo dispari, 9 esiti.
- $D_1$ dispari e somma pari: entrambi dispari, 9 esiti.
- $D_1$ dispari e somma dispari: primo dispari e secondo pari, 9 esiti.

La matrice di probabilità congiunte è

$$
P=\begin{pmatrix}\frac14&\frac14\\\frac14&\frac14\end{pmatrix}
=\begin{pmatrix}\frac12\\\frac12\end{pmatrix}
\begin{pmatrix}\frac12&\frac12\end{pmatrix}.
$$

Le righe distinguono la parità di $D_1$, le colonne quella della somma. La matrice non è nulla e ha una decomposizione con un solo prodotto colonna-riga, dunque $r(P)=1$.

Le due parità sono indipendenti. Il fatto che la somma contenga $D_1$ non basta a dimostrare dipendenza della sua parità da quella di $D_1$.

Prerequisito: [[21 Rango e Prodotti Colonna per Riga]].

## 2 Sviluppo di Laplace con molti zeri

Esempio del tutor:

$$
C=\begin{pmatrix}1&0&2\\0&3&0\\4&0&5\end{pmatrix}.
$$

Sviluppando sulla seconda riga, sopravvive solo l'entrata $(2,2)$, con segno positivo:

$$
\det C
=3(-1)^{2+2}\det\begin{pmatrix}1&2\\4&5\end{pmatrix}
=3(5-8)=-9.
$$

Non si devono calcolare i minori dei due termini moltiplicati per zero.

Prerequisito: [[22 Determinante e Sviluppo di Laplace]].

## 3 Rango e determinante di una triangolare

$$
T=\begin{pmatrix}0&1&0\\0&0&1\\0&0&0\end{pmatrix}.
$$

È triangolare superiore e a scala. I pivot sono in posizione $(1,2)$ e $(2,3)$, quindi $r(T)=2$.

Il determinante è invece $0\cdot0\cdot0=0$. Il rango non è il numero di entrate diagonali non nulle e non coincide con il determinante.

Prerequisiti: [[23 Matrici Diagonali e Triangolari]], [[25 Pivot e Matrici a Scala]], [[27 Calcolo del Rango con Gauss]].

## 4 Esempio completo di Gauss della Lezione 6

Fonte: [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=15|PDF pp. 15-16, stampate 59-60]]. I dati e le scelte di pivot sono quelli del professore; i calcoli sono esplicitati dal tutor. Si lavora su $\mathbb R$.

$$
A=\begin{pmatrix}0&0&2&0\\1&0&1&-1\\2&0&1&4\end{pmatrix}.
$$

### Primo pivot

La prima colonna non è nulla. Scegliamo il valore 1 nella seconda riga e applichiamo $R_1\leftrightarrow R_2$:

$$
A_1=\begin{pmatrix}1&0&1&-1\\0&0&2&0\\2&0&1&4\end{pmatrix}.
$$

### Eliminazione nella prima colonna

$$
R_3\leftarrow R_3-2R_1.
$$

La terza riga diventa

$$
(2,0,1,4)-2(1,0,1,-1)=(0,0,-1,6).
$$

Quindi

$$
A_2=\begin{pmatrix}1&0&1&-1\\0&0&2&0\\0&0&-1&6\end{pmatrix}.
$$

### Secondo pivot

Nelle righe inferiori le prime due colonne sono nulle. La prima colonna utile è la terza. Scegliamo $-1$ e scambiamo $R_2$ con $R_3$:

$$
A_3=\begin{pmatrix}1&0&1&-1\\0&0&-1&6\\0&0&2&0\end{pmatrix}.
$$

### Eliminazione nella terza colonna

Il coefficiente da eliminare è 2 e il pivot è $-1$:

$$
R_3\leftarrow R_3-\frac2{-1}R_2=R_3+2R_2.
$$

La terza riga diventa $(0,0,2,0)+2(0,0,-1,6)=(0,0,0,12)$:

$$
U=\begin{pmatrix}1&0&1&-1\\0&0&-1&6\\0&0&0&12\end{pmatrix}.
$$

### Interpretazione

Le colonne dei pivot sono 1, 3 e 4. Ci sono tre righe non nulle, dunque $r(A)=3$.

La matrice è $3\times4$: non ha un determinante come matrice intera e non ammette un'inversa bilatera.

Prerequisiti: [[24 Operazioni Elementari e Metodo di Gauss]], [[27 Calcolo del Rango con Gauss]].
