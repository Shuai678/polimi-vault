---
course: Analisi 1
type: method
status: studied
source:
  - Lezione 01, PDF p. 21
  - Libro, cap. 1.2, pp. 6-7
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

**1. Caso base.** Per $n=1$ il primo membro vale $1$, mentre il secondo vale

$$
\frac{1(1+1)}2=\frac22=1.
$$

I due membri coincidono, quindi $P(1)$ è vera.

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

## Errori comuni

- Assumere $P(n+1)$ e cercare di dimostrare $P(n)$: questa è la direzione opposta a quella del passo induttivo.
- Assumere già vera $P(n+1)$, che è invece ciò che si deve dimostrare.
- Verificare soltanto il caso base.
- Dimostrare soltanto un passaggio particolare, per esempio da $P(3)$ a $P(4)$, invece del passaggio generale.
- Usare l'ipotesi induttiva senza dichiararla.

## Connessioni

- Il principio di induzione dimostra implicazioni universali indicizzate dai numeri naturali.
- La disuguaglianza di Bernoulli, presentata subito dopo nella lezione, è dimostrata per induzione.

## Prospettiva d'esame

In una dimostrazione per induzione devono essere riconoscibili la proprietà $P(n)$, il caso base, l'ipotesi induttiva, la tesi $P(n+1)$ e la conclusione finale.
