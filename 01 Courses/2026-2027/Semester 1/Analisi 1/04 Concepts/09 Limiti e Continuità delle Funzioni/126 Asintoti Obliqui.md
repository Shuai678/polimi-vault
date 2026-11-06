---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 13, PDF pp. 14-16
  - Libro, §5.12, pp. 172-174
---

# Asintoti obliqui

## Definizione del docente

La funzione $f$ ha **asintoto obliquo** $y=mx+q$, con $m\in\mathbb R\setminus\{0\}$ e $q\in\mathbb R$, per $x\to+\infty$ se

$$
\boxed{\lim_{x\to+\infty}\bigl[f(x)-(mx+q)\bigr]=0.}
$$

Per $x\to-\infty$ si usa la stessa condizione in quella direzione. Le due direzioni vanno studiate separatamente.

## Interpretazione e osservazione del docente

La quantità $|f(x)-(mx+q)|$ è la lunghezza del segmento **verticale** che unisce $(x,f(x))$ al punto $(x,mx+q)$ sulla retta. Questa distanza deve tendere a zero.

Equivalentemente, nella direzione considerata,

$$
f(x)-(mx+q)=o(1),\qquad
f(x)=mx+q+o(1).
$$

È l'uso della [[93 Notazione o-Piccolo|notazione di resto infinitesimo]] applicato alle funzioni.

## Proposizione: come determinare $m$ e $q$

Il docente enuncia che esiste un asintoto obliquo nella direzione considerata se e solo se valgono **entrambe** le condizioni:

$$
1)\quad\lim_{x\to\pm\infty}\frac{f(x)}x=m\in\mathbb R\setminus\{0\},
$$

$$
2)\quad\lim_{x\to\pm\infty}\bigl[f(x)-mx\bigr]=q\in\mathbb R.
$$

In tal caso l'asintoto è $y=mx+q$. Il simbolo $\pm\infty$ indica di fissare una direzione per tutto il calcolo.

## Esempi del docente

### $f(x)=2x+3+e^{-x}$

A $+\infty$, $e^{-x}\to0$, quindi

$$
f(x)=2x+3+o(1).
$$

L'asintoto è $y=2x+3$. Infatti $f(x)-(2x+3)=e^{-x}\to0$.

A $-\infty$, invece,

$$
\frac{f(x)}x=2+\frac3x+\frac{e^{-x}}x\longrightarrow-\infty,
$$

per la prevalenza dell'esponenziale sulla potenza. La prima condizione fallisce: non esiste asintoto obliquo in quella direzione.

### $f(x)=2x+3+\log x$, definita per $x>0$

A $+\infty$,

$$
\frac{f(x)}x=2+\frac3x+\frac{\log x}{x}\longrightarrow2.
$$

Il candidato coefficiente angolare è $m=2$. Ma

$$
f(x)-2x=3+\log x\longrightarrow+\infty,
$$

quindi non esiste $q\in\mathbb R$. **Non c'è asintoto obliquo**, pur avendo ottenuto un coefficiente angolare finito non nullo.

![[126 Asintoto Obliquo e Scarto Verticale.svg|900]]

## Commenti e dimostrazione di supporto del criterio

> [!info] Approfondimento dal libro
> Il PDF enuncia il criterio senza svilupparne la prova. Il libro, §5.12, p. 173, esplicita come ricavare i due coefficienti. Il passaggio seguente è tenuto separato dagli esempi del docente.

Se $f(x)=mx+q+r(x)$ con $r(x)\to0$, allora

$$
\frac{f(x)}x=m+\frac qx+\frac{r(x)}x\to m,
\qquad f(x)-mx=q+r(x)\to q.
$$

Viceversa, una volta trovato $m\neq0$ e verificato $f(x)-mx\to q\in\mathbb R$, sottrarre $q$ dà $f(x)-(mx+q)\to0$, cioè la definizione.

### Metodo ed errori comuni

Calcolare prima $m$; soltanto se è reale e non nullo calcolare $q$ con quel valore preciso. Un rapporto $f(x)/(mx+q)\to1$ non sostituisce la differenza che tende a zero. Nell'ultimo esempio $f(x)/(2x)\to1$, ma lo scarto verticale cresce senza limite. Per $m=0$ si ricade negli [[124 Limiti Finiti all'Infinito e Asintoti Orizzontali|asintoti orizzontali]], non in quelli obliqui.

### Da dire all'orale

> Una retta con coefficiente angolare non nullo è asintoto obliquo se la differenza tra la funzione e la retta tende a zero nella direzione considerata. Determino prima il limite di f di x su x; se è reale e non nullo, calcolo il limite di f di x meno emme x. Anche questo secondo limite deve essere finito.
