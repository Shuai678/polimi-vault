---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 10, PDF pp. 3-6, 22-23
  - Libro, §3.8, pp. 105-106; esempio 3.53
---

# Equivalenti asintotici nelle funzioni composte

## Intuizione e quando si usa

Una composizione può nascondere più argomenti infinitesimi uno dentro l'altro. Il metodo del docente consiste nel partire dalla funzione **più esterna**, applicare un equivalente notevole al suo argomento effettivo e proseguire verso l'interno.

Non stiamo affermando che da $u_n\sim v_n$ segua sempre $f(u_n)\sim f(v_n)$: i controesempi sono in [[94 Equivalenza Asintotica]]. A ogni passaggio applichiamo invece una precisa formula di [[95 Equivalenti e Sviluppi Asintotici Notevoli]], verificandone le ipotesi.

## Procedura e giustificazione

1. Controllare il dominio dell'espressione nella coda.
2. Isolare l'argomento della funzione esterna e dimostrare che tende a zero, quando la formula lo richiede.
3. Applicare il limite notevole con quell'argomento, definitivamente non nullo.
4. Ripetere sull'espressione ottenuta e concatenare le equivalenze per transitività.
5. Nei prodotti e quozienti raccogliere coefficienti e potenze; nelle differenze trasformare prima l'espressione con un'identità esatta.

Perché si possono concatenare i passaggi? Se $a_n\sim b_n$ e $b_n\sim c_n$, allora $a_n/c_n=(a_n/b_n)(b_n/c_n)\to1$. Il controllo dei singoli rapporti è ciò che rende valida la catena.

## Esempio 1 — Seno di un logaritmo di un coseno

### Testo — PDF pp. 3-4

$$
a_n=\sin\!\left(\log\!\left(\cos\frac1n\right)\right),\qquad n\geq1.
$$

### Idea

Partiamo dal seno e poi trattiamo il logaritmo. Il coseno tende a $1$: per usare $\log(1+\varepsilon_n)$ bisogna individuare l'incremento $\cos(1/n)-1$.

### Svolgimento passo per passo

Per $n\geq1$, $0<\cos(1/n)<1$, quindi il logaritmo è definito e negativo. Dal limite del coseno,

$$
u_n=\cos\frac1n-1\sim-\frac1{2n^2}\to0.
$$

Scrivendo il logaritmo come $v_n=\log(1+u_n)$, otteniamo $v_n\sim u_n$ e quindi $v_n\to0$. Inoltre $u_n$ e $v_n$ non sono nulli. Possiamo applicare il limite del seno all'argomento $v_n$:

$$
\boxed{
a_n=\sin v_n\sim v_n
=\log\!\left(\cos\frac1n\right)
\sim\cos\frac1n-1
\sim-\frac1{2n^2}.}
$$

La verifica delle ipotesi si è fatta dall'interno; le **sostituzioni nella catena**, come nel PDF, partono dall'esterno.

### Risultato e cosa imparare

$$
\lim_{n\to+\infty}a_n=0,
\qquad a_n\sim-\frac1{2n^2}.
$$

L'equivalente fornisce anche segno e scala, informazioni più precise del solo limite zero. Sarebbe sbagliato scrivere $\log(\cos(1/n))\sim\cos(1/n)$: l'argomento del logaritmo tende a $1$, quindi conta la sua differenza da $1$.

## Esempio 2 — Argomenti piccoli e argomenti grandi

### Testo — PDF pp. 5-6

$$
a_n=\frac{\log(1+e^n)\,\log(\cos(1/n))}
{\arctan n\,\sin(2/n)}.
$$

### Idea

$e^n$ non è infinitesimo e non si può applicare direttamente lo sviluppo di $\log(1+\varepsilon_n)$ con $\varepsilon_n=e^n$. Prima raccogliamo $e^n$ all'interno del logaritmo.

### Svolgimento passo per passo

Per $n\geq1$ le espressioni sono definite; $\arctan n>0$ e $\sin(2/n)>0$ perché $0<2/n<\pi$.

$$
\begin{aligned}
\log(1+e^n)
&=\log\!\left(e^n(1+e^{-n})\right)\\
&=n+\log(1+e^{-n})\\
&=n+e^{-n}+o(e^{-n})\sim n.
\end{aligned}
$$

L'ultima equivalenza segue dividendo per $n$: $e^{-n}/n\to0$ e anche il resto diviso per $n$ tende a zero. Dall'esempio precedente,

$$
\log(\cos(1/n))\sim-\frac1{2n^2},\qquad
\sin(2/n)\sim\frac2n.
$$

Per l'arcotangente grande usiamo l'identità, valida per $n>0$,

$$
\arctan n=\frac\pi2-\arctan(1/n)\to\frac\pi2.
$$

L'identità deriva da $\tan(\pi/2-t)=1/\tan t$ per $t=\arctan(1/n)\in(0,\pi/2)$. Poiché $\arctan(1/n)\sim1/n\to0$, segue $\arctan n\sim\pi/2$, una costante non nulla.

Nei prodotti e nei quozienti le equivalenze si possono sostituire:

$$
a_n\sim\frac{n\,(-1/(2n^2))}{(\pi/2)(2/n)}
=\frac{-1/(2n)}{\pi/n}=-\frac1{2\pi}.
$$

### Risultato ed errore comune

$$
\boxed{\lim_{n\to+\infty}a_n=-\frac1{2\pi}.}
$$

La formula $\arctan\varepsilon_n\sim\varepsilon_n$ richiede $\varepsilon_n\to0$: non si può usare con argomento $n$. Il fattore $2$ in $\sin(2/n)$ e il segno del logaritmo del coseno sono essenziali.

## Esempio 3 — Esercizio assegnato e poi risolto dal docente

### Testo — PDF p. 4 e soluzione pp. 22-23

$$
a_n=n^3\bigl[\log(n^2+7)-2\log n\bigr]
\frac{\log(1+\arctan(1/n^2))}{e^{1/(3n)}-1},\qquad n\geq1.
$$

### Idea

La differenza dei logaritmi va trasformata **esattamente** prima di prendere equivalenti. Seguono una composizione logaritmo-arcotangente e un esponenziale con argomento piccolo.

### Svolgimento passo per passo

Gli argomenti dei logaritmi sono positivi e il denominatore è positivo. Dalle proprietà di [[36 Logaritmi]],

$$
\begin{aligned}
\log(n^2+7)-2\log n
&=\log\!\left(n^2\left(1+\frac7{n^2}\right)\right)-\log(n^2)\\
&=\log\!\left(1+\frac7{n^2}\right)
=\frac7{n^2}+o(1/n^2)\sim\frac7{n^2}.
\end{aligned}
$$

Per la composizione, $t_n=\arctan(1/n^2)\sim1/n^2\to0$ e $t_n>0$, quindi

$$
\log(1+\arctan(1/n^2))\sim\arctan(1/n^2)\sim\frac1{n^2}.
$$

Infine $e^{1/(3n)}-1\sim1/(3n)$. Allora

$$
a_n\sim n^3\frac7{n^2}\frac{1/n^2}{1/(3n)}
=21\,n^{3-2-2+1}=21.
$$

### Risultato e cosa imparare

$$
\boxed{\lim_{n\to+\infty}a_n=21.}
$$

Sostituire prima $\log(n^2+7)$ con $2\log n$ farebbe sparire proprio la differenza che determina il risultato. È il problema di precisione descritto in [[97 Cancellazioni e Precisione del Resto Asintotico]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: scegliere l'argomento infinitesimo corretto nelle composizioni, normalizzare i logaritmi di quantità grandi e giustificare ogni passaggio della catena.

### Da dire all'orale

> In una funzione composta applico l'equivalente notevole alla funzione esterna dopo aver controllato il suo argomento. Poi proseguo verso l'interno e concateno i rapporti che tendono a uno. Questo procedimento non autorizza a sostituire equivalenti dentro una funzione arbitraria o dentro una differenza.
