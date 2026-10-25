---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 04, PDF pp. 22-23
  - Libro, §3.1, p. 75
---

# Successioni di numeri reali

## Perché si introducono

Una successione è una funzione i cui ingressi sono indici naturali. Serve a descrivere una lista ordinata di numeri reali e sarà l'oggetto su cui verranno introdotti i primi limiti del corso.

L'ordine dei termini è essenziale: lo stesso insieme di valori disposto in un ordine diverso può definire una successione diversa.

## Intuizione

Una successione assegna un numero reale a ciascun indice naturale ammesso:

$$
n\longmapsto a_n.
$$

L'indice $n$ indica la posizione del termine, mentre $a_n$ è il valore che occupa quella posizione.

## Definizione formale

Una **successione di numeri reali** è una funzione

$$
a:A\to\mathbb{R},
$$

dove il dominio è un sottoinsieme dei naturali della forma

$$
A=\{n\in\mathbb{N}:n\geq n_0\}
$$

per un opportuno $n_0\in\mathbb{N}$.

Quando la successione è definita su tutti i naturali si scrive semplicemente

$$
a:\mathbb{N}\to\mathbb{R}.
$$

### Da dire all'orale

> Una successione di numeri reali è una funzione definita sui naturali, o su una loro coda $\{n\in\mathbb{N}:n\geq n_0\}$, e a valori reali.

## Notazione

Al posto di $a(n)$ si usa normalmente la scrittura

$$
a_n.
$$

La successione può essere indicata con

$$
(a_n)_{n\geq n_0}
$$

oppure, secondo la notazione adottata negli appunti della lezione, con

$$
\{a_n\}_{n\geq n_0}.
$$

Il pedice specifica quali indici sono ammessi. Se il punto iniziale è già chiaro dal contesto, si scrive spesso soltanto $(a_n)$ o $a_n$.

> [!info] Approfondimento dal libro
> La notazione della successione e l'insieme dei suoi valori non vanno confusi. Una successione conserva l'associazione tra indice e valore; l'immagine $\operatorname{Im}a$ registra invece soltanto quali valori vengono assunti.

## Esempi della lezione

### La successione reciproca

$$
a_n=\frac1n,
\qquad
n\geq1.
$$

I primi termini sono

$$
a_1=1,
\quad
a_2=\frac12,
\quad
a_3=\frac13,
\quad
a_4=\frac14,
\ldots
$$

Il dominio parte da $1$ perché la formula non è definita per $n=0$.

### Una successione con denominatore traslato

$$
b_n=\frac1{(n-42)^2},
\qquad
n\geq43.
$$

Il punto iniziale $43$ garantisce che $n-42\neq0$. In realtà la formula sarebbe definita anche per molti indici precedenti, ma la successione dichiarata nella lezione ha precisamente dominio

$$
\{n\in\mathbb{N}:n\geq43\}.
$$

I primi termini sono

$$
b_{43}=1,
\quad
b_{44}=\frac14,
\quad
b_{45}=\frac19,
\ldots
$$

### Una successione logaritmica

$$
c_n=\log(n-5),
\qquad
n\geq6.
$$

La condizione $n\geq6$ assicura

$$
n-5\geq1>0,
$$

quindi l'argomento del logaritmo è positivo. I primi termini sono

$$
c_6=\log1=0,
\qquad
c_7=\log2,
\qquad
c_8=\log3.
$$

## Come si legge e si controlla una successione

Data una formula per $a_n$:

1. identificare gli indici naturali ammessi;
2. controllare denominatori, radici e logaritmi;
3. determinare il primo indice $n_0$ dichiarato;
4. calcolare alcuni termini sostituendo gli indici;
5. non trattare $n$ come una variabile reale: l'indice assume soltanto valori naturali del dominio.

## Immagine di una successione

Poiché una successione è una funzione, la sua immagine è

$$
\operatorname{Im}a
=\{a_n:n\in A\}
\subseteq\mathbb{R}.
$$

Per esempio, per $a_n=1/n$ con $n\geq1$,

$$
\operatorname{Im}a
=\left\{1,\frac12,\frac13,\ldots\right\}.
$$

L'indice appartiene al dominio; il termine appartiene al codominio:

$$
n\in A,
\qquad
a_n\in\mathbb{R}.
$$

## Errori comuni

- Confondere l'indice $n$ con il valore $a_n$.
- Dimenticare che $n$ è naturale e trattarlo come una variabile reale continua.
- Usare una formula senza controllare da quale indice è definita.
- Scrivere $a_0=1/0$ per la successione $a_n=1/n$ invece di far partire il dominio da $1$.
- Confondere la successione ordinata con il solo insieme dei valori che assume.
- Omettere il pedice iniziale quando esso è necessario per capire il dominio.

## Connessioni

- È un caso particolare di [[55 Funzioni Dominio Codominio e Immagine|funzione]].
- Usa [[01 Numeri Naturali|numeri naturali]] come indici.
- L'esempio logaritmico richiede le condizioni di [[36 Logaritmi|esistenza del logaritmo]].
- Prepara lo studio dei limiti di successioni.

## Prospettiva d'esame

Potenziale rilevanza d'esame: riconoscere una successione come funzione, dichiararne correttamente il dominio, tradurre tra $a(n)$ e $a_n$ e controllare da quale indice una formula è ben definita.
