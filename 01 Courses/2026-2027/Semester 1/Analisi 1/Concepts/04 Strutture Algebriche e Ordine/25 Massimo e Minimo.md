---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 02, PDF pp. 8-11
  - Libro, cap. 1.3
---

# Massimo e minimo

## Intuizione

Il massimo non è un maggiorante qualsiasi: è un maggiorante che appartiene all'insieme. Analogamente, il minimo è un minorante appartenente all'insieme.

## Definizione formale

Sia $E\subseteq X$ non vuoto.

Un elemento $x_0\in X$ è il **massimo** di $E$ se valgono entrambe le condizioni

$$
x_0\in E
$$

e

$$
x\leq x_0 \qquad \forall x\in E.
$$

In tal caso si scrive

$$
x_0=\max E.
$$

Un elemento $x_1\in X$ è il **minimo** di $E$ se

$$
x_1\in E
$$

e

$$
x_1\leq x \qquad \forall x\in E.
$$

In tal caso si scrive

$$
x_1=\min E.
$$

### Da dire all'orale

> Il massimo di un insieme non vuoto è un elemento dell'insieme maggiore o uguale a ogni altro suo elemento; il minimo è un elemento dell'insieme minore o uguale a ogni altro suo elemento.

## Notazione

- $\max E$ indica il massimo di $E$, quando esiste.
- $\min E$ indica il minimo di $E$, quando esiste.
- L'appartenenza $x_0\in E$ o $x_1\in E$ è parte essenziale della definizione.

## Condizioni

- Se $E$ possiede massimo, allora è limitato superiormente.
- Se $E$ possiede minimo, allora è limitato inferiormente.
- Le condizioni converse non valgono: un insieme limitato può non possedere massimo o minimo.
- Se massimo o minimo esistono, sono unici.

## Metodo / Dimostrazione

### Unicità del massimo

Supponiamo che $M_1$ e $M_2$ siano entrambi massimi di $E$. Poiché $M_1$ è massimo e $M_2\in E$,

$$
M_2\leq M_1.
$$

Poiché $M_2$ è massimo e $M_1\in E$,

$$
M_1\leq M_2.
$$

Per l'antisimmetria dell'ordine segue $M_1=M_2$. La dimostrazione per il minimo è analoga.

## Esempi

### Intervallo semiaperto

Per

$$
E=(-2,3]
$$

si ha $\max E=3$, perché $3\in E$ e $x\leq3$ per ogni $x\in E$.

L'insieme non possiede minimo: $-2$ è un minorante ma non appartiene a $E$, e ogni $x\in E$ può essere sostituito da un elemento di $E$ più piccolo e più vicino a $-2$.

Il numero $4$ è un maggiorante di $E$, ma non è il massimo perché $4\notin E$.

### Insieme reciproco dei naturali positivi

Per

$$
F=\left\{\frac1n:n\in\mathbb{N},\ n\neq0\right\}
$$

si ha $\max F=1$. L'insieme non possiede minimo, perché per ogni $\frac1n\in F$ vale

$$
\frac1{n+1}<\frac1n.
$$

## Errori comuni

- Verificare soltanto che il candidato sia un maggiorante o un minorante, dimenticando l'appartenenza all'insieme.
- Confondere un maggiorante con il massimo o un minorante con il minimo.
- Credere che la limitatezza garantisca massimo e minimo.
- Affermare che un insieme non ha estremo inferiore soltanto perché non ha minimo.

## Connessioni

- [[24 Maggioranti Minoranti e Insiemi Limitati|Maggioranti e minoranti]] diventano massimo o minimo quando appartengono all'insieme.
- L'estremo superiore e l'estremo inferiore descriveranno le migliori barriere anche quando queste non appartengono all'insieme.

## Prospettiva d'esame

Per verificare un massimo o un minimo bisogna controllare separatamente due condizioni: appartenenza all'insieme e confronto con tutti i suoi elementi.

## Sintassi LaTeX Suite

Le formule sono scritte con sintassi già espansa e renderizzabile, tra cui $\max E$, $\min E$, $\in$ e $\forall$.
