---
course: Analisi 1
type: concept
status: Da studiare
source:
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
