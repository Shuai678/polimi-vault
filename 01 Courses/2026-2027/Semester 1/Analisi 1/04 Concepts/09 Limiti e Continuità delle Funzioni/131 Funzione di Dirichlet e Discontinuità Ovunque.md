---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 11-12
---

# Funzione di Dirichlet e discontinuità ovunque

## Esempio del docente

La **funzione di Dirichlet** è

$$
f(x)=\begin{cases}
0,&x\in\mathbb R\setminus\mathbb Q,\\
1,&x\in\mathbb Q.
\end{cases}
$$

Per ogni $x_0\in\overline{\mathbb R}$, quindi anche per $x_0=+\infty$ e $x_0=-\infty$, il limite $\lim_{x\to x_0}f(x)$ non esiste nella retta reale estesa. In particolare $f$ è discontinua in ogni punto reale.

## Dimostrazione del professore

Se $x_0\in\overline{\mathbb R}$, possiamo trovare due successioni $(x_n)$ e $(z_n)$ tali che

1. $z_n\neq x_0$ e $x_n\neq x_0$ per ogni $n\geq1$;
2. $z_n\in\mathbb R\setminus\mathbb Q$ e $x_n\in\mathbb Q$ per ogni $n\geq1$;
3. $\lim_{n\to+\infty}z_n=\lim_{n\to+\infty}x_n=x_0$.

Questo è possibile perché $\mathbb Q$ e $\mathbb R\setminus\mathbb Q$ sono densi in $\mathbb R$.

Si ha quindi

$$
f(x_n)=1,\qquad f(z_n)=0\qquad\forall n\geq1,
$$

e pertanto

$$
\lim_{n\to+\infty}f(x_n)=1
\neq0=\lim_{n\to+\infty}f(z_n).
$$

Quindi $\lim_{x\to x_0}f(x)$ non esiste, per ogni $x_0\in\overline{\mathbb R}$. $\square$

## Osservazione successiva del docente: prima controllare il dominio

Per

$$
f:\mathbb R\setminus\{0\}\to\mathbb R,\qquad f(x)=\frac1x,
$$

domandare se la funzione sia continua o discontinua in zero **non ha senso secondo la definizione adottata**, perché zero non appartiene al dominio. Si possono invece studiare i limiti della funzione in zero, come già fatto in [[128 Limiti Laterali e Asintoti Verticali]].

## Commenti alla prova

Per $x_0\in\mathbb R$, per scegliere $x_n$ e $z_n$ si prendono rispettivamente un razionale e un irrazionale in ogni intorno di raggio $1/n$ del punto, escludendo il centro. Si usa la stessa idea dei [[120 Punti di Accumulazione]] e la [[32 Densità dei Razionali nei Reali|densità]]. Non serve una formula esplicita per le successioni. Per esplicitare anche i casi infiniti compresi nell'enunciato del PDF, a $+\infty$ si possono scegliere $x_n=n$ e $z_n=n+\sqrt2$; a $-\infty$, $x_n=-n$ e $z_n=-n-\sqrt2$. Le prime sono razionali, le seconde irrazionali, e le immagini restano rispettivamente $1$ e $0$. Queste scelte esplicite sono commenti alla prova del docente.

Il problema non è che i valori di $f$ diventino grandi: la funzione assume soltanto $0$ e $1$ ed è limitata. Il problema è che valori incompatibili con uno stesso limite si trovano arbitrariamente vicini a ogni punto. La limitatezza non basta per la continuità e non basta neppure per l'esistenza del limite.

Non è possibile rappresentare fedelmente questa funzione tracciando due normali curve: ogni intervallo contiene punti con valore $0$ e punti con valore $1$. Un disegno con un numero finito di punti ha soltanto valore illustrativo; la dimostrazione usa la densità.

### Da dire all'orale

> La funzione di Dirichlet vale uno sui razionali e zero sugli irrazionali. In ogni punto della retta reale estesa posso scegliere una successione di razionali e una di irrazionali, entrambe tendenti al punto e diverse da esso. Le immagini tendono rispettivamente a uno e a zero, quindi il limite non esiste, nemmeno agli infiniti. La funzione è discontinua in ogni punto reale del suo dominio.
