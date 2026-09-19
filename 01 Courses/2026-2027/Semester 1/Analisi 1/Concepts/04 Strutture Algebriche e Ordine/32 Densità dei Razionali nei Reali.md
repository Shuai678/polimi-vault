---
course: Analisi 1
type: theorem
status: studied
source: Lezione 02, PDF p. 24
---

# Densità dei razionali nei reali

## Teorema

Per ogni $x,y\in\mathbb{R}$ con $x<y$, esiste $r\in\mathbb{Q}$ tale che

$$
x<r<y.
$$

Si dice che $\mathbb{Q}$ è denso in $\mathbb{R}$.

## In parole semplici

Tra due numeri reali distinti, ordinati come $x<y$, esiste sempre almeno un numero razionale.

## Condizioni

- $x,y\in\mathbb{R}$;
- $x<y$;
- il numero costruito deve appartenere a $\mathbb{Q}$ ed essere strettamente compreso tra i due estremi.

## Conclusione

$$
\exists r\in\mathbb{Q}:\ x<r<y.
$$

## Perché è utile

La densità consente di approssimare numeri reali mediante razionali e garantisce la presenza di punti razionali in ogni intervallo aperto non vuoto.

## Intuizione

I razionali possono avvicinarsi arbitrariamente a un numero irrazionale, come $\sqrt2$, senza coincidere necessariamente con esso.

## Strategia della dimostrazione

Si sceglie una griglia razionale di passo $1/n$ più fine della distanza $y-x$, quindi si prende il primo punto della griglia posto a destra di $x$.

## Dimostrazione passo per passo

Siano $x,y\in\mathbb{R}$ con $x<y$. Poiché $y-x>0$, per la proprietà archimedea esiste $n\in\mathbb{N}$, $n>0$, tale che

$$
\frac1n<y-x.
$$

Scegliamo il più piccolo intero $m$ strettamente maggiore di $nx$. Allora

$$
m-1\leq nx<m.
$$

Poniamo

$$
r=\frac mn\in\mathbb{Q}.
$$

Dalla disuguaglianza $nx<m$, dividendo per $n>0$, segue

$$
x<\frac mn=r.
$$

Inoltre, da $m-1\leq nx$ segue $m\leq nx+1$, quindi

$$
r=\frac mn\leq x+\frac1n<y.
$$

Pertanto $x<r<y$.

## Esempi

Tra $1{,}41$ e $1{,}42$ si trova il razionale

$$
\frac{283}{200}=1{,}415.
$$

La densità permette inoltre di costruire successioni razionali che approssimano $\sqrt2$ sempre meglio, senza rendere $\sqrt2$ razionale.

## Uso all'esame

Bisogna dichiarare esplicitamente l'ordine $x<y$ e concludere con un razionale strettamente compreso tra i due numeri.

## Errore comune

- Omettere la condizione $x<y$.
- Credere che la densità implichi $\mathbb{Q}=\mathbb{R}$.
- Confondere un'approssimazione razionale con l'uguaglianza al numero irrazionale approssimato.
- Confondere densità e completezza: $\mathbb{Q}$ è denso in $\mathbb{R}$ ma non è completo.

## Da dire all'orale

> L'insieme dei razionali è denso nei reali: per ogni $x,y\in\mathbb{R}$ con $x<y$ esiste $r\in\mathbb{Q}$ tale che $x<r<y$.

## Connessioni

- [[27 Completezza dei Numeri Reali|La completezza]] distingue $\mathbb{R}$ da $\mathbb{Q}$, nonostante la densità dei razionali.
- [[31 Retta Reale e Intervalli|Ogni intervallo aperto]] non vuoto contiene numeri razionali.
