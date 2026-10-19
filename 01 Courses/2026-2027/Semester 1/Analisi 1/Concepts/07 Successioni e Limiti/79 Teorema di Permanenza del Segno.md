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

## 1) [[Enunciato]]: dal limite ai termini

Sia $(a_n)$ una successione e si supponga che esista

$$
\ell=\lim_{n\to+\infty}a_n\in\overline{\mathbb R}.
$$

- Se $\ell>0$, cioè $\ell\in(0,+\infty]$, allora $a_n>0$ definitivamente.
- Se $\ell<0$, cioè $\ell\in[-\infty,0)$, allora $a_n<0$ definitivamente.

“Definitivamente” significa che esiste una soglia dopo la quale la proprietà vale per tutti gli indici, secondo [[71 Proprietà Definitivamente Vere]]. Non si impone nulla ai primi termini.

## Dimostrazione del punto 1: dal limite ai termini

Si supponga $\ell\in(0,+\infty]$. Si distinguono due casi, perché la definizione di limite cambia a seconda che $\ell$ sia infinito o finito.

### Caso 1: $\ell=+\infty$

Qui $a_n\to+\infty$: si usa la **definizione di limite infinito**.

Per definizione, per ogni $M>0$ esiste $N\in\mathbb N$ tale che, per ogni $n\geq N$,

$$
a_n>M>0.
$$

Quindi $a_n>0$ definitivamente: da un certo indice in poi, tutti i termini superano una soglia positiva.

### Caso 2: $\ell\in(0,+\infty)$

Qui $\ell$ è un **numero finito e positivo**: la parentesi tonda esclude $+\infty$. La successione tende a quel numero $\ell$, quindi si usa la [[72 Limite Finito di una Successione|definizione di limite finito]].

Per definizione, per ogni $\varepsilon>0$ esiste $N\in\mathbb N$ tale che, per ogni $n\geq N$,

$$
\ell-\varepsilon<a_n<\ell+\varepsilon.
$$

Tutti i termini da $N$ in poi stanno nella fascia tra $\ell-\varepsilon$ e $\ell+\varepsilon$. È equivalente a $|a_n-\ell|<\varepsilon$.

Si sceglie ora

$$
\varepsilon=\frac{\ell}{2}>0.
$$

La scelta è possibile perché $\ell>0$. Si prende metà di $\ell$ per avere una fascia che rimanga tutta sopra lo zero.

Con questa scelta, per ogni $n\geq N$, si ottiene:

$$
(\ell+\varepsilon )>a_n>\ell-\varepsilon
=\frac{\ell}{2}>0.
$$

L'uguaglianza $\ell-\varepsilon=\ell/2$ segue dalla scelta $\varepsilon=\ell/2$: sottrarre a $\ell$ la sua metà dà $\ell/2$.
Per concludere che $a_n>0$ basta la parte a destra di $a_n$; il richiamo al limite superiore $\ell+\varepsilon$ è riportato tra parentesi.

In parole semplici: **$a_n$ è maggiore di un numero positivo, quindi è positivo**. Dunque $a_n>0$ definitivamente.

Per esempio, se $\ell=4$, si sceglie $\varepsilon=2$: da un certo indice in poi vale $2<a_n<6$, quindi tutti quei termini sono positivi.

> In $\lim_{n\to+\infty}a_n=\ell$, è l'indice $n$ che cresce senza limite. I valori $a_n$ si avvicinano invece a $\ell$, che in questo secondo caso è finito.

### Limite negativo: ragionamento analogo

Il ragionamento è analogo per $\ell<0$. Anche qui si distinguono infinito e finito:

- Se $\ell=-\infty$, per ogni $M>0$ esiste $N\in\mathbb N$ tale che, per ogni $n\geq N$, vale $a_n<-M<0$.
- Se $\ell\in(-\infty,0)$, nella definizione di limite finito si sceglie $\varepsilon=-\ell/2>0$. Da un certo indice in poi si ottiene $a_n<\ell+\varepsilon=\ell/2<0$.

In entrambi i casi, $a_n<0$ definitivamente.

## 2) [[Enunciato]]: dai termini al limite

Si supponga che il limite $\ell\in\overline{\mathbb R}$ **esista**.

- Se $a_n\geq0$ definitivamente, allora $\ell\geq0$, cioè $\ell\in[0,+\infty]$.
- Se $a_n\leq0$ definitivamente, allora $\ell\leq0$, cioè $\ell\in[-\infty,0]$.

Non si afferma che una successione di termini non negativi ammetta necessariamente limite.

### Dimostrazione per assurdo

Siano $a_n\geq0$ per ogni $n\geq N_0$.
Si supponga **per assurdo** che $\ell<0$. Per la prima parte del teorema, esisterebbe allora $N_1$ tale che $a_n<0$ per ogni $n\geq N_1$.
Per $n\geq\max\{N_0,N_1\}$ si avrebbero contemporaneamente $a_n\geq0$ e $a_n<0$, impossibile.
Quindi $\ell\geq0$. Il caso non positivo si dimostra invertendo i segni.

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

Il termine $5/n$ tende a zero, quindi $a_n\to2>0$ (il calcolo è formalizzato nella [[80 Algebra dei Limiti di Successioni|successiva algebra dei limiti]]). Il teorema garantisce positività definitiva. Si può anche trovare la soglia:

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
