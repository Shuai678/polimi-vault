---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 3, PDF pp. 9-11, pagine stampate 29-31"
---

# Uguaglianza e somma di matrici

## Uguaglianza

L'uguaglianza tra due [[11 Matrici come Funzioni e Indici|matrici]] richiede le stesse dimensioni e la coincidenza delle entrate in ogni posizione:

$$
A=B
\iff
a_{ij}=b_{ij}\quad
\forall i=1,\ldots,m,\ \forall j=1,\ldots,n.
$$

Per matrici di forme diverse non si ha uguaglianza. Per esempio, una matrice $1\times2$ e una $2\times1$ sono diverse anche quando contengono gli stessi due numeri.

Interpretando le matrici come funzioni, si riconduce l'uguaglianza alla coincidenza dei valori sullo stesso insieme di indici.

## Definizione della somma

Per $A,B\in M_{\mathbb K}(m,n)$ si definisce l'operazione di somma:

$$
+:M_{\mathbb K}(m,n)\times M_{\mathbb K}(m,n)
\longrightarrow M_{\mathbb K}(m,n),
\qquad (A,B)\longmapsto A+B,
$$

con

$$
(A+B)_{ij}=a_{ij}+b_{ij}.
$$

La somma si esegue sommando le entrate che occupano la stessa posizione. Si richiede che le dimensioni coincidano e si applicano le regole di addizione del campo $\mathbb K$.

> [!note] Stesso dominio e stesse dimensioni
> Una matrice di tipo $(m,n)$ è una funzione con dominio $[m]\times[n]$, cioè l'insieme delle posizioni delle caselle. Per le matrici, richiedere lo **stesso dominio** equivale quindi a richiedere le **stesse dimensioni**:
>
> $$
> A:[m]\times[n]\to\mathbb K,
> \qquad
> B:[m]\times[n]\to\mathbb K.
> $$
>
> Per calcolare $A(i,j)+B(i,j)$, la posizione $(i,j)$ deve appartenere al dominio di entrambe le matrici: devono essere definiti entrambi i valori da sommare.
>
> Per esempio, una matrice $2\times3$ e una $2\times2$ hanno domini diversi. La posizione $(1,3)$ esiste nella prima, ma manca nella seconda; la somma delle due matrici non è quindi definita.

Per funzioni con domini diversi, si può prima effettuare una restrizione alla loro intersezione e poi sommare le funzioni ristrette. Questo procedimento modifica i domini iniziali; per la somma diretta delle matrici qui definita si richiede lo stesso dominio.

## Esempio di somma

Si considerano le matrici:

$$
A=\begin{bmatrix}1&-2\\0&3\end{bmatrix},
\qquad
B=\begin{bmatrix}-1&1\\4&7\end{bmatrix}.
$$

Poiché entrambe appartengono a $M_{\mathbb R}(2,2)$, si può eseguire la somma:

$$
\begin{aligned}
A+B
&=\begin{bmatrix}
1+(-1)&-2+1\\
0+4&3+7
\end{bmatrix}\\
&=\begin{bmatrix}0&-1\\4&10\end{bmatrix}.
\end{aligned}
$$

Si sommano, nell'ordine, le entrate nelle posizioni $(1,1)$, $(1,2)$, $(2,1)$ e $(2,2)$.

## Proprietà e dimostrazioni per componenti

Le proprietà della somma di matrici derivano da quelle dell'addizione nel campo $\mathbb K$. Le dimostrazioni si svolgono confrontando le entrate nella stessa posizione.

### Associatività

Per $A,B,C\in M_{\mathbb K}(m,n)$ e per ogni posizione $(i,j)$:

$$
\begin{aligned}
((A+B)+C)_{ij}
&=(a_{ij}+b_{ij})+c_{ij}\\
&=a_{ij}+(b_{ij}+c_{ij})\\
&=(A+(B+C))_{ij}.
\end{aligned}
$$

Nel passaggio centrale si applica l'associatività in $\mathbb K$. Dalla coincidenza di tutte le entrate si conclude:

$$
(A+B)+C=A+(B+C).
$$

### Commutatività

$$
(A+B)_{ij}
=a_{ij}+b_{ij}
=b_{ij}+a_{ij}
=(B+A)_{ij}.
$$

Applicando la commutatività in $\mathbb K$ a ogni entrata, si ottiene $A+B=B+A$.

### Matrice nulla

Si indica con $0_{m,n}$ la matrice di tipo $(m,n)$ con tutte le entrate nulle. Per ogni posizione $(i,j)$ si ha:

$$
(A+0_{m,n})_{ij}=a_{ij}+0=a_{ij}.
$$

Si ottiene quindi $A+0_{m,n}=0_{m,n}+A=A$. Si richiede che la matrice nulla abbia le stesse dimensioni di $A$.

Per verificare l'unicità dell'elemento neutro, si suppone che $N$ sia neutro. Applicando la proprietà di $N$ alla matrice nulla, si ottiene $0_{m,n}+N=0_{m,n}$. Poiché il primo membro coincide con $N$, si conclude $N=0_{m,n}$.

### Matrice opposta

Si definisce l'opposta di $A$ cambiando il segno di ogni entrata:

$$
-A=(-a_{ij})_{ij}.
$$

Per ogni posizione $(i,j)$ si verifica:

$$
(A+(-A))_{ij}=a_{ij}+(-a_{ij})=0.
$$

Si ottiene quindi $A+(-A)=(-A)+A=0_{m,n}$.

Nella fonte si indica l'opposta anche con $A'$. Si adotta la notazione $-A$ per rendere esplicito il significato additivo.

Per verificare l'unicità dell'opposta, si suppone che $A+C=0_{m,n}$. In ogni posizione si ha $a_{ij}+c_{ij}=0$, da cui si ricava $c_{ij}=-a_{ij}$. Si conclude quindi $C=-A$.

Per la matrice $A$ dell'esempio si ottiene:

$$
-\begin{bmatrix}1&-2\\0&3\end{bmatrix}
=\begin{bmatrix}-1&2\\0&-3\end{bmatrix}.
$$

## Differenza

La differenza si definisce mediante la somma con la matrice opposta:

$$
A-B=A+(-B),\qquad
(A-B)_{ij}=a_{ij}-b_{ij}.
$$

Anche per la differenza si richiede che le dimensioni coincidano.

## Condizioni e precisazioni

- Per la somma si richiedono le stesse dimensioni; il solo numero totale di entrate non è sufficiente.
- Nella lettura delle entrate si mantiene distinto l'indice di riga da quello di colonna.
- Per costruire l'opposta si cambia il segno di tutte le entrate.
- Nel campo [[12 Campi Numerici e Campo F2| F]] si applicano le regole di addizione del campo.

## Sintesi per l'orale

> La somma di due matrici dello stesso tipo si definisce sommando le entrate corrispondenti. È associativa e commutativa, ha come elemento neutro la matrice nulla e ogni matrice ha un'unica opposta.

## Collegamenti e fonte

- [[14 Prodotto di una Matrice per uno Scalare]].
- [[15 Proprietà e Costo dei Calcoli Matriciali]].
- Esempi svolti: [[03 Esempi Svolti sulle Matrici]].
- Fonte: [[GAL 2026-2027 - 20260930 - LEZIONE 3.pdf#page=9|Lezione 3, pp. 9-11, stampate 29-31]]. Le dimostrazioni per componenti e le verifiche di unicità costituiscono approfondimenti aggiuntivi.
