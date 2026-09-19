---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 02, PDF pp. 13-15
  - Libro, cap. 1.3
---

# Completezza dei numeri reali

## Intuizione

La completezza esprime il fatto che la retta reale non presenta buchi: ogni insieme non vuoto che possiede una barriera superiore ammette in $\mathbb{R}$ una migliore barriera superiore. Questa proprietà distingue $\mathbb{R}$ da $\mathbb{Q}$.

## Definizione formale

Ogni insieme non vuoto $E\subseteq\mathbb{R}$ limitato superiormente possiede estremo superiore in $\mathbb{R}$:

$$
E\neq\varnothing,\quad E\subseteq\mathbb{R},\quad E\text{ limitato superiormente}
\Longrightarrow
\exists\sup E\in\mathbb{R}.
$$

Equivalentemente, ogni insieme non vuoto $E\subseteq\mathbb{R}$ limitato inferiormente possiede estremo inferiore in $\mathbb{R}$.

Nella presentazione assiomatica della lezione, questa proprietà prende il nome di **assioma di completezza** o **assioma di continuità**.

### Da dire all'orale

> Ogni sottoinsieme non vuoto di $\mathbb{R}$ limitato superiormente possiede estremo superiore in $\mathbb{R}$; equivalentemente, ogni sottoinsieme non vuoto limitato inferiormente possiede estremo inferiore. Questa proprietà, detta completezza, non vale in $\mathbb{Q}$.

## Notazione

- $E\neq\varnothing$ significa che $E$ non è vuoto.
- $\sup E\in\mathbb{R}$ indica che l'estremo superiore esiste come numero reale.
- La completezza riguarda l'esistenza degli estremi, non necessariamente di massimo e minimo.

## Condizioni

Per applicare la proprietà dell'estremo superiore bisogna verificare:

1. $E\subseteq\mathbb{R}$;
2. $E\neq\varnothing$;
3. $E$ è limitato superiormente.

Per la versione inferiore si sostituisce la terza condizione con la limitatezza inferiore.

## Metodo / Dimostrazione

### Equivalenza con la proprietà dell'estremo inferiore

Supponiamo valida la proprietà dell'estremo superiore e sia $E\subseteq\mathbb{R}$ non vuoto e limitato inferiormente. Definiamo

$$
-E=\{-x:x\in E\}.
$$

Se $h$ è un minorante di $E$, allora $-h$ è un maggiorante di $-E$; dunque $-E$ è limitato superiormente. Per completezza esiste

$$
s=\sup(-E).
$$

Poniamo $t=-s$. Per ogni $x\in E$ si ha $-x\leq s$, quindi $x\geq-s=t$: pertanto $t$ è un minorante di $E$.

Se $h$ è un qualsiasi minorante di $E$, allora $-h$ è un maggiorante di $-E$. Dalla minimalità di $s$ segue $s\leq-h$, cioè $t=-s\geq h$. Quindi $t$ è il più grande minorante e

$$
\inf E=-\sup(-E).
$$

## Esempi

### Incompletezza di $\mathbb{Q}$

Consideriamo

$$
A=\{q\in\mathbb{Q}:q\geq0,\ q^2\leq2\}.
$$

L'insieme è non vuoto, perché $0\in A$, ed è limitato superiormente, per esempio da $2$. Osservato in $\mathbb{R}$, ha estremo superiore

$$
\sup A=\sqrt2.
$$

Poiché $\sqrt2\notin\mathbb{Q}$ e nessun razionale può sostituirlo come più piccolo maggiorante, $A$ non possiede estremo superiore in $\mathbb{Q}$. Pertanto $\mathbb{Q}$ non è completo.

### Intervallo aperto

Per $E=(0,1)$, la completezza garantisce l'esistenza di $\sup E=1$ e $\inf E=0$, ma non l'esistenza di massimo e minimo.

## Errori comuni

- Applicare la completezza senza verificare che l'insieme sia non vuoto e limitato nella direzione richiesta.
- Dimenticare che l'ambiente deve essere $\mathbb{R}$: la proprietà non vale in $\mathbb{Q}$.
- Credere che la completezza garantisca massimo e minimo invece degli estremi superiore e inferiore.
- Dire che l'insieme razionale è “limitato in $\sqrt2$” invece di precisare che è limitato superiormente e che il suo estremo superiore in $\mathbb{R}$ è $\sqrt2$.

## Connessioni

- [[26 Estremo Superiore e Inferiore|Gli estremi]] sono gli oggetti la cui esistenza è garantita dalla completezza.
- L'irrazionalità di $\sqrt2$ mostra concretamente il buco presente in $\mathbb{Q}$.
- La completezza sarà alla base dell'esistenza di radici, limiti e altri oggetti definiti per approssimazione.

## Prospettiva d'esame

Prima di invocare la completezza bisogna elencarne le ipotesi. Per mostrare che $\mathbb{Q}$ non è completo, si usa un insieme razionale non vuoto e limitato la cui barriera ottimale reale è $\sqrt2\notin\mathbb{Q}$.
