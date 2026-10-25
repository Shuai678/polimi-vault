---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF pp. 11-12
---

# Luoghi geometrici nel piano complesso

## Intuizione

Un'equazione in $z$ può descrivere un insieme di punti del piano complesso. Scrivendo $z=x+iy$, la parte reale controlla la coordinata orizzontale, la parte immaginaria quella verticale e il modulo la distanza dall'origine.

## Parte reale costante

Sia $z=x+iy$. La condizione

$$
\operatorname{Re}z=c
$$

equivale a $x=c$, mentre $y$ può assumere qualunque valore reale. Il luogo geometrico è quindi la retta verticale di equazione $x=c$.

### Da dire all'orale

> L'insieme dei numeri complessi con parte reale uguale a $c$ è la retta verticale di equazione $x=c$, perché l'ascissa è fissata mentre l'ordinata è libera.

## Parte immaginaria costante

La condizione

$$
\operatorname{Im}z=c
$$

equivale a $y=c$, mentre $x$ può assumere qualunque valore reale. Il luogo geometrico è quindi la retta orizzontale di equazione $y=c$.

### Da dire all'orale

> L'insieme dei numeri complessi con parte immaginaria uguale a $c$ è la retta orizzontale di equazione $y=c$, perché l'ordinata è fissata mentre l'ascissa è libera.

## Modulo costante

Per $z=x+iy$, la condizione

$$
|z|=\rho
$$

diventa

$$
\sqrt{x^2+y^2}=\rho.
$$

Se $\rho>0$, elevando al quadrato si ottiene

$$
x^2+y^2=\rho^2,
$$

che è la circonferenza con centro nell'origine e raggio $\rho$.

### Da dire all'orale

> Per $\rho>0$, l'insieme dei numeri complessi di modulo $\rho$ è la circonferenza con centro nell'origine e raggio $\rho$, perché il modulo rappresenta la distanza dall'origine.

## Condizioni

- Se $\rho>0$, $|z|=\rho$ descrive una circonferenza.
- Se $\rho=0$, l'unica soluzione è $z=0$.
- Se $\rho<0$, non esistono soluzioni, perché il modulo è sempre non negativo.

## Rappresentazione geometrica

![[Assets/43 Luoghi Geometrici nel Piano Complesso.svg|700]]

## Metodo

1. Scrivere $z=x+iy$.
2. Tradurre $\operatorname{Re}z$ con $x$, $\operatorname{Im}z$ con $y$ e $|z|$ con $\sqrt{x^2+y^2}$.
3. Riconoscere il luogo nel piano: coordinata reale costante significa retta verticale, coordinata immaginaria costante significa retta orizzontale, distanza dall'origine costante significa circonferenza.
4. Controllare le condizioni, in particolare il segno del raggio.

## Esempi

- $\operatorname{Re}z=2$ descrive la retta verticale $x=2$.
- $\operatorname{Im}z=-1$ descrive la retta orizzontale $y=-1$.
- $|z|=3$ descrive la circonferenza con centro nell'origine e raggio $3$.

## Errori comuni

- Scambiare verticale e orizzontale: $x$ costante dà una retta verticale, $y$ costante una retta orizzontale.
- Dire “asse immaginaria” invece di “asse immaginario”.
- Confondere la circonferenza $|z|=\rho$ con il disco $|z|\leq\rho$.
- Dimenticare che un raggio negativo non produce alcuna soluzione.

## Connessioni

- La lettura delle coordinate usa il [[40 Piano Complesso e Interpretazione Vettoriale|piano complesso]].
- Il luogo $|z|=\rho$ usa il [[41 Coniugato e Modulo dei Numeri Complessi|modulo]] come distanza dall'origine.
- Più in generale, grazie alla [[42 Distanza nel Piano Complesso|distanza]], $|z-w|=\rho$ descrive la circonferenza con centro $w$ e raggio $\rho$, quando $\rho>0$.

## Prospettiva d'esame

Potenziale rilevanza d'esame: tradurre rapidamente una condizione algebrica in un luogo geometrico e distinguere tra retta verticale, retta orizzontale, circonferenza e disco.
