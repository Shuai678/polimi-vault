---
course: Analisi 1
type: method
status: studied
source:
  - Lezione 01, PDF pp. 21-23
  - Libro, cap. 1.2, pp. 6-8
---

# Dimostrazione per induzione

## Intuizione

Il principio di induzione funziona come una catena di tessere del domino: si verifica che cada la prima tessera e si dimostra che ogni tessera, cadendo, fa cadere la successiva. In questo modo la proprietà si trasmette a tutti i numeri naturali.

## Definizione formale

Sia $P(n)$ una proposizione che dipende da $n\in\mathbb N$. Se valgono entrambe le condizioni

$$
P(0)\text{ è vera}
$$

e

$$
\forall n\in\mathbb N,\qquad P(n)\Rightarrow P(n+1),
$$

allora

$$
\forall n\in\mathbb N,\qquad P(n)\text{ è vera}.
$$

### Da dire all'orale

> Per dimostrare una proprietà per induzione verifico il caso base e poi il passo induttivo: assumendo la proprietà vera per un naturale $n$ arbitrario, dimostro che essa è vera anche per $n+1$. Concludo quindi che la proprietà vale per ogni numero naturale.

## Notazione

- $P(n)$ è la proprietà riferita al naturale $n$.
- $P(0)$ è il caso base adottato nella lezione.
- $P(n)$, assunta vera nel passo induttivo, prende il nome di ipotesi induttiva.
- $P(n+1)$ è la tesi del passo induttivo.

## Condizioni

- Bisogna verificare un caso base.
- Il passo induttivo deve valere per un $n$ arbitrario, non soltanto per un valore particolare.
- Nel passo induttivo si assume $P(n)$ e si dimostra $P(n+1)$.
- Se il caso iniziale è $n_0$ invece di $0$, la conclusione vale per ogni $n\geq n_0$.

## Metodo

1. Formulare con precisione la proprietà $P(n)$.
2. Verificare il caso base $P(0)$, oppure $P(n_0)$ se la proprietà parte da un indice diverso.
3. Fissare un $n$ arbitrario e assumere vera $P(n)$.
4. Usare l'ipotesi induttiva per dimostrare $P(n+1)$.
5. Concludere, per il principio di induzione, che la proprietà vale per tutti i naturali considerati.

## Esempi

### Esempio intuitivo

Se si assume che $P(5)$ sia vera, il passo induttivo permette di dedurre $P(6)$. Applicato in generale, il passaggio $P(n)\Rightarrow P(n+1)$ propaga la proprietà dal caso base a tutti i casi successivi.

### Approfondimento dal libro: somma dei primi $n$ naturali positivi

Vogliamo dimostrare che, per ogni $n\in\mathbb N$ con $n\geq1$,

$$
1+2+\cdots+n=\frac{n(n+1)}2.
$$

Definiamo

$$
P(n):\ 1+2+\cdots+n=\frac{n(n+1)}2.
$$

## Base dell'induzione
**1. Caso base.** Per $n=1$ il primo membro vale $1$, mentre il secondo vale

$$
\frac{1(1+1)}2=\frac22=1.
$$

I due membri coincidono, quindi $P(1)$ è vera.

## Passo induttivo

**2. Ipotesi induttiva.** Sia $n\geq1$ arbitrario e assumiamo vera $P(n)$:

$$
1+2+\cdots+n=\frac{n(n+1)}2.
$$

**3. Tesi del passo induttivo.** Dobbiamo dimostrare $P(n+1)$, cioè

$$
1+2+\cdots+n+(n+1)=\frac{(n+1)(n+2)}2.
$$

**4. Uso dell'ipotesi induttiva.** Partiamo dal primo membro della tesi e separiamo l'ultimo termine:

$$
1+2+\cdots+n+(n+1).
$$

Per l'ipotesi induttiva, la somma fino a $n$ può essere sostituita con $\frac{n(n+1)}2$:

$$
\begin{aligned}
1+2+\cdots+n+(n+1)
&=\frac{n(n+1)}2+(n+1)\\
&=(n+1)\left(\frac n2+1\right)\\
&=(n+1)\frac{n+2}{2}\\
&=\frac{(n+1)(n+2)}2.
\end{aligned}
$$

Abbiamo ottenuto esattamente il secondo membro di $P(n+1)$.

**5. Conclusione.** Il caso base è vero e il passo $P(n)\Rightarrow P(n+1)$ è valido per ogni $n\geq1$. Per il principio di induzione,

$$
1+2+\cdots+n=\frac{n(n+1)}2
$$

per ogni naturale $n\geq1$.

### Esempio fondamentale: disuguaglianza di Bernoulli

#### Enunciato

Per ogni $x\in\mathbb R$ con $x\geq-1$ e per ogni $n\in\mathbb N$ con $n\geq1$, vale

$$
(1+x)^n\geq 1+nx.
$$

La condizione $x\geq-1$ garantisce che $1+x\geq0$. Questo fatto sarà indispensabile nel passo induttivo: moltiplicando una disuguaglianza per un numero non negativo, il suo verso non cambia.

#### Proprietà da dimostrare

Fissato un numero reale $x\geq-1$, definiamo

$$
P(n):\quad (1+x)^n\geq1+nx.
$$

Vogliamo dimostrare $P(n)$ per ogni naturale $n\geq1$.

#### 1. Caso base

Per $n=1$ la proprietà diventa

$$
(1+x)^1\geq1+1\cdot x.
$$

Entrambi i membri sono uguali a $1+x$:

$$
1+x\geq1+x.
$$

La disuguaglianza è vera come uguaglianza, quindi $P(1)$ è vera.

#### 2. Ipotesi induttiva

Sia $n\geq1$ arbitrario. Assumiamo che $P(n)$ sia vera, cioè

$$
(1+x)^n\geq1+nx.
$$

Questa è l'ipotesi induttiva. Dobbiamo usarla per dimostrare $P(n+1)$.

#### 3. Tesi del passo induttivo

La proprietà riferita a $n+1$ è

$$
(1+x)^{n+1}\geq1+(n+1)x.
$$

#### 4. Moltiplicazione dell'ipotesi induttiva

Poiché $x\geq-1$, si ha

$$
1+x\geq0.
$$

Possiamo quindi moltiplicare entrambi i membri dell'ipotesi induttiva per $1+x$ senza invertire il verso della disuguaglianza:

$$
(1+x)^n(1+x)\geq(1+nx)(1+x).
$$

Usando la proprietà delle potenze $(1+x)^n(1+x)=(1+x)^{n+1}$, otteniamo

$$
(1+x)^{n+1}\geq(1+nx)(1+x).
$$

#### 5. Sviluppo del prodotto

Sviluppiamo completamente il prodotto a destra:

$$
\begin{aligned}
(1+nx)(1+x)
&=1\cdot1+1\cdot x+nx\cdot1+nx\cdot x\\
&=1+x+nx+nx^2\\
&=1+(n+1)x+nx^2.
\end{aligned}
$$

Pertanto

$$
(1+x)^{n+1}\geq1+(n+1)x+nx^2.
$$

#### 6. Uso della non negatività di $nx^2$

Poiché $n\geq1$ e $x^2\geq0$, vale

$$
nx^2\geq0.
$$

Di conseguenza,

$$
1+(n+1)x+nx^2\geq1+(n+1)x.
$$

Per la transitività della relazione d'ordine,

$$
(1+x)^{n+1}\geq1+(n+1)x+nx^2\geq1+(n+1)x.
$$

Abbiamo quindi dimostrato $P(n+1)$.

#### 7. Conclusione

Il caso base $P(1)$ è vero e, per ogni $n\geq1$, dall'ipotesi $P(n)$ segue $P(n+1)$. Per il principio di induzione,

$$
(1+x)^n\geq1+nx
$$

per ogni $n\in\mathbb N$ con $n\geq1$ e per ogni $x\in\mathbb R$ con $x\geq-1$.

#### Perché le condizioni sono necessarie nella dimostrazione

- La condizione $x\geq-1$ assicura che $1+x\geq0$, quindi consente di moltiplicare l'ipotesi induttiva per $1+x$ senza cambiare il verso della disuguaglianza.
- La condizione $n\geq1$ assicura che $n$ sia non negativo; insieme a $x^2\geq0$, implica $nx^2\geq0$.

#### Esempio numerico di controllo

Prendiamo $x=2$ e $n=3$. Il primo membro vale

$$
(1+2)^3=3^3=27,
$$

mentre il secondo membro vale

$$
1+3\cdot2=7.
$$

Poiché $27\geq7$, la disuguaglianza è verificata in questo caso. Questo controllo numerico non costituisce una dimostrazione generale: la dimostrazione per induzione serve a provare la proprietà per tutti i naturali $n\geq1$.

#### Da dire all'orale

> Verifico il caso base $n=1$. Suppongo poi la disuguaglianza vera per un naturale $n$ arbitrario. Poiché $x\geq-1$, il fattore $1+x$ è non negativo e posso moltiplicare l'ipotesi induttiva per esso senza cambiare il verso della disuguaglianza. Sviluppando il prodotto compare il termine $nx^2$, che è non negativo; ottengo così la tesi per $n+1$ e concludo per induzione.

## Errori comuni

- Assumere $P(n+1)$ e cercare di dimostrare $P(n)$: questa è la direzione opposta a quella del passo induttivo.
- Assumere già vera $P(n+1)$, che è invece ciò che si deve dimostrare.
- Verificare soltanto il caso base.
- Dimostrare soltanto un passaggio particolare, per esempio da $P(3)$ a $P(4)$, invece del passaggio generale.
- Usare l'ipotesi induttiva senza dichiararla.
- Nella dimostrazione di Bernoulli, moltiplicare per $1+x$ senza verificare che $1+x\geq0$.
- Dimenticare di spiegare perché il termine $nx^2$ è non negativo.

## Connessioni

- Il principio di induzione dimostra implicazioni universali indicizzate dai numeri naturali.
- La disuguaglianza di Bernoulli, presentata subito dopo nella lezione, è dimostrata per induzione.

## Prospettiva d'esame

In una dimostrazione per induzione devono essere riconoscibili la proprietà $P(n)$, il caso base, l'ipotesi induttiva, la tesi $P(n+1)$ e la conclusione finale.
