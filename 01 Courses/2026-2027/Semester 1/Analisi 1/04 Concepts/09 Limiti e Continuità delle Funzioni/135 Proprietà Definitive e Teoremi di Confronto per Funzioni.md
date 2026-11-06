---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 18-22
---

# Proprietà definitive e teoremi di confronto per funzioni

## Proprietà definitivamente vere: definizione del docente

Siano $f:I\subseteq\mathbb R\to\mathbb R$ e $x_0\in\overline{\mathbb R}$ punto di accumulazione per $I$. Una proprietà $P$ vale **definitivamente per $x\to x_0$** se esiste un intorno $\mathcal U(x_0)$ tale che $P$ sia soddisfatta per tutti gli $x\in I\cap\mathcal U(x_0)$ diversi da $x_0$.

Con $I=\mathbb N$ e $x_0=+\infty$ si ritrova la definizione delle [[71 Proprietà Definitivamente Vere|proprietà definitive delle successioni]].

### Esempio del docente

Per $f(x)=1/x^2-17$, la funzione è definitivamente positiva per $x\to0$, ma non su tutto il suo dominio. Infatti

$$
\frac1{x^2}-17>0\iff0<|x|<\frac1{\sqrt{17}},
$$

mentre, per esempio, $f(1)=-16<0$.

## Teorema del confronto: due carabinieri

Siano $f,g,h:I\subseteq\mathbb R\to\mathbb R$, con $x_0$ di accumulazione per $I$. Se

$$
\lim_{x\to x_0}f(x)=\lim_{x\to x_0}h(x)=\ell
$$

con $\ell\in\overline{\mathbb R}$, e definitivamente per $x\to x_0$ vale $f(x)\leq g(x)\leq h(x)$, allora

$$
\lim_{x\to x_0}g(x)=\ell.
$$

Il risultato controlla il limite della funzione intermedia senza richiedere che esso sia già noto.

## Teorema del confronto per limiti infiniti

Se definitivamente $f(x)\leq g(x)$, allora

1. da $f(x)\to+\infty$ segue $g(x)\to+\infty$;
2. da $g(x)\to-\infty$ segue $f(x)\to-\infty$.

> [!note] Dimostrazioni nel PDF
> Il docente indica **«no dim.»** e rinvia ai corrispondenti argomenti per le successioni. I riferimenti sono [[82 Teorema dei Due Carabinieri]] e [[83 Teorema del confronto per successioni divergenti]]. Qui si conservano enunciati, ordine e applicazioni; non si aggiunge una prova attribuita al professore.

Gli stessi confronti valgono per limiti da destra e da sinistra, con le rispettive ipotesi sul dominio e sulle disuguaglianze definitive.

## Primo corollario: confronto in modulo

Se $g(x)\to0$ e $|f(x)|\leq g(x)$ definitivamente per $x\to x_0$, allora $f(x)\to0$. Infatti la disuguaglianza racchiude $f$ fra $-g$ e $g$, entrambi tendenti a zero. La condizione impone anche $g\geq0$ nella zona considerata.

## Secondo corollario: infinitesimo per funzione limitata

Se $g(x)\to0$ e $h$ è limitata definitivamente per $x\to x_0$, allora

$$
\lim_{x\to x_0}g(x)h(x)=0.
$$

Non si richiede che $h$ abbia un limite. Come per [[84 Confronto in Modulo e Prodotto con un Infinitesimo]], basta una costante $C>0$ con $|h(x)|\leq C$ nella zona necessaria: il prodotto è in modulo al più $C|g(x)|\to0$.

## Esempi del docente

### $\sin x/x$ per $x\to+\infty$

Per $x>0$,

$$
\left|\frac{\sin x}{x}\right|\leq\frac1x\longrightarrow0.
$$

Per confronto in modulo,

$$
\lim_{x\to+\infty}\frac{\sin x}{x}=0.
$$

Il seno non ha limite a $+\infty$, ma è limitato. Questo basta per moltiplicarlo per l'infinitesimo $1/x$.

### $x^7\sin(1/x)$ per $x\to0$

Per $x\neq0$,

$$
\left|x^7\sin\frac1x\right|\leq|x|^7\longrightarrow0.
$$

Quindi $\lim_{x\to0}x^7\sin(1/x)=0$, benché $\sin(1/x)$ non abbia limite in zero.

![[135 Confronti per Funzioni.svg|900]]

## Commenti per gli esercizi

Individuare un fattore che tende a zero e uno che rimane limitato, oppure costruire due funzioni con lo stesso limite che racchiudano quella da studiare. Le disuguaglianze devono valere per tutti i punti sufficientemente vicini, non soltanto lungo una successione scelta.

Nei confronti infiniti non invertire il ruolo di maggiorante e minorante: una funzione maggiore di una che diverge a $+\infty$ diverge anch'essa; essere minore di una funzione divergente a $+\infty$ non basta.

### Da dire all'orale

> Una proprietà vale definitivamente vicino a un punto se vale su tutti i punti del dominio di un opportuno intorno, escluso il centro. I due carabinieri trasferiscono il limite comune dei due estremi alla funzione intermedia. In particolare, una funzione dominata in modulo da un infinitesimo tende a zero, e il prodotto di un infinitesimo per una funzione definitivamente limitata tende a zero.
