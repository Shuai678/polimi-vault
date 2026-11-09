---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 15, PDF pp. 6-11
  - Libro, §5.11, pp. 165-166, definizione e proprietà
  - Lezione 10, PDF pp. 2-5
  - Lezione 08, PDF pp. 20-22
  - Lezione 09, PDF pp. 2-3, 5-8
  - Libro, §3.8, pp. 102-106 (definizione e proprietà pertinenti)
---

# Equivalenza asintotica

## Intuizione

Due successioni sono equivalenti asintoticamente quando una approssima l'altra con un **errore relativo che tende a zero**. Non devono essere uguali e la loro differenza può perfino divergere.

## Definizione formale

Siano $a_n$ e $b_n$ successioni reali, con $b_n\neq0$ definitivamente. Si scrive

$$
\boxed{a_n\sim b_n\quad\Longleftrightarrow\quad\frac{a_n}{b_n}\to1.}
$$

La scrittura si legge “$a_n$ è asintoticamente equivalente a $b_n$”, per $n\to+\infty$. L'ipotesi del rapporto che tende a $1$ implica anche $a_n\neq0$ definitivamente e che $a_n$ e $b_n$ abbiano lo stesso segno tra loro per ogni indice sufficientemente grande. Il segno comune può anche alternare: per esempio $a_n=b_n=(-1)^n$.

### Da dire all'orale

> Due successioni sono asintoticamente equivalenti se il loro rapporto tende a uno, con denominatore definitivamente non nullo. Equivalentemente, la loro differenza è un o-piccolo della successione di riferimento: l'errore relativo tende a zero.

## Equivalenza e resto: dimostrazione

Per [[93 Notazione o-Piccolo]],

$$
\begin{aligned}
a_n\sim b_n
&\Longleftrightarrow\frac{a_n}{b_n}\to1\\
&\Longleftrightarrow\frac{a_n-b_n}{b_n}\to0\\
&\Longleftrightarrow a_n-b_n=o(b_n).
\end{aligned}
$$

Pertanto

$$
\boxed{a_n\sim b_n\quad\Longleftrightarrow\quad a_n=b_n+o(b_n).}
$$

Il resto riguarda la scala $b_n$; non si tratta in generale di un resto infinitesimo in valore assoluto.

## Stesso ordine ed equivalenza sono distinti

Se $a_n/b_n\to\ell\in\mathbb R\setminus\{0\}$, allora

$$
\frac{a_n}{\ell b_n}=\frac1\ell\frac{a_n}{b_n}\to1,
\qquad\text{cioè }a_n\sim\ell b_n.
$$

Per infiniti o infinitesimi questo dà lo stesso ordine, ma $a_n\sim b_n$ richiede specificamente $\ell=1$. L'esempio è

$$
\log(n^2)=2\log n\sim2\log n,
\qquad \log(n^2)\not\sim\log n.
$$

Il coefficiente moltiplicativo non può essere scartato.

## Esempio conclusivo della lezione

Per la successione del Concept [[93 Notazione o-Piccolo]], abbiamo dimostrato

$$
a_n=7n^{47}+o(n^{47}).
$$

Dividendo per $7n^{47}$,

$$
\frac{a_n}{7n^{47}}
=1+\frac17\frac{a_n-7n^{47}}{n^{47}}\to1.
$$

Dunque

$$
\boxed{a_n\sim7n^{47}.}
$$

Anche $o(n^{47})=o(7n^{47})$ nel senso delle classi di resti: dividere per una costante non nulla non modifica il limite zero.

## Uso nei prodotti e nei quozienti

> [!info] Approfondimento dal libro
> Le proprietà seguenti e le cautele sulle somme sviluppano §3.8, pp. 103-106. Sono conseguenze della definizione; non si introducono qui i limiti notevoli ulteriori presenti nella stessa sezione del testo.

Se $a_n\sim A_n$ e $b_n\sim B_n$, con le successioni di riferimento definitivamente non nulle, allora

$$
\frac{a_nb_n}{A_nB_n}
=\frac{a_n}{A_n}\frac{b_n}{B_n}\to1,
\quad\text{quindi }a_nb_n\sim A_nB_n.
$$

Per i quozienti, anche $b_n$ è definitivamente non nullo, e

$$
\frac{a_n/b_n}{A_n/B_n}
=\frac{a_n/A_n}{b_n/B_n}\to1,
\quad\text{quindi }\frac{a_n}{b_n}\sim\frac{A_n}{B_n}.
$$

### Esempio svolto

$$
\frac{3n^2+n}{2n^3-5}\sim\frac{3n^2}{2n^3}=\frac3{2n}\to0.
$$

Infatti $(3n^2+n)/(3n^2)=1+1/(3n)\to1$ e $(2n^3-5)/(2n^3)=1-5/(2n^3)\to1$. L'equivalenza finale significa che il rapporto fra la frazione originale e $3/(2n)$ tende a uno. Da questo segue il limite zero dell'originale, scrivendola come prodotto di $3/(2n)$ e di un fattore con limite $1$.

## Perché le sottrazioni richiedono attenzione

Consideriamo

$$
a_n=n^2+n,\qquad b_n=n^2.
$$

Si ha $a_n/b_n=1+1/n\to1$, dunque $a_n\sim b_n$. Però

$$
a_n-b_n=n\to+\infty.
$$

![[94 Errore Relativo ed Errore Assoluto.svg|760]]

Inoltre $n^2+n\sim n^2$ e $n^2-n\sim n^2$, ma

$$
(n^2+n)-(n^2-n)=2n.
$$

Sostituire entrambi i termini con $n^2$ produrrebbe zero e perderebbe il risultato. Il problema è la **cancellazione dei termini dominanti**: la differenza dipende proprio dai resti scartati. È quanto accade anche in [[88 Razionalizzazione e Differenze di Radicali]].

## Proprietà di relazione

La relazione è riflessiva, simmetrica e transitiva sulle successioni definitivamente non nulle:

$$
\frac{a_n}{a_n}=1,\qquad
\frac{b_n}{a_n}=\frac1{a_n/b_n}\to1,
\qquad
\frac{a_n}{c_n}=\frac{a_n}{b_n}\frac{b_n}{c_n}\to1.
$$

L'ultimo passaggio vale se $a_n\sim b_n$ e $b_n\sim c_n$. Queste proprietà consentono di concatenare equivalenze **giustificate**; non consentono sostituzioni arbitrarie dentro ogni operazione.

## Integrazione della Lezione 09

La caratterizzazione mediante il resto e le proprietà di relazione già dimostrate sopra. Nelle pp. 5-8 la proposizione include prodotti, quozienti, potenze fisse e conservazione del carattere; prodotti e quozienti non vengono duplicati qui.

### Potenze con esponente fissato

Se $a_n\sim A_n$ e $\alpha\in\mathbb R$ è fissato, allora

$$
\boxed{a_n^\alpha\sim A_n^\alpha,}
$$

purché le operazioni abbiano senso nella coda. Per un esponente reale arbitrario è sufficiente assumere $a_n,A_n>0$ definitivamente; per esponenti interi si possono ammettere anche basi negative definitivamente non nulle. Le potenze razionali su basi negative richiedono il controllo del loro dominio reale.

La dimostrazione, nel dominio ammesso, usa

$$
\frac{a_n^\alpha}{A_n^\alpha}
=\left(\frac{a_n}{A_n}\right)^\alpha\to1^\alpha=1.
$$

Il limite delle potenze a base tendente a $1>0$ è quello di [[89 Limiti di Potenze con Base ed Esponente Variabili]]. È essenziale che l'esponente qui sia fissato. Il controesempio $(1+1/n)^n$ riportato sotto mostra perché non si può estendere automaticamente la regola a un esponente variabile.

### Stesso carattere e stesso limite

Se $a_n\sim A_n$, le due successioni:

- convergono allo stesso limite finito;
- oppure divergono entrambe a $+\infty$;
- oppure divergono entrambe a $-\infty$;
- oppure sono entrambe irregolari, cioè non hanno limite nemmeno infinito.

**Dimostrazione.** Poniamo $q_n=a_n/A_n\to1$. Allora $a_n=q_nA_n$. Se $A_n\to\ell\in\mathbb R$, l'algebra dei limiti dà $a_n\to\ell$.

Definitivamente $1/2<q_n<3/2$. Se $A_n\to+\infty$, è definitivamente positiva e $a_n>A_n/2\to+\infty$. Se $A_n\to-\infty$, è definitivamente negativa e $a_n<A_n/2\to-\infty$. Si conclude con il [[83 Teorema del confronto per successioni divergenti]].

Infine, se $A_n$ è irregolare ma $a_n$ avesse limite finito o infinito, usando l'equivalenza simmetrica $A_n\sim a_n$ e i casi appena provati anche $A_n$ avrebbe quel limite. È una contraddizione. Lo stesso argomento vale scambiando i ruoli: i caratteri coincidono.

L'equivalenza quindi permette di calcolare il limite, ma **non coincide** con la sola uguaglianza del limite. Per esempio $1/n$ e $2/n$ tendono entrambi a zero, ma il loro rapporto tende a $1/2$ e non a $1$.

### Tutte le cautele richiamate dal docente

**Somme e differenze.** Oltre all'esempio di sottrazione già presente, anche una somma può cancellare i termini principali. Si ha

$$
n^2+n\sim n^2,\qquad -n^2+1\sim -n^2+2,
$$

ma le somme sono $n+1$ e $2$: il loro rapporto diverge, quindi non sono equivalenti.

**Esponenziali.** Da $a_n\sim A_n$ non segue in generale $e^{a_n}\sim e^{A_n}$. Per esempio $n+1\sim n$, mentre

$$
\frac{e^{n+1}}{e^n}=e\neq1.
$$

**Logaritmi.** Nemmeno $\log a_n\sim\log A_n$ segue automaticamente, anche quando gli argomenti sono positivi. Consideriamo $a_n=1+1/n$ e $A_n=1+1/n^2$. Il loro rapporto tende a $1$, ma per [[95 Equivalenti e Sviluppi Asintotici Notevoli]]

$$
\frac{\log(1+1/n)}{\log(1+1/n^2)}
\sim\frac{1/n}{1/n^2}=n\to+\infty.
$$

**Differenza infinitesima.** Abbiamo già visto che $a_n\sim A_n$ non implica $a_n-A_n\to0$. Anche l'implicazione opposta è falsa: $a_n=2/n$ e $A_n=1/n$ hanno differenza $1/n\to0$, ma rapporto costante $2$. L'errore assoluto tende a zero, quello relativo no.

Questi sono controesempi alle implicazioni generali. Per una particolare espressione una sostituzione può essere valida, ma occorre giustificarla; non basta citare $a_n\sim A_n$.

## Integrazione della Lezione 10 — Da studiare

### Quando il passaggio al logaritmo è giustificato

La cautela generale sui logaritmi resta valida. Il docente precisa però un caso in cui si può concludere: se $a_n,A_n>0$ definitivamente, $a_n\sim A_n$ e il loro limite comune è

$$
\ell\in[0,+\infty],\qquad \ell\neq1,
$$

allora

$$
\boxed{\log a_n\sim\log A_n.}
$$

Qui il valore $\ell=0$ si intende raggiunto da argomenti positivi. Poniamo $q_n=a_n/A_n\to1$. Dalle proprietà del logaritmo,

$$
\log a_n=\log A_n+\log q_n,\qquad
\frac{\log a_n}{\log A_n}
=1+\frac{\log q_n}{\log A_n}.
$$

Il numeratore dell'ultimo resto tende a zero. Se $0<\ell<+\infty$ e $\ell\neq1$, $\log A_n\to\log\ell\neq0$, e il rapporto del resto tende a zero. Se $\ell=0$, $\log A_n\to-\infty$; se $\ell=+\infty$, $\log A_n\to+\infty$: anche in questi casi il resto tende a zero. Questi limiti del logaritmo si verificano per monotonia: per esempio $A_n<e^{-M}$ implica $\log A_n<-M$, mentre $A_n>e^M$ implica $\log A_n>M$.

La non nullità definitiva di $\log A_n$ segue dal limite dell'argomento diverso da $1$. Se invece $\ell=1$, numeratore e denominatore dei logaritmi tendono a zero e questo ragionamento non decide: il controesempio $1+1/n$ e $1+1/n^2$ riportato sopra resta applicabile.

Per esempio $1+e^n\sim e^n\to+\infty$, dunque $\log(1+e^n)\sim\log(e^n)=n$. La trasformazione esatta e gli esercizi sulle composizioni sono in [[98 Equivalenti Asintotici nelle Funzioni Composte]].

## Errori comuni e prospettiva d'esame

- Confondere $\sim$ con uguaglianza esatta o con il semplice “stesso ordine”.
- Deducere $a_n-b_n\to0$ da $a_n\sim b_n$.
- Scartare coefficienti non nulli, come il $7$ nell'esempio conclusivo.
- Sostituire equivalenti dentro una differenza con cancellazione dominante.
- Elevare equivalenti a esponenti variabili senza controlli: per esempio $1+1/n\sim1$, ma $(1+1/n)^n\to e$ mentre $1^n=1$.

Potenziale rilevanza d'esame: definizione, equivalenza con il resto $o$-piccolo, uso nei rapporti e riconoscimento delle cancellazioni. Definizione ed esempio iniziale concludono il PDF della Lezione 08; le integrazioni sopra coprono i richiami e le proprietà della Lezione 09. Le applicazioni successive sono in [[95 Equivalenti e Sviluppi Asintotici Notevoli]], [[96 Calcolo dei Limiti con Equivalenti Asintotici]] e [[97 Cancellazioni e Precisione del Resto Asintotico]].

## Lezione 15 - Equivalenza asintotica per funzioni - Da studiare

> [!note] Nuova parte da studiare
> La sezione segue il PDF L15, pp. 6-11: definizioni, osservazioni, caratterizzazione col resto, proprietà, prove e cautele. Le parti precedenti conservano il contesto delle successioni.

### Definizione del docente

Per due funzioni $f,g$ e $x_0\in\overline{\mathbb R}$ di accumulazione del dominio comune, con $g(x)\neq0$ definitivamente,

$$
\boxed{f(x)\sim g(x)\text{ per }x\to x_0
\iff\lim_{x\to x_0}\frac{f(x)}{g(x)}=1.}
$$

Nella stessa pagina il professore introduce poi [[93 Notazione o-Piccolo#Lezione 15 - o-piccolo e infinitesimi per funzioni - Da studiare|o-piccolo, funzione infinitesima e funzione infinita]]. L'equivalenza riguarda un errore **relativo** che tende a zero.

### Osservazioni del docente sui rapporti

Se

$$
\lim_{x\to x_0}\frac{f(x)}{g(x)}=\lambda\in\mathbb R\setminus\{0\},
$$

allora $f(x)/(\lambda g(x))\to1$, cioè $f(x)\sim\lambda g(x)$. La costante va conservata.

Se invece $f(x)/g(x)\to\pm\infty$, allora $g(x)/f(x)\to0$, cioè $g(x)=o(f(x))$.

### Caratterizzazione col resto: passaggi del professore

Il docente osserva che $f(x)\sim g(x)$ se e solo se $f(x)=g(x)+o(g(x))$. Infatti, sempre per $x\to x_0$,

$$
\begin{aligned}
f(x)\sim g(x)
&\iff\lim_{x\to x_0}\frac{f(x)}{g(x)}=1\\
&\iff\lim_{x\to x_0}\left(\frac{f(x)}{g(x)}-1\right)=0\\
&\iff\lim_{x\to x_0}\frac{f(x)-g(x)}{g(x)}=0\\
&\iff f(x)-g(x)=o(g(x))\\
&\iff f(x)=g(x)+o(g(x)).
\end{aligned}
$$

### Proposizione del docente

**1. Operazioni.** Se $f_1\sim f_2$ e $g_1\sim g_2$ per $x\to x_0$, allora

$$
f_1g_1\sim f_2g_2,\qquad
\frac{f_1}{g_1}\sim\frac{f_2}{g_2},\qquad
(f_1)^\alpha\sim(f_2)^\alpha.
$$

L'esponente $\alpha\in\mathbb R$ è fissato. Il PDF precisa che le due potenze devono essere ben definite in un intorno di $x_0$, escluso al più $x_0$. I rapporti richiedono la non nullità definitiva dei denominatori; le equivalenze la garantiscono anche per le funzioni corrispondenti.

**2. Esistenza e valore del limite.** Se $f\sim g$, allora esiste $\lim_{x\to x_0}f(x)\in\overline{\mathbb R}$ se e solo se esiste $\lim_{x\to x_0}g(x)\in\overline{\mathbb R}$. Quando esistono, i limiti sono uguali.

### Dimostrazione del professore delle proprietà

**1. Nelle ipotesi**, per il prodotto,

$$
\frac{f_1(x)g_1(x)}{f_2(x)g_2(x)}
=\frac{f_1(x)}{f_2(x)}\frac{g_1(x)}{g_2(x)}\longrightarrow1
$$

per algebra dei limiti. Quindi $f_1g_1\sim f_2g_2$.

Per il quoziente,

$$
\frac{f_1(x)/g_1(x)}{f_2(x)/g_2(x)}
=\frac{f_1(x)g_2(x)}{f_2(x)g_1(x)}
=\frac{f_1(x)}{f_2(x)}
\left(\frac{g_1(x)}{g_2(x)}\right)^{-1}
\longrightarrow1
$$

per algebra dei limiti. Quindi $f_1/g_1\sim f_2/g_2$.

Per la potenza,

$$
\frac{(f_1(x))^\alpha}{(f_2(x))^\alpha}
=\left(\frac{f_1(x)}{f_2(x)}\right)^\alpha\longrightarrow1
$$

per algebra dei limiti. Quindi $(f_1)^\alpha\sim(f_2)^\alpha$.

**2.** Per $x\to x_0$ scriviamo

$$
f(x)=\frac{f(x)}{g(x)}\,g(x).
$$

Poiché $f(x)/g(x)\to1$, se esiste $\lim_{x\to x_0}g(x)=\ell\in\overline{\mathbb R}$, per algebra dei limiti e aritmetizzazione dell'infinito vale

$$
\lim_{x\to x_0}f(x)
=\lim_{x\to x_0}\left[\frac{f(x)}{g(x)}g(x)\right]
=1\cdot\ell=\ell.
$$

Invertendo i ruoli di $f,g$ e ripetendo l'argomento, se esiste $\lim f(x)=\ell$, allora esiste $\lim g(x)=\ell$. Segue la tesi. $\square$

### Osservazione successiva del docente: operazioni non ammesse in generale

Da $f_1\sim f_2$ e $g_1\sim g_2$ **non** seguono in generale

$$
f_1\pm g_1\sim f_2\pm g_2,\qquad
\log f_1\sim\log f_2,\qquad
e^{f_1}\sim e^{f_2}.
$$

Si controllano anche i domini delle espressioni scritte. Il professore colloca questa cautela prima dell'elenco dei limiti notevoli.

### Commenti alle prove ed errori da evitare

Il prodotto e il quoziente delle equivalenze sono giustificati da rapporti tendenti a $1$. Nelle potenze l'esponente è **fisso**: la proposizione non autorizza una potenza con esponente variabile.

La seconda proprietà riguarda anche limiti infiniti e limite zero. Non dice che un limite esista sempre: due funzioni equivalenti possono essere entrambe prive di limite.

Per vedere il pericolo delle cancellazioni, a $+\infty$ siano $f_1=x$, $f_2=x+1$, $g_1=-x+1$, $g_2=-x+2$. I due rapporti di partenza tendono a $1$, ma le somme sono $1$ e $3$ e non sono equivalenti. Inoltre $x+1\sim x$, ma $e^{x+1}/e^x=e\neq1$.

Per i logaritmi, a zero $1+x\sim1+x^2$, ma $\log(1+x)/\log(1+x^2)\sim x/x^2=1/x$: non tende a $1$. Gli argomenti sono positivi vicino a zero e i logaritmi sono non nulli per $x\neq0$ sufficientemente piccolo. Si usano i [[95 Equivalenti e Sviluppi Asintotici Notevoli#Lezione 15 - Limiti notevoli di funzioni - Da studiare|limiti notevoli successivi]]. Questi sono controesempi aggiunti come commento.

L'equivalenza non richiede che i grafici abbiano la stessa forma: il controesempio del docente è in [[140 Grafici Locali e Grafici Probabili]].

### Da dire all'orale

> Due funzioni sono asintoticamente equivalenti in un dato processo di limite se il loro rapporto tende a uno. Equivalentemente, la differenza è un o-piccolo della funzione di riferimento. Le equivalenze si moltiplicano, si dividono e si elevano a una potenza reale fissa quando le espressioni sono definite. Conservano esistenza e valore del limite, ma non si sostituiscono in generale nelle somme, nei logaritmi o negli esponenziali.
