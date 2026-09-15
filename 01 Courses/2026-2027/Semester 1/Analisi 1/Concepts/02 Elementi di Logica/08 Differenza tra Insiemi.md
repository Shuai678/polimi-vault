---
course: Analisi 1
type: concept
status: studied
source: Lezione 01, PDF p. 6
---

# Differenza tra insiemi

## Intuizione

La differenza $A\setminus B$ conserva gli elementi di $A$ ed elimina quelli che appartengono anche a $B$.

## Definizione formale

$$
A\setminus B=\{x\in A:x\notin B\}.
$$

### Da dire all'orale

> La differenza tra due insiemi $A$ e $B$ è l'insieme degli elementi che appartengono ad $A$ ma non appartengono a $B$.

## Esempi

### Esempio svolto: calcolare entrambe le differenze

Siano

$$
A=\{1,2,3\},
\qquad
B=\{2,4\}.
$$

Per calcolare $A\setminus B$ partiamo dagli elementi di $A$:

- $1$ non appartiene a $B$, quindi rimane;
- $2$ appartiene a $B$, quindi viene eliminato;
- $3$ non appartiene a $B$, quindi rimane.

Pertanto

$$
A\setminus B=\{1,3\}.
$$

Per calcolare $B\setminus A$ partiamo invece dagli elementi di $B$:

- $2$ appartiene ad $A$, quindi viene eliminato;
- $4$ non appartiene ad $A$, quindi rimane.

Pertanto

$$
B\setminus A=\{4\}.
$$

L'esempio mostra che l'ordine è essenziale:

$$
A\setminus B\ne B\setminus A.
$$

### Esempio importante

La differenza

$$
\mathbb R\setminus\mathbb Q
$$

contiene i numeri reali che non sono razionali, cioè i numeri irrazionali. Per esempio, $\sqrt2\in\mathbb R\setminus\mathbb Q$, mentre $\frac12\notin\mathbb R\setminus\mathbb Q$ perché è razionale.

## Connessioni

$$
\mathbb R\setminus\mathbb Q
$$

è l'insieme dei numeri irrazionali.

## Errori comuni

- In generale $A\setminus B\ne B\setminus A$.
- Non usare un simbolo non definito come $\mathbb I$ per gli irrazionali; in questa lezione usare $\mathbb R\setminus\mathbb Q$.
