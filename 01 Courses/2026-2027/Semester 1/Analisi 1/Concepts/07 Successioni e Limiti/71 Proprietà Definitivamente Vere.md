---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF p. 11
  - Libro, §3.2, p. 78
---

# Proprietà definitivamente vere

## Definizione

Una proprietà $P(n)$ si dice vera **definitivamente**, oppure **eventualmente**, se esiste un indice $N\in\mathbb N$ tale che

$$
n\geq N
\quad\Longrightarrow\quad
P(n)\text{ è vera}.
$$

In simboli:

$$
\exists N\in\mathbb N\;\forall n\geq N: P(n).
$$

La proprietà può fallire per un numero finito di indici iniziali: ciò che conta è che sia sempre vera da un certo punto in poi.

## Esempio

Per la successione $a_n=1/n$, la proprietà

$$
a_n<\frac1\pi
$$

è definitivamente vera. Infatti

$$
\frac1n<\frac1\pi
\quad\Longleftrightarrow\quad
n>\pi,
$$

quindi è sufficiente scegliere $N=4$.

## Negazione logica

La proprietà $P$ **non** è definitivamente vera se

$$
\forall N\in\mathbb N\;\exists n\geq N: P(n)\text{ è falsa}.
$$

Ciò significa che, per quanto avanti si vada, si trova ancora un indice per cui la proprietà fallisce.

### Da dire all'orale

> “Definitivamente” significa “per tutti gli indici abbastanza grandi”: prima si sceglie una soglia $N$, poi la proprietà deve valere per ogni $n\geq N$.

## Perché serve

Le definizioni di limite non richiedono un comportamento particolare dei primi termini. Descrivono ciò che accade sulla coda della successione e quindi usano precisamente il linguaggio delle proprietà definitivamente vere.

## Errori comuni

- Confondere “definitivamente” con “per qualche indice grande”.
- Scegliere $N$ ma non verificare tutti gli $n\geq N$.
- Pensare che la proprietà debba valere fin dal primo termine.
- Invertire l'ordine dei quantificatori $\exists N$ e $\forall n\geq N$.

## Connessioni

- Formalizza il comportamento delle code di [[70 Grafico e Limitatezza delle Successioni|una successione]].
- È il linguaggio centrale di [[72 Limite Finito di una Successione|limiti finiti]] e [[74 Limiti Infiniti e Regolarità delle Successioni|limiti infiniti]].

## Prospettiva d'esame

Quando si usa una proprietà definitivamente vera, bisogna esibire o giustificare l'esistenza della soglia $N$ e mantenere il corretto ordine dei quantificatori.
