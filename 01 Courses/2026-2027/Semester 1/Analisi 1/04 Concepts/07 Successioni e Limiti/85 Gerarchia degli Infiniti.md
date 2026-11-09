---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 15, PDF pp. 15-17
  - Libro, §5.10, p. 163, gerarchia e sostituzione reciproca
  - Lezione 07, PDF p. 20
  - Lezione 08, PDF pp. 15-17 e 21
  - Libro, §3.7, pp. 99-101 (enunciati e interpretazione)
---

# Gerarchia degli infiniti

## Perché viene introdotta

Sapere che numeratore e denominatore crescono entrambi senza limite non determina il limite del loro rapporto. Dobbiamo confrontare le velocità di crescita. La gerarchia fornisce quattro confronti fondamentali già enunciati nella Lezione 07.

## Teorema

Per $\alpha>0$ e $a>1$,

$$
\lim_{n\to+\infty}\frac{\log_a n}{n^\alpha}=0,
\qquad
\lim_{n\to+\infty}\frac{n^\alpha}{a^n}=0.
$$

Per ogni $a>1$,

$$
\lim_{n\to+\infty}\frac{a^n}{n!}=0.
$$

Infine,

$$
\lim_{n\to+\infty}\frac{n!}{n^n}=0.
$$

Gli indici si considerano almeno da $n=1$; per rapporti con logaritmo al denominatore si parte da $n=2$. Le costanti $a$ e $\alpha$ sono **fissate**, indipendenti da $n$.

## Notazione e significato

Il fattoriale è

$$
n!=1\cdot2\cdot\ldots\cdot n\quad(n\geq1),\qquad0!=1.
$$

Per esempio $4!=24$, mentre $4^4=256$. In $n!$ i fattori variano da $1$ a $n$; in $n^n$ ci sono $n$ fattori tutti uguali a $n$.

Il primo limite dice che qualunque potenza positiva dell'indice cresce più rapidamente del logaritmo. Il secondo dice che un'esponenziale con base maggiore di uno cresce più rapidamente di qualunque potenza positiva fissata. Il terzo pone il fattoriale sopra le esponenziali a base fissata, il quarto pone $n^n$ sopra il fattoriale.

L'ordine da ricordare, nella forma più generale, è:

$$
(\log_a n)^\beta\ll n^\alpha\ll a^n\ll n!\ll n^n.
$$

Qui $a>1$, $\alpha>0$ e $\beta>0$ sono **fissati**, indipendenti da $n$.

La scrittura $(\log_a n)^\beta$ indica una **potenza del logaritmo**: si calcola prima $\log_a n$, poi si eleva il risultato alla potenza $\beta$. Questa forma estende la gerarchia con il solo logaritmo: anche una potenza positiva fissa del logaritmo cresce più lentamente di qualunque potenza $n^\alpha$ con esponente positivo fisso. La giustificazione è riportata nella sezione sulle potenze positive del logaritmo.

Il simbolo $\ll$ riassume qui un confronto di crescita tramite rapporto nullo. In questa lista ogni termine cresce più lentamente del successivo **nel senso dei rapporti sopra**, non nel senso di una disuguaglianza valida per ogni indice. La gerarchia descrive il comportamento per $n$ grande: una potenza di esponente molto alto può superare un'esponenziale per molti indici iniziali.

### Da dire all'orale

> A base esponenziale maggiore di uno ed esponente della potenza positivo, entrambi fissati, il logaritmo cresce più lentamente della potenza, la potenza dell'esponenziale, l'esponenziale del fattoriale e il fattoriale di $n^n$. Il significato rigoroso è che ciascuno dei quattro rapporti enunciati tende a zero.

## Dimostrazioni e confine della lezione

A p. 20 della Lezione 07 il docente enuncia i quattro limiti senza dimostrarli. La Lezione 08 introduce gli strumenti per giustificare i due confronti con il fattoriale e amplia il primo confronto alle potenze positive del logaritmo. Le integrazioni seguenti sono ancora **Da studiare**.

## Metodo di riconoscimento

1. Identificare logaritmi, potenze dell'indice, esponenziali a base fissata, fattoriali e $n^n$.
2. Controllare che la base sia maggiore di uno e che gli esponenti richiesti siano positivi e fissati.
3. Riscrivere il rapporto in una delle forme del teorema, eventualmente moltiplicata per una costante.
4. Se compaiono somme, dividerle per il termine adatto e verificare il limite di ogni addendo. Il quoziente finale con limiti finiti si giustifica con [[80 Algebra dei Limiti di Successioni]].

## Esercizio svolto: rapporto con una somma

### Testo

Calcolare

$$
\lim_{n\to+\infty}\frac{n^3+\log_2 n}{2^n}.
$$

### Idea

L'esponenziale deve essere confrontata prima con la potenza. Per il logaritmo usiamo una catena di rapporti già noti.

### Svolgimento passo per passo

Separiamo esattamente i due addendi:

$$
\frac{n^3+\log_2 n}{2^n}
=\frac{n^3}{2^n}+\frac{\log_2 n}{2^n}.
$$

Il primo rapporto tende a zero per il secondo limite della gerarchia, con $\alpha=3$ e $a=2$. Per il secondo, scriviamo

$$
\frac{\log_2 n}{2^n}
=\frac{\log_2 n}{n}\cdot\frac{n}{2^n}.
$$

Entrambi i fattori tendono a zero per i primi due confronti del teorema. Per la regola del prodotto il secondo addendo tende a zero, e per la somma il risultato è

$$
\lim_{n\to+\infty}\frac{n^3+\log_2 n}{2^n}=0.
$$

### Cosa imparare

Il confronto di quantità non adiacenti nella lista si può costruire attraverso un prodotto di rapporti adiacenti, ciascuno con limite noto.

## Esercizio svolto: fattoriale

### Testo e svolgimento

Calcolare il limite di $\displaystyle\frac{5^n+n!}{n!}$. Per $n\geq1$,

$$
\frac{5^n+n!}{n!}=\frac{5^n}{n!}+1\to0+1=1,
$$

usando il terzo confronto con base fissata $a=5>1$. Il risultato nasce da una riscrittura esatta, non dalla cancellazione approssimativa del termine $5^n$.

## Integrazione dalla Lezione 08

### Potenze positive del logaritmo

Per ogni $\beta>0$, $\alpha>0$ e $a>1$ fissati,

$$
\frac{(\log_a n)^\beta}{n^\alpha}
=\left(\frac{\log_a n}{n^{\alpha/\beta}}\right)^\beta\to0.
$$

Infatti $\alpha/\beta>0$, perciò il rapporto interno tende a zero per il primo limite della gerarchia; è positivo per $n\geq2$ e la sua potenza positiva tende a zero. Il risultato comprende potenze reali positive, non soltanto esponenti interi.

La gerarchia ampliata del PDF è quindi

$$
(\log_a n)^\beta\ll n^\alpha\ll a^n\ll n!\ll n^n,
$$

dove ogni confronto significa che il rapporto del termine a sinistra con quello a destra tende a zero. In [[93 Notazione o-Piccolo]] gli stessi confronti sono scritti usando $o$.

### Dimostrazioni dei confronti con il fattoriale

Per $u_n=a^n/n!$ con $a>1$ fissato,

$$
\frac{u_{n+1}}{u_n}=\frac a{n+1}\to0<1.
$$

Il [[91 Criterio del Rapporto per Successioni]] dà $u_n\to0$.

Per $v_n=n^n/n!$,

$$
\frac{v_{n+1}}{v_n}=\left(1+\frac1n\right)^n\to e>1,
$$

per [[90 Numero di Nepero e Limiti di Tipo Esponenziale]]. Quindi $v_n\to+\infty$ e il suo reciproco $n!/n^n$ tende a zero. I calcoli completi sono nel Concept 91; qui si collegano le prove ai confronti già enunciati.

## Errori comuni e prospettiva d'esame

- Interpretare la gerarchia come ordine puntuale valido già per i primi indici.
- Confondere $a^n$ con $n^a$ o $n^n$: il ruolo dell'indice è diverso.
- Applicare $a^n/n!\to0$ con una base che dipende da $n$: il caso $a=n$ non rientra nelle ipotesi.
- Applicare $n^\alpha/a^n\to0$ con $a=1$ o con $0<a<1$.
- Sostituire simbolicamente un rapporto di due infiniti con $1$, $0$ o un valore non giustificato.

Potenziale rilevanza d'esame: enunciare i quattro limiti con le condizioni e riconoscerli dentro espressioni più articolate. Gli enunciati della Lezione 07 sono ora integrati con l'ampliamento e le applicazioni della Lezione 08; tutto il materiale aggiunto resta da studiare.

## Lezione 15 - Gerarchia per funzioni - Da studiare

> [!note] Nuova parte da studiare
> La gerarchia per funzioni e il suo uso col cambio di variabile seguono il PDF L15, pp. 15-17. La parte precedente della nota riguarda le successioni.

### Teorema del docente

Siano $a>1$ e $\alpha,\beta>0$ costanti fissate. Allora, nell'ordine del PDF,

$$
\boxed{\lim_{x\to+\infty}\frac{(\log_a x)^\alpha}{x^\beta}=0,}
\qquad (\log_a x)^\alpha=o(x^\beta),
$$

$$
\boxed{\lim_{x\to+\infty}\frac{x^\beta}{a^x}=0,}
\qquad x^\beta=o(a^x).
$$

La base $a>1$ rende positivi i logaritmi per $x>1$, così anche la loro potenza reale positiva è definita nella coda. Le costanti non dipendono da $x$.

Il professore annota **«dim. con il teorema di de l'Hospital»**. Non svolge qui tale dimostrazione: il riferimento è conservato senza introdurre un metodo non ancora trattato in queste lezioni.

### Osservazione del docente: argomento generico divergente

Se $f(x)\to+\infty$ per $x\to x_0\in\overline{\mathbb R}$, il cambio di variabile $t=f(x)$ dà

$$
\lim_{x\to x_0}\frac{(\log_a f(x))^\alpha}{(f(x))^\beta}
=\lim_{t\to+\infty}\frac{(\log_a t)^\alpha}{t^\beta}=0,
$$

$$
\lim_{x\to x_0}\frac{(f(x))^\beta}{a^{f(x)}}
=\lim_{t\to+\infty}\frac{t^\beta}{a^t}=0.
$$

La condizione $f(x)\to+\infty$ garantisce definitivamente $f(x)>1$ e quindi tutti i domini necessari. Non basta che $f$ sia soltanto illimitata.

### Osservazione successiva sulle successioni

Se $x_n\to+\infty$, allora

$$
\lim_{n\to+\infty}\frac{(\log_a x_n)^\alpha}{x_n^\beta}=0,
\qquad
\lim_{n\to+\infty}\frac{x_n^\beta}{a^{x_n}}=0.
$$

Con $x_n=n$ si ritrova la gerarchia per successioni già studiata. Non si introduce invece un fattoriale di variabile reale: i confronti con $n!$ della prima parte restano nel contesto delle successioni.

### Esempio del docente: una potenza contro un logaritmo in zero

Per $a>1$ e $\alpha,\beta>0$,

$$
\lim_{t\to0^+}t^\beta|\log_a t|^\alpha=0.
$$

La forma iniziale è $[0\cdot\infty]$. Il docente pone

$$
x=\frac1t,\qquad\lim_{t\to0^+}\frac1t=+\infty.
$$

Quindi

$$
\begin{aligned}
\lim_{t\to0^+}t^\beta|\log_a t|^\alpha
&=\lim_{x\to+\infty}\frac1{x^\beta}
\left|\log_a\frac1x\right|^\alpha\\
&=\lim_{x\to+\infty}\frac{(\log_a x)^\alpha}{x^\beta}=0.
\end{aligned}
$$

### Commenti, condizioni ed errori comuni

Per $x>1$, $\log_a(1/x)=-\log_a x$ e $\log_a x>0$, dunque il valore assoluto elimina il segno meno prima della potenza reale. Per esempio, con $a=e$, $\alpha=2$ e $\beta=1/2$, $\sqrt t\,|\log t|^2\to0$ per $t\to0^+$.

La gerarchia confronta rapporti: non sostituisce automaticamente un'espressione dentro somme con cancellazioni. Per basi $0<a<1$ l'esponenziale decresce e il secondo teorema qui enunciato non si applica. Per esponenti dipendenti dalla variabile occorre uno studio diverso.

### Da dire all'orale

> A più infinito, con base maggiore di uno ed esponenti positivi fissati, ogni potenza del logaritmo è trascurabile rispetto a ogni potenza positiva della variabile, e ogni potenza positiva è trascurabile rispetto all'esponenziale. Il cambio di variabile trasferisce i confronti a un argomento che tende a più infinito e permette di trattare anche una potenza per un logaritmo vicino a zero.
