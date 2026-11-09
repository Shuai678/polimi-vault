---
course: Analisi 1
type: concept
status: Da studiare
updated: 2026-11-06
source:
  - Lezione 15, PDF pp. 18-20
---

# Grafici locali e grafici probabili

## Osservazioni iniziali del docente

Le stime tramite sviluppi asintotici servono per il calcolo dei limiti e anche per tracciare **grafici qualitativi, soltanto probabili**, in un intorno di $x_0\in\overline{\mathbb R}$. Per uno studio completo del grafico servono ulteriori strumenti, comprese le derivate, che qui non vengono introdotte.

Il docente avverte che da $f\sim g$ per $x\to x_0$ **non segue in generale che i grafici di $f$ e $g$ si assomiglino**. L'equivalenza controlla un rapporto, non tutta la forma del grafico.

## Primo esempio del docente: equivalenza con oscillazioni

Il professore introduce, nell'ordine,

$$
g(x)=x^2+x^4,\qquad h(x)=x^2-x^4,\qquad u(x)=x^2,
$$

$$
f(x)=x^2+x^4\sin\frac1{x^3},\qquad x\neq0.
$$

Poiché $\sin(1/x^3)\in[-1,1]$,

$$
h(x)\leq f(x)\leq g(x)\qquad\text{per ogni }x\neq0.
$$

Per $x\to0$,

$$
g(x)\sim h(x)\sim f(x)\sim x^2.
$$

Il grafico di $f$ è racchiuso fra i due grafici di controllo ma oscilla all'interno della fascia. L'equivalenza con la parabola descrive il termine principale, non elimina queste oscillazioni.

![[140 Equivalenza e Oscillazioni.svg|1000]]

## Secondo esempio del docente: radice cubica più quadrato

Sia

$$
f(x)=\sqrt[3]{x}+x^2.
$$

Il dominio è $\mathbb R$ e la funzione è continua. Il professore raccoglie i seguenti dati:

1. $\lim_{x\to+\infty}f(x)=+\infty$ e $f(x)\sim x^2$ per $x\to+\infty$;
2. $\lim_{x\to-\infty}f(x)=+\infty$ e $f(x)\sim x^2$ per $x\to-\infty$;
3. $f(0)=0$;
4. $f(x)\sim\sqrt[3]{x}$ per $x\to0$.

Il comportamento dominante cambia con il punto considerato: il quadrato prevale lontano dall'origine; la radice cubica prevale vicino a zero. Queste informazioni guidano lo schizzo del grafico probabile.

![[140 Radice Cubica e Termine Quadratico.svg|1000]]

## Terzo esempio del docente: seno di una radice

Per

$$
f(x)=\sin\sqrt{|x|},
$$

in un intorno di zero si ha

$$
f(x)\sim\sqrt{|x|}\qquad(x\to0).
$$

Fra i quattro schizzi presentati dal docente è compatibile soltanto il **primo**: i due rami sono positivi e si incontrano nell'origine, con il comportamento locale di $\sqrt{|x|}$. Gli altri schizzi mostrano attraversamenti con cambio di segno oppure un comportamento parabolico che non ha il rapporto richiesto con $\sqrt{|x|}$.

![[140 Seno di Radice e Grafici Compatibili.svg|1100]]

## Commenti e verifiche dei calcoli

### Perché il primo esempio è equivalente a $x^2$

Per $x\neq0$,

$$
\frac{g(x)}{x^2}=1+x^2\to1,\qquad
\frac{h(x)}{x^2}=1-x^2\to1,
$$

$$
\frac{f(x)}{x^2}=1+x^2\sin\frac1{x^3}.
$$

Poiché $|x^2\sin(1/x^3)|\leq x^2\to0$, l'ultimo rapporto tende a $1$. Il fattore $\sin(1/x^3)$ oscilla sempre più rapidamente, mentre l'ampiezza dello scarto verticale è al più $x^4$. La formula di $f$ esclude zero; assegnare $f(0)=0$ produrrebbe un'estensione continua, senza cambiare le equivalenze.

### Le due scale del secondo esempio

A $\pm\infty$,

$$
\frac{f(x)}{x^2}=1+\frac{\sqrt[3]{x}}{x^2}\to1,
$$

perché $|\sqrt[3]{x}/x^2|=1/|x|^{5/3}\to0$. In zero, usando $x=(\sqrt[3]{x})^3$,

$$
\frac{f(x)}{\sqrt[3]{x}}
=1+\frac{x^2}{\sqrt[3]{x}}
=1+(\sqrt[3]{x})^5\to1.
$$

Un'ulteriore verifica algebrica individua le intersezioni con l'asse: posto $t=\sqrt[3]{x}$,

$$
f(x)=0\iff t+t^6=0\iff t(1+t^5)=0.
$$

Le soluzioni sono $t=0$ e $t=-1$, cioè $x=0$ e $x=-1$. Questo completa lo schizzo senza usare derivate, ma non costituisce uno studio di monotonia.

### Il rapporto decisivo del terzo esempio

Ponendo $t=\sqrt{|x|}$, per $x\to0$ e $x\neq0$ si ha $t\to0^+$ e $t\neq0$. Pertanto

$$
\frac{\sin\sqrt{|x|}}{\sqrt{|x|}}
=\frac{\sin t}t\longrightarrow1
$$

per [[95 Equivalenti e Sviluppi Asintotici Notevoli#Lezione 15 - Limiti notevoli di funzioni - Da studiare|il limite notevole del seno]]. Il rapporto è definitivamente positivo e $\sqrt{|x|}>0$, quindi $f(x)>0$ vicino a zero sui due lati. Inoltre $f(0)=0$ e la funzione è pari. Una parabola $x^2$ non è una buona sostituzione: $x^2/\sqrt{|x|}=|x|^{3/2}\to0$, invece di $1$.

## Metodo operativo e limiti dello schizzo

Determinare prima il dominio. Studiare separatamente i diversi punti e le due direzioni infinite. Trovare una scala dominante in ciascuna zona, conservando coefficienti e segni; aggiungere valori effettivi, simmetrie e intersezioni che si possono ricavare con gli strumenti già disponibili.

La [[94 Equivalenza Asintotica#Lezione 15 - Equivalenza asintotica per funzioni - Da studiare|equivalenza]] suggerisce il comportamento relativo, mentre gli [[124 Limiti Finiti all'Infinito e Asintoti Orizzontali|asintoti]] richiedono le loro condizioni specifiche. Per esempio $\sqrt[3]{x}+x^2\sim x^2$ all'infinito non significa che la differenza da $x^2$ tenda a zero: la differenza è $\sqrt[3]{x}$ e diverge.

Non dedurre dall'equivalenza monotonia, convessità o assenza di oscillazioni. I grafici di supporto visualizzano le formule degli esempi; le proprietà dimostrate restano quelle ottenute dai calcoli espliciti.

### Da dire all'orale

> Gli equivalenti consentono di riconoscere una scala dominante e orientare un grafico locale o probabile. Il confronto cambia con il punto di avvicinamento e non determina tutte le proprietà del grafico. Due funzioni equivalenti possono differire per oscillazioni; per affermare proprietà come monotonia occorrono giustificazioni ulteriori.
