---
course: Analisi 1
type: concept
status: Da studiare
updated: 2026-11-06
source:
  - Lezione 15, PDF pp. 21-26
  - Libro, §6.3, pp. 191-194, teorema 6.18 e bisezione
---

# Teorema degli zeri e metodo di bisezione

## Teorema del docente

Sia $f:[a,b]\to\mathbb R$, con $a,b\in\mathbb R$ e $a<b$, continua in $[a,b]$ e tale che

$$
f(a)f(b)<0,
$$

cioè $f(a)$ e $f(b)$ sono discordi in segno. Allora

$$
\boxed{\exists x_0\in(a,b):\quad f(x_0)=0.}
$$

Inoltre, se $f$ è **strettamente monotona**, tale zero è unico.

## Osservazioni del docente, prima della prova

Il teorema fornisce condizioni che garantiscono una soluzione dell'equazione $f(x)=0$, localizza la soluzione nell'intervallo aperto $(a,b)$ e fornisce un algoritmo per approssimarla: la **bisezione**.

Nella costruzione dell'algoritmo, $a_n$ cresce, $b_n$ decresce ed entrambe tendono allo stesso $x_0$. Il docente anticipa le stime

$$
0\leq x_0-a_n\leq b_n-a_n=\frac{b-a}{2^n},
$$

$$
0\leq b_n-x_0\leq b_n-a_n=\frac{b-a}{2^n},\qquad n\in\mathbb N.
$$

## Dimostrazione del professore

### 1. Unicità se la funzione è strettamente monotona

Cominciamo mostrando che, se $f$ è strettamente monotona, allora, se esiste, è unico il punto $x_0\in(a,b)$ tale che $f(x_0)=0$.

Se $f$ è strettamente crescente,

$$
f(x)>f(x_0)=0\qquad\forall x\in(x_0,b),
$$

$$
f(x)<f(x_0)=0\qquad\forall x\in(a,x_0).
$$

Se invece $f$ è strettamente decrescente, le disuguaglianze sono invertite. In ogni caso

$$
f(x)\neq f(x_0)=0\qquad
\forall x\in(a,b),\ x\neq x_0.
$$

Quindi $x_0$ è l'unica soluzione di $f(x)=0$ in $(a,b)$.

### 2. Esistenza tramite il metodo di bisezione

Mostriamo ora che nelle ipotesi del teorema esiste $x_0\in[a,b]$ tale che $f(x_0)=0$.

Poniamo

$$
a_0=a,\qquad b_0=b,\qquad c_0=\frac{a_0+b_0}{2},
$$

punto medio del segmento $[a_0,b_0]$.

Se $f(c_0)=0$, allora $x_0=c_0$ e abbiamo finito. Se $f(c_0)\neq0$, allora vale o $f(c_0)f(a_0)<0$ oppure $f(c_0)f(b_0)<0$, non entrambe, perché $f(a_0)$ e $f(b_0)$ sono discordi in segno.

Se $f(a_0)f(c_0)<0$, poniamo

$$
a_1=a_0,\qquad b_1=c_0,\qquad
c_1=\frac{a_1+b_1}{2}.
$$

Se $f(c_0)f(b_0)<0$, poniamo

$$
a_1=c_0,\qquad b_1=b_0,\qquad
c_1=\frac{a_1+b_1}{2}.
$$

Ripetiamo il ragionamento con $[a_1,b_1]$, con $[a_2,b_2]$ e così via. L'algoritmo procede e si ferma se troviamo $c_n$, per qualche $n\in\mathbb N$, tale che $f(c_n)=0$: in tal caso $x_0=c_n$ e abbiamo concluso.

Altrimenti l'algoritmo procede all'infinito e produce due successioni $a_n,b_n$ con le seguenti proprietà:

1. $a_n$ cresce e $b_n$ decresce;
2. $a_n,b_n\in[a,b]$ per ogni $n\in\mathbb N$;
3. $\displaystyle0\leq b_n-a_n=\frac{b-a}{2^n}$ per ogni $n\in\mathbb N$;
4. $f(a_n)f(b_n)<0$ per ogni $n\in\mathbb N$;

con $c_n=(a_n+b_n)/2$.

Da 1 e 2, $a_n,b_n$ sono successioni monotone e limitate. Esistono quindi

$$
\bar a=\lim_{n\to+\infty}a_n\in\mathbb R,
\qquad\bar b=\lim_{n\to+\infty}b_n\in\mathbb R,
$$

per il teorema di regolarità delle successioni monotone.

Da 2, per permanenza del segno, segue $\bar a,\bar b\in[a,b]$. Da 3, per algebra dei limiti,

$$
\bar b-\bar a
=\lim_{n\to+\infty}(b_n-a_n)
=\lim_{n\to+\infty}\frac{b-a}{2^n}=0.
$$

Quindi $\bar b=\bar a$. Chiamiamo

$$
x_0=\bar b=\bar a\in[a,b].
$$

Per continuità di $f$,

$$
\lim_{n\to+\infty}f(a_n)=f(x_0)=f(\bar a),
$$

$$
\lim_{n\to+\infty}f(b_n)=f(x_0)=f(\bar b).
$$

Da 4, per permanenza del segno e algebra dei limiti,

$$
0\geq\lim_{n\to+\infty}f(b_n)f(a_n)
=(f(x_0))^2\geq0.
$$

Pertanto $(f(x_0))^2=0$, da cui $f(x_0)=0$. $\square$

## Commenti alla dimostrazione

La sequenza della prova è quella del PDF: **prima unicità, poi esistenza**. Non si sostituisce il passaggio finale del docente con una prova basata sulla scelta preventiva $f(a)<0<f(b)$: il docente conserva i prodotti discordi e conclude con il quadrato di $f(x_0)$.

La stretta monotonia è richiesta soltanto per l'unicità. L'esistenza usa continuità, intervallo e segni discordi agli estremi. La costruzione produce intervalli annidati, $[a_{n+1},b_{n+1}]\subseteq[a_n,b_n]$, e a ogni passo dimezza la lunghezza. “Cresce” e “decresce” per le successioni degli estremi sono qui in senso non stretto: a ogni passo uno dei due estremi può restare fermo.

Il [[76 Teorema del Limite delle Successioni Monotone]] assicura i due limiti finiti; [[79 Teorema di Permanenza del Segno]] permette di mantenere le disuguaglianze **non strette** nel limite. Dal prodotto sempre negativo non si deduce un limite negativo: si deduce un limite al più zero. La [[130 Continuità di una Funzione|continuità]] è usata esattamente per passare da $a_n,b_n\to x_0$ a $f(a_n),f(b_n)\to f(x_0)$.

Per completare esplicitamente la localizzazione nell'intervallo aperto, $f(a)f(b)<0$ implica $f(a)\neq0$ e $f(b)\neq0$. Il punto $x_0$ appena costruito soddisfa $f(x_0)=0$, quindi non può coincidere con nessuno dei due estremi: $x_0\in(a,b)$.

Il punto medio soddisfa inoltre

$$
|c_n-x_0|\leq\frac{b_n-a_n}{2}
=\frac{b-a}{2^{n+1}}.
$$

Questa stima sul punto medio è un commento operativo aggiunto alle due stime sugli estremi date dal docente. Se l'algoritmo si ferma, lo zero è trovato esattamente; le formule per le successioni infinite riguardano il caso in cui prosegue.

![[141 Bisezione e Intervalli Annidati.svg|1000]]

## Metodo operativo con esempio svolto

### Testo e idea

Approssimare lo zero di $f(x)=x^2-2$ in $[1,2]$ con la bisezione. La funzione è continua per [[138 Algebra delle Funzioni Continue]], $f(1)=-1$ e $f(2)=2$: lo zero esiste. È unico perché, se $1\leq x<y\leq2$,

$$
f(y)-f(x)=y^2-x^2=(y-x)(y+x)>0.
$$

Non si usano derivate per provare la stretta crescenza.

### Svolgimento passo per passo

A ogni passo si conserva la metà i cui estremi hanno valori discordi.

| $n$ | $[a_n,b_n]$ | $c_n$ | $f(c_n)$ | Intervallo successivo |
|---|---|---|---|---|
| 0 | $[1,2]$ | $3/2$ | $1/4>0$ | $[1,3/2]$ |
| 1 | $[1,3/2]$ | $5/4$ | $-7/16<0$ | $[5/4,3/2]$ |
| 2 | $[5/4,3/2]$ | $11/8$ | $-7/64<0$ | $[11/8,3/2]$ |
| 3 | $[11/8,3/2]$ | $23/16$ | $17/256>0$ | $[11/8,23/16]$ |

Dopo quattro dimezzamenti,

$$
\sqrt2\in\left[\frac{11}{8},\frac{23}{16}\right],
\qquad b_4-a_4=\frac1{16}.
$$

Il punto medio è $c_4=45/32=1{,}40625$ e

$$
\boxed{\left|\sqrt2-\frac{45}{32}\right|\leq\frac1{32}.}
$$

### Risultato e cosa imparare

La bisezione produce un intervallo certificato e un errore controllato. Non serve esprimere lo zero con una formula: l'esempio usa $\sqrt2$ per rendere riconoscibile il risultato. Per una tolleranza $\varepsilon>0$, si sceglie $n\geq0$ tale che $(b-a)/2^{n+1}\leq\varepsilon$ e si usa $c_n$.

## Ruolo delle ipotesi ed errori comuni

> [!info] Approfondimento dal libro
> Il libro, §6.3, pp. 191-194, insiste sulla continuità e presenta anch'esso la bisezione. Per esempio $F(x)=1/2+\operatorname{sign}x$ in $[-1,1]$ ha valori negativi in $-1$ e positivi in $1$, ma non si annulla mai: assume soltanto $-1/2$, $1/2$, $3/2$. In zero è discontinua, quindi il teorema non si applica.

I segni discordi sono una condizione sufficiente, non necessaria: $x^2$ ha uno zero in $[-1,1]$ anche se i due valori agli estremi sono positivi. Senza stretta monotonia non si conclude l'unicità: la funzione potrebbe annullarsi più volte.

Nel metodo non si conserva “la metà che sembra più vicina” a uno zero: si conserva quella che mantiene i segni discordi. Se $f(c_n)=0$, si termina prima di scegliere una metà. Non confondere l'ampiezza dell'intervallo $(b-a)/2^n$ con la stima sul suo punto medio, che ha un ulteriore fattore $1/2$.

## Prospettiva d'esame

Il regolamento ufficiale include il teorema di esistenza degli zeri alla voce **D15**, oltre il programma del primo parziale chiuso nella Lezione 12. La scheda [[D15 Teorema di Esistenza degli Zeri|D15 del Formulario]] incorpora questa stessa prova, così il testo rimane allineato.

### Da dire all'orale

> Una funzione continua su un intervallo chiuso e limitato, con valori di segno opposto agli estremi, ha almeno uno zero nell'intervallo aperto. Se è strettamente monotona, lo zero è unico. La bisezione conserva una metà con valori discordi e produce intervalli annidati di lunghezza dimezzata. Le successioni degli estremi convergono allo stesso punto; per continuità e permanenza del segno il quadrato del valore della funzione in quel punto è zero.
