---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-10-16
source: esempi del tutor sui contenuti della Lezione 4
---

# Esempi svolti su prodotto composizione e navigazione

Stato: **da studiare**. Gli svolgimenti sono preparati dal tutor e non sono esercizi completati dallo studente.

## 1 Due prodotti definiti ma diversi

Siano

$$
A=\begin{pmatrix}1&2\\0&1\end{pmatrix},
\qquad B=\begin{pmatrix}1&0\\3&1\end{pmatrix}.
$$

Entrambe sono $2\times2$, quindi $AB$ e $BA$ sono definiti e quadrati dello stesso ordine.

$$
\begin{aligned}
AB
&=\begin{pmatrix}
1\cdot1+2\cdot3&1\cdot0+2\cdot1\\
0\cdot1+1\cdot3&0\cdot0+1\cdot1
\end{pmatrix}
=\begin{pmatrix}7&2\\3&1\end{pmatrix},\\
BA
&=\begin{pmatrix}
1\cdot1+0\cdot0&1\cdot2+0\cdot1\\
3\cdot1+1\cdot0&3\cdot2+1\cdot1
\end{pmatrix}
=\begin{pmatrix}1&2\\3&7\end{pmatrix}.
\end{aligned}
$$

I risultati sono diversi. La compatibilità dimensionale non implica commutatività.

Prerequisiti: [[16 Prodotto Matriciale Righe per Colonne]], [[19 Proprietà del Prodotto e Matrice Identità]].

## 2 Prodotto nullo con fattori non nulli

$$
P=\begin{pmatrix}1&0\\0&0\end{pmatrix},
\qquad Q=\begin{pmatrix}0&0\\0&1\end{pmatrix}.
$$

$$
PQ=\begin{pmatrix}
1\cdot0+0\cdot0&1\cdot0+0\cdot1\\
0\cdot0+0\cdot0&0\cdot0+0\cdot1
\end{pmatrix}
=0_{2,2}.
$$

Nessuno dei due fattori è nullo. Non si può usare senza ipotesi la legge di annullamento del prodotto dei numeri.

## 3 Navigazione in due passi

Usiamo la matrice del modello a tre pagine della [[GAL 2026-2027 - 20261001 - LEZIONE 4.pdf#page=6|Lezione 4, p. 6, stampata 40]]:

$$
T=\begin{pmatrix}
0&1&0\\
\frac12&0&1\\
\frac12&0&0
\end{pmatrix}.
$$

Il prodotto dà

$$
T^2=\begin{pmatrix}
\frac12&0&1\\
\frac12&\frac12&0\\
0&\frac12&0
\end{pmatrix}.
$$

Per esempio:

$$
(T^2)_{32}
=t_{31}t_{12}+t_{32}t_{22}+t_{33}t_{32}
=\frac12\cdot1+0+0=\frac12.
$$

Partendo dalla pagina 2, il primo passo porta necessariamente alla pagina 1; da lì il secondo passo porta alla 3 con probabilità $1/2$.

Gli altri termini della stessa entrata corrispondono a percorsi che passano per le pagine intermedie 2 o 3 e hanno probabilità zero.

La distribuzione iniziale $x^{(0)}=(0,1,0)$, scritta come colonna, evolve in

$$
x^{(1)}=\begin{pmatrix}1\\0\\0\end{pmatrix},
\qquad
x^{(2)}=\begin{pmatrix}0\\\frac12\\\frac12\end{pmatrix}.
$$

Le colonne di $T^2$ sommano a 1: i risultati sono ancora distribuzioni di probabilità.

Prerequisiti: [[17 Prodotto Matriciale e Composizione]], [[18 PageRank e Matrici di Transizione]].

## Composizione dei frutti

L'esempio completo del professore con frutti, iniziali e tipo di lettera è svolto in [[17 Prodotto Matriciale e Composizione]], compreso il controllo dell'ordine $BA$.
