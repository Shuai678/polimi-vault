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

Stato: **da studiare**.

## Uguaglianza

Due [[11 Matrici come Funzioni e Indici|matrici]] sono uguali quando hanno le stesse dimensioni e coincidono in ogni posizione:

$$
A=B
\iff
a_{ij}=b_{ij}\quad
\forall i=1,\ldots,m,\ \forall j=1,\ldots,n.
$$

Matrici di forme diverse non sono uguali. Per esempio, una matrice $1\times2$ e una $2\times1$ non sono uguali anche se contengono gli stessi due numeri.

L'uguaglianza si interpreta come uguaglianza di funzioni sullo stesso insieme di indici.

## Definizione della somma

Per $A,B\in M_{\mathbb K}(m,n)$:

$$
+:M_{\mathbb K}(m,n)\times M_{\mathbb K}(m,n)
\longrightarrow M_{\mathbb K}(m,n),
\qquad (A,B)\longmapsto A+B,
$$

con

$$
(A+B)_{ij}=a_{ij}+b_{ij}.
$$

Si sommano le entrate che occupano la stessa posizione. Le dimensioni devono coincidere e le somme si eseguono nel campo $\mathbb K$.

Il richiamo alle funzioni del PDF significa che, per la somma puntuale sull'intero dominio dichiarato, i due addendi devono avere lo stesso dominio. Per funzioni con domini diversi si può eventualmente lavorare sulla loro intersezione, dopo una restrizione esplicita.

## Esempio del professore

$$
A=\begin{pmatrix}1&-2\\0&3\end{pmatrix},
\qquad
B=\begin{pmatrix}-1&1\\4&7\end{pmatrix}.
$$

Entrambe sono $2\times2$ su $\mathbb R$. Quindi:

$$
\begin{aligned}
A+B
&=\begin{pmatrix}
1+(-1)&-2+1\\
0+4&3+7
\end{pmatrix}\\
&=\begin{pmatrix}0&-1\\4&10\end{pmatrix}.
\end{aligned}
$$

Le quattro operazioni riguardano, nell'ordine, le posizioni $(1,1)$, $(1,2)$, $(2,1)$ e $(2,2)$.

## Proprietà e dimostrazioni per componenti

Il professore enuncia le proprietà come ereditate dalla somma del campo. I passaggi seguenti ne esplicitano la giustificazione.

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

Il passaggio centrale usa l'associatività in $\mathbb K$. Poiché tutte le entrate coincidono:

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

Quindi $A+B=B+A$.

### Matrice nulla

La matrice $0_{m,n}$ ha tutte le entrate nulle. Per ogni $(i,j)$:

$$
(A+0_{m,n})_{ij}=a_{ij}+0=a_{ij}.
$$

Quindi $A+0_{m,n}=0_{m,n}+A=A$. Occorre la matrice nulla delle dimensioni corrette.

L'elemento neutro è unico: se $N$ è neutro, applicando la sua proprietà alla matrice nulla si ottiene $0_{m,n}+N=0_{m,n}$; ma il primo membro è $N$. Dunque $N=0_{m,n}$.

### Matrice opposta

L'opposta di $A$ è

$$
-A=(-a_{ij})_{ij}.
$$

Infatti:

$$
(A+(-A))_{ij}=a_{ij}+(-a_{ij})=0.
$$

Quindi $A+(-A)=(-A)+A=0_{m,n}$.

Nel PDF l'opposta è indicata anche con $A'$. Qui si usa $-A$ per rendere esplicito il significato additivo.

L'opposta è unica: se $A+C=0_{m,n}$, ogni entrata soddisfa $a_{ij}+c_{ij}=0$, quindi $c_{ij}=-a_{ij}$ e $C=-A$.

Nell'esempio:

$$
-\begin{pmatrix}1&-2\\0&3\end{pmatrix}
=\begin{pmatrix}-1&2\\0&-3\end{pmatrix}.
$$

## Differenza

Come conseguenza delle definizioni:

$$
A-B=A+(-B),\qquad
(A-B)_{ij}=a_{ij}-b_{ij}.
$$

Anche la differenza richiede dimensioni uguali.

## Errori da evitare

- Sommare matrici che hanno soltanto lo stesso numero totale di entrate ma forme diverse.
- Scambiare gli indici di riga e colonna.
- Cambiare il segno solo ad alcune entrate per costruire l'opposta.
- Usare la somma reale quando il campo è [[12 Campi Numerici e Campo F2|$\mathbb F_2$]].

## Da dire all'orale

> La somma di due matrici dello stesso tipo si definisce sommando le entrate corrispondenti. È associativa e commutativa, ha come elemento neutro la matrice nulla e ogni matrice ha un'unica opposta.

## Collegamenti e fonte

- [[14 Prodotto di una Matrice per uno Scalare]].
- [[15 Proprietà e Costo dei Calcoli Matriciali]].
- Esempi svolti: [[03 Esempi Svolti sulle Matrici]].
- Fonte: [[GAL 2026-2027 - 20260930 - LEZIONE 3.pdf#page=9|Lezione 3, pp. 9-11, stampate 29-31]]. Le dimostrazioni per componenti e le verifiche di unicità sono sviluppate dal tutor.
