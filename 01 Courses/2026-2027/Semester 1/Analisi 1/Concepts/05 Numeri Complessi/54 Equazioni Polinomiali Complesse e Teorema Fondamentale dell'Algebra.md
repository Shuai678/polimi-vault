---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 04, PDF pp. 14-17
---

# Equazioni polinomiali complesse e teorema fondamentale dell'algebra

## Perché servono

Il passaggio da $\mathbb{R}$ a $\mathbb{C}$ permette di risolvere equazioni polinomiali che nei reali non hanno soluzioni. Il risultato centrale è che, nel campo complesso, un polinomio non costante possiede tutte le radici previste dal suo grado, purché siano contate con la corretta molteplicità.

## Equazioni di secondo grado in C

Siano

$$
a,b,c\in\mathbb{C},
\qquad
a\neq0.
$$

Consideriamo l'equazione

$$
az^2+bz+c=0.
$$

Il discriminante è il numero complesso

$$
\Delta=b^2-4ac.
$$

Se $\delta$ è una radice quadrata complessa di $\Delta$, cioè

$$
\delta^2=\Delta,
$$

le soluzioni sono

$$
z_0=\frac{-b+\delta}{2a},
\qquad
z_1=\frac{-b-\delta}{2a}.
$$

In forma abbreviata,

$$
z_{0,1}=\frac{-b\pm\sqrt{\Delta}}{2a},
$$

dove il simbolo $\sqrt{\Delta}$ deve essere interpretato tramite le due radici quadrate complesse opposte di $\Delta$.

### Da dire all'orale

> Per un'equazione quadratica a coefficienti complessi, con coefficiente principale non nullo, si definisce il discriminante $\Delta=b^2-4ac$. Scelta una radice quadrata complessa $\delta$ di $\Delta$, le soluzioni sono $(-b+\delta)/(2a)$ e $(-b-\delta)/(2a)$.

## Derivazione della formula quadratica

Partiamo da

$$
az^2+bz+c=0.
$$

### 1. Dividere per il coefficiente principale

Poiché $a\neq0$, possiamo dividere tutta l'equazione per $a$:

$$
z^2+\frac ba z+\frac ca=0.
$$

### 2. Completare il quadrato

Portiamo il termine costante al secondo membro:

$$
z^2+\frac ba z=-\frac ca.
$$

Aggiungiamo a entrambi i membri

$$
\left(\frac b{2a}\right)^2=\frac{b^2}{4a^2}.
$$

Otteniamo

$$
z^2+\frac ba z+\frac{b^2}{4a^2}
=\frac{b^2}{4a^2}-\frac ca.
$$

Il primo membro è un quadrato perfetto:

$$
\left(z+\frac b{2a}\right)^2
=\frac{b^2-4ac}{4a^2}.
$$

Usando il discriminante,

$$
\left(z+\frac b{2a}\right)^2
=\frac{\Delta}{4a^2}.
$$

### 3. Estrarre le radici quadrate complesse

Se $\delta^2=\Delta$, allora

$$
\left(\frac{\delta}{2a}\right)^2
=\frac{\Delta}{4a^2}.
$$

Le due possibilità sono quindi

$$
z+\frac b{2a}=\frac{\delta}{2a}
$$

oppure

$$
z+\frac b{2a}=-\frac{\delta}{2a}.
$$

Isolando $z$ si ottiene

$$
z=\frac{-b+\delta}{2a}
$$

oppure

$$
z=\frac{-b-\delta}{2a}.
$$

## Numero di soluzioni e molteplicità nel caso quadratico

- Se $\Delta\neq0$, le due radici quadrate di $\Delta$ sono non nulle e opposte; le soluzioni $z_0$ e $z_1$ sono distinte.
- Se $\Delta=0$, l'unica radice quadrata distinta è $\delta=0$ e si ottiene

$$
z_0=z_1=-\frac b{2a}.
$$

In questo secondo caso la soluzione è una radice doppia: è un solo valore complesso, ma viene contato con molteplicità $2$.

## Fattorizzazione del polinomio quadratico

Se $z_0$ e $z_1$ sono le due radici, contate con molteplicità, allora

$$
az^2+bz+c=a(z-z_0)(z-z_1).
$$

Sviluppando il secondo membro,

$$
\begin{aligned}
a(z-z_0)(z-z_1)
&=a\bigl(z^2-(z_0+z_1)z+z_0z_1\bigr)\\
&=az^2-a(z_0+z_1)z+az_0z_1.
\end{aligned}
$$

Confrontando i coefficienti si ritrovano le relazioni

$$
z_0+z_1=-\frac ba,
\qquad
z_0z_1=\frac ca.
$$

## Molteplicità di una radice

Sia $p$ un polinomio e sia $\alpha\in\mathbb{C}$. Si dice che $\alpha$ è una radice di molteplicità $m\geq1$ se

$$
p(z)=(z-\alpha)^m q(z),
$$

dove $q$ è un polinomio tale che

$$
q(\alpha)\neq0.
$$

Questo significa che il fattore $(z-\alpha)$ compare esattamente $m$ volte nella fattorizzazione di $p$.

### Da dire all'orale

> Una radice $\alpha$ ha molteplicità $m$ quando il polinomio è divisibile per $(z-\alpha)^m$ ma non per $(z-\alpha)^{m+1}$.

## Teorema fondamentale dell'algebra

### In parole semplici

Ogni polinomio complesso di grado positivo si scompone completamente in fattori lineari su $\mathbb{C}$.

### Condizioni

Sia

$$
p(z)=a_nz^n+a_{n-1}z^{n-1}+\cdots+a_1z+a_0,
$$

con

$$
a_0,a_1,\ldots,a_n\in\mathbb{C},
\qquad
a_n\neq0,
\qquad
n\geq1.
$$

### Conclusione

Il polinomio $p$ possiede esattamente $n$ radici in $\mathbb{C}$, se ogni radice è contata con la propria molteplicità.

Se tali radici, ripetute secondo la molteplicità, sono

$$
z_0,z_1,\ldots,z_{n-1},
$$

allora

$$
p(z)=a_n(z-z_0)(z-z_1)\cdots(z-z_{n-1}).
$$

Le radici non devono necessariamente essere tutte distinte.

### Da dire all'orale

> Il teorema fondamentale dell'algebra afferma che ogni polinomio non costante a coefficienti complessi, di grado $n$, possiede esattamente $n$ radici complesse contate con molteplicità e si fattorizza come prodotto di $n$ fattori lineari, moltiplicato per il coefficiente principale.

## Perché è utile

Il teorema garantisce che $\mathbb{C}$ è un ambiente sufficiente per trovare tutte le radici di qualsiasi equazione polinomiale. Permette inoltre di:

- controllare il numero totale delle radici con molteplicità;
- ricostruire il polinomio dalla sua fattorizzazione;
- distinguere il numero di valori distinti dalla somma delle loro molteplicità;
- riconoscere quando un'equazione non rientra nell'ipotesi polinomiale.

## Intuizione

Nei reali un polinomio può non avere radici, come $z^2+1$. Nei complessi le radici mancanti diventano disponibili. Una volta trovata una radice $\alpha$, il polinomio contiene il fattore $(z-\alpha)$; ripetendo la fattorizzazione si arriva a fattori tutti lineari.

## Strategia della dimostrazione

La dimostrazione completa del teorema fondamentale dell'algebra non è sviluppata nella lezione. Il risultato viene usato come teorema di esistenza e fattorizzazione:

1. un polinomio complesso non costante possiede almeno una radice;
2. trovata una radice, si estrae il relativo fattore lineare;
3. si applica nuovamente il ragionamento al polinomio di grado inferiore;
4. si prosegue fino a ottenere $n$ fattori lineari, contando le ripetizioni.

Questa è la struttura logica del risultato, non una dimostrazione completa del primo passo di esistenza.

## Esempio della lezione: conteggio delle molteplicità

Consideriamo l'equazione

$$
18(z-i)^4z^5(z-7i+4)^{18}=0.
$$

Il fattore costante $18$ è diverso da zero e non produce radici. Per la legge di annullamento del prodotto, almeno uno dei fattori variabili deve annullarsi.

### Prima radice

$$
(z-i)^4=0
\Longleftrightarrow
z=i.
$$

La radice $i$ ha molteplicità $4$.

### Seconda radice

$$
z^5=0
\Longleftrightarrow
z=0.
$$

La radice $0$ ha molteplicità $5$.

### Terza radice

$$
(z-7i+4)^{18}=0
\Longleftrightarrow
z-7i+4=0
\Longleftrightarrow
z=-4+7i.
$$

La radice $-4+7i$ ha molteplicità $18$.

### Controllo del grado

La somma delle molteplicità è

$$
4+5+18=27.
$$

Il polinomio ha infatti grado

$$
4+5+18=27.
$$

Le radici distinte sono soltanto tre, ma le radici contate con molteplicità sono ventisette, in accordo con il teorema fondamentale dell'algebra.

## Un'equazione non polinomiale: z meno il suo coniugato

Consideriamo

$$
z-\overline z=0.
$$

Ponendo

$$
z=x+iy,
\qquad
\overline z=x-iy,
$$

si ottiene

$$
\begin{aligned}
z-\overline z
&=(x+iy)-(x-iy)\\
&=2iy.
\end{aligned}
$$

Quindi

$$
2iy=0
\Longleftrightarrow
y=0.
$$

Le soluzioni sono tutti e soli i numeri reali:

$$
z=x,
\qquad x\in\mathbb{R}.
$$

L'equazione ha dunque infinite soluzioni. Questo non contraddice il teorema fondamentale dell'algebra, perché $z-\overline z$ non è un polinomio nella variabile $z$: compare anche l'operazione di coniugio, che non può essere espressa come una somma finita di potenze di $z$ con coefficienti complessi costanti.

### Da dire all'orale

> Il teorema fondamentale dell'algebra non si applica a $z-\overline z=0$, perché l'espressione contiene il coniugato e non è un polinomio in $z$. Scrivendo $z=x+iy$, l'equazione diventa $2iy=0$ e ha come soluzioni tutti i numeri reali.

## Metodo per riconoscere e risolvere il problema

1. Controllare che l'espressione sia davvero un polinomio in $z$.
2. Individuare il grado e il coefficiente principale.
3. Se il grado è $2$, calcolare il discriminante complesso.
4. Calcolare tutte le radici complesse necessarie, ricordando che una radice quadrata non nulla ha due valori opposti.
5. Fattorizzare il polinomio quando possibile.
6. Distinguere radici distinte e molteplicità.
7. Controllare che la somma delle molteplicità coincida con il grado.

## Errori comuni

- Applicare la formula quadratica senza verificare $a\neq0$.
- Trattare il discriminante come necessariamente reale.
- Scegliere una sola radice quadrata complessa di $\Delta$ e perdere una soluzione.
- Dire che un'equazione con radice doppia ha due valori distinti.
- Confondere il numero di radici distinte con il numero di radici contate con molteplicità.
- Dimenticare il coefficiente principale nella fattorizzazione.
- Leggere $(z-7i+4)$ come se la radice fosse $4-7i$ invece di $-4+7i$.
- Applicare il teorema fondamentale dell'algebra a espressioni che contengono $\overline z$, $|z|$ o $\operatorname{Re}z$ e che non sono polinomi in $z$.

## Connessioni

- Le radici del discriminante si calcolano con [[53 Radici Ennesime Complesse|radici ennesime complesse]].
- La soluzione di equazioni con coniugato riprende il metodo di [[46 Equazioni in una Variabile Complessa|equazioni in una variabile complessa]].
- La fattorizzazione traduce le radici in fattori lineari e rende visibile la loro molteplicità.

## Uso all'esame

Potenziale rilevanza d'esame: risolvere equazioni quadratiche a coefficienti complessi, calcolare correttamente le radici del discriminante, fattorizzare polinomi e controllare il numero totale delle radici mediante le molteplicità.

## Errore comune all'orale

Dire soltanto che un polinomio di grado $n$ “ha $n$ soluzioni” è incompleto: bisogna specificare che i coefficienti sono complessi, che il polinomio non è costante e che le radici sono contate con molteplicità.
