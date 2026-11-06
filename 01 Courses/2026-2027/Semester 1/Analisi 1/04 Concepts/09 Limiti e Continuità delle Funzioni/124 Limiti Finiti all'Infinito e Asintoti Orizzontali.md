---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 13, PDF pp. 10-13
  - Libro, §5.2, pp. 136-138; §5.12, pp. 171-172
---

# Limiti finiti all'infinito e asintoti orizzontali

## 1. Limite finito per $x\to+\infty$

Sia $\ell\in\mathbb R$ e sia $+\infty$ punto di accumulazione del dominio $I$. Esplicitando gli intorni della [[123 Definizione Topologica di Limite e Teorema Ponte|definizione topologica]],

$$
\lim_{x\to+\infty}f(x)=\ell
\iff
\forall\varepsilon>0\ \exists M>0\ \forall x\in I:
\quad x>M\Longrightarrow|f(x)-\ell|<\varepsilon.
$$

La conclusione equivale a $\ell-\varepsilon<f(x)<\ell+\varepsilon$. La soglia $M$ controlla l'ascissa; $\varepsilon$ controlla la distanza verticale dal valore limite.

## 2. Limite finito per $x\to-\infty$

Sia $-\infty$ punto di accumulazione per $I$. Si ha

$$
\lim_{x\to-\infty}f(x)=\ell
\iff
\forall\varepsilon>0\ \exists M>0\ \forall x\in I:
\quad x<-M\Longrightarrow|f(x)-\ell|<\varepsilon.
$$

Si deve stare sufficientemente a sinistra, non semplicemente richiedere che $|x|$ sia grande: quella condizione includerebbe entrambe le direzioni.

## Esempi del docente

$$
\lim_{x\to+\infty}e^{-x}=0,
\qquad
\lim_{x\to-\infty}\frac1x=0.
$$

## Asintoto orizzontale

Il docente chiama $y=\ell$, con $\ell\in\mathbb R$, **asintoto orizzontale per $x\to+\infty$**, oppure per $x\to-\infty$, quando il corrispondente limite di $f(x)$ vale $\ell$. In particolare $e^{-x}$ ha asintoto orizzontale $y=0$ a $+\infty$.

![[124 Limite Finito e Asintoto Orizzontale.svg|900]]

## Limite per eccesso e per difetto — definizione del docente

Se $\ell\in\mathbb R$ e $x_0\in\overline{\mathbb R}$, si scrive

$$
\lim_{x\to x_0}f(x)=\ell^+
\quad\text{oppure}\quad
\lim_{x\to x_0}f(x)=\ell^-
$$

se il limite è $\ell$ e, in un opportuno intorno di $x_0$, per i punti del dominio diversi dal centro vale rispettivamente $f(x)\geq\ell$ oppure $f(x)\leq\ell$. Si mantengono le **disuguaglianze non strette del PDF**.

Il segno qui è sul **valore limite**, non sul punto al quale tende $x$. Per esempio,

$$
\lim_{x\to+\infty}e^{-x}=0^+,
\qquad
\lim_{x\to-\infty}\frac1x=0^-.
$$

Per $x\to+\infty$, il limite per eccesso equivale a

$$
\forall\varepsilon>0\ \exists M>0:\quad
x\in I,\ x>M\Longrightarrow\ell\leq f(x)<\ell+\varepsilon.
$$

Quello per difetto equivale a

$$
\forall\varepsilon>0\ \exists M>0:\quad
x\in I,\ x>M\Longrightarrow\ell-\varepsilon<f(x)\leq\ell.
$$

Per $x\to-\infty$ si sostituisce $x>M$ con $x<-M$.

## Commenti ed esempio svolto con la definizione

Per $e^{-x}\to0$, fissato $\varepsilon>0$, scegliamo $M=\max\{1,\log(1/\varepsilon)\}$. Se $x>M$, allora $0<e^{-x}<\varepsilon$. Per $1/x\to0$ a $-\infty$, basta $M=\max\{1,1/\varepsilon\}$: se $x<-M$, allora $|1/x|<\varepsilon$ e $1/x<0$.

Questi calcoli esplicitano le soglie degli esempi del PDF.

> [!info] Approfondimento dal libro
> Un asintoto non richiede che il grafico non intersechi mai la retta: richiede che la distanza verticale tenda a zero. Il libro, §5.12, p. 172, lo illustra con $\sin x/x$, esempio ripreso dal docente nella Lezione 14.

### Da dire all'orale

> Il limite finito a più infinito significa che, per ogni precisione positiva, tutti i punti del dominio oltre una soglia hanno valori a distanza dal limite minore della precisione. La retta orizzontale alla quota del limite è un asintoto in quella direzione. Eccesso e difetto descrivono il lato dal quale i valori della funzione si avvicinano al limite.
