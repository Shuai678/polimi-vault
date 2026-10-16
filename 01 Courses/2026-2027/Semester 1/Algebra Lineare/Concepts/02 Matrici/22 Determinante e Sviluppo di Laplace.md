---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 6, PDF pp. 7-10, stampate 51-54"
---

# Determinante e sviluppo di Laplace

Stato: **da studiare**.

## Definizione 6.4

Il determinante associa a una matrice quadrata un elemento del campo:

$$
\det:M_{\mathbb K}(n,n)\longrightarrow\mathbb K.
$$

Nella definizione ricorsiva:

$$
\det\begin{pmatrix}a_{11}\end{pmatrix}=a_{11}.
$$

Per $n>1$, fissata una riga $i$:

$$
\det A=\sum_{j=1}^{n}(-1)^{i+j}a_{ij}\det\widehat A_{ij}.
$$

La matrice $\widehat A_{ij}$ si ottiene eliminando la riga $i$ e la colonna $j$ e ha ordine $n-1$. Il numero $\det\widehat A_{ij}$ è il minore relativo alla posizione; il prodotto $(-1)^{i+j}\det\widehat A_{ij}$ è il relativo cofattore.

I nomi minore e cofattore sono precisazioni del tutor; il PDF usa la notazione con il cappello.

## Sviluppo per colonna e teorema di Laplace

Fissata una colonna $j$:

$$
\det A=\sum_{i=1}^{n}(-1)^{i+j}a_{ij}\det\widehat A_{ij}.
$$

Il teorema di Laplace enunciato nel PDF afferma che il risultato non dipende dalla riga o dalla colonna scelta. Gli esempi seguenti illustrano questo risultato; il confronto numerico non ne sostituisce la dimostrazione generale.

## Segni

Nelle prime tre righe e colonne, il fattore $(-1)^{i+j}$ segue lo schema

$$
\begin{pmatrix}
+&-&+\\
-&+&-\\
+&-&+
\end{pmatrix}.
$$

Si conta la posizione originale $(i,j)$, non la nuova posizione dentro la matrice minore.

## Caso due per due

Sviluppando sulla prima colonna:

$$
\begin{aligned}
\det\begin{pmatrix}a&b\\c&d\end{pmatrix}
&=a\det\begin{pmatrix}d\end{pmatrix}
-c\det\begin{pmatrix}b\end{pmatrix}\\
&=ad-cb=ad-bc.
\end{aligned}
$$

L'ultima uguaglianza usa la commutatività del campo.

## Esempio del professore

$$
B=\begin{pmatrix}
9&2&-2\\
2&2&0\\
-2&0&2
\end{pmatrix}.
$$

### Sviluppo sulla prima riga

$$
\begin{aligned}
\det B
&=9\det\begin{pmatrix}2&0\\0&2\end{pmatrix}
-2\det\begin{pmatrix}2&0\\-2&2\end{pmatrix}
+(-2)\det\begin{pmatrix}2&2\\-2&0\end{pmatrix}\\
&=9(2\cdot2-0\cdot0)
-2(2\cdot2-0(-2))
-2(2\cdot0-2(-2))\\
&=36-8-8=20.
\end{aligned}
$$

### Sviluppo sulla terza colonna

La presenza di uno zero riduce i termini da calcolare:

$$
\begin{aligned}
\det B
&=(-2)\det\begin{pmatrix}2&2\\-2&0\end{pmatrix}
-0\det\widehat B_{23}
+2\det\begin{pmatrix}9&2\\2&2\end{pmatrix}\\
&=-2(4)+2(18-4)\\
&=-8+28=20.
\end{aligned}
$$

## Riga o colonna nulla

Se una riga è tutta nulla, sviluppando su quella riga ogni addendo contiene il fattore zero: $\det A=0$. Lo stesso vale per una colonna nulla.

Il viceversa non vale: una matrice può avere determinante nullo senza avere righe o colonne nulle.

## Metodo e condizioni

1. Controllare che la matrice sia quadrata.
2. Scegliere una riga o una colonna, preferibilmente con molti zeri.
3. Fissare i segni usando gli indici originali.
4. Scrivere i minori eliminando esattamente una riga e una colonna.
5. Calcolare fino al caso $1\times1$ o alla formula $2\times2$.

Per matrici più grandi, [[29 Calcolo del Determinante con Gauss|Gauss]] evita di sviluppare numerosi minori.

## Da dire all'orale

> Il determinante è una funzione dalle matrici quadrate al campo. Lo sviluppo di Laplace lo esprime come somma delle entrate di una riga o colonna moltiplicate per i relativi cofattori.

## Collegamenti e fonte

- [[23 Matrici Diagonali e Triangolari]], [[28 Teorema di Binet e Proprietà del Determinante]].
- Fonte: [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=7|Lezione 6, pp. 7-10, stampate 51-54]].
