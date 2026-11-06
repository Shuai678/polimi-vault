---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 2-3
  - Libro, §5.1, pp. 134-136, esempio 5.5
---

# Limiti infiniti al finito

## Definizioni metriche del docente

Siano $f:I\subseteq\mathbb R\to\mathbb R$ e $x_0\in\mathbb R$ punto di accumulazione per $I$. Il caso ora considerato ha **punto di avvicinamento finito e valore limite infinito**.

Si ha

$$
\lim_{x\to x_0}f(x)=+\infty
$$

se e solo se

$$
\forall M>0\ \exists\delta>0\ \forall x\in I:
\quad0<|x-x_0|<\delta\Longrightarrow f(x)>M.
$$

La condizione sull'ascissa significa $x\in(x_0-\delta,x_0+\delta)$ e $x\neq x_0$; la condizione sul valore significa $f(x)\in(M,+\infty)$.

Analogamente,

$$
\lim_{x\to x_0}f(x)=-\infty
\iff
\forall M>0\ \exists\delta>0\ \forall x\in I:
\quad0<|x-x_0|<\delta\Longrightarrow f(x)<-M.
$$

Queste definizioni seguono dalla [[123 Definizione Topologica di Limite e Teorema Ponte|formulazione tramite intorni]]. Il valore della funzione nel centro è escluso dal controllo.

## Esempio del docente

$$
\boxed{\lim_{x\to0}\frac1{x^2}=+\infty.}
$$

I valori crescono senza limite avvicinandosi a zero da entrambi i lati.

![[127 Limite Infinito al Finito.svg|900]]

## Commento con verifica della definizione

> [!info] Approfondimento dal libro
> L'esempio 5.5, §5.1, p. 135, sviluppa la scelta di $\delta$ per l'esempio enunciato dal professore. Questa verifica è aggiunta dopo la sua presentazione.

Fissato $M>0$, per $x\neq0$,

$$
\frac1{x^2}>M
\iff x^2<\frac1M
\iff0<|x|<\frac1{\sqrt M}.
$$

È quindi sufficiente scegliere $\delta=1/\sqrt M>0$. Ogni punto del dominio con $0<|x|<\delta$ soddisfa la richiesta, non soltanto alcuni punti di una successione.

Per $-1/x^2$ lo stesso calcolo dà il limite $-\infty$: moltiplicando la disuguaglianza precedente per $-1$ si ottiene $-1/x^2<-M$.

## Uso negli esercizi ed errori comuni

$M$ è una soglia sui valori e viene scelta arbitrariamente; $\delta$ è una distanza sul dominio e può dipendere da $M$. Per dimostrare il limite bisogna produrre una scelta valida di $\delta$, eventualmente più piccola del necessario.

Un denominatore che tende a zero non determina da solo il segno del limite. Per $1/x^2$ il denominatore è positivo sui due lati; per $1/x$ cambia segno, e serviranno i [[128 Limiti Laterali e Asintoti Verticali|limiti laterali]]. Non scrivere $1/0=+\infty$: il valore in zero non è definito e il limite riguarda i punti vicini.

### Da dire all'orale

> Una funzione tende a più infinito in un punto finito di accumulazione se, per ogni soglia positiva, esiste una distanza positiva dal punto tale che tutti i punti del dominio a distanza non nulla minore di quella distanza hanno valore maggiore della soglia. Per meno infinito il valore deve essere minore dell'opposto della soglia.
