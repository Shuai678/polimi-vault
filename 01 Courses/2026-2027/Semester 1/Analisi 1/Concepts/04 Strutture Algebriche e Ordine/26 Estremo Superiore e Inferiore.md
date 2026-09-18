---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 02, PDF pp. 11-15
  - Libro, cap. 1.3
---

# Estremo superiore e inferiore

## Intuizione

L'estremo superiore è la migliore barriera superiore di un insieme: il più piccolo tra tutti i maggioranti. L'estremo inferiore è la migliore barriera inferiore: il più grande tra tutti i minoranti. Queste barriere non devono necessariamente appartenere all'insieme.

## Definizione formale

Sia $E\subseteq X$ non vuoto e limitato superiormente. Un elemento $s\in X$ è l'**estremo superiore** di $E$ se:

$$
x\leq s \qquad \forall x\in E
$$

e, per ogni maggiorante $k$ di $E$,

$$
s\leq k.
$$

Si scrive

$$
s=\sup E.
$$

Sia $E$ limitato inferiormente. Un elemento $t\in X$ è l'**estremo inferiore** di $E$ se:

$$
t\leq x \qquad \forall x\in E
$$

e, per ogni minorante $h$ di $E$,

$$
h\leq t.
$$

Si scrive

$$
t=\inf E.
$$

### Da dire all'orale

> L'estremo superiore di un insieme non vuoto e limitato superiormente è il minimo dei suoi maggioranti; l'estremo inferiore è il massimo dei suoi minoranti.

## Notazione

- $\sup E$ indica l'estremo superiore di $E$.
- $\inf E$ indica l'estremo inferiore di $E$.
- $\max E$ e $\min E$ indicano invece elementi appartenenti a $E$.

## Condizioni

- Per cercare $\sup E$, l'insieme deve essere non vuoto e limitato superiormente.
- Per cercare $\inf E$, l'insieme deve essere non vuoto e limitato inferiormente.
- In $\mathbb{R}$ queste condizioni garantiscono l'esistenza dei rispettivi estremi grazie alla completezza.
- L'estremo superiore e l'estremo inferiore non devono appartenere a $E$.

## Metodo / Dimostrazione

### Relazione con massimo e minimo

Se $M=\max E$, allora $M$ è un maggiorante. Inoltre, ogni maggiorante $k$ soddisfa $M\leq k$, perché $M\in E$. Quindi

$$
\sup E=M=\max E.
$$

Viceversa, se $\sup E\in E$, allora l'estremo superiore è un maggiorante appartenente a $E$ e quindi

$$
\sup E=\max E.
$$

Analogamente,

$$
\inf E\in E \Longleftrightarrow \inf E=\min E.
$$

## Esempi

### Intervallo aperto

Per $E=(0,1)$:

$$
\sup E=1,
\qquad
\inf E=0.
$$

Poiché $0,1\notin E$, l'insieme non possiede né massimo né minimo.

### Intervallo semiaperto

Per $F=(-2,3]$:

$$
\sup F=3=\max F,
\qquad
\inf F=-2.
$$

Poiché $-2\notin F$, il minimo non esiste.

### Insieme dei reciproci

Per

$$
G=\left\{\frac1n:n\in\mathbb{N},\ n\neq0\right\}
$$

si ha

$$
\sup G=\max G=1,
\qquad
\inf G=0,
$$

ma il minimo non esiste perché $0\notin G$.

## Errori comuni

- Confondere un maggiorante qualsiasi con l'estremo superiore.
- Credere che l'estremo superiore o inferiore debba appartenere all'insieme.
- Concludere che l'assenza del massimo implichi l'assenza dell'estremo superiore.
- Confondere il minimo dell'insieme con il minimo dell'insieme dei maggioranti.
- Affermare che gli estremi non esistono quando le barriere ottimali non appartengono all'insieme.

## Connessioni

- [[24 Maggioranti Minoranti e Insiemi Limitati|Maggioranti e minoranti]] forniscono le barriere tra le quali si cercano gli estremi.
- [[25 Massimo e Minimo|Massimo e minimo]] esistono quando gli estremi appartengono all'insieme.
- La completezza di $\mathbb{R}$ garantisce l'esistenza degli estremi per gli insiemi non vuoti opportunamente limitati.

## Prospettiva d'esame

Per verificare un estremo superiore bisogna dimostrare sia che è un maggiorante sia che nessun maggiorante più piccolo è possibile. L'appartenenza all'insieme deve essere controllata separatamente per stabilire l'esistenza del massimo.

## Sintassi LaTeX Suite

Le formule sono scritte con sintassi già espansa e renderizzabile, tra cui $\sup E$, $\inf E$, $\max E$ e $\min E$.
