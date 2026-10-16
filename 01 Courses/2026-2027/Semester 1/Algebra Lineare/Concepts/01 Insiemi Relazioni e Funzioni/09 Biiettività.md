---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 1, PDF pp. 8-10, pagine stampate 18-20"
  - "Lezione 3, PDF pp. 7-8, pagine stampate 27-28"
---

# Biiettività

Stato: **da studiare**.

## Definizione e intuizione

Una funzione $F:A\to B$ è **biiettiva** se è sia [[07 Iniettività|iniettiva]] sia [[08 Suriettività|suriettiva]].

Equivalentemente:

$$
\forall b\in B,\quad \exists! a\in A:\ F(a)=b.
$$

La suriettività dà l'esistenza di un ingresso per ogni $b$; l'iniettività ne dà l'unicità. È un abbinamento uno a uno tra tutti gli elementi dei due insiemi.

Nel pannello biiettivo di [[07 Funzioni Iniettive Suriettive e Biiettive.svg|questo schema]] ogni punto di arrivo riceve esattamente una freccia.

## Esempio del tutor

Siano $A=\{1,2,3\}$ e $B=\{a,b,c\}$ e sia

$$
F=\{(1,a),(2,b),(3,c)\}.
$$

È una funzione perché ogni elemento di $A$ compare una volta come prima componente. È iniettiva perché le immagini sono distinte; è suriettiva perché raggiunge tutto $B$. Quindi è biiettiva.

## Biiezioni usate dal professore

### Coppie annidate e terne

La corrispondenza

$$
((a,b),c)\longmapsto(a,b,c)
$$

è una biiezione da $(A\times B)\times C$ ad $A\times B\times C$. La dimostrazione è in [[10 Prodotti Cartesiani di Più Insiemi]].

### Matrici e liste ordinate

Il professore usa le corrispondenze

$$
\begin{aligned}
M_{\mathbb K}(1,1)&\longleftrightarrow\mathbb K,\\
M_{\mathbb K}(1,n)&\longleftrightarrow\mathbb K^n,\\
M_{\mathbb K}(m,1)&\longleftrightarrow\mathbb K^m.
\end{aligned}
$$

Si associano alla matrice le sue entrate lette nell'ordine indicato. La corrispondenza consente un'identificazione convenzionale, ma una matrice riga e una matrice colonna hanno comunque forme diverse.

## Conseguenza per insiemi finiti

Se esiste una biiezione tra due insiemi finiti, essi hanno lo stesso numero di elementi.

Avere lo stesso numero di elementi non rende automaticamente biiettiva una funzione già assegnata: occorre controllare quella funzione. Per esempio, una funzione costante da $\{1,2\}$ a $\{a,b\}$ non è né iniettiva né suriettiva.

## Precisazione del tutor sulla funzione inversa

Una biiezione consente di associare a ogni $b\in B$ il suo unico ingresso $a\in A$. Questa è la funzione inversa $F^{-1}:B\to A$.

L'insieme delle controimmagini $F^{-1}(\{b\})$ è invece definibile anche quando $F$ non è biiettiva: può essere vuoto o contenere più elementi.

## Da dire all'orale

> Una funzione è biiettiva se è contemporaneamente iniettiva e suriettiva; ogni elemento del codominio ha allora esattamente una controimmagine.

## Collegamenti e fonti

- [[10 Prodotti Cartesiani di Più Insiemi]] e [[11 Matrici come Funzioni e Indici]].
- [[GAL 2026-2027 - 20260917 - LEZIONE 1.pdf#page=8|Lezione 1, pp. 8-10, stampate 18-20]].
- [[GAL 2026-2027 - 20260930 - LEZIONE 3.pdf#page=7|Lezione 3, pp. 7-8, stampate 27-28]].
