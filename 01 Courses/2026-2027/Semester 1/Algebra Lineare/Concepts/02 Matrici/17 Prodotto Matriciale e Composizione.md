---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 4, PDF pp. 4-5, stampate 38-39"
---

# Prodotto matriciale e composizione

Stato: **da studiare**.

## Due associazioni successive

Il professore considera

$$
F\xrightarrow{f}L\xrightarrow{g}T,
$$

dove $F$ contiene arancia, limone e lampone, $L=\{a,b,l\}$ e $T=\{\text{vocale},\text{consonante}\}$.

- $f$ assegna al frutto la sua iniziale.
- $g$ assegna alla lettera il tipo vocale o consonante.
- $g\circ f$ assegna direttamente al frutto il tipo della sua iniziale.

La composizione si legge da destra verso sinistra:

$$
(g\circ f)(x)=g(f(x)).
$$

## Convenzione delle matrici

Le colonne rappresentano gli elementi di partenza e le righe quelli di arrivo. Per una funzione ogni colonna contiene esattamente un 1 e tutte le altre entrate sono 0.

Con colonne di $A$ ordinate come arancia, limone, lampone e righe come $a,b,l$:

$$
A=\begin{pmatrix}1&0&0\\0&0&0\\0&1&1\end{pmatrix}.
$$

Per $g$, con righe vocale, consonante e colonne $a,b,l$:

$$
B=\begin{pmatrix}1&0&0\\0&1&1\end{pmatrix}.
$$

Si calcola $BA$, di tipo $(2,3)$, perché prima si applica l'associazione rappresentata da $A$:

$$
BA=
\begin{pmatrix}1&0&0\\0&1&1\end{pmatrix}
\begin{pmatrix}1&0&0\\0&0&0\\0&1&1\end{pmatrix}
=\begin{pmatrix}1&0&0\\0&1&1\end{pmatrix}.
$$

Il prodotto $AB$ non è definito: le dimensioni sarebbero $(3\times3)(2\times3)$.

## Perché la formula funziona

Siano $a_{kx}$ e $b_{tk}$ gli indicatori delle due associazioni. La formula

$$
(BA)_{tx}=\sum_k b_{tk}a_{kx}
$$

esamina tutti i possibili elementi intermedi $k$.

Per ogni ingresso $x$, un solo termine può avere $a_{kx}=1$, quello con $k=f(x)$. Pertanto:

$$
(BA)_{tx}=b_{t,f(x)}=
\begin{cases}
1,&t=g(f(x)),\\
0,&t\ne g(f(x)).
\end{cases}
$$

Il prodotto registra quindi la funzione composta. La giustificazione è esplicitata dal tutor.

## Interpretazione

Il prodotto somma i contributi dei percorsi che passano per lo stesso insieme intermedio. Nell'esempio delle funzioni il percorso intermedio è unico; nelle [[18 PageRank e Matrici di Transizione|transizioni probabilistiche]] si sommano invece probabilità di percorsi alternativi.

## Errori da evitare

- Scrivere $AB$ soltanto perché i nomi delle funzioni sono elencati come prima $f$, poi $g$.
- Cambiare l'ordine degli elementi intermedi fra le righe di $A$ e le colonne di $B$.
- Interpretare questo esempio come una definizione generale di ogni matrice tramite una funzione fra insiemi: qui si usa una specifica codifica con indicatori.

## Da dire all'orale

> Usando colonne per gli ingressi e righe per le uscite, la composizione di due funzioni codificate con matrici è rappresentata dal prodotto della matrice della seconda funzione per quella della prima.

## Collegamenti e fonte

- [[05 Funzioni]], [[16 Prodotto Matriciale Righe per Colonne]].
- [[18 PageRank e Matrici di Transizione]].
- Fonte: [[GAL 2026-2027 - 20261001 - LEZIONE 4.pdf#page=4|Lezione 4, pp. 4-5, stampate 38-39]].
