---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 22-23
---

# Permanenza del segno per funzioni

## Teorema del docente: dal limite al segno

Sia $f:I\subseteq\mathbb R\to\mathbb R$, con $x_0\in\overline{\mathbb R}$ punto di accumulazione per $I$, e supponiamo che esista

$$
\lim_{x\to x_0}f(x)=\ell\in\overline{\mathbb R}.
$$

1. Se $\ell>0$, allora $f(x)>0$ definitivamente per $x\to x_0$.
2. Se $\ell<0$, allora $f(x)<0$ definitivamente per $x\to x_0$.

Il primo caso comprende $\ell=+\infty$; il secondo $\ell=-\infty$.

## Seconda parte del teorema: dal segno al vincolo sul limite

Se $f(x)\geq0$ definitivamente e il limite $\ell$ esiste nella retta estesa, allora $\ell\geq0$. Se $f(x)\leq0$ definitivamente e il limite esiste, allora $\ell\leq0$.

È una conclusione **non stretta** sul limite. In particolare, anche se $f(x)>0$ definitivamente, il limite può essere zero.

## Esempio del docente

Per $f(x)=x^2$ si ha $f(x)>0$ per ogni $x\neq0$, ma

$$
\lim_{x\to0}f(x)=\lim_{x\to0}x^2=0.
$$

Quindi dal segno positivo dei valori non si può dedurre un limite strettamente positivo.

## Dimostrazioni nel PDF

Il docente scrive **«no dim.»** e osserva che si possono usare le definizioni metriche, come per le successioni. La prova precedente da richiamare è in [[79 Teorema di Permanenza del Segno]]. Non si sostituisce questa indicazione con una dimostrazione diversa attribuita alla lezione.

## Commenti e uso negli esercizi

Il risultato giustifica, dopo aver calcolato un limite positivo, la positività del termine nella zona in cui serve per logaritmi, potenze reali o confronti. Se il limite vale zero, la prima parte non decide il segno: $x$, $x^2$ e $-x^2$ tendono tutti a zero ma hanno comportamenti di segno diversi vicino a zero.

La seconda parte richiede l'esistenza del limite. Una funzione non negativa può non avere limite, per esempio $1+\sin x$ a $+\infty$. “Definitivamente” ha il significato locale precisato in [[135 Proprietà Definitive e Teoremi di Confronto per Funzioni]], non significa necessariamente su tutto il dominio.

### Da dire all'orale

> Se il limite è strettamente positivo, la funzione è definitivamente positiva; se è strettamente negativo, è definitivamente negativa. Viceversa, un segno non negativo o non positivo nella zona del limite impone lo stesso vincolo non stretto al limite, purché questo esista. La positività dei valori non esclude un limite uguale a zero.
