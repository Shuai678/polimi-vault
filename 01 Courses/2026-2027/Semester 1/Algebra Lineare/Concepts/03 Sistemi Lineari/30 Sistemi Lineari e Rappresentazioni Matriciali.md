---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 9, PDF pp. 2-4, stampate 74-76"
---

# Sistemi lineari e rappresentazioni matriciali

Stato: **da studiare**.

## Quale problema descriviamo

Un sistema lineare impone più condizioni alle stesse incognite. Una soluzione deve soddisfarle **tutte contemporaneamente**. Il campo $\mathbb K$ specifica dove cerchiamo coefficienti e soluzioni: qui può essere, per esempio, $\mathbb R$ o $\mathbb F_2$.

Con $m$ equazioni e $n$ incognite scriviamo

$$
\begin{cases}
a_{11}x_1+\cdots+a_{1n}x_n=b_1,\\
\vdots\\
a_{m1}x_1+\cdots+a_{mn}x_n=b_m.
\end{cases}
$$

I coefficienti $a_{ij}$ e i termini noti $b_i$ sono fissati; gli $x_j$ sono da determinare. Sono ammesse equazioni ridondanti o con tutti i coefficienti nulli.

**Lineare** significa che ogni incognita compare solo al primo grado, moltiplicata per un coefficiente fissato. $xy=1$, $x^2+y=0$ e $\sin x=y$ non sono equazioni lineari nelle incognite indicate.

Un parametro nei coefficienti non è automaticamente un'incognita: nel sistema del PDF con $a,b\in\mathbb R$, si fissano $a,b$ e si risolve rispetto a $x,y$.

## I tre tipi del professore

Poniamo

$$
A=(a_{ij})\in M_{\mathbb K}(m,n),\qquad
x=\begin{pmatrix}x_1\\\vdots\\x_n\end{pmatrix}\in\mathbb K^n,\qquad
b=\begin{pmatrix}b_1\\\vdots\\b_m\end{pmatrix}\in\mathbb K^m.
$$

Si identifica una colonna di altezza $n$ con una $n$-upla. Il simbolo $x$ può quindi indicare sia la colonna sia le sue coordinate.

### I tipo: combinazione di colonne

Se $C_j(A)$ è la colonna $j$ di $A$, il sistema equivale a

$$
x_1C_1(A)+\cdots+x_nC_n(A)=b.
$$

Le $m$ uguaglianze scalari sono raccolte in un'uguaglianza tra colonne di altezza $m$. Cercare una soluzione significa cercare coefficienti che ricostruiscano $b$ dalle colonne di $A$.

Una combinazione lineare è precisamente una somma di multipli scalari di vettori; non richiede che i vettori siano frecce geometriche.

### II tipo: prodotto matriciale

La definizione del [[16 Prodotto Matriciale Righe per Colonne|prodotto]] dà

$$
\boxed{Ax=b.}
$$

Le dimensioni sono $(m\times n)(n\times1)=m\times1$. La riga $i$ del prodotto è $\sum_{j=1}^n a_{ij}x_j$.

### III tipo: matrice completa

Con l'ordine delle incognite fissato si conserva solo

$$
[A\mid b]=
\begin{bmatrix}
a_{11}&\cdots&a_{1n}&b_1\\
\vdots&&\vdots&\vdots\\
a_{m1}&\cdots&a_{mn}&b_m
\end{bmatrix}\in M_{\mathbb K}(m,n+1).
$$

La barra distingue i coefficienti dai termini noti. Non è una moltiplicazione. La matrice dei coefficienti è $A$, non l'intera matrice completa.

Le incognite non sono cancellate dal problema: è soltanto sottinteso che le prime $n$ colonne corrispondano, nell'ordine, a $x_1,\ldots,x_n$.

## Esempio della lezione, con soluzione esplicitata dal tutor

$$
\begin{cases}x-3y=2,\\4x+5y=1.\end{cases}
$$

Le rappresentazioni sono

$$
x\begin{pmatrix}1\\4\end{pmatrix}
+y\begin{pmatrix}-3\\5\end{pmatrix}
=\begin{pmatrix}2\\1\end{pmatrix},
\qquad
\begin{pmatrix}1&-3\\4&5\end{pmatrix}
\begin{pmatrix}x\\y\end{pmatrix}
=\begin{pmatrix}2\\1\end{pmatrix},
$$

$$
[A\mid b]=\begin{bmatrix}1&-3&2\\4&5&1\end{bmatrix}.
$$

Sottraendo quattro volte la prima equazione dalla seconda si ottiene $17y=-7$, quindi $y=-7/17$. Dalla prima $x=2+3y=13/17$.

Verifica:

$$
\frac{13}{17}-3\left(-\frac7{17}\right)=2,\qquad
4\frac{13}{17}+5\left(-\frac7{17}\right)=1.
$$

Il risultato è una singola colonna, non due soluzioni separate.

## Che cosa significa risolvere

1. Stabilire se l'insieme delle soluzioni è vuoto.
2. Se non è vuoto, descriverne **tutti e soli** gli elementi.

Cambiare i nomi delle incognite non cambia il problema, purché si mantengano posizioni e corrispondenze. Scambiare colonne senza tenere traccia dell'ordine delle incognite, invece, cambia l'interpretazione delle coordinate.

## Da dire all'orale

> Un sistema lineare con $m$ equazioni e $n$ incognite si rappresenta come combinazione delle colonne dei coefficienti, come equazione $Ax=b$ oppure tramite la matrice completa $[A\mid b]$. Le tre rappresentazioni descrivono lo stesso insieme di soluzioni.

## Collegamenti e fonte

- [[11 Matrici come Funzioni e Indici]], [[31 Risoluzione dei Sistemi con Gauss e Parametri]], [[32 Teorema di Rouché-Capelli]].
- [[GAL 2026-2027 - 20261012 - LEZIONE 9.pdf#page=2|Lezione 9, pp. 2-4, stampate 74-76]].
