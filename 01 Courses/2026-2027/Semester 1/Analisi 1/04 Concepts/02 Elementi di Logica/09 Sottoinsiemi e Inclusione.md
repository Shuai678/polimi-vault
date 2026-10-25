---
course: Analisi 1
type: concept
status: studied
source: Lezione 01, PDF p. 6
---

# Sottoinsiemi e inclusione

## Intuizione

$A$ è contenuto in $B$ quando non esiste alcun elemento di $A$ che sia esterno a $B$.

## Definizione formale

$$
A\subset B
\Longleftrightarrow
\forall x,\;x\in A\Rightarrow x\in B.
$$

### Da dire all'orale

> L'insieme $A$ è un sottoinsieme di $B$ se ogni elemento di $A$ appartiene anche a $B$.

## Esempi

### Esempio svolto: verificare un'inclusione

Siano

$$
A=\{1,2\},
\qquad
B=\{0,1,2,3\}.
$$

Gli unici elementi di $A$ sono $1$ e $2$, ed entrambi appartengono a $B$. Quindi ogni elemento di $A$ appartiene a $B$ e possiamo concludere che

$$
A\subset B.
$$

### Esempio svolto: negare un'inclusione

Per mostrare che $\mathbb R\not\subset\mathbb Q$ basta trovare un reale che non sia razionale. Scegliamo $\sqrt2$:

$$
\sqrt2\in\mathbb R,
\qquad
\sqrt2\notin\mathbb Q.
$$

Pertanto

$$
\mathbb R\not\subset\mathbb Q.
$$

Al contrario, ogni razionale è reale; dunque $\mathbb Q\subset\mathbb R$. Nel complesso:

$$
\mathbb N\subset\mathbb Z\subset\mathbb Q\subset\mathbb R\subset\mathbb C.
$$

## Errori comuni

- $x\in A$ riguarda un elemento $x$; $A\subset B$ riguarda due insiemi.
- Per negare un'inclusione basta trovare un elemento di $A$ che non appartiene a $B$.
