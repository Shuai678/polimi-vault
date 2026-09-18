---
course: Analisi 1
type: concept
status: da-consolidare
source:
  - Lezione 02, PDF pp. 16-17
  - Libro, cap. 1.3
---

# Caratterizzazione degli estremi

## Intuizione

Per dimostrare che un numero è l'estremo superiore non basta verificare che sia un maggiorante: bisogna anche mostrare che ogni numero più piccolo viene superato da almeno un elemento dell'insieme. La caratterizzazione dell'estremo inferiore è simmetrica.

## Definizione formale

Sia $E\subseteq\mathbb{R}$ non vuoto e limitato superiormente. Vale

$$
s=\sup E
$$

se e solo se:

$$
x\leq s \qquad \forall x\in E
$$

e

$$
\forall k<s,\ \exists x\in E:\ k<x\leq s.
$$

Equivalentemente, la seconda condizione può essere scritta come

$$
\forall\varepsilon>0,\ \exists x\in E:\ s-\varepsilon<x\leq s.
$$

Per l'estremo inferiore:

$$
t=\inf E
$$

se e solo se

$$
t\leq x \qquad \forall x\in E
$$

e

$$
\forall h>t,\ \exists x\in E:\ t\leq x<h.
$$

Equivalentemente,

$$
\forall\varepsilon>0,\ \exists x\in E:\ t\leq x<t+\varepsilon.
$$

### Da dire all'orale

> Un numero $s$ è l'estremo superiore di $E$ se è un maggiorante e se ogni numero strettamente minore di $s$ non è un maggiorante; equivalentemente, per ogni $\varepsilon>0$ esiste un elemento di $E$ compreso tra $s-\varepsilon$ e $s$.

## Notazione

- $s$ è il candidato estremo superiore.
- $k<s$ è un candidato più piccolo di $s$.
- $\varepsilon>0$ rappresenta una distanza positiva arbitraria.
- L'elemento costruito deve soddisfare $x\in E$.

## Condizioni

- Occorre verificare che il candidato specifico $s$ sia un maggiorante; la sola limitatezza superiore di $E$ non basta.
- L'elemento $x$ usato nella seconda condizione deve appartenere a $E$.
- Le due condizioni devono essere verificate entrambe.

## Metodo / Dimostrazione

### Necessità

Supponiamo $s=\sup E$. Allora $s$ è un maggiorante, quindi $x\leq s$ per ogni $x\in E$.

Sia $k<s$. Se non esistesse $x\in E$ con $x>k$, allora $x\leq k$ per ogni $x\in E$ e $k$ sarebbe un maggiorante più piccolo di $s$. Ciò contraddirebbe la minimalità di $s$. Quindi

$$
\forall k<s,\ \exists x\in E:\ k<x\leq s.
$$

### Sufficienza

Supponiamo valide le due condizioni. La prima mostra che $s$ è un maggiorante.

Sia $M$ un maggiorante di $E$. Se fosse $M<s$, la seconda condizione fornirebbe $x\in E$ tale che $M<x$. Ma, essendo $M$ un maggiorante, dovrebbe valere $x\leq M$: contraddizione. Dunque $s\leq M$ per ogni maggiorante $M$, quindi $s=\sup E$.

La dimostrazione per l'estremo inferiore si ottiene invertendo le disuguaglianze e usando il più grande minorante.

## Esempi

Per $E=(0,1)$ e $s=1$:

1. ogni $x\in E$ soddisfa $x\leq1$, quindi $1$ è un maggiorante;
2. per ogni $k<1$ si può trovare $x\in E$ con $k<x\leq1$.

Se $0\leq k<1$, una scelta è

$$
x=\frac{k+1}{2},
$$

perché $k<x<1$. Se $k<0$, si può scegliere $x=\frac12$.

Il numero $2$ è un maggiorante di $E$, ma non è l'estremo superiore: scegliendo $k=\frac32<2$, non esiste alcun $x\in(0,1)$ tale che $x>\frac32$.

## Errori comuni

- Sostituire la verifica “$s$ è un maggiorante” con la più debole affermazione “$E$ è limitato superiormente”.
- Scegliere come elemento di approssimazione un numero che non appartiene a $E$, per esempio $x=1$ quando $E=(0,1)$.
- Verificare soltanto la prima condizione.
- Dimenticare l'ordine dei quantificatori: per ogni $k<s$ deve esistere un opportuno $x\in E$.

## Connessioni

- [[26 Estremo Superiore e Inferiore|La definizione di estremo superiore]] richiede il minimo dei maggioranti; questa caratterizzazione fornisce un metodo operativo equivalente.
- La formulazione con $\varepsilon$ anticipa il linguaggio che verrà usato nelle definizioni di limite.

## Prospettiva d'esame

Per dimostrare che $s=\sup E$, separare chiaramente i due passaggi: prima dimostrare che $s$ è un maggiorante, poi costruire, per ogni $k<s$ o $\varepsilon>0$, un elemento valido di $E$ sufficientemente vicino a $s$.

## Sintassi LaTeX Suite

Le formule sono scritte con sintassi già espansa e renderizzabile, tra cui $\forall$, $\exists$, $\varepsilon$, $\sup E$ e $\inf E$.
