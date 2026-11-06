---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 13-15
  - Libro, §6.1-6.2, pp. 185-186
---

# Discontinuità eliminabili ed estensione per continuità

## Primo caso della classificazione del docente

Siano $f:I\subseteq\mathbb R\to\mathbb R$ e $x_0\in I$ punto di accumulazione per $I$. Se

$$
\lim_{x\to x_0}f(x)=\ell\in\mathbb R,
\qquad \ell\neq f(x_0),
$$

allora $x_0$ è un punto di **discontinuità eliminabile** per $f$. Il comportamento vicino al punto suggerisce un valore finito, ma la funzione nel punto ne assume un altro.

## Esempio del docente: il quadrato del segno

Il professore considera $f(x)=(\operatorname{sign}x)^2$, dove

$$
\operatorname{sign}x=\begin{cases}
1,&x>0,\\
0,&x=0,\\
-1,&x<0.
\end{cases}
$$

Quindi

$$
f(x)=\begin{cases}1,&x\neq0,\\0,&x=0.\end{cases}
$$

Il limite in zero è $1$, mentre $f(0)=0$. La discontinuità è eliminabile.

![[132 Discontinuita Eliminabile.svg|900]]

## Ridefinire il valore nel punto

Si pone

$$
\widetilde f(x)=\begin{cases}
f(x),&x\neq x_0,\\
\ell,&x=x_0.
\end{cases}
$$

La funzione così ridefinita è continua in $x_0$, perché

$$
\lim_{x\to x_0}\widetilde f(x)
=\lim_{x\to x_0}f(x)=\ell=\widetilde f(x_0).
$$

Nel caso del quadrato del segno basta porre $\widetilde f(0)=1$: la nuova funzione è costantemente uguale a $1$.

## Osservazione del docente: estendere il dominio

Se invece $x_0\notin I$ ma esiste $\lim_{x\to x_0}f(x)=\ell\in\mathbb R$, si può **estendere per continuità** la funzione a $I\cup\{x_0\}$ con la stessa formula a tratti. La nuova funzione coincide con $f$ nel suo dominio originario ed è definita e continua anche nel nuovo punto.

Nel primo caso si cambia un valore già assegnato; nel secondo si aggiunge un punto al dominio. La [[131 Funzione di Dirichlet e Discontinuità Ovunque|precisazione sul dominio]] impedisce di confondere i due casi.

## Esempio successivo del docente: $\sin x/x$

Il professore richiama il valore

$$
\lim_{x\to0}\frac{\sin x}{x}=1,
$$

senza svilupparne qui la dimostrazione. Si può quindi estendere la funzione, originariamente definita per $x\neq0$, ponendo

$$
\widetilde f(x)=\begin{cases}
\dfrac{\sin x}{x},&x\neq0,\\
1,&x=0.
\end{cases}
$$

La funzione estesa è continua in zero. Il valore $1$ è obbligato: qualunque altro valore non coinciderebbe con il limite.

## Commenti e uso negli esercizi

Nelle funzioni a tratti con un parametro nel solo punto, calcolare prima il limite della formula valida fuori dal punto. Se è finito, l'unico valore che rende la funzione continua è quel limite. Se il limite non esiste oppure è infinito, nessun valore reale assegnato al solo punto può ottenere la continuità.

Il libro, §6.2, pp. 185-186, presenta gli stessi due meccanismi, distinguendo l'estensione dalla correzione di un valore. Non basta dire “il denominatore si annulla”: occorre studiare il limite dell'intera espressione.

### Da dire all'orale

> Una discontinuità è eliminabile se il limite nel punto esiste finito ma non coincide con il valore assegnato. Si elimina ridefinendo il valore uguale al limite. Se il punto era fuori dal dominio, la stessa costruzione è un'estensione per continuità, che aggiunge il punto al dominio.
