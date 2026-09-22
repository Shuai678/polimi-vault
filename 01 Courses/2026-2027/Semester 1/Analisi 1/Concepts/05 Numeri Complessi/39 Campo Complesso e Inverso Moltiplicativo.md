---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF pp. 6-7
  - Libro, cap. 1.8, pp. 18-19
---

# Campo complesso e inverso moltiplicativo

## Intuizione

Le operazioni definite in $\mathbb C$ permettono di sommare, sottrarre, moltiplicare e dividere, purché nella divisione il divisore non sia nullo. Il passaggio caratteristico consiste nel costruire l'inverso di $z=a+ib$ usando $a-ib$, così da cancellare i termini immaginari nel prodotto.

## Definizione formale

L'insieme $\mathbb C$, dotato delle operazioni di somma e prodotto, è un campo.

- L'elemento neutro della somma è $0=0+i0$.
- L'elemento neutro del prodotto è $1=1+i0$.
- L'opposto di $z=a+ib$ è

$$
-z=-a-ib.
$$

- Se $z=a+ib\neq0$, il suo inverso moltiplicativo è

$$
z^{-1}=\frac{1}{z}
=\frac{a-ib}{a^2+b^2}
=\frac{a}{a^2+b^2}-i\frac{b}{a^2+b^2}.
$$

### Da dire all'orale

> Ogni numero complesso non nullo $z=a+ib$ possiede inverso moltiplicativo, dato da $\frac{a-ib}{a^2+b^2}$; il denominatore è strettamente positivo perché $a$ e $b$ non sono entrambi nulli.

## Notazione

- $-z$ indica l'opposto additivo di $z$.
- $z^{-1}$ indica l'inverso moltiplicativo di $z$ e non l'opposto.
- Il numero $a^2+b^2$ è reale e non negativo.

## Condizioni

La formula dell'inverso richiede $z\neq0$. Questa condizione equivale a dire che $a$ e $b$ non sono entrambi nulli; pertanto almeno uno tra $a^2$ e $b^2$ è positivo e

$$
a^2+b^2>0.
$$

La divisione per $a^2+b^2$ è quindi lecita.

## Metodo / Dimostrazione

Per costruire l'inverso si osserva che

$$
\begin{aligned}
(a+ib)(a-ib)
&=a^2-iab+iab-i^2b^2\\
&=a^2+b^2.
\end{aligned}
$$

I termini immaginari opposti si cancellano e si usa $i^2=-1$. Dividendo per $a^2+b^2$ si ottiene

$$
(a+ib)\frac{a-ib}{a^2+b^2}
=\frac{a^2+b^2}{a^2+b^2}
=1.
$$

Questo verifica che il numero costruito è effettivamente l'inverso di $z$.

## Esempi

Per

$$
z=-2+5i
$$

l'opposto è

$$
-z=2-5i.
$$

Per

$$
z=3-4i
$$

si ha $a=3$, $b=-4$ e $a^2+b^2=25$. Quindi

$$
z^{-1}=\frac{3}{25}+i\frac{4}{25}.
$$

## Errori comuni

- Confondere l'opposto $-z$ con l'inverso $z^{-1}$.
- Cambiare anche il segno della parte reale nel numeratore dell'inverso.
- Scrivere $a^2-b^2$ al denominatore invece di $a^2+b^2$.
- Dimenticare la condizione $z\neq0$.
- Dividere per $a^2+b^2$ soltanto una delle due parti.

## Connessioni

- La formula usa le [[38 Operazioni con i Numeri Complessi|operazioni con i numeri complessi]].
- L'espressione $a-ib$ sarà formalizzata come coniugato di $a+ib$.
- L'espressione $a^2+b^2$ sarà collegata al quadrato del modulo.
- La rappresentazione geometrica viene sviluppata nel [[40 Piano Complesso e Interpretazione Vettoriale|piano complesso]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: saper ricavare e verificare la formula dell'inverso, dichiarando esplicitamente la condizione $z\neq0$ e giustificando perché il denominatore è positivo.
