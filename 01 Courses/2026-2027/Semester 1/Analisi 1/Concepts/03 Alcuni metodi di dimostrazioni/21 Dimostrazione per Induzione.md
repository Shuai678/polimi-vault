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

Se si assume che $P(5)$ sia vera, il passo induttivo permette di dedurre $P(6)$. Applicato in generale, il passaggio $P(n)\Rightarrow P(n+1)$ propaga la proprietà dal caso base a tutti i casi successivi.

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
