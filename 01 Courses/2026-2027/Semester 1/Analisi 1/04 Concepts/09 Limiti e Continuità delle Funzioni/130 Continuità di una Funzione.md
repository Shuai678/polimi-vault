---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 8-11
  - Libro, §6.1, pp. 183-184; §5.1, pp. 133-134, esempio 5.3
---

# Continuità di una funzione

## Definizione del docente

Siano $f:I\subseteq\mathbb R\to\mathbb R$ e $x_0\in I$ un punto di accumulazione per $I$. Se

$$
\boxed{\lim_{x\to x_0}f(x)=f(x_0),}
$$

diciamo che $f$ è **continua in $x_0$**. È continua in $I$ se lo è in ogni punto di $I$ al quale si applica questa definizione. Il docente usa la notazione

$$
f\in C^0(I).
$$

Occorre che il punto appartenga al dominio: nella continuità si confronta il limite con un valore reale effettivamente assegnato.

## Osservazione metrica

$f$ è continua in $x_0$ se e solo se

$$
\forall\varepsilon>0\ \exists\delta>0\ \forall x\in I:
\quad |x-x_0|<\delta\Longrightarrow|f(x)-f(x_0)|<\varepsilon.
$$

Qui **non si esclude $x=x_0$**: in quel caso la differenza dei valori è zero. Il limite finito usava invece $0<|x-x_0|<\delta$.

## Osservazione successionale

Per ogni successione $(x_n)\subset I$ con $x_n\to x_0$, deve valere

$$
\lim_{n\to+\infty}f(x_n)=f(x_0)
=f\left(\lim_{n\to+\infty}x_n\right).
$$

L'uguaglianza fra limite dell'immagine e immagine del limite è giustificata dalla continuità. Non è una regola da usare senza verificarne l'ipotesi.

## Esempio del docente: la funzione esponenziale

Il professore verifica prima la continuità di $e^x$ in zero e poi in un punto $x_0\neq0$.

## Dimostrazione del professore

### Primo caso: $x_0=0$

Si ha $f(0)=1$. Verifichiamo che $e^x$ è continua in zero. Fissiamo $\varepsilon>0$ e cerchiamo di ottenere

$$
1-\varepsilon<e^x<1+\varepsilon.
$$

La richiesta si scrive come il sistema

$$
\begin{cases}
e^x<1+\varepsilon,\\
e^x>1-\varepsilon.
\end{cases}
$$

Il docente considera $\varepsilon\in(0,1)$. Passando ai logaritmi, il sistema equivale a

$$
\begin{cases}
x<\log(1+\varepsilon),\\
x>\log(1-\varepsilon).
\end{cases}
$$

cioè

$$
\log(1-\varepsilon)<x<\log(1+\varepsilon),
$$

dove $\log(1-\varepsilon)<0$ e $\log(1+\varepsilon)>0$. Con

$$
\delta=\min\left\{\log(1+\varepsilon),
\log\bigl((1-\varepsilon)^{-1}\bigr)\right\}>0,
$$

si ha

$$
x\in(-\delta,\delta)
\Longrightarrow x\in\bigl(\log(1-\varepsilon),\log(1+\varepsilon)\bigr)
\Longrightarrow e^x\in(1-\varepsilon,1+\varepsilon).
$$

Quindi, per definizione di limite,

$$
\lim_{x\to0}e^x=1=e^0,
$$

cioè $e^x$ è continua in zero.

### Secondo caso: $x_0\neq0$

Il docente scrive

$$
e^x-e^{x_0}=e^{x_0}\bigl(e^{x-x_0}-1\bigr).
$$

Quindi

$$
\begin{aligned}
\lim_{x\to x_0}(e^x-e^{x_0})
&=\lim_{x\to x_0}e^{x_0}(e^{x-x_0}-1)\\
&=e^{x_0}\lim_{x\to x_0}(e^{x-x_0}-1)\\
&=e^{x_0}\lim_{t\to0}(e^t-1)=0.
\end{aligned}
$$

Pertanto

$$
\lim_{x\to x_0}e^x=e^{x_0}.
$$

$e^x$ è continua in $x_0$, per ogni $x_0\in\mathbb R$. $\square$

## Commenti alla dimostrazione

La sequenza della prova è quella del PDF, pp. 9-11. La scelta del minimo garantisce che l'intervallo simmetrico $(-\delta,\delta)$ sia interamente contenuto fra i due logaritmi. Si usa la monotonia dell'esponenziale e del logaritmo già studiata, non la continuità dell'esponenziale ancora da dimostrare.

La restrizione $0<\varepsilon<1$ permette di definire $\log(1-\varepsilon)$. Per ricondurre a questo caso un qualsiasi $\varepsilon>0$, basta usare nella costruzione $\eta=\min\{\varepsilon,1/2\}$: la stima ottenuta è $|e^x-1|<\eta\leq\varepsilon$. Questo esplicita il passaggio sottinteso nel PDF.

Nel secondo caso $t=x-x_0\to0$; il limite in zero è già stato provato. Le regole algebriche dei limiti, qui usate dal docente, sono riepilogate alla fine della lezione in [[137 Algebra dei Limiti di Funzioni]].

## Uso negli esercizi ed errori comuni

Per verificare continuità in un punto, controllare nell'ordine che sia nel dominio, che il limite sia finito e che coincida con il valore assegnato. Una formula diversa nel solo centro può cambiare la continuità senza cambiare il limite.

Un punto di discontinuità può dipendere dal dominio: la [[131 Funzione di Dirichlet e Discontinuità Ovunque|funzione di Dirichlet]] fornisce l'esempio successivo. I punti isolati non sono trattati dalla definizione limitata ai punti di accumulazione adottata qui dal docente.

### Da dire all'orale

> Una funzione è continua in un punto del dominio, di accumulazione per esso, se il limite della funzione nel punto coincide con il valore della funzione. Nella definizione metrica controllo tutti i punti del dominio abbastanza vicini, incluso il centro. Per una funzione continua posso passare al limite dentro la funzione lungo ogni successione del dominio che converge al punto.
