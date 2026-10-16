---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-10-16
source: esempi originali del tutor
---

# Esempi svolti su prodotti cartesiani e relazioni

Stato: **da studiare**. Gli svolgimenti sono preparati dal tutor; non sono soluzioni attribuite allo studente né esercizi ufficiali numerati.

## 1 Elencare un prodotto cartesiano

### Problema

Dati $C=\{0,2\}$ e $D=\{1,3,5\}$, descrivere $C\times D$ e stabilire se $(1,2)$ vi appartiene.

### Svolgimento

Per ogni primo elemento di $C$ si scelgono tutte le seconde componenti in $D$:

$$
\begin{aligned}
C\times D=\{&(0,1),(0,3),(0,5),\\
&(2,1),(2,3),(2,5)\}.
\end{aligned}
$$

Ci sono $2\cdot3=6$ coppie.

La coppia $(1,2)$ non appartiene al prodotto: la sua prima componente $1$ non appartiene a $C$ e la seconda componente $2$ non appartiene a $D$.

Invece $(2,1)\in C\times D$, perché $2\in C$ e $1\in D$.

Prerequisito: [[01 Prodotto Cartesiano]].

## 2 Verificare una relazione di equivalenza

### Problema

Su $A=\{1,2,3\}$ si considera

$$
R=\{(1,1),(2,2),(3,3),(1,2),(2,1)\}.
$$

Descriverne le proprietà.

### Svolgimento

**Riflessività:** tutte le coppie $(a,a)$ per $a\in A$ sono presenti.

**Simmetria:** le coppie diagonali sono inverse di se stesse; $(1,2)$ e $(2,1)$ sono entrambe presenti.

**Transitività:** se un collegamento riguarda $3$, l'unico collegamento possibile è $3R3$, e la conclusione richiesta è già presente. Se riguarda $1$ o $2$, tutte le quattro coppie fra questi due elementi sono presenti. Ogni concatenazione resta quindi in $R$.

La relazione è di equivalenza.

Non è antisimmetrica: $1R2$ e $2R1$, ma $1\ne2$.

Prerequisiti: [[02 Relazioni Binarie]], [[03 Relazioni di Equivalenza]], [[04 Relazioni di Ordine]].

## 3 Distinguere simmetria e antisimmetria

### Problema

Confrontare l'inclusione e l'uguaglianza sulla famiglia

$$
S=\{\varnothing,\{1\},\{2\},\{1,2\}\}.
$$

### Svolgimento

L'inclusione è riflessiva, antisimmetrica e transitiva, quindi è un ordine. Non è simmetrica:

$$
\varnothing\subseteq\{1\},
\qquad
\{1\}\not\subseteq\varnothing.
$$

Non tutti gli elementi sono confrontabili: $\{1\}\not\subseteq\{2\}$ e $\{2\}\not\subseteq\{1\}$.

L'uguaglianza è riflessiva, simmetrica e transitiva, quindi è un'equivalenza. È anche antisimmetrica, poiché $A=B$ e $B=A$ implicano $A=B$.

Quest'ultimo esempio mostra che simmetria e antisimmetria non sono negazioni l'una dell'altra.

Prerequisito: [[04 Relazioni di Ordine]].

## Collegamento alle lezioni

- [[01 Courses/2026-2027/Semester 1/Algebra Lineare/Lectures/Lecture 00|Lezione 0]]: prodotti e relazioni.
- [[01 Courses/2026-2027/Semester 1/Algebra Lineare/Lectures/Lecture 01|Lezione 1]]: inclusione e ordine.
