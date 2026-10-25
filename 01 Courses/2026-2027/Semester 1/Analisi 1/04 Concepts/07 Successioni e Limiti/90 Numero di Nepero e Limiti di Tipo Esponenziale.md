---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 08, PDF pp. 12-14
  - Libro, §3.4.1, pp. 91-92 e §3.5.3, p. 97
---

# Numero di Nepero e limiti di tipo esponenziale

## Perché viene introdotto

La successione

$$
s_n=\left(1+\frac1n\right)^n,\qquad n\geq1,
$$

combina una base che tende a $1$ con un esponente che cresce senza limite. È una forma indeterminata $1^{+\infty}$, ma in questo caso il limite esiste ed è una costante fondamentale.

## Teorema e definizione

La successione $(s_n)$ è strettamente crescente e limitata superiormente. Per [[76 Teorema del Limite delle Successioni Monotone]], ha un limite finito, detto **numero di Nepero**:

$$
\boxed{e:=\lim_{n\to+\infty}\left(1+\frac1n\right)^n
=\sup\left\{\left(1+\frac1n\right)^n:n\geq1\right\}.}
$$

Numericamente $e\approx2{,}71828$. La stretta crescita implica

$$
\left(1+\frac1n\right)^n<e\qquad\text{per ogni }n\geq1:
$$

infatti $s_n<s_{n+1}\leq\sup\{s_k:k\geq1\}=e$. Il supremo non è un termine raggiunto dalla successione.

![[90 Avvicinamento al Numero di Nepero.svg|760]]

Il grafico mostra alcuni termini e la retta del limite; non sostituisce la dimostrazione di crescita e limitatezza.

### Da dire all'orale

> Il numero di Nepero è il limite della successione $(1+1/n)^n$. Questo limite esiste ed è finito perché la successione è crescente e limitata superiormente. Coincide con il suo estremo superiore e ogni termine è strettamente minore di $e$.

## Strategia della dimostrazione

Il PDF indica l'uso della [[21 Dimostrazione per Induzione|disuguaglianza di Bernoulli]] per crescita e limitatezza, senza sviluppare tutti i calcoli. Il libro permette di completare proprio questi passaggi.

> [!info] Approfondimento dal libro
> La prova seguente sviluppa §3.4.1, pp. 91-92. Si usa Bernoulli, $(1+t)^m\geq1+mt$ per $t>-1$ e $m\in\mathbb N$. Per $m\geq2$ e $t\neq0$ l'ineguaglianza è stretta: nel passo induttivo compare un contributo positivo proporzionale a $t^2$.

### Crescita di $s_n$

Per $n\geq2$, tutti i fattori sono positivi e

$$
\frac{s_n}{s_{n-1}}
=\frac{\left(\frac{n+1}{n}\right)^n}
{\left(\frac n{n-1}\right)^{n-1}}
=\left(1-\frac1{n^2}\right)^n\frac n{n-1}.
$$

Bernoulli, con $t=-1/n^2>-1$ e $m=n\geq2$, dà

$$
\left(1-\frac1{n^2}\right)^n>1-\frac1n=\frac{n-1}{n}.
$$

Quindi $s_n/s_{n-1}>1$, ossia $s_n>s_{n-1}$.

### Limitatezza tramite una successione ausiliaria

Introduciamo

$$
t_n=\left(1+\frac1n\right)^{n+1}.
$$

Per $n\geq2$,

$$
\frac{t_{n-1}}{t_n}
=\left(1+\frac1{n^2-1}\right)^n\frac n{n+1}.
$$

Bernoulli dà

$$
\left(1+\frac1{n^2-1}\right)^n
\geq1+\frac n{n^2-1}>1+\frac1n=\frac{n+1}{n}.
$$

L'ineguaglianza centrale usa $n/(n^2-1)>1/n$, equivalente a $n^2>n^2-1$. Ne segue $t_{n-1}/t_n>1$: $(t_n)$ è decrescente. Inoltre

$$
0<s_n<t_n\leq t_1=4.
$$

Dunque $(s_n)$ è limitata superiormente. Il teorema monotono conclude l'esistenza del limite finito; poiché $e\geq s_2=9/4$, in particolare $e>1$.

## Teorema: indice reale che tende a infinito

Sia $(c_n)$ una successione reale con $c_n\to+\infty$ **oppure** $c_n\to-\infty$. Allora

$$
\boxed{\left(1+\frac1{c_n}\right)^{c_n}\to e.}
$$

L'espressione è definita definitivamente: $c_n\neq0$ e $1+1/c_n>0$. Nel caso negativo basta che $c_n<-1$. Il teorema del PDF vale quindi anche per l'avvicinamento a $-\infty$, non soltanto per indici naturali. È enunciato senza dimostrazione completa nelle pp. 13-14.

## Corollario e dimostrazione: parametro reale

Per ogni $a\in\mathbb R$ fissato,

$$
\boxed{\left(1+\frac an\right)^n\to e^a.}
$$

La base è definitivamente positiva anche per $a<0$, scegliendo $n>|a|$. Se $a=0$, la successione è costante uguale a $1=e^0$.

Se $a\neq0$, poniamo $c_n=n/a$. Allora

$$
\left(1+\frac an\right)^n
=\left[\left(1+\frac1{c_n}\right)^{c_n}\right]^a.
$$

Infatti $ac_n=n$. Per $a>0$, $c_n\to+\infty$; per $a<0$, $c_n\to-\infty$. In entrambi i casi la quantità tra parentesi tende a $e>0$. Il limite della potenza di esponente fissato è pertanto $e^a$.

## Metodo per riconoscere la forma

Il modello è **base $1+$ quantità piccola**, elevata a un esponente grande. Non basta riconoscere $1^\infty$: occorre confrontare il piccolo incremento con l'esponente.

Se $u_n\to0$, $u_n\neq0$ definitivamente, $1+u_n>0$ definitivamente e $v_nu_n\to L\in\mathbb R$, allora

$$
(1+u_n)^{v_n}
=\left[(1+u_n)^{1/u_n}\right]^{u_nv_n}\to e^L.
$$

Se $u_n$ ha segno definitivamente positivo o negativo, il teorema precedente si applica a $c_n=1/u_n$. Se cambia segno, lo stesso limite della base tra parentesi segue trattando separatamente gli indici positivi e negativi: entrambe le parti tendono a $e$, quindi per ogni precisione le due code soddisfano la medesima stima. Questa conseguenza non introduce nuovi limiti notevoli dal libro.

## Esempi svolti

Per $n>2$,

$$
\left(1-\frac2n\right)^n\to e^{-2}.
$$

Il parametro è $a=-2$ e la positività definitiva evita potenze reali di una base negativa.

Inoltre

$$
\left(1+\frac3n\right)^{2n}
=\left[\left(1+\frac3n\right)^n\right]^2\to(e^3)^2=e^6.
$$

Per distinguere diversi esiti della forma $1^\infty$,

$$
\left(1+\frac1{n^2}\right)^n\to1:
$$

qui $u_n=1/n^2$ e $v_n=n$, dunque $v_nu_n=1/n\to0$ e il limite è $e^0=1$.

## Formula soltanto annunciata dal docente

> [!note] Rimando alle lezioni sulle serie — PDF p. 13
> Il docente scrive $e=\displaystyle\sum_{n=0}^{+\infty}\frac1{n!}$ e aggiunge «Vedremo». Si conserva qui l'annuncio per completezza del riferimento al PDF. In questa lezione non sono spiegate né dimostrate la somma infinita e questa rappresentazione; la trattazione seguirà le lezioni sulle serie. La definizione di $e$ da usare nella Lezione 08 resta il limite di $(1+1/n)^n$.

## Errori comuni e prospettiva d'esame

- Concludere che ogni forma $1^\infty$ vale $e$.
- Dimenticare il coefficiente dell'incremento o quello dell'esponente.
- Usare soltanto il caso $c_n\to+\infty$ nella dimostrazione con parametro negativo.
- Confondere supremo e massimo, o giustificare la crescita soltanto con un grafico.

Potenziale rilevanza d'esame: definizione di $e$, ruolo del teorema monotono, corollario con parametro reale e trasformazioni esatte. Il PDF accenna a una futura rappresentazione mediante serie; tale argomento non viene sviluppato qui.
