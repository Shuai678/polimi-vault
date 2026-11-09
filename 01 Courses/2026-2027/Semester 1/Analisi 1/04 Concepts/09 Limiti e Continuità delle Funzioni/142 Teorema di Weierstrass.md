---
course: Analisi 1
type: concept
status: Da studiare
updated: 2026-11-09
source:
  - Lezione 16, PDF pp. 2-6
  - Lezione 15, PDF pp. 26-28
  - Libro, §6.3, pp. 197-199, teorema 6.24 e osservazioni 6.25-6.26
---

# Teorema di Weierstrass

## Teorema del docente

Sia $f:[a,b]\to\mathbb R$ continua in $[a,b]$, con $a,b\in\mathbb R$ e $a<b$. Allora $f$ assume **massimo e minimo assoluti** in $[a,b]$. Esistono cioè $x_m,x_M\in[a,b]$ tali che

$$
\boxed{f(x_m)\leq f(x)\leq f(x_M)\qquad\forall x\in[a,b].}
$$

In particolare,

$$
f(x_m)=\min_{x\in[a,b]}f(x)\in\mathbb R,
\qquad
f(x_M)=\max_{x\in[a,b]}f(x)\in\mathbb R.
$$

## Osservazione del docente: punti e valori di estremo

$x_m$ si dice **punto di minimo assoluto** per $f$, mentre $f(x_m)$ è il **minimo assoluto** di $f$. Analogamente $x_M$ è un **punto di massimo assoluto**, mentre $f(x_M)$ è il **massimo assoluto**.

I punti appartengono al dominio $[a,b]$; i valori appartengono all'immagine della funzione. Si riprende così la distinzione già introdotta in [[59 Funzioni Limitate ed Estremi di Funzione]], senza creare una nuova definizione di estremo.

## Conseguenza del docente: limitatezza

Se $f:[a,b]\to\mathbb R$ è continua, per Weierstrass è limitata in $[a,b]$, perché

$$
\sup_{[a,b]}f=f(x_M)=\max_{[a,b]}f\in\mathbb R,
$$

$$
\inf_{[a,b]}f=f(x_m)=\min_{[a,b]}f\in\mathbb R.
$$

Il teorema garantisce sia barriere finite sia che le migliori barriere siano effettivamente raggiunte.

## Osservazione successiva del docente: ipotesi che possono mancare

Se $f:I\subseteq\mathbb R\to\mathbb R$, con $I$ intervallo, non è continua, oppure $I$ non è limitato, oppure $I$ non è chiuso, la tesi **può non valere**.

“Può” è essenziale: il fallimento di un'ipotesi non prova che massimo o minimo siano assenti. Significa che non si può più garantirne l'esistenza con questo teorema.

## Dimostrazione del professore

### Osservazione iniziale e prima bisezione

Cominciamo osservando che, se $f:I\to\mathbb R$ con $I=I_1\cup I_2$, allora

$$
\sup_I f=\max\left\{\sup_{I_1}f,\sup_{I_2}f\right\}.
$$

Procediamo col metodo di bisezione. Siano

$$
a_0=a,\qquad b_0=b,\qquad c_0=\frac{b_0+a_0}{2}.
$$

Se $\Lambda=\sup_{[a,b]}f\in\overline{\mathbb R}$, per quanto visto sopra

$$
\Lambda=\sup_{[a,b]}f
=\max\left\{\sup_{[a_0,c_0]}f,\sup_{[c_0,b_0]}f\right\}.
$$

Quindi $\sup_{[a_0,c_0]}f=\Lambda$ oppure $\sup_{[c_0,b_0]}f=\Lambda$.

Se $\sup_{[a_0,c_0]}f=\Lambda$, definiamo

$$
a_1=a_0,\qquad b_1=c_0,\qquad c_1=\frac{a_1+b_1}{2}.
$$

Altrimenti deve essere $\sup_{[c_0,b_0]}f=\Lambda$ e definiamo

$$
a_1=c_0,\qquad b_1=b_0,\qquad c_1=\frac{a_1+b_1}{2}.
$$

### Iterazione e punto limite

Ripetiamo per ogni $n\in\mathbb N$ questa costruzione iterativamente. Otteniamo due successioni $a_n,b_n$ tali che

1. $a_n$ cresce, $b_n$ decresce;
2. $a\leq a_n\leq b_n\leq b$ per ogni $n\in\mathbb N$;
3. $\displaystyle0\leq b_n-a_n=\frac{b-a}{2^n}$ per ogni $n\in\mathbb N$;
4. $\displaystyle\sup_{[a_n,b_n]}f=\Lambda=\sup_{[a,b]}f$.

Poiché $a_n$ cresce e $b_n$ decresce ed entrambe sono limitate per 1 e 2, per il teorema di regolarità delle successioni monotone esistono

$$
\bar a=\lim_{n\to+\infty}a_n,\qquad
\bar b=\lim_{n\to+\infty}b_n,\qquad\bar a,\bar b\in\mathbb R.
$$

Per permanenza del segno, da 2 segue

$$
a\leq\bar a\leq\bar b\leq b,
\qquad\bar a,\bar b\in[a,b].
$$

Inoltre da 3, per algebra dei limiti,

$$
\bar b-\bar a
=\lim_{n\to+\infty}(b_n-a_n)
=\lim_{n\to+\infty}\frac{b-a}{2^n}=0.
$$

Quindi $\bar b=\bar a\in[a,b]$. Indichiamo con

$$
x_M=\bar b=\bar a\in[a,b].
$$

Ci sono due possibilità: $\Lambda=+\infty$ oppure $\Lambda\in\mathbb R$. Verifichiamo che $\Lambda=+\infty$ non può essere.

### Esclusione del superiore infinito

Per assurdo, se $\Lambda=+\infty$, allora

$$
\sup_{[a_n,b_n]}f=\Lambda=+\infty\qquad\forall n\in\mathbb N.
$$

Quindi per ogni $n\in\mathbb N$ esiste $x_n\in[a_n,b_n]$ tale che $f(x_n)>n$. Per confronto

$$
\lim_{n\to+\infty}f(x_n)=+\infty.\tag{*}
$$

Per il teorema dei due carabinieri, essendo $a_n\leq x_n\leq b_n$,

$$
\lim_{n\to+\infty}x_n=x_M=\bar a=\bar b.
$$

Per continuità,

$$
\lim_{n\to+\infty}f(x_n)
=f\!\left(\lim_{n\to+\infty}x_n\right)
=f(x_M)\in\mathbb R.
$$

Assurdo, perché contraddice $(*)$. Pertanto

$$
\sup_{[a,b]}f=\Lambda\in\mathbb R.
$$

### Il superiore finito è assunto

Poiché per ogni $n\in\mathbb N$ si ha $\Lambda=\sup_{[a_n,b_n]}f$, per ogni $\varepsilon>0$ esiste $x\in[a_n,b_n]$, dipendente da $n$ e da $\varepsilon$, tale che

$$
\Lambda-\varepsilon<f(x)\leq\Lambda.
$$

Scegliamo $\varepsilon=1/n$. Per ogni $n\geq1$ esiste $x_n\in[a_n,b_n]$ tale che

$$
\Lambda-\frac1n<f(x_n)\leq\Lambda.
$$

Segue che $\lim_{n\to+\infty}f(x_n)=\Lambda$. Poiché $a_n\leq x_n\leq b_n$, per i due carabinieri

$$
\lim_{n\to+\infty}x_n=x_M=\bar a=\bar b.
$$

Per continuità,

$$
\lim_{n\to+\infty}f(x_n)
=f\!\left(\lim_{n\to+\infty}x_n\right)=f(x_M).
$$

Per unicità del limite,

$$
f(x_M)=\lim_{n\to+\infty}f(x_n)
=\Lambda=\sup_{[a,b]}f.
$$

Quindi $f(x_M)=\max_{[a,b]}f$.

Similmente si dimostra che esiste $x_m\in[a,b]$ tale che $f(x_m)=\min_{[a,b]}f$. $\square$

## Commenti alla dimostrazione

Questa è la prova del docente nel PDF L16, pp. 2-6, nell'ordine effettivo: identità per il superiore di un'unione, bisezione, quattro proprietà, punto limite, esclusione di $+\infty$, approssimazione del superiore finito e raggiungimento del massimo. Non si suppone già che $f$ sia limitata o che possieda un massimo: sono proprio le conclusioni da ottenere.

Il superiore esiste nella retta estesa perché l'immagine è un insieme non vuoto di reali. Non può essere $-\infty$, dato che contiene, per esempio, il valore reale $f(a)$. Restano perciò i due casi considerati dal docente.

A ogni bisezione si sceglie una metà il cui **superiore rimane $\Lambda$**. Entrambe possono soddisfare la condizione: in tal caso la prima scelta del docente è comunque valida. La costruzione è teorica; non richiede di conoscere un punto di massimo prima di averlo dimostrato e non costituisce da sola un procedimento numerico per calcolare i superiori.

I due limiti degli estremi esistono per [[76 Teorema del Limite delle Successioni Monotone]]; i [[82 Teorema dei Due Carabinieri|due carabinieri]] portano poi ogni scelta $x_n\in[a_n,b_n]$ allo stesso punto. La chiusura e la limitatezza del dominio assicurano che quel punto sia ancora in $[a,b]$, dove la [[130 Continuità di una Funzione|continuità]] può essere usata.

Le due successioni chiamate $x_n$ nelle due parti della prova sono scelte distinte: la prima appartiene al caso assurdo $\Lambda=+\infty$, la seconda al caso $\Lambda\in\mathbb R$. Nella seconda scelta si usa la [[28 Caratterizzazione degli Estremi|caratterizzazione del superiore]], senza pretendere di trovare subito un punto con valore esattamente $\Lambda$. La precisione $1/n$ fa tendere i valori scelti al superiore.

Per esplicitare soltanto il «similmente» finale, si può applicare il risultato appena provato alla funzione continua $-f$: se $-f$ raggiunge il suo massimo in $x_m$, allora $-f(x)\leq-f(x_m)$ per ogni $x$, cioè $f(x_m)\leq f(x)$. Questo chiarimento è un commento aggiunto, non un ulteriore passaggio trascritto dal PDF.

![[142 Weierstrass e Bisezione del Superiore.svg|1100]]

## Commenti: significato delle ipotesi

L'intervallo è **chiuso e limitato**: i due estremi sono reali, appartengono al dominio e la funzione è continua anche in essi, nel senso del dominio. I punti di estremo possono essere interni oppure coincidere con gli estremi dell'intervallo. Non è richiesta la stretta monotonia e i punti che realizzano massimo o minimo non devono essere unici. Una funzione costante li realizza in ogni punto.

Per ottenere una barriera simmetrica, dai valori minimo $m=f(x_m)$ e massimo $M=f(x_M)$ basta porre

$$
K=\max\{|m|,|M|\},\qquad |f(x)|\leq K\quad\forall x\in[a,b].
$$

## Esempi sul ruolo delle ipotesi

> [!info] Approfondimento dal libro
> Il libro, §6.3, pp. 197-199, illustra l'enunciato con esempi che separano chiusura, limitatezza e continuità. Non si usa una prova alternativa del teorema.

### Intervallo non chiuso

$f(x)=x$ su $(-1,1)$ è continua e limitata, ma non ha massimo né minimo. Il superiore è $1$ e l'inferiore è $-1$, entrambi esclusi dall'immagine. Per ogni $x<1$ nell'intervallo esiste ancora $(x+1)/2>x$ nell'intervallo; analogamente si può trovare un valore minore di ogni $x>-1$.

### Intervallo non limitato

$f(x)=x$ su $\mathbb R$ è continua, ma non ha massimo né minimo: dati un valore $f(x)$, $f(x+1)=f(x)+1$ è maggiore e $f(x-1)=f(x)-1$ è minore.

### Funzione non continua

Su $[0,1]$ poniamo

$$
f(x)=\begin{cases}
1/x,&x\in(0,1],\\
1,&x=0.
\end{cases}
$$

Il dominio è chiuso e limitato, ma $f$ non è continua in zero: $f(x)\to+\infty$ da destra, mentre $f(0)=1$. Non ha massimo, perché è illimitata superiormente. Il minimo esiste e vale $1$: l'esempio mostra che la conclusione completa può fallire anche se uno dei due estremi viene raggiunto.

![[142 Weierstrass e Ruolo delle Ipotesi.svg|1100]]

## Esempio svolto con tutte le ipotesi

Per $f(x)=x^2$ su $[-1,2]$, la continuità segue da [[138 Algebra delle Funzioni Continue]] e il dominio è chiuso e limitato. Il teorema assicura entrambi gli estremi; per individuarli basta osservare

$$
0\leq x^2\leq4\quad\forall x\in[-1,2],
$$

con $f(0)=0$ e $f(2)=4$. Quindi

$$
x_m=0,\quad\min_{[-1,2]}f=0,
\qquad x_M=2,\quad\max_{[-1,2]}f=4.
$$

Il minimo è assunto all'interno e il massimo a un estremo. Weierstrass ne garantisce l'esistenza, ma non fornisce da solo le coordinate: qui le ricaviamo da disuguaglianze elementari.

## Prospettiva d'esame ed errori comuni

Il regolamento ufficiale elenca il teorema alla voce **D17**, oltre la prima prova in itinere. La [[D17 Teorema di Weierstrass|scheda del Formulario]] incorpora ora la stessa dimostrazione del professore della Lezione 16, con i commenti separati. Non viene attribuito uno stato di apprendimento al materiale soltanto perché è scritto.

Non confondere il punto di massimo con il valore massimo, né un massimo con un semplice maggiorante. Non applicare il teorema su $(a,b)$ o su $\mathbb R$ senza un argomento ulteriore. Se manca un'ipotesi, si studia direttamente la funzione invece di concludere automaticamente che non ha estremi.

### Da dire all'orale

> Una funzione reale continua su un intervallo chiuso e limitato assume massimo e minimo assoluti: esistono due punti del dominio i cui valori racchiudono tutti i valori della funzione. In particolare la funzione è limitata e superiore e inferiore coincidono con massimo e minimo. Il punto di estremo è un'ascissa, mentre l'estremo è il valore della funzione in quel punto.
