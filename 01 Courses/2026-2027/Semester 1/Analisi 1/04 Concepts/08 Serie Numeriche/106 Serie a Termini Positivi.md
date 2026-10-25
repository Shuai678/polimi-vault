---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 4-5
  - Libro, §4.1, p. 116; teorema 4.9
---

# Serie a termini positivi

## Definizione e terminologia del docente

Nel corso, una serie $\sum_{n=1}^{+\infty}a_n$ è detta **a termini positivi** se $a_n\geq0$ per ogni $n$. In questa denominazione sono quindi ammessi termini nulli: matematicamente sono termini **non negativi**.

È a termini **definitivamente positivi** se esiste $n_0$ tale che

$$
a_n\geq0\qquad\text{per ogni }n\geq n_0.
$$

Gli eventuali termini precedenti possono avere qualunque segno, senza alterare il carattere della serie. Quando un criterio contiene il rapporto $a_{n+1}/a_n$, servirà invece la non nullità del denominatore nella coda, come precisato in [[110 Criterio del Rapporto per Serie]].

## Intuizione

Dopo l'indice $n_0$, aggiungiamo soltanto quantità non negative: le somme parziali non possono più diminuire. Quindi non possono oscillare senza limite; o si avvicinano a un valore finito, oppure crescono senza limite.

## Teorema di regolarità

Una serie a termini definitivamente non negativi è regolare: **converge oppure diverge a $+\infty$**. Non può essere irregolare né divergere a $-\infty$.

### Ipotesi e tesi

L'ipotesi è il segno non negativo dei termini da un certo indice. La tesi riguarda la successione delle somme parziali $S_N=\sum_{n=1}^{N}a_n$:

$$
\boxed{\exists\lim_{N\to+\infty}S_N\in\mathbb R\cup\{+\infty\}.}
$$

### Strategia e dimostrazione

Per $N$ sufficientemente grande,

$$
S_N-S_{N-1}=a_N\geq0.
$$

Dunque $(S_N)$ è definitivamente crescente in senso non stretto. Per [[76 Teorema del Limite delle Successioni Monotone]] la coda ha un limite reale esteso. Essendo crescente da un valore iniziale finito, è limitata inferiormente e il limite non può essere $-\infty$.

Se le somme parziali sono limitate superiormente, il teorema monotono assicura un limite finito e la serie converge. Se non sono limitate superiormente, lo stesso teorema dà $S_N\to+\infty$.

## Condizione equivalente per la convergenza

Per queste serie,

$$
\boxed{\text{la serie converge}\quad\Longleftrightarrow\quad
\text{le somme parziali sono limitate superiormente}.}
$$

Un verso è la prova precedente. Il viceversa usa [[77 Limitatezza delle Successioni Convergenti]]: se la serie converge, $(S_N)$ è limitata. È sufficiente limitare superiormente la coda delle somme, perché i valori precedenti sono soltanto in numero finito.

Questa equivalenza fonda il [[107 Criterio del Confronto per Serie]]: un maggiorante sommabile può fornire proprio il limite superiore necessario.

## Positività definitiva e segno della somma

Se **tutti** i termini sono non negativi, anche $S_N\geq0$ e l'eventuale somma è non negativa. Se soltanto la coda ha termini non negativi, la somma finita può invece essere negativa.

Per esempio poniamo $a_1=-10$ e $a_n=1/[n(n+1)]$ per $n\geq2$. Dalla serie di Mengoli,

$$
\sum_{n=1}^{+\infty}a_n
=-10+\left(1-\frac12\right)=-\frac{19}{2}.
$$

La serie è definitivamente positiva e converge, ma la sua somma è negativa. L'invarianza del carattere rispetto ai termini iniziali non implica l'invarianza della somma.

## Collegamento con la condizione necessaria

Se $a_n\geq0$ definitivamente e $a_n$ non tende a zero, la [[103 Condizione Necessaria di Convergenza di una Serie]] esclude la convergenza. Il teorema di questa nota esclude l'irregolarità e la divergenza negativa: resta soltanto la divergenza a $+\infty$.

Se invece $a_n\to0$, occorre ancora decidere il carattere. La [[104 Serie Armonica]] dimostra che il limite zero del termine non basta neppure per termini positivi.

### Da dire all'orale

> Una serie a termini definitivamente non negativi converge oppure diverge positivamente, perché le sue somme parziali sono definitivamente crescenti. La convergenza equivale alla loro limitatezza superiore. Non serve che i primi termini siano positivi, ma questi possono cambiare il valore della somma.

Potenziale rilevanza d'esame: dimostrazione con il teorema monotono e distinzione tra positività dei termini, limitatezza delle somme e limite del termine generale.
