---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 5-8, 11-12
  - Libro, §4.2.1, pp. 117-118; teorema 4.10 e osservazione 4.11
---

# Criterio del confronto per serie

## Intuizione e quando si usa

Per termini non negativi, sommare quantità più piccole di quelle di una serie convergente mantiene l'accumulo limitato. Viceversa, se una serie più piccola diverge positivamente, anche quella più grande deve divergere.

Il metodo serve quando esistono disuguaglianze semplici: funzioni limitate, denominatori da minorare o maggiorare e confronti con geometriche, armoniche e [[108 Serie Armoniche Generalizzate e di Bertrand|serie campione]].

## Quattro criteri per serie a termini non negativi

Questi quattro criteri permettono di studiare il carattere delle serie a termini non negativi. Le ipotesi sul segno devono valere almeno **definitivamente**; per il confronto asintotico e il rapporto si richiede la **positività stretta**.

### 1. Confronto diretto

Cerchi una disuguaglianza $0\leq a_n\leq b_n$, valida almeno definitivamente:

- se $\sum b_n$ converge, converge anche $\sum a_n$;
- se $\sum a_n$ diverge a $+\infty$, diverge a $+\infty$ anche $\sum b_n$.

È il **principio di base**: può richiedere inventiva per trovare una maggiorazione o una minorazione utile. Non decide automaticamente ogni serie: occorre trovare un confronto adatto.

### 2. Confronto asintotico

Nel [[109 Criterio del Confronto Asintotico per Serie|confronto asintotico]] confronti $a_n$ con un termine più semplice $b_n$. Se sono definitivamente positivi e $a_n\sim b_n$, cioè

$$
\lim_{n\to+\infty}\frac{a_n}{b_n}=1,
$$

le due serie hanno **lo stesso carattere**. Si dimostra usando il confronto diretto.

### 3. Criterio del rapporto

Nel [[110 Criterio del Rapporto per Serie|criterio del rapporto]] calcoli, con termini definitivamente positivi,

$$
L=\lim_{n\to+\infty}\frac{a_{n+1}}{a_n}.
$$

È spesso comodo con **fattoriali e prodotti**. Il rapporto riguarda due termini consecutivi della stessa successione.

### 4. Criterio della radice

Nel [[111 Criterio della Radice per Serie|criterio della radice]] calcoli, con termini definitivamente non negativi,

$$
L=\lim_{n\to+\infty}\sqrt[n]{a_n}.
$$

È spesso comodo con **espressioni elevate alla $n$**.

Per **rapporto e radice**, se il limite esiste, $L<1$ implica convergenza, $L>1$ implica divergenza a $+\infty$ e **$L=1$ non decide**. Entrambi si dimostrano mediante confronti con serie geometriche.

## Teorema

Siano $a_n,b_n$ successioni reali tali che, definitivamente,

$$
0\leq a_n\leq b_n.
$$

Allora:

$$
\boxed{
\begin{aligned}
\sum b_n\text{ converge}&\Longrightarrow\sum a_n\text{ converge},\\
\sum a_n=+\infty&\Longrightarrow\sum b_n=+\infty.
\end{aligned}}
$$

La **convergenza passa alla serie minore**; la **divergenza positiva passa alla maggiore**. Il segno non negativo è un'ipotesi essenziale per il teorema qui studiato.

## Dimostrazione passo per passo

Se le disuguaglianze valgono soltanto dopo $n_0$, consideriamo prima le code: per [[105 Code e Resto di una Serie]] il carattere è lo stesso. Possiamo quindi dimostrare il risultato supponendo $0\leq a_n\leq b_n$ per ogni $n\geq1$.

Poniamo

$$
S_N=\sum_{n=1}^{N}a_n,\qquad
\sigma_N=\sum_{n=1}^{N}b_n.
$$

Sommando le disuguaglianze finite,

$$
0\leq S_N\leq\sigma_N\qquad\text{per ogni }N.
$$

Entrambe le successioni sono crescenti per [[106 Serie a Termini Positivi]]. Per il [[76 Teorema del Limite delle Successioni Monotone]] esistono quindi i limiti

$$
S=\lim_{N\to\infty}S_N,\qquad
\sigma=\lim_{N\to\infty}\sigma_N,
\qquad S,\sigma\in\mathbb R\cup\{+\infty\}.
$$

**1. Divergenza della minore.** Se $\sum_{n=1}^{\infty}a_n$ diverge, allora

$$
S=\sum_{n=1}^{\infty}a_n=\lim_{N\to\infty}S_N=+\infty.
$$

Poiché $\sigma_N\geq S_N$ per ogni $N\geq1$, per il [[83 Teorema del confronto per successioni divergenti]] segue

$$
\sum_{n=1}^{\infty}b_n=\lim_{N\to\infty}\sigma_N=\sigma=+\infty.
$$

Quindi anche la serie maggiore diverge a $+\infty$.

**2. Convergenza della maggiore.** Se $\sum_{n=1}^{\infty}b_n$ converge, allora

$$
\sum_{n=1}^{\infty}b_n=\lim_{N\to\infty}\sigma_N=\sigma\in\mathbb R.
$$

Essendo $(\sigma_N)$ crescente,

$$
\sigma=\sup_{N\geq1}\sigma_N\geq\sigma_N.
$$

Pertanto, per ogni $N\geq1$,

$$
0\leq S_N\leq\sigma_N\leq\sigma\in\mathbb R.
$$

La successione $(S_N)$ è dunque crescente e limitata superiormente, quindi converge a un numero reale:

$$
\sum_{n=1}^{\infty}a_n=\lim_{N\to\infty}S_N=S\in\mathbb R.
$$

La serie minore converge.

## Confronto fra le somme: attenzione ai primi termini

Se $0\leq a_n\leq b_n$ vale **per ogni indice**, passando al limite in $S_N\leq\sigma_N$ otteniamo

$$
\sum_{n=1}^{+\infty}a_n\leq\sum_{n=1}^{+\infty}b_n
$$

nei reali estesi. Se invece il confronto vale soltanto nella coda, determina il carattere ma non necessariamente l'ordine fra le somme totali.

Per esempio $a_1=100$, $a_n=0$ per $n\geq2$ e $b_n=1/[n(n+1)]$ soddisfano $a_n\leq b_n$ per $n\geq2$. Tuttavia le somme sono $100$ e $1$: i termini iniziali impediscono il confronto globale.

## Esercizio del PDF — Numeratore oscillante ma limitato

### Testo

Studiare

$$
\sum_{n=2}^{+\infty}\frac{18+\cos n}{n^2\log n}.
$$

### Idea e svolgimento passo per passo

Per $n\geq2$ il denominatore è positivo. Poiché $-1\leq\cos n\leq1$,

$$
0<\frac{18+\cos n}{n^2\log n}
\leq\frac{19}{n^2\log n}.
$$

Il logaritmo è crescente e $\log n\geq\log2>0$, quindi

$$
\frac{19}{n^2\log n}
\leq\frac{19}{\log2}\frac1{n^2}.
$$

La serie $\sum1/n^2$ converge, per la classificazione delle armoniche generalizzate enunciata dal docente e raccolta nel Concept 108. Moltiplicare per $19/\log2$ non ne cambia la convergenza. Il criterio dà quindi

$$
\boxed{\sum_{n=2}^{+\infty}\frac{18+\cos n}{n^2\log n}\text{ converge}.}
$$

### Cosa imparare ed errore comune

Non serve un equivalente del numeratore oscillante. La stima uniforme è sufficiente e il denominatore è controllato soltanto dove $\log n>0$. Un confronto con una serie convergente decide il carattere, non calcola la somma esatta.

## Come scegliere la direzione e gli errori comuni

- Per dimostrare convergenza, cercare un **maggiorante** con serie convergente.
- Per dimostrare divergenza, cercare un **minorante** con serie divergente positivamente.
- Essere più piccoli di una serie divergente non decide; essere più grandi di una convergente non decide.

La disuguaglianza $1/n^2\leq1/n$ mostra entrambe le cautele: la serie minore converge mentre la maggiore diverge. Non si possono invertire le due implicazioni del teorema.

### Da dire all'orale

> Per due serie con zero minore o uguale ad a con indice n minore o uguale a b con indice n definitivamente, la convergenza della maggiore implica quella della minore e la divergenza positiva della minore implica quella della maggiore. La prova confronta le somme parziali, che sono crescenti. Il confronto dei valori delle somme richiede la disuguaglianza per tutti gli indici.

Potenziale rilevanza d'esame: ipotesi, verso del confronto, prova con somme parziali e uso delle stime per termini oscillanti limitati.
