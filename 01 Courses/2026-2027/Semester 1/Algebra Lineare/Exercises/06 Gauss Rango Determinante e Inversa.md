---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 7, PDF p. 6, stampata 67"
  - "Lezione 6, PDF pp. 8-9, per la matrice B"
  - integrazioni operative del tutor
---

# Esempi svolti su Gauss rango determinante e inversa

Stato: **da studiare**. Tutte le soluzioni sono preparate dal tutor e non attribuite allo studente.

## 1 Rango dell'esempio della Lezione 7

Fonte: [[GAL 2026-2027 - 20261008 - LEZIONE 7.pdf#page=6|Lezione 7, p. 6, stampata 67]]. Si lavora su $\mathbb R$.

$$
A=\begin{pmatrix}1&0&-1&2\\2&0&3&1\\1&0&4&-1\end{pmatrix}.
$$

### Prima operazione

$$
R_2\leftarrow R_2-2R_1:
\quad
A_1=\begin{pmatrix}1&0&-1&2\\0&0&5&-3\\1&0&4&-1\end{pmatrix}.
$$

Le entrate della seconda riga sono $2-2=0$, $0-0=0$, $3-2(-1)=5$ e $1-4=-3$.

### Seconda operazione

$$
R_3\leftarrow R_3-R_1:
\quad
A_2=\begin{pmatrix}1&0&-1&2\\0&0&5&-3\\0&0&5&-3\end{pmatrix}.
$$

La terza riga diventa $(1-1,0-0,4-(-1),-1-2)=(0,0,5,-3)$.

### Terza operazione

$$
R_3\leftarrow R_3-R_2:
\quad
U=\begin{pmatrix}1&0&-1&2\\0&0&5&-3\\0&0&0&0\end{pmatrix}.
$$

I pivot sono 1 e 5, nelle colonne 1 e 3: $r(A)=2$.

Prerequisito: [[27 Calcolo del Rango con Gauss]].

## 2 Il determinante 20 ricalcolato con Gauss

La matrice è quella della [[22 Determinante e Sviluppo di Laplace|Lezione 6]]; questa procedura è una verifica indipendente del tutor:

$$
B=\begin{pmatrix}9&2&-2\\2&2&0\\-2&0&2\end{pmatrix}.
$$

Scambiamo $R_1$ e $R_2$:

$$
B_1=\begin{pmatrix}2&2&0\\9&2&-2\\-2&0&2\end{pmatrix},
\qquad \det B_1=-\det B.
$$

Applichiamo $R_2\leftarrow R_2-\frac92R_1$:

$$
B_2=\begin{pmatrix}2&2&0\\0&-7&-2\\-2&0&2\end{pmatrix}.
$$

Applichiamo $R_3\leftarrow R_3+R_1$:

$$
B_3=\begin{pmatrix}2&2&0\\0&-7&-2\\0&2&2\end{pmatrix}.
$$

Per eliminare 2 sotto il pivot $-7$:

$$
R_3\leftarrow R_3+\frac27R_2:
\quad
U=\begin{pmatrix}2&2&0\\0&-7&-2\\0&0&\frac{10}7\end{pmatrix}.
$$

L'ultima entrata è $2+\frac27(-2)=\frac{10}7$.

È stato eseguito un solo scambio, nessun riscalamento di riga:

$$
\det U=2(-7)\frac{10}7=-20=-\det B,
\qquad \det B=20.
$$

Prerequisito: [[29 Calcolo del Determinante con Gauss]].

## 3 Calcolare un'inversa usando l'identità affiancata

Integrazione del tutor alla [[26 Matrici Elementari e Reversibilità del MEG|codifica delle operazioni]]. Consideriamo

$$
A=\begin{pmatrix}1&2\\3&7\end{pmatrix}.
$$

Si applicano le stesse operazioni ad $A$ e a $I_2$:

$$
\left[\begin{array}{cc|cc}
1&2&1&0\\
3&7&0&1
\end{array}\right].
$$

Con $R_2\leftarrow R_2-3R_1$:

$$
\left[\begin{array}{cc|cc}
1&2&1&0\\
0&1&-3&1
\end{array}\right].
$$

Con $R_1\leftarrow R_1-2R_2$:

$$
\left[\begin{array}{cc|cc}
1&0&7&-2\\
0&1&-3&1
\end{array}\right].
$$

La parte sinistra è $I_2$. La parte destra è la matrice $T$ delle operazioni: poiché $TA=I_2$ e $T$ è invertibile, è $A^{-1}$.

$$
A^{-1}=\begin{pmatrix}7&-2\\-3&1\end{pmatrix}.
$$

Verifica nei due ordini:

$$
\begin{aligned}
AA^{-1}
&=\begin{pmatrix}7-6&-2+2\\21-21&-6+7\end{pmatrix}=I_2,\\
A^{-1}A
&=\begin{pmatrix}7-6&14-14\\-3+3&-6+7\end{pmatrix}=I_2.
\end{aligned}
$$

La riduzione fino all'identità è un'integrazione operativa: il PDF della Lezione 7 esplicita la codifica del MEG, non presenta questo specifico esempio affiancato.

## 4 Due righe uguali anche in F2

$$
C=\begin{pmatrix}1&1\\1&1\end{pmatrix}\quad\text{su }\mathbb F_2.
$$

$$
\det C=1\cdot1-1\cdot1=0.
$$

In questo campo $-1=1$, quindi lo stesso conto si può scrivere $1+1=0$. Non si ricava la conclusione dividendo per 2.

Prerequisito: [[28 Teorema di Binet e Proprietà del Determinante]].
