---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 9-14
  - Libro, §4.2.1, pp. 119-120; teorema 4.14, caso di rapporto positivo finito
---

# Criterio del confronto asintotico per serie

## Intuizione

Se due successioni positive sono equivalenti, da un certo indice ognuna è compresa fra due multipli positivi dell'altra. Il [[107 Criterio del Confronto per Serie|confronto diretto]] trasferisce allora la convergenza e la divergenza da una serie all'altra.

L'equivalenza riguarda il **termine generale**; il risultato riguarda il **carattere delle serie**, non l'uguaglianza delle loro somme.

## Teorema

Siano $a_n,b_n$ definitivamente strettamente positivi e supponiamo che

$$
a_n\sim b_n,\qquad\text{cioè }\frac{a_n}{b_n}\to1.
$$

Allora

$$
\boxed{\sum a_n\text{ e }\sum b_n\text{ hanno lo stesso carattere}:}
$$

convergono entrambe oppure divergono entrambe a $+\infty$. La positività assicura che non si presenti il caso irregolare, per [[106 Serie a Termini Positivi]].

## Strategia e dimostrazione completa

Dalla [[72 Limite Finito di una Successione|definizione di limite]], scegliendo la tolleranza $\varepsilon=1/2$, esiste $N_1$ tale che

$$
\frac12<\frac{a_n}{b_n}<\frac32\qquad(n\geq N_1).
$$

Scegliamo anche un indice dopo il quale $a_n,b_n>0$ e prendiamo il massimo dei due indici. Moltiplicando per $b_n>0$ otteniamo definitivamente

$$
\frac12b_n<a_n<\frac32b_n.
$$

![[109 Equivalenza e Confronto con Multipli.svg|900]]

Se $\sum b_n$ converge, il maggiorante $3b_n/2$ ha serie convergente e il confronto dà la convergenza di $\sum a_n$. Viceversa $b_n<2a_n$: se $\sum a_n$ converge, converge anche $\sum b_n$.

Se $\sum b_n$ diverge positivamente, dal minorante $a_n>b_n/2$ segue la divergenza di $\sum a_n$. Viceversa, da $b_n>2a_n/3$ segue la divergenza di $\sum b_n$ quando diverge $\sum a_n$. Le costanti positive non cambiano il carattere, per [[101 Linearità e Algebra delle Serie]]. Tutti i confronti sono sufficienti nella coda.

## Stesso carattere non significa stessa somma

Per $n\geq1$, consideriamo $a_n=2^{-n}$ e $b_n=2^{-n}+4^{-n}$. Si ha

$$
\frac{b_n}{a_n}=1+2^{-n}\to1,
$$

quindi $a_n\sim b_n$. Ma le formule geometriche danno

$$
\sum_{n=1}^{+\infty}a_n=1,\qquad
\sum_{n=1}^{+\infty}b_n=1+\frac13=\frac43.
$$

Il criterio trasferisce il carattere; non permette di calcolare la somma sostituendo il termine con un equivalente.

## Esercizio — Discussione con parametro

### Testo — pp. 12-13

Per $\alpha\in\mathbb R$, studiare

$$
\sum_{k=1}^{+\infty}\frac{5k^2-1}{k^\alpha+k}\arctan\frac1k.
$$

### Idea

Il termine è positivo per ogni $k\geq1$. Il numeratore è equivalente a $5k^2$ e $\arctan(1/k)\sim1/k$. Nel denominatore decide il confronto fra $k^\alpha$ e $k$: il caso $\alpha=1$ va separato perché i contributi hanno la stessa grandezza.

### Svolgimento passo per passo

Poniamo $a_k=(5k^2-1)\arctan(1/k)/(k^\alpha+k)$. Si ha

$$
5k^2-1\sim5k^2,\qquad \arctan(1/k)\sim\frac1k.
$$

Per il denominatore:

$$
\begin{array}{ll}
\alpha>1:&k^\alpha+k=k^\alpha(1+k^{1-\alpha})\sim k^\alpha,\\
\alpha=1:&k^\alpha+k=2k,\\
\alpha<1:&k^\alpha+k=k(1+k^{\alpha-1})\sim k.
\end{array}
$$

Le proprietà di [[94 Equivalenza Asintotica]] per prodotti e quozienti danno

$$
a_k\sim
\begin{cases}
\dfrac5{k^{\alpha-1}},&\alpha>1,\\[4pt]
\dfrac52,&\alpha=1,\\[4pt]
5,&\alpha<1.
\end{cases}
$$

Se $\alpha\leq1$, il termine non tende a zero: tende a $5/2$ oppure a $5$. La [[103 Condizione Necessaria di Convergenza di una Serie]] esclude la convergenza; la positività implica divergenza a $+\infty$.

Se $\alpha>1$, confrontiamo con la [[108 Serie Armoniche Generalizzate e di Bertrand|serie armonica generalizzata]] di esponente $p=\alpha-1$: converge se $p>1$, cioè $\alpha>2$; diverge se $p\leq1$, cioè $1<\alpha\leq2$.

### Risultato

$$
\boxed{
\text{la serie converge per }\alpha>2;
\quad\text{diverge a }+\infty\text{ per }\alpha\leq2.}
$$

### Cosa imparare

Il passaggio $\alpha=1$ cambia il termine dominante del denominatore; la soglia di **convergenza della serie** è invece $\alpha=2$. Per $1<\alpha\leq2$ i termini tendono a zero e la serie diverge comunque.

## Rapporto con limite positivo diverso da uno

> [!info] Approfondimento dal libro
> Il teorema 4.14, pp. 119-120, comprende il caso in cui $a_n/b_n\to c\in(0,+\infty)$. Esso si riconduce alla forma del docente: $a_n\sim cb_n$ e moltiplicare una serie per $c>0$ non ne cambia il carattere. Non si devono perdere i coefficienti nell'equivalenza; per decidere il carattere si può poi separare la costante positiva.

## Osservazione: Concordanza di segno e ipotesi del criterio

Da $a_n\sim b_n$ si deduce che i due termini sono **definitivamente concordi di segno**: il rapporto tende a $1>0$ e, per il [[79 Teorema di Permanenza del Segno|teorema di permanenza del segno]], è definitivamente positivo. Non si può però dedurre che il segno comune sia fisso: per esempio, con $a_n=b_n=(-1)^n$ il segno cambia a ogni indice.

Per applicare il criterio si deve quindi verificare, oltre all'equivalenza, la **positività definitiva**. La sola concordanza di segno non è sufficiente.

## Procedura ed errori comuni

1. Verificare il segno e il dominio nella coda.
2. Trovare un equivalente del termine intero con [[95 Equivalenti e Sviluppi Asintotici Notevoli]] e termini dominanti.
3. Riconoscere una serie campione e applicare la classificazione con tutte le soglie.
4. Concludere sul carattere, senza attribuire la stessa somma alle due serie.

Con un parametro, non trattare una somma come se il termine dominante fosse lo stesso per ogni valore. Per un numeratore oscillante limitato può essere più utile il confronto diretto, come nell'esempio $18+\cos n$ del Concept 107.

### Da dire all'orale

> Due serie con termini definitivamente positivi e asintoticamente equivalenti hanno lo stesso carattere. Dal rapporto che tende a uno ottengo che ogni termine è definitivamente compreso fra metà e tre mezzi del termine di riferimento. Il confronto diretto dà entrambe le implicazioni. Le somme, se le serie convergono, possono essere diverse.

Potenziale rilevanza d'esame: prova delle stime, discussioni parametriche e distinzione tra limite del termine, carattere e valore della somma.
