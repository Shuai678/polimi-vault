---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 08, PDF pp. 10-12 e 17
  - Libro, §3.3, p. 85
---

# Limiti di potenze con base ed esponente variabili

## Intuizione e condizione sulla base

In $a_n^{b_n}$ possono variare sia la base sia l'esponente. La sola conoscenza del comportamento della base non basta: una base vicina a $1$, elevata a un esponente enorme, può produrre un effetto significativo.

Per applicare la teoria delle potenze con esponente reale variabile richiediamo

$$
a_n>0\qquad\text{definitivamente}.
$$

Questo permette di usare il logaritmo e l'identità fondamentale

$$
\boxed{a_n^{b_n}=e^{b_n\log a_n}.}
$$

Il numero $e$ e i limiti associati sono trattati in [[90 Numero di Nepero e Limiti di Tipo Esponenziale]]. La notazione $\log$ del PDF è quella del logaritmo naturale, cioè di base $e$.

## Regole determinate

Supponiamo $a_n\to a\in[0,+\infty]$ e $b_n\to b\in\mathbb R\cup\{-\infty,+\infty\}$. La tabella riassume i casi con limite determinato. In tutte le righe resta l'ipotesi $a_n>0$ definitivamente.

| Limite della base $a$ | $b>0$ finito | $b<0$ finito | $b=0$ | $b=+\infty$ | $b=-\infty$ |
|---|---|---|---|---|---|
| $0$ | $0$ | $+\infty$ | indeterminata | $0$ | $+\infty$ |
| $0<a<1$ | $a^b$ | $a^b$ | $1$ | $0$ | $+\infty$ |
| $a=1$ | $1$ | $1$ | $1$ | indeterminata | indeterminata |
| $1<a<+\infty$ | $a^b$ | $a^b$ | $1$ | $+\infty$ | $0$ |
| $a=+\infty$ | $+\infty$ | $0$ | indeterminata | $+\infty$ | $0$ |

Il caso con $a>0$ e $b$ entrambi finiti è già in [[80 Algebra dei Limiti di Successioni]]. Le altre righe precisano l'estensione trattata nella Lezione 08.

## Come leggere la tabella attraverso il logaritmo

Studiamo prima $L_n=b_n\log a_n$. Se il suo limite esiste, allora

$$
a_n^{b_n}=e^{L_n}\to
\begin{cases}
e^L,&L_n\to L\in\mathbb R,\\
+\infty,&L_n\to+\infty,\\
0,&L_n\to-\infty.
\end{cases}
$$

Per esempio, se $a_n\to a\in(0,1)$, allora $\log a_n\to\log a<0$. Se anche $b_n\to+\infty$, il prodotto tende a $-\infty$ e la potenza tende a zero. Se $b_n\to-\infty$, il prodotto tende a $+\infty$ e la potenza diverge a $+\infty$.

Per $a_n\to0^+$, $\log a_n\to-\infty$; per $a_n\to+\infty$, $\log a_n\to+\infty$. I segni si studiano con [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate]]. Il passaggio al limite attraverso logaritmo ed esponenziale è usato nel PDF; la sua giustificazione generale sarà collegata più avanti alla continuità.

## Dimostrazione del caso finito svolta nel PDF

Supponiamo $a_n\to a>0$ e $b_n\to b\in\mathbb R$. La permanenza del segno assicura $a_n>0$ definitivamente. Il passaggio al limite nel logaritmo, usato dal docente, dà

$$
\log a_n\to\log a\in\mathbb R.
$$

Poiché anche $b$ è finito, la regola del prodotto di [[80 Algebra dei Limiti di Successioni]] implica

$$
b_n\log a_n\to b\log a.
$$

Passando all'esponenziale, come nelle pp. 10-11 del PDF,

$$
\lim_{n\to+\infty}a_n^{b_n}
=\lim_{n\to+\infty}e^{b_n\log a_n}
=e^{b\log a}=a^b.
$$

L'ultimo passaggio usa l'identità $a^b=e^{b\log a}$ con $a>0$. La condizione sulla base garantisce un logaritmo con limite finito; le forme indeterminate richiedono invece lo studio concreto del prodotto nell'esponente.

## Forme indeterminate delle potenze

$$
\boxed{0^0,\qquad(+\infty)^0,\qquad1^{\pm\infty}.}
$$

Sono etichette di comportamenti limite, non valori assegnati a un'espressione numerica. Tramite il logaritmo si trasformano in prodotti del tipo $0\cdot\infty$:

- base a $1$ ed esponente infinito: $\log a_n\to0$;
- base a zero o infinito ed esponente a zero: il logaritmo diverge.

Occorre studiare $b_n\log a_n$; non si può applicare la tabella del caso finito.

## Esempio del PDF: la radice $n$-esima di $n$

### Testo e idea

Calcolare $\lim n^{1/n}$. La base tende a $+\infty$ e l'esponente a zero: è la forma indeterminata $(+\infty)^0$.

### Svolgimento

Per $n\geq1$,

$$
n^{1/n}=e^{\frac{\log n}{n}}.
$$

La [[85 Gerarchia degli Infiniti|gerarchia]] dà $\log n/n\to0$. Quindi

$$
\boxed{n^{1/n}\to e^0=1.}
$$

### Cosa imparare

Il risultato non viene dal simbolo $\infty^0$, ma dal limite concreto dell'esponente dopo la trasformazione.

## Esempi che distinguono le possibilità

Per $n\geq2$,

$$
n^{1/\log n}=e^{\log n/\log n}=e,
\qquad
n^{1/\sqrt{\log n}}=e^{\sqrt{\log n}}\to+\infty.
$$

In entrambi i casi la base tende a infinito e l'esponente a zero, ma il risultato differisce da $n^{1/n}\to1$. Anche $(1/n)^{1/n}\to1$, mentre $(e^{-n})^{1/n}=e^{-1}$: il simbolo $0^0$ non determina un unico limite.

## Base identicamente uguale a $1$ o a $0$

Se $a_n=1$ per ogni indice, allora $a_n^{b_n}=1$ per ogni esponente reale: non occorre alcuna stima. Questo è diverso dall'ipotesi più debole $a_n\to1$.

Il PDF osserva anche che $0^n=0$ per $n\geq1$. È un caso definito separatamente, con esponente intero positivo; la base identicamente nulla non soddisfa l'ipotesi di positività necessaria per usare il logaritmo.

### Da dire all'orale

> Per una potenza a base definitivamente positiva scrivo $a_n^{b_n}=e^{b_n\log a_n}$ e studio prima il limite dell'esponente. Le forme $0^0$, infinito elevato a zero e uno elevato a infinito sono indeterminate perché i soli limiti di base ed esponente non fissano il risultato.

## Errori comuni e prospettiva d'esame

- Usare il logaritmo di una base nulla o negativa.
- Confondere una base costantemente uguale a $1$ con una base che tende a $1$.
- Applicare $a_n^{b_n}\to a^b$ quando $a=0$ o quando l'esponente non ha limite finito.
- Dimenticare che cambiare il segno dell'esponente può invertire il comportamento tra zero e infinito.

Potenziale rilevanza d'esame: condizioni della trasformazione logaritmica, tabella dei casi determinati e riconoscimento dei limiti di tipo esponenziale.
