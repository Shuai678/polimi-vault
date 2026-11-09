---
course: Analisi 1
type: concept
status: Da studiare
updated: 2026-11-06
source:
  - Lezione 15, PDF pp. 3-5
---

# Cambio di variabile nei limiti e continuità della composta

## Teorema del docente: cambio di variabile nei limiti

Siano $f,g$ due funzioni per cui sia ben definita la [[64 Composizione di Funzioni|composizione]]

$$
(f\circ g)(x)=f(g(x))
$$

almeno in un intorno di $x_0\in\overline{\mathbb R}$, escluso al più $x_0$. Nei limiti si considerano sempre i punti del dominio pertinente e i punti di accumulazione richiesti.

Se

1. $\displaystyle\lim_{x\to x_0}g(x)=t_0\in\overline{\mathbb R}$;
2. $\displaystyle\lim_{t\to t_0}f(t)=\ell\in\overline{\mathbb R}$;
3. $g(x)\neq t_0$ definitivamente per $x\to x_0$;

allora

$$
\boxed{
\lim_{x\to x_0}f(g(x))
=\lim_{t\to t_0}f(t)=\ell,\qquad t=g(x).
}
$$

Nel PDF il teorema è indicato **«no dim.»**. Qui si conservano enunciato, condizioni e impiego.

## Osservazione del docente sull'ipotesi 3

La condizione $g(x)\neq t_0$ non serve se $t_0=\pm\infty$, perché $g(x)$ assume valori reali, oppure se $f$ è continua in $t_0$: in quest'ultimo caso $\ell=f(t_0)$.

## Corollario del docente: continuità della funzione composta

Sia $g$ definita in un intorno di $x_0$ e continua in $x_0$, con

$$
\lim_{x\to x_0}g(x)=g(x_0).
$$

Sia $f$ definita in un intorno di $t_0=g(x_0)$ e continua in $t_0$, con

$$
\lim_{t\to t_0}f(t)=f(t_0).
$$

Allora $f\circ g$ è definita in un intorno di $x_0$ ed è continua in $x_0$:

$$
\boxed{\lim_{x\to x_0}f(g(x))=f(g(x_0)).}
$$

## Dimostrazione del professore del corollario

Per il teorema di cambio di variabile nei limiti, essendo entrambe le funzioni continue,

$$
\lim_{x\to x_0}f(g(x))
=\lim_{t\to t_0}f(t)
=f(t_0)=f(g(x_0)),\qquad t=g(x).
$$

$\square$

## Osservazione successiva del docente

Se $f$ è continua in $t_0$ e $g(x)\to t_0$, si può scrivere

$$
\lim_{x\to x_0}f(g(x))
=\lim_{t\to t_0}f(t)
=f(t_0)
=f\!\left(\lim_{x\to x_0}g(x)\right).
$$

## Commenti alle condizioni e alla prova

La variabile nuova è **l'intero argomento della funzione esterna**. Il suo limite deve essere ricalcolato: non si mantiene automaticamente il punto di avvicinamento originario. La continuità dell'esterna permette di sostituire il limite del suo argomento anche quando l'interna assume proprio quel valore.

L'ipotesi 3 del teorema generale ha una ragione precisa: il limite di $f$ in $t_0$ esclude il punto $t_0$ e non controlla $f(t_0)$. Se l'interna continua a produrre quel valore, il solo limite esterno non basta.

### Controesempio di supporto se si omette l'ipotesi

Poniamo $f(t)=1$ per $t\neq0$, $f(0)=7$ e $g(x)=0$ per ogni $x$. Si ha $g(x)\to0$ e $\lim_{t\to0}f(t)=1$, ma $f(g(x))=7$ per ogni $x$, quindi il limite della composta è $7$. Qui $g(x)\neq0$ non vale e $f$ non è continua in zero.

## Metodo con esempio svolto

Calcolare

$$
\lim_{x\to0}\frac{\sin(3x)}x.
$$

Poniamo $t=3x$. Allora $t\to0$ e $t\neq0$ per $x\neq0$. Riscriviamo **esattamente**

$$
\frac{\sin(3x)}x
=3\frac{\sin(3x)}{3x}.
$$

Il limite notevole enunciato nella [[95 Equivalenti e Sviluppi Asintotici Notevoli#Lezione 15 - Limiti notevoli di funzioni - Da studiare|Lezione 15]] dà

$$
\lim_{x\to0}\frac{\sin(3x)}x
=3\lim_{t\to0}\frac{\sin t}t=3.
$$

L'esempio è un'applicazione aggiunta dopo gli enunciati, non una prova del limite notevole.

Per una composta continua, per esempio $e^{x^2}$ in zero, la [[130 Continuità di una Funzione|continuità dell'esponenziale]] e quella di $x^2$ danno direttamente $e^{x^2}\to e^0=1$.

### Da dire all'orale

> Per cambiare variabile in una composta verifico che l'argomento interno tenda al nuovo punto, che esista il limite della funzione esterna e che l'argomento eviti il punto escluso dalla definizione di quel limite. Quest'ultima condizione non serve se l'esterna è continua nel punto. In particolare, la composizione di funzioni continue, quando è definita, è continua.
