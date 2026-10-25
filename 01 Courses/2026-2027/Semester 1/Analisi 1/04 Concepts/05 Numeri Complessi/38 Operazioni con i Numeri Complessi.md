---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF p. 6
  - Libro, cap. 1.8, p. 18
---

# Operazioni con i numeri complessi

## Intuizione

La somma combina separatamente le parti reali e le parti immaginarie. Il prodotto si sviluppa con la proprietà distributiva e si riduce alla forma algebrica usando $i^2=-1$.

## Definizione formale

Siano

$$
z=a+ib,
\qquad
w=x+iy,
\qquad
a,b,x,y\in\mathbb R.
$$

La somma è definita da

$$
z+w=(a+x)+i(b+y).
$$

Il prodotto è definito da

$$
zw=(ax-by)+i(ay+bx).
$$

### Da dire all'orale

> La somma di due numeri complessi si ottiene sommando separatamente le parti reali e le parti immaginarie. Il prodotto si calcola distributivamente e si riconduce alla forma algebrica mediante la relazione $i^2=-1$.

## Notazione

- $a$ e $x$ sono le parti reali di $z$ e $w$.
- $b$ e $y$ sono le rispettive parti immaginarie.
- Il termine $ax-by$ è la parte reale del prodotto.
- Il termine $ay+bx$ è la parte immaginaria del prodotto.

## Condizioni

I coefficienti $a,b,x,y$ sono reali. Per somma e prodotto non è necessario imporre che $z$ o $w$ siano diversi da zero.

## Metodo / Dimostrazione

Per ricavare la formula del prodotto si applica la proprietà distributiva:

$$
\begin{aligned}
(a+ib)(x+iy)
&=ax+aiy+ibx+i^2by\\
&=ax+iay+ibx-by\\
&=(ax-by)+i(ay+bx).
\end{aligned}
$$

Il segno meno davanti a $by$ deriva da $i^2=-1$.

## Esempi

Siano

$$
z=2+3i,
\qquad
w=1-2i.
$$

Allora

$$
z+w=3+i.
$$

Per il prodotto,

$$
\begin{aligned}
zw
&=(2+3i)(1-2i)\\
&=2-4i+3i-6i^2\\
&=2-i+6\\
&=8-i.
\end{aligned}
$$

## Errori comuni

- Dimenticare i prodotti incrociati nel prodotto.
- Sostituire $i^2$ con $1$ invece che con $-1$.
- Scrivere $ax+by$ al posto di $ax-by$.
- Confondere il termine immaginario $i(ay+bx)$ con la parte immaginaria $ay+bx$.

## Connessioni

- Le operazioni usano la [[37 Unità Immaginaria e Forma Algebrica|forma algebrica]] dei numeri complessi.
- Queste definizioni rendono $\mathbb C$ chiuso rispetto alla somma e al prodotto.
- L'[[39 Campo Complesso e Inverso Moltiplicativo|inverso moltiplicativo]] completa la verifica della struttura di campo.

## Prospettiva d'esame

Potenziale rilevanza d'esame: saper sviluppare un prodotto senza perdere il segno generato da $i^2=-1$ e riportare il risultato nella forma $a+ib$.
