---
course: Analisi 1
type: concept
status: Da studiare
updated: 2026-11-09
source:
  - Lezione 16, PDF pp. 10-13
  - Libro, §5.8, pp. 154-156, teorema 5.44 e osservazione 5.45
---

# Limiti delle funzioni monotone su un intervallo

## Teorema del docente: limiti in un punto interno

Sia $f:(a,b)\to\mathbb R$ [[62 Funzioni Monotone|monotona crescente]], con $-\infty\leq a<b\leq+\infty$. Per ogni $x_0\in(a,b)$ esistono **finiti** i due limiti laterali

$$
\lim_{x\to x_0^-}f(x)\in\mathbb R,
\qquad\lim_{x\to x_0^+}f(x)\in\mathbb R.
$$

Inoltre

$$
\lim_{x\to x_0^-}f(x)=\sup_{x\in(a,x_0)}f(x),
\qquad
\lim_{x\to x_0^+}f(x)=\inf_{x\in(x_0,b)}f(x),
$$

con

$$
\boxed{\lim_{x\to x_0^-}f(x)\leq f(x_0)\leq\lim_{x\to x_0^+}f(x).}
$$

La monotonia è in senso non stretto; non è richiesta la continuità.

## Limiti agli estremi per la funzione crescente

Il docente precisa che esistono, eventualmente infiniti,

$$
\lim_{x\to a^+}f(x)=\inf_{x\in(a,b)}f(x)\in\mathbb R\cup\{-\infty\},
$$

$$
\lim_{x\to b^-}f(x)=\sup_{x\in(a,b)}f(x)\in\mathbb R\cup\{+\infty\}.
$$

Se un estremo del dominio è infinito, la notazione indica il corrispondente limite a $-\infty$ o $+\infty$. Se l'estremo è reale, il limite è laterale dall'interno del dominio.

## Caso decrescente, nell'ordine del richiamo del docente

Se $f$ è monotona decrescente, per ogni $x_0\in(a,b)$

$$
\lim_{x\to x_0^-}f(x)=\inf_{x\in(a,x_0)}f(x)\in\mathbb R,
$$

$$
\lim_{x\to x_0^+}f(x)=\sup_{x\in(x_0,b)}f(x)\in\mathbb R,
$$

con

$$
\boxed{\lim_{x\to x_0^-}f(x)\geq f(x_0)\geq\lim_{x\to x_0^+}f(x).}
$$

Agli estremi, i limiti eventualmente infiniti sono

$$
\lim_{x\to a^+}f(x)=\sup_{x\in(a,b)}f(x)\in\mathbb R\cup\{+\infty\},
$$

$$
\lim_{x\to b^-}f(x)=\inf_{x\in(a,b)}f(x)\in\mathbb R\cup\{-\infty\}.
$$

## Indicazione del docente sulla dimostrazione

Il PDF, p. 12, indica **«no dim., simile alla dimostrazione del teorema di regolarità per le successioni monotone»**. Si richiamano quindi [[75 Successioni Monotone]] e [[76 Teorema del Limite delle Successioni Monotone]], senza attribuire al professore una nuova prova non sviluppata nel PDF.

## Corollario del docente: discontinuità e comportamento agli estremi

Se $f:(a,b)\to\mathbb R$ è monotona, gli eventuali punti di discontinuità **interni a $(a,b)$ sono soltanto di tipo salto**.

Agli estremi del dominio la funzione ammette un limite, finito oppure infinito. Se un estremo è reale e il limite dall'interno è finito, si può prolungare la funzione per continuità assegnandole quel valore. Se il limite è infinito, la retta verticale nell'estremo reale è un asintoto verticale.

## Commenti: perché distinguere interno ed estremi

In un punto interno i due limiti sono finiti: scegliendo $u<x_0<v$ nel dominio, per una funzione crescente $f(u)\leq f(x)\leq f(v)$ quando $u<x<v$. I valori reali $f(u),f(v)$ forniscono barriere locali da entrambi i lati. Agli estremi una delle due barriere può mancare, perciò un limite infinito è possibile. Questo commento chiarisce le ipotesi, non sostituisce il rinvio del docente.

Se i limiti laterali coincidono, la disuguaglianza che racchiude $f(x_0)$ impone che coincidano anche con $f(x_0)$: il punto è continuo. Se sono diversi, essendo entrambi finiti, la discontinuità è [[133 Discontinuità a Salto|a salto]]. In un punto interno non può quindi comparire né una discontinuità eliminabile né una di seconda specie, mantenendo la monotonia su tutto l'intervallo.

Per gli estremi infiniti non si aggiunge un valore reale alla funzione nel punto infinito: la [[132 Discontinuità Eliminabili ed Estensione per Continuità|possibilità di estendere il dominio]] descritta dal corollario riguarda estremi reali.

![[144 Limiti Laterali di una Funzione Monotona.svg|1100]]

## Esempio svolto: monotonia con salto

Consideriamo su $(-2,2)$

$$
f(x)=\begin{cases}
x,&x<0,\\
1,&x=0,\\
x+2,&x>0.
\end{cases}
$$

Su ciascun lato è strettamente crescente. Se $x<0<y$, si ha $f(x)=x<0<1<2<y+2=f(y)$; anche il valore in zero mantiene l'ordine. La funzione è quindi strettamente crescente sull'intero intervallo, pur avendo un salto:

$$
\lim_{x\to0^-}f(x)=0<1=f(0)<2=\lim_{x\to0^+}f(x).
$$

Il salto è $2-0=2$. La monotonia non impone continuità; impone che i limiti laterali esistano e che il valore assegnato stia fra essi.

## Esempio agli estremi

$f(x)=\log x$ è crescente su $(0,+\infty)$. Si ha

$$
\lim_{x\to0^+}\log x=-\infty=\inf_{(0,+\infty)}\log x,
\qquad
\lim_{x\to+\infty}\log x=+\infty=\sup_{(0,+\infty)}\log x.
$$

In zero c'è un asintoto verticale, mentre nessun punto interno positivo presenta un limite laterale infinito. La continuità del logaritmo, richiamata nella parte successiva della lezione, non è necessaria per enunciare il teorema sulle funzioni monotone.

## Uso negli esercizi ed errori comuni

Usare il teorema per stabilire l'esistenza dei laterali prima di calcolarli, per classificare discontinuità compatibili con la monotonia e per controllare i limiti agli estremi. Specificare sempre l'intervallo: la monotonia su due parti separate del dominio non implica quella sull'intero dominio.

Non invertire superiore e inferiore: per una funzione crescente, arrivando da sinistra si raggiunge il superiore dei valori a sinistra; da destra l'inferiore dei valori a destra. Non concludere che tutti i limiti della funzione siano finiti: la finitezza del teorema riguarda i punti interni.

### Da dire all'orale

> Una funzione monotona su un intervallo ammette limiti laterali finiti in ogni punto interno. Nel caso crescente, il sinistro è il superiore dei valori a sinistra e il destro è l'inferiore dei valori a destra; il valore nel punto sta fra i due. Nel caso decrescente i versi si invertono. Le discontinuità interne possono essere soltanto a salto, mentre agli estremi i limiti possono essere infiniti.
