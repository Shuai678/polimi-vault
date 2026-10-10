---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 09, PDF pp. 11-16
  - Libro, §3.5.2, pp. 94-96; §3.8, pp. 104-105
---

# Cancellazioni e precisione del resto asintotico

## Intuizione: la precisione serve dopo la cancellazione

Un equivalente descrive il termine principale di una successione. Quando questo termine viene sottratto, il risultato dipende dall'errore che prima era trascurabile. Occorre quindi confrontare il **resto con la scala del denominatore finale**, non soltanto con la scala del termine originario.

Nel terzo e nel quarto esercizio di [[96 Calcolo dei Limiti con Equivalenti Asintotici]], lo sviluppo della potenza con incremento infinitesimo fornisce già un resto abbastanza piccolo. L'ultimo esercizio del PDF mostra un caso in cui la prima formula disponibile non basta.

## Esercizio conclusivo della lezione

### Testo — PDF pp. 15-16

Calcolare, per $n\geq1$,

$$
a_n=\frac{\sin(1/n)-1/n}{1/n^3}=n^3\left(\sin\frac1n-\frac1n\right).
$$

### Il punto raggiunto nel PDF

Dal [[95 Equivalenti e Sviluppi Asintotici Notevoli|limite notevole del seno]] segue

$$
\sin\frac1n=\frac1n+o(1/n).
$$

Sottraendo $1/n$ e moltiplicando per $n^3$ otteniamo

$$
a_n=n^3o(1/n)=o(n^2).
$$

Questo passaggio è corretto, ma significa soltanto $a_n/n^2\to0$. **Non determina il limite di $a_n$.** Il PDF termina chiedendo quale sia tale limite, senza completare il calcolo.

### Perché la sola informazione di primo ordine non basta

Poniamo $x_n=1/n$. Le tre successioni seguenti sono tutte equivalenti a $x_n$:

$$
u_n=x_n+x_n^2,\qquad
v_n=x_n-\frac{x_n^3}{6},\qquad
w_n=x_n+x_n^4.
$$

Infatti i loro rapporti con $x_n$ sono rispettivamente $1+x_n$, $1-x_n^2/6$ e $1+x_n^3$, tutti tendenti a $1$. Eppure

$$
\frac{u_n-x_n}{x_n^3}=n\to+\infty,\qquad
\frac{v_n-x_n}{x_n^3}=-\frac16,\qquad
\frac{w_n-x_n}{x_n^3}=\frac1n\to0.
$$

In tutti e tre i casi il risultato è $o(n^2)$. La stessa stima è compatibile con limiti diversi e perfino con una divergenza.

![[97 Precisione del Resto Asintotico.svg|900]]

## Completamento dell'esercizio con strumenti già introdotti

La soluzione seguente è un'integrazione didattica: usa il confronto geometrico del seno, l'identità di duplicazione e una somma **finita** di potenze geometriche. Non è una dimostrazione riportata nel PDF.

### Idea

Per $0<t<\pi/2$ studiamo l'espressione ausiliaria

$$
F(t)=\frac{\sin t-t}{t^3}.
$$

Dall'identità $\sin t=2\sin(t/2)\cos(t/2)$ ricaveremo una relazione fra $F(t)$ e $F(t/2)$. Il fattore davanti a $F(t/2)$ è al più $1/4$: ripetendo il passaggio, l'errore si riduce geometricamente. Le stime valgono per ogni argomento positivo sufficientemente piccolo; alla fine le applichiamo a $t=1/n$.

### 1. Una stima che rende $F$ limitata vicino a zero

Il confronto geometrico in [[95 Equivalenti e Sviluppi Asintotici Notevoli]] dà

$$
t\cos t\leq\sin t\leq t.
$$

Sottraendo $t$ e dividendo per $t^3>0$,

$$
-\frac{1-\cos t}{t^2}\leq F(t)\leq0.
$$

Dalle stime già provate, $(1-\cos t)/t^2\to1/2$ quando l'argomento positivo tende a zero. In particolare, per $t$ sufficientemente piccolo, $-1\leq F(t)\leq0$. Perciò anche $R(t)=F(t)+1/6$ è limitata; possiamo usare, per esempio, $|R(t)|\leq M$ con $M=2$.

### 2. La relazione esatta tra due scale

Scriviamo

$$
\begin{aligned}
\sin t-t
&=2\cos(t/2)\left(\sin(t/2)-\frac t2\right)
+t\bigl(\cos(t/2)-1\bigr).
\end{aligned}
$$

Poiché $\sin(t/2)-t/2=(t/2)^3F(t/2)$, dividendo per $t^3$ otteniamo

$$
F(t)=\frac{\cos(t/2)}4F(t/2)
+\frac{\cos(t/2)-1}{t^2}.
$$

Il secondo termine tende a $-1/8$:

$$
\frac{\cos(t/2)-1}{t^2}
=-\frac14\frac{1-\cos(t/2)}{(t/2)^2}\to-\frac18.
$$

Se $F$ avesse limite $L$, questa relazione imporrebbe $L=L/4-1/8$, cioè $L=-1/6$. Ma tale osservazione **non prova ancora l'esistenza del limite**: la dimostriamo nel passaggio successivo.

### 3. Dimostrare che l'errore tende a zero

Poniamo $R(t)=F(t)+1/6$. Dalla relazione esatta segue

$$
R(t)=\frac{\cos(t/2)}4R(t/2)+h(t),
$$

con

$$
h(t)=\frac{\cos(t/2)-1}{t^2}
+\frac{1-\cos(t/2)/4}{6}.
$$

Quando $t$ tende a zero, i due addendi tendono a $-1/8$ e $1/8$, quindi $h(t)\to0$. Le stime geometriche valgono per tutti gli argomenti piccoli; questa affermazione significa che, per ogni $\delta>0$, esiste $t_0>0$ tale che $|h(t)|<\delta$ per $0<t<t_0$.

Poiché $0<\cos(t/2)\leq1$, per questi argomenti

$$
|R(t)|\leq\frac14|R(t/2)|+|h(t)|.
$$

Applicando la stessa disuguaglianza a $t/2$ e sostituendo,

$$
|R(t)|\leq\frac1{4^2}|R(t/4)|
+|h(t)|+\frac14|h(t/2)|.
$$

Dopo $k$ passaggi, per [[21 Dimostrazione per Induzione|induzione]],

$$
|R(t)|\leq\frac{M}{4^k}
+\sum_{j=0}^{k-1}\frac1{4^j}|h(t/2^j)|.
$$

Tutti gli argomenti $t/2^j$ restano nell'intervallo piccolo scelto. Inoltre, dalla formula algebrica della somma geometrica finita,

$$
\sum_{j=0}^{k-1}\frac1{4^j}
=\frac{1-4^{-k}}{1-1/4}\leq\frac43.
$$

Dato $\eta>0$, scegliamo $\delta=3\eta/8$ e poi $k$ tale che $M/4^k<\eta/2$: quest'ultima scelta è possibile per [[78 Limiti di Potenze e Progressioni Geometriche]]. Restringiamo $t_0$ anche per garantire la precedente limitatezza di $R$. Per ogni $0<t<t_0$,

$$
|R(t)|\leq\frac{M}{4^k}+\frac43\delta
<\frac\eta2+\frac\eta2=\eta.
$$

Questa è una prova del limite: $R(t)\to0$ e quindi $F(t)\to-1/6$. In particolare $t=1/n$ cade definitivamente in tale intervallo e

$$
\boxed{\lim_{n\to+\infty}
\frac{\sin(1/n)-1/n}{1/n^3}=-\frac16.}
$$

### Risultato anche in forma di resto

Il limite appena dimostrato equivale a

$$
\boxed{\sin\frac1n=\frac1n-\frac1{6n^3}+o(1/n^3).}
$$

Questa formula è stata ottenuta per risolvere l'esercizio conclusivo; non deriva dalla sola equivalenza $\sin(1/n)\sim1/n$.

## Regola pratica sulla precisione

Se dopo aver sottratto i termini principali si deve dividere per $b_n$, un resto $r_n$ è trascurabile soltanto se $r_n=o(b_n)$. Sapere $r_n=o(c_n)$ con $b_n=o(c_n)$ è in generale insufficiente: il denominatore finale è una scala più piccola.

Nell'esercizio $b_n=1/n^3$ e la prima stima aveva solo scala $c_n=1/n$. Il completamento trova il coefficiente del termine cubico e un resto $o(1/n^3)$: dopo la divisione quest'ultimo tende a zero.

## Errori comuni e prospettiva d'esame

- Dedurre $a_n\to0$ da $a_n=o(n^2)$: la scala $n^2$ diverge.
- Cancellare gli equivalenti dentro una differenza, perdendo il primo termine non nullo.
- Scrivere un resto senza confrontarlo con il denominatore finale.
- Ricavare un candidato al limite da un'identità e assumere già l'esistenza del limite.
- Considerare due occorrenze di $o(b_n)$ come lo stesso resto.

Potenziale rilevanza d'esame: riconoscere quando un equivalente non basta, giustificare la precisione dei resti e spiegare perché una stima corretta può non essere conclusiva.

### Da dire all'orale

> Quando i termini principali si cancellano, il limite dipende dai termini successivi. Devo conservare un resto trascurabile rispetto alla scala con cui dividerò. Nell'esempio del seno, il resto di primo ordine dà soltanto un o-piccolo di n quadrato; il limite richiede invece conoscere la differenza alla scala di uno su n cubo.
