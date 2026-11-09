---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 16, PDF pp. 18-20
  - Libro, §5.9.3, pp. 159-160, supporto per logaritmo, esponenziale e potenza
  - Lezione 15, PDF pp. 11-15
  - Libro, §5.9, pp. 156 e 159, enunciati pertinenti
  - Lezione 10, PDF p. 6 (collegamento annunciato con i limiti di funzioni)
  - Lezione 09, PDF pp. 4-5, 8-10
  - Libro, §3.5.2, pp. 94-96; §3.5.3, pp. 97-98; §3.8, p. 104
---

# Equivalenti e sviluppi asintotici notevoli

## Intuizione: riconoscere la scala giusta vicino a zero

Se un argomento $\varepsilon_n$ tende a zero, alcune espressioni complicate hanno un termine principale molto semplice. Per esempio $\sin\varepsilon_n$ si comporta come $\varepsilon_n$, mentre $1-\cos\varepsilon_n$ si comporta come $\varepsilon_n^2/2$: il secondo è più piccolo del primo in valore assoluto, a parità di argomento.

La [[94 Equivalenza Asintotica|equivalenza]] consente di usare il termine principale nei prodotti e nei quozienti. Lo **sviluppo con resto** precisa l'errore e diventa necessario quando si sottraggono termini che si cancellano.

Qui “sviluppo” significa soltanto una scrittura con [[93 Notazione o-Piccolo|resto o-piccolo]] giustificata da un limite notevole.

## Ipotesi e notazione

In tutta la nota:

$$
\varepsilon_n\to0,\qquad \varepsilon_n\neq0\text{ definitivamente}.
$$

$\varepsilon_n$ è una **successione di argomenti**, distinta dalla tolleranza $\varepsilon>0$ nella definizione di limite. Può essere positiva, negativa o cambiare segno. Gli angoli sono misurati in **radianti**. Il simbolo $\log$ indica il logaritmo naturale.

Poiché $\varepsilon_n\to0$, definitivamente $|\varepsilon_n|<1/2$ e quindi $1+\varepsilon_n>0$: logaritmi e potenze reali delle basi $1+\varepsilon_n$ sono definiti nella coda. Per le potenze, $\alpha\in\mathbb R$ è **fissato**; l'equivalenza con $\alpha\varepsilon_n$ richiede $\alpha\neq0$.

## Le sei formule della lezione

Tutti gli equivalenti si riferiscono a $n\to+\infty$.

| Espressione | Equivalente | Scrittura con resto |
|---|---|---|
| $\sin\varepsilon_n$ | $\varepsilon_n$ | $\sin\varepsilon_n=\varepsilon_n+o(\varepsilon_n)$ |
| $1-\cos\varepsilon_n$ | $\varepsilon_n^2/2$ | $\cos\varepsilon_n=1-\varepsilon_n^2/2+o(\varepsilon_n^2)$ |
| $e^{\varepsilon_n}-1$ | $\varepsilon_n$ | $e^{\varepsilon_n}=1+\varepsilon_n+o(\varepsilon_n)$ |
| $\log(1+\varepsilon_n)$ | $\varepsilon_n$ | $\log(1+\varepsilon_n)=\varepsilon_n+o(\varepsilon_n)$ |
| $(1+\varepsilon_n)^\alpha-1$, $\alpha\neq0$ | $\alpha\varepsilon_n$ | $(1+\varepsilon_n)^\alpha=1+\alpha\varepsilon_n+o(\varepsilon_n)$ |
| $\arctan\varepsilon_n$ | $\varepsilon_n$ | $\arctan\varepsilon_n=\varepsilon_n+o(\varepsilon_n)$ |

Per esempio la prima riga significa

$$
\frac{\sin\varepsilon_n}{\varepsilon_n}\to1,
\qquad
\frac{\sin\varepsilon_n-\varepsilon_n}{\varepsilon_n}\to0.
$$

Nella riga del coseno, il resto è piccolo rispetto a $\varepsilon_n^2$, non soltanto rispetto a $\varepsilon_n$. Il fattore $1/2$ non si può perdere. Il passaggio fra equivalenza e resto usa $a_n\sim b_n\iff a_n=b_n+o(b_n)$ e il fatto che una costante non nulla non cambia la classe dei resti.

Se $\alpha=0$, la potenza è esattamente $1$. La scrittura $1=1+0\varepsilon_n+o(\varepsilon_n)$ è valida scegliendo resto nullo; non ha invece senso l'equivalenza $0\sim0$, che richiederebbe dividere per zero.

### Il caso $\varepsilon_n=1/n$ presentato all'inizio del PDF

Per $n\geq1$:

$$
\begin{aligned}
\sin\frac1n&=\frac1n+o\!\left(\frac1n\right),\\
e^{1/n}&=1+\frac1n+o\!\left(\frac1n\right),\\
\log\!\left(1+\frac1n\right)&=\frac1n+o\!\left(\frac1n\right),\\
\cos\frac1n&=1-\frac1{2n^2}+o\!\left(\frac1{n^2}\right),\\
\left(1+\frac1n\right)^\alpha&=1+\frac\alpha n+o\!\left(\frac1n\right),\\
\arctan\frac1n&=\frac1n+o\!\left(\frac1n\right).
\end{aligned}
$$

Nella quinta riga $\alpha$ è fissato. Le corrispondenti equivalenze si ottengono togliendo gli eventuali termini costanti prima di confrontare: per esempio $e^{1/n}-1\sim1/n$.

## Perché non è richiesto un segno fisso

Con $\varepsilon_n=(-1)^n/(n+1)$ si ha ancora $\varepsilon_n\to0$ e $\varepsilon_n\neq0$. Vale $\sin\varepsilon_n/\varepsilon_n\to1$, anche se i punti si avvicinano a zero alternando il segno. Le condizioni sono sull'argomento e sul dominio, non sulla sua monotonia.

![[95 Infinitesimo di Segno Alterno.svg|900]]

## Giustificazione dei limiti notevoli

Il PDF elenca queste formule e le usa negli esercizi, rinviando anche al foglio degli asintotici su WeBeep. Le giustificazioni seguenti sono di supporto; il rinvio non significa che sia stata letta una risorsa non allegata.

### Seno e coseno: confronto geometrico

> [!info] Approfondimento dal libro
> §3.5.2, pp. 94-96, dimostra i due limiti usando aree nella circonferenza goniometrica e il teorema dei due carabinieri. Qui si esplicitano i passaggi necessari per studiarli.

Per $0<t<\pi/2$ poniamo $O=(0,0)$, $A=(1,0)$, $B=(\cos t,\sin t)$ e $T=(1,\tan t)$. Il triangolo $OAB$ è contenuto nel settore circolare $OAB$, che è contenuto nel triangolo $OAT$. Le rispettive aree sono $\sin t/2$, $t/2$ e $\tan t/2$; l'area del settore è $t/2$ perché il raggio è $1$ e $t$ è in radianti. Dunque

$$
\sin t\leq t\leq\tan t.
$$

![[95 Confronto Geometrico per il Seno.svg|900]]

Da $t\leq\sin t/\cos t$, essendo $t,\cos t>0$, e da $\sin t\leq t$, segue

$$
\cos t\leq\frac{\sin t}{t}\leq1.
$$

Il rapporto è pari, perciò la stessa stima vale per $-\pi/2<t<0$. Inoltre $|\sin t|\leq|t|$ e

$$
0\leq1-\cos t
=\frac{\sin^2 t}{1+\cos t}
\leq\sin^2 t\leq t^2
$$

per $|t|<\pi/2$, dove $\cos t>0$. Per $t=\varepsilon_n\to0$ abbiamo quindi $\cos\varepsilon_n\to1$. Il [[82 Teorema dei Due Carabinieri]] dà

$$
\frac{\sin\varepsilon_n}{\varepsilon_n}\to1.
$$

Infine, usando $1-\cos^2t=\sin^2t$,

$$
\frac{1-\cos\varepsilon_n}{\varepsilon_n^2}
=\left(\frac{\sin\varepsilon_n}{\varepsilon_n}\right)^2
\frac1{1+\cos\varepsilon_n}\to\frac12.
$$

### Logaritmo, esponenziale e potenza

> [!info] Approfondimento dal libro
> §3.5.3, pp. 97-98, collega questi tre limiti al numero di Nepero. Si riporta la catena essenziale, completando la gestione del segno e dei domini.

Se $\varepsilon_n>0$, ponendo $c_n=1/\varepsilon_n\to+\infty$, [[90 Numero di Nepero e Limiti di Tipo Esponenziale]] dà

$$
(1+\varepsilon_n)^{1/\varepsilon_n}
=\left(1+\frac1{c_n}\right)^{c_n}\to e.
$$

Se $y_n>0$ e $y_n\to e$, allora $\log y_n\to1$: per ogni $\eta>0$, definitivamente $e^{1-\eta}<y_n<e^{1+\eta}$, e applicando il logaritmo crescente si ottiene $1-\eta<\log y_n<1+\eta$. Pertanto

$$
\frac{\log(1+\varepsilon_n)}{\varepsilon_n}
=\log\!\left((1+\varepsilon_n)^{1/\varepsilon_n}\right)\to1.
$$

Per $\varepsilon_n<0$ usiamo $t_n=-\varepsilon_n/(1+\varepsilon_n)>0$, che tende a zero, e $1+\varepsilon_n=1/(1+t_n)$. Allora

$$
\frac{\log(1+\varepsilon_n)}{\varepsilon_n}
=\frac{\log(1+t_n)}{t_n}\frac1{1+\varepsilon_n}\to1.
$$

Se il segno alterna, le stime delle due parti valgono entrambe definitivamente: il limite resta $1$.

Per l'esponenziale, $u_n=e^{\varepsilon_n}-1\to0$, per la regola delle potenze con base positiva ed esponente tendente a zero in [[89 Limiti di Potenze con Base ed Esponente Variabili]]. Inoltre $u_n\neq0$ e $\log(1+u_n)=\varepsilon_n$. Quindi

$$
\frac{e^{\varepsilon_n}-1}{\varepsilon_n}
=\frac{u_n}{\log(1+u_n)}\to1.
$$

Per $\alpha\neq0$ fissato poniamo $v_n=\alpha\log(1+\varepsilon_n)\to0$, definitivamente non nullo. Dalla definizione di [[35 Potenze con Esponente Reale|potenza reale]] e dai due limiti appena ottenuti,

$$
\frac{(1+\varepsilon_n)^\alpha-1}{\varepsilon_n}
=\frac{e^{v_n}-1}{v_n}\,
\alpha\frac{\log(1+\varepsilon_n)}{\varepsilon_n}\to\alpha.
$$

Dividendo ancora per $\alpha$ si ottiene l'equivalenza con $\alpha\varepsilon_n$.

### Arcotangente: passaggio all'inversa

Una giustificazione aggiuntiva della formula usata nel PDF impiega [[69 Funzioni Goniometriche Inverse]]. Poniamo $t_n=\arctan\varepsilon_n$, così $t_n\in(-\pi/2,\pi/2)$ e $\tan t_n=\varepsilon_n$. Dal confronto geometrico $|t_n|\leq|\tan t_n|=|\varepsilon_n|$ segue $t_n\to0$. Per $n$ grande $t_n\neq0$ e

$$
\frac{\arctan\varepsilon_n}{\varepsilon_n}
=\frac{t_n}{\tan t_n}
=\cos t_n\frac{t_n}{\sin t_n}\to1.
$$

## Collegamento annunciato nella Lezione 10 — Da studiare

A p. 6 del PDF L10 il docente mette in relazione gli equivalenti per successioni con i corrispondenti limiti notevoli di funzioni:

$$
\lim_{x\to0}\frac{\sin x}{x}=1,\qquad
\lim_{x\to0}\frac{e^x-1}{x}=1,\qquad
\lim_{x\to0}\frac{\log(1+x)}{x}=1,\qquad
\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12.
$$

Sono le stesse formule applicate a un argomento $x$ che si avvicina a zero; qui $\log(1+x)$ è considerato nel suo dominio e i rapporti per $x\neq0$. Il PDF rinvia la trattazione dei limiti di funzioni a un momento successivo. Negli esercizi attuali le formule si usano con gli argomenti infinitesimi $\varepsilon_n$ già descritti.

## Uso negli esercizi ed errori comuni

- Individuare **l'argomento che tende a zero**: in $e^{7/n}-1$ è $7/n$, quindi l'equivalente è $7/n$.
- Conservare il segno: $1-e^{2/n}\sim-2/n$.
- Prima di sviluppare $(n+1)^{1/3}$, raccogliere $n^{1/3}$ e ottenere un incremento $1/n$. La formula per $(1+\varepsilon_n)^\alpha$ non vale con incremento $n$.
- Non sostituire $e^{\varepsilon_n}$ con $\varepsilon_n$: il termine costante è $1$.
- Non usare $\sin\varepsilon_n\sim\varepsilon_n$ per cancellare una differenza $\sin\varepsilon_n-\varepsilon_n$: il resto può determinare tutto il risultato.

Gli esercizi del docente sono sviluppati in [[96 Calcolo dei Limiti con Equivalenti Asintotici]]. Il limite della differenza tra seno e argomento richiede la precisione discussa in [[97 Cancellazioni e Precisione del Resto Asintotico]].

### Da dire all'orale

> Per una successione di argomenti infinitesima e definitivamente non nulla, seno, arcotangente, esponenziale meno uno e logaritmo di uno più l'argomento sono equivalenti all'argomento. Uno meno il coseno è equivalente a metà del quadrato. La potenza di uno più l'argomento, meno uno, è equivalente ad alfa volte l'argomento, con alfa fissato e non nullo. Gli angoli sono in radianti e le espressioni devono essere definite nella coda.

Potenziale rilevanza d'esame: riconoscere l'argomento, formulare le ipotesi, conservare coefficienti e segni e distinguere equivalenza da sviluppo con resto.

## Lezione 15 - Limiti notevoli di funzioni - Da studiare

> [!note] Enunciati nell'ordine del professore
> Nel PDF L15, pp. 11-13, il docente elenca **otto** limiti e scrive «dimostrazioni in seguito». Le giustificazioni di supporto per le successioni presenti sopra non sono presentate come dimostrazioni svolte in questa lezione. Le pp. 13-15 spiegano il passaggio a un argomento infinitesimo generico.

Tutti gli angoli sono in radianti e $\log$ è naturale. In un rapporto con denominatore $x$ si considera $x\neq0$; per logaritmi e potenze si conserva il dominio reale. Il significato di $o$ e $\sim$ per funzioni è nelle integrazioni della Lezione 15 dei Concept [[93 Notazione o-Piccolo]] e [[94 Equivalenza Asintotica]].

### 1. Seno

$$
\lim_{x\to0}\frac{\sin x}{x}=1,
\qquad \sin x\sim x,
\qquad \sin x=x+o(x).
$$

### 2. Coseno

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12,
\qquad1-\cos x\sim\frac{x^2}{2}.
$$

$$
1-\cos x=\frac{x^2}{2}+o(x^2),
\qquad\cos x=1-\frac{x^2}{2}+o(x^2).
$$

### 3. Limite che restituisce il numero di Nepero

$$
\boxed{\lim_{x\to\pm\infty}\left(1+\frac1x\right)^x=e.}
$$

La scrittura contiene due limiti, a $+\infty$ e a $-\infty$. La base è positiva nelle due code considerate: per $x>0$ e per $x<-1$. È il corrispondente per funzioni del limite in [[90 Numero di Nepero e Limiti di Tipo Esponenziale]].

### 4. Logaritmo

$$
\lim_{x\to0}\frac{\log(1+x)}x=1,
\qquad\log(1+x)\sim x,
\qquad\log(1+x)=x+o(x).
$$

Il dominio richiede $1+x>0$, condizione soddisfatta vicino a zero.

### 5. Esponenziale

$$
\lim_{x\to0}\frac{e^x-1}x=1,
\qquad e^x-1\sim x.
$$

$$
e^x-1=x+o(x),\qquad e^x=1+x+o(x).
$$

### 6. Potenza con esponente fissato

Per ogni $\alpha\in\mathbb R$ **fissato**,

$$
\lim_{x\to0}\frac{(1+x)^\alpha-1}x=\alpha.
$$

Per $\alpha\neq0$,

$$
(1+x)^\alpha-1\sim\alpha x.
$$

Per ogni $\alpha\in\mathbb R$,

$$
(1+x)^\alpha-1=\alpha x+o(x),
\qquad(1+x)^\alpha=1+\alpha x+o(x).
$$

La base $1+x$ è positiva vicino a zero. Se $\alpha=0$ il numeratore è identicamente nullo e il limite è zero: vale lo sviluppo con resto nullo, mentre $0\sim0$ non è un'equivalenza definita.

### 7. Tangente

$$
\lim_{x\to0}\frac{\tan x}x=1,
\qquad\tan x\sim x,
\qquad\tan x=x+o(x).
$$

Il denominatore interno $\cos x$ è non nullo vicino a zero, quindi la tangente è definita nella zona richiesta.

### 8. Arcotangente

$$
\lim_{x\to0}\frac{\arctan x}x=1,
\qquad\arctan x\sim x,
\qquad\arctan x=x+o(x).
$$

### Osservazione del docente: sostituzione di un infinitesimo

Se $\varepsilon(x)\to0$ per $x\to x_0\in\overline{\mathbb R}$ e $\varepsilon(x)\neq0$ definitivamente, dal [[139 Cambio di Variabile nei Limiti e Continuità della Composta|cambio di variabile]] segue, ponendo $t=\varepsilon(x)$,

$$
\lim_{x\to x_0}\frac{\sin\varepsilon(x)}{\varepsilon(x)}
=\lim_{t\to0}\frac{\sin t}t=1.
$$

Quindi, per $x\to x_0$,

$$
\sin\varepsilon(x)\sim\varepsilon(x),
\qquad\sin\varepsilon(x)=\varepsilon(x)+o(\varepsilon(x)).
$$

Il docente scrive poi, nello stesso ordine,

$$
\begin{aligned}
1-\cos\varepsilon(x)&\sim\frac{(\varepsilon(x))^2}{2},\\
\log(1+\varepsilon(x))&\sim\varepsilon(x),\\
e^{\varepsilon(x)}-1&\sim\varepsilon(x),\\
(1+\varepsilon(x))^\alpha-1&\sim\alpha\varepsilon(x)\quad(\alpha\neq0).
\end{aligned}
$$

Le rispettive scritture con resto si ottengono sostituendo lo stesso argomento negli sviluppi precedenti, con scala $\varepsilon(x)^2$ per il coseno e $\varepsilon(x)$ negli altri casi. La non nullità definitiva consente di formare i rapporti richiesti. La funzione $\varepsilon(x)$ può cambiare segno; non deve essere monotona.

### Osservazione successiva: ritorno alle successioni

Se $\varepsilon_n\to0$ e $\varepsilon_n\neq0$ definitivamente, si ritrovano

$$
\sin\varepsilon_n\sim\varepsilon_n,\qquad
1-\cos\varepsilon_n\sim\frac{\varepsilon_n^2}{2},\qquad
\log(1+\varepsilon_n)\sim\varepsilon_n,
$$

$$
e^{\varepsilon_n}-1\sim\varepsilon_n,\qquad
(1+\varepsilon_n)^\alpha-1\sim\alpha\varepsilon_n\quad(\alpha\neq0).
$$

È il collegamento con la parte precedente della nota: le formule per successioni sono casi particolari della definizione successionale di limite di funzione.

### Commenti ed esempio svolto con un argomento composto

Calcoliamo

$$
L=\lim_{x\to0}\frac{1-\cos(3x)}{x\log(1+2x)}.
$$

Gli argomenti $3x$ e $2x$ tendono a zero e sono non nulli per $x\neq0$; inoltre $1+2x>0$ vicino a zero. Il logaritmo si annulla soltanto quando $x=0$. Applicando le formule agli **argomenti interi**,

$$
1-\cos(3x)\sim\frac{(3x)^2}{2}=\frac92x^2,
\qquad \log(1+2x)\sim2x.
$$

Prodotti e quozienti di equivalenti danno

$$
\frac{1-\cos(3x)}{x\log(1+2x)}
\sim\frac{(9/2)x^2}{2x^2}=\frac94,
\qquad\boxed{L=\frac94.}
$$

Per usare invece la formula 3, a $+\infty$ poniamo $t=3x$:

$$
\left(1+\frac1{3x}\right)^{2x}
=\left[\left(1+\frac1t\right)^t\right]^{2/3}
\longrightarrow e^{2/3}.
$$

Il controllo della base positiva rende lecita la riscrittura e la potenza esterna ha esponente fissato.

### Uso negli esercizi ed errori comuni

Prima di sostituire un equivalente, verificare il limite dell'argomento. $\sin(1/x)\sim1/x$ vale per $x\to\pm\infty$, quando $1/x\to0$, non per $x\to0$. Conservare i coefficienti e il termine costante: $e^x\sim x$ in zero è falso. Nelle differenze con cancellazioni usare la precisione discussa in [[97 Cancellazioni e Precisione del Resto Asintotico]], senza inventare resti più piccoli di quelli disponibili.

### Da dire all'orale

> I limiti notevoli descrivono il termine principale delle funzioni elementari vicino a zero. Posso sostituire alla variabile un argomento infinitesimo, definitivamente non nullo, controllando i domini. Per il coseno la scala è il quadrato dell'argomento; per le altre formule locali elencate la scala è l'argomento, con i coefficienti previsti. In questa lezione i limiti sono enunciati e le dimostrazioni sono rimandate.

## Lezione 16 - Dimostrazioni di logaritmo, esponenziale e potenza - Da studiare

> [!note] Nuova parte da studiare
> Il PDF L16, pp. 18-20, riprende il limite che restituisce $e$ e sviluppa poi, nell'ordine, logaritmo, esponenziale e potenza. Si conserva la catena del professore. Le prove di supporto per successioni presenti nella prima parte della nota rimangono distinte da questa trascrizione.

### Richiamo del docente sul numero di Nepero

Il professore richiama

$$
\lim_{x\to\pm\infty}\left(1+\frac1x\right)^x=e.\tag{*}
$$

Per la definizione successionale di limite questo equivale a

$$
\lim_{n\to+\infty}\left(1+\frac1{c_n}\right)^{c_n}=e
$$

per ogni successione $c_n$ tale che $c_n\to+\infty$ oppure $c_n\to-\infty$, nel dominio dell'espressione.

Il docente precisa che questo risultato era stato **enunciato, ma non dimostrato**, quando era stato definito $e$ tramite

$$
e=\lim_{n\to+\infty}\left(1+\frac1n\right)^n.
$$

Lo richiama come risultato disponibile e passa alle prove successive; queste righe non costituiscono una dimostrazione autonoma del passaggio dall'indice naturale a un argomento reale generico.

### Dimostrazione del professore: logaritmo

Vogliamo il limite

$$
\lim_{x\to0}\frac{\log(1+x)}x=1.
$$

Poiché $\log t$ è una funzione continua, usando $(*)$,

$$
\lim_{t\to\pm\infty}
\log\left(\left(1+\frac1t\right)^t\right)
=\log e=1.
$$

Pertanto

$$
\lim_{t\to\pm\infty}t\log\left(1+\frac1t\right)=1.
$$

Per cambio di variabile $x=1/t$, $t\to+\infty$ corrisponde a $x\to0^+$ e $t\to-\infty$ a $x\to0^-$. Quindi

$$
1=\lim_{t\to\pm\infty}t\log\left(1+\frac1t\right)
=\lim_{x\to0^{\pm}}\frac1x\log(1+x).
$$

I due limiti laterali valgono $1$ e dunque

$$
\boxed{\lim_{x\to0}\frac{\log(1+x)}x=1.}
$$

### Dimostrazione del professore: esponenziale

Per cambio di variabile,

$$
e^x-1=t\iff e^x=t+1\iff x=\log(t+1).
$$

Allora

$$
\begin{aligned}
\lim_{x\to0}\frac{e^x-1}x
&=\lim_{t\to0}\frac{t}{\log(t+1)}\\
&=\lim_{t\to0}\left(\frac{\log(t+1)}t\right)^{-1}=1.
\end{aligned}
$$

### Dimostrazione del professore: potenza

Per $\alpha\in\mathbb R$ vogliamo

$$
\lim_{x\to0}\frac{(1+x)^\alpha-1}x=\alpha.
$$

Se $\alpha=0$ il numeratore è nullo e il limite vale zero. Sia dunque $\alpha\neq0$. Il docente riscrive

$$
(1+x)^\alpha-1
=e^{\log((1+x)^\alpha)}-1
=e^{\alpha\log(1+x)}-1.
$$

Poi

$$
\begin{aligned}
\lim_{x\to0}\frac{(1+x)^\alpha-1}x
&=\lim_{x\to0}\frac{e^{\alpha\log(1+x)}-1}{x}\\
&=\lim_{x\to0}
\frac{e^{\alpha\log(1+x)}-1}{\alpha\log(1+x)}
\frac{\alpha\log(1+x)}x\\
&=\left(\lim_{t\to0}\frac{e^t-1}t\right)
\alpha\left(\lim_{x\to0}\frac{\log(1+x)}x\right)\\
&=1\cdot\alpha\cdot1=\alpha,
\end{aligned}
$$

ponendo $t=\alpha\log(1+x)$. $\square$

### Commenti alle dimostrazioni e precisazione della notazione

La catena del PDF è: richiamo di $(*)$, continuità del logaritmo, sostituzione reciproca, esponenziale tramite l'inversa del logaritmo, potenza tramite esponenziale e logaritmo. Si usano [[145 Continuità delle Funzioni Elementari]] e [[139 Cambio di Variabile nei Limiti e Continuità della Composta]]. L'argomento delle prove rimane quello del professore.

Nel passaggio del logaritmo il PDF scrive $x\to0^+$ in una riga che parte da $t\to\pm\infty$. Si è esplicitata sopra la corrispondenza corretta dei due lati: $+\infty\mapsto0^+$ e $-\infty\mapsto0^-$. È una precisazione della freccia di limite, non una prova alternativa; permette di giustificare il limite bilatero concluso dal docente.

Vicino a zero $1+x>0$, quindi logaritmo e potenza reale hanno il dominio richiesto. Per il cambio $t=e^x-1$, la continuità dell'esponenziale dà $t\to0$, e $x\neq0$ implica $t\neq0$. Inoltre $t>-1$ e $\log(1+t)\neq0$ per $t\neq0$: il reciproco del rapporto logaritmico è ben definito nella zona necessaria.

Nella potenza, $\alpha\neq0$ e $x\neq0$ vicino a zero garantiscono $\alpha\log(1+x)\neq0$. La nuova variabile tende a zero perché $\log(1+x)\to\log1=0$. Il caso $\alpha=0$ viene separato prima di dividere per $\alpha$, esattamente come nel PDF.

La definizione successionale in $(*)$ riguarda successioni di **numeri reali**, non soltanto indici naturali: non basta controllare il valore della funzione nei soli interi per concludere un limite di funzione. Per $c_n\to\pm\infty$ la base è comunque positiva definitivamente; gli eventuali termini iniziali fuori dominio non intervengono dopo aver considerato la coda ammissibile.

### Applicazione svolta con coefficienti

Per $x\to0$, il dominio del logaritmo richiede $1+3x>0$, verificato vicino a zero. I due rapporti

$$
\frac{\log(1+3x)}{3x}\to1,
\qquad\frac{e^{2x}-1}{2x}\to1
$$

usano precisamente gli argomenti $3x$ e $2x$. Quindi

$$
\frac{\log(1+3x)}{e^{2x}-1}
=\frac{\log(1+3x)}{3x}
\left(\frac{e^{2x}-1}{2x}\right)^{-1}\frac32
\longrightarrow\frac32.
$$

Le prove appena lette giustificano i due fattori tendenti a uno; l'esempio non richiede derivate né sviluppi di ordine superiore.

### Da dire all'orale

> Dal limite di tipo Nepero e dalla continuità del logaritmo, con la sostituzione reciproca ottengo logaritmo di uno più x diviso x tendente a uno. Ponendo t uguale a e alla x meno uno ricavo il limite dell'esponenziale. Per la potenza separo alfa uguale a zero; negli altri casi scrivo la potenza come esponenziale di alfa per il logaritmo e ottengo il prodotto dei due limiti già provati.
