---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 07, PDF pp. 8-10
  - Libro, §3.3.1, Teorema 3.25 e Corollario 3.27, pp. 87-88
---

# Teorema di permanenza del segno

## Intuizione

Se il limite è strettamente positivo, una fascia abbastanza stretta attorno a esso resta tutta sopra zero. I termini avanzati entrano in quella fascia e diventano positivi. Il limite zero è diverso: qualunque fascia centrata in zero contiene valori di entrambi i segni.

![[79 Permanenza del Segno.svg|700]]

## [[Enunciato]]: dal limite ai termini

Sia $(a_n)$ una successione con limite $\ell\in\overline{\mathbb R}$.

- Se $\ell>0$, incluso $\ell=+\infty$, allora $a_n>0$ definitivamente.
- Se $\ell<0$, incluso $\ell=-\infty$, allora $a_n<0$ definitivamente.

“Definitivamente” significa che esiste una soglia dopo la quale la proprietà vale per tutti gli indici, secondo [[71 Proprietà Definitivamente Vere]]. Non si impone nulla ai primi termini.

## Dimostrazione: limite positivo finito

Supponiamo $0<\ell<+\infty$. Nella definizione di limite scegliamo

$$
\varepsilon=\frac\ell2>0.
$$

Esiste $N$ tale che, per ogni $n\geq N$,

$$
|a_n-\ell|<\frac\ell2.
$$

Sviluppando la disuguaglianza,

$$
-\frac\ell2<a_n-\ell<\frac\ell2
\quad\Longrightarrow\quad
0<\frac\ell2<a_n<\frac{3\ell}{2}.
$$

Dunque $a_n>0$ definitivamente. Per $\ell<0$ finito, scegliendo $\varepsilon=-\ell/2>0$, si ottiene $a_n<\ell+\varepsilon=\ell/2<0$ definitivamente.

## Dimostrazione: limite infinito

Se $a_n\to+\infty$, dalla definizione con soglia $M=1$ esiste $N$ tale che $a_n>1>0$ per ogni $n\geq N$. Se $a_n\to-\infty$, con la stessa soglia si ottiene $a_n<-1<0$ definitivamente.

## [[Enunciato]]: dai termini al limite

Supponiamo che il limite $\ell\in\overline{\mathbb R}$ **esista**.

- Se $a_n\geq0$ definitivamente, allora $\ell\geq0$.
- Se $a_n\leq0$ definitivamente, allora $\ell\leq0$.

Non si afferma che una successione di termini non negativi ammetta necessariamente limite.

### Dimostrazione per assurdo

Siano $a_n\geq0$ per ogni $n\geq N_0$. Se fosse $\ell<0$, la prima parte del teorema darebbe $a_n<0$ per ogni $n\geq N_1$. Prendendo $n\geq\max\{N_0,N_1\}$ avremmo contemporaneamente $a_n\geq0$ e $a_n<0$, impossibile. Quindi $\ell\geq0$. Il caso non positivo si dimostra invertendo i segni.

### Da dire all'orale

> Un limite strettamente positivo rende i termini definitivamente positivi, e analogamente per il segno negativo. Viceversa, se i termini sono definitivamente non negativi e il limite esiste, il limite è non negativo, ma può essere zero.

## Perché non si conservano sempre le disuguaglianze strette

Per $n\geq1$,

$$
\frac1n>0,\qquad \frac1n\to0,
$$

quindi termini positivi non implicano limite strettamente positivo. Inoltre

$$
-\frac1n<0,\qquad -\frac1n\to0,
$$

quindi un limite non negativo non implica termini non negativi. Anche $(-1)^n/n\to0$ cambia segno infinite volte.

## Esercizio svolto: segno definitivo

### Testo

Stabilire il segno definitivo di $a_n=2-5/n$, $n\geq1$.

### Idea e svolgimento

Il termine $5/n$ tende a zero, quindi $a_n\to2>0$ (il calcolo è formalizzato nella [[80 Algebra dei Limiti di Successioni|successiva algebra dei limiti]]). Il teorema garantisce positività definitiva. Qui possiamo anche trovare la soglia:

$$
2-\frac5n>0\Longleftrightarrow2n>5\Longleftrightarrow n>\frac52.
$$

Perciò $a_n>0$ per ogni $n\geq3$, benché $a_1$ e $a_2$ siano negativi.

## Uso negli esercizi

Se $b_n\to b\neq0$, allora $b_n$ ha definitivamente il segno di $b$, dunque è definitivamente diverso da zero. Questo permette di definire sulla coda quozienti con denominatore $b_n$. Per basi variabili di potenze reali, $a_n\to a>0$ assicura una base definitivamente positiva.

## Errori comuni e prospettiva d'esame

- Confondere $\ell>0$ e $\ell\geq0$; il caso zero non impone un segno.
- Trasformare una conclusione definitiva in una proprietà valida per ogni indice.
- Concludere l'esistenza del limite dal solo segno dei termini.
- Dimenticare il massimo delle soglie nella prova per assurdo.

Potenziale rilevanza d'esame: enunciato in entrambe le direzioni, scelta $\varepsilon=\ell/2$, casi infiniti e controesempi con limite zero. La prova combina [[72 Limite Finito di una Successione|definizione di limite]] e [[20 Dimostrazione per Assurdo|ragionamento per assurdo]].
