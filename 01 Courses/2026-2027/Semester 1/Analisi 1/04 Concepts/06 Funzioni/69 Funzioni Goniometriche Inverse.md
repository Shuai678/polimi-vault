---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF pp. 5-8
  - Libro, §2.4.9, pp. 63-64
---

# Funzioni goniometriche inverse

Le funzioni goniometriche sono periodiche e quindi non sono iniettive sui loro domini naturali. Per definirne le inverse si scelgono intervalli sui quali siano strettamente monotone e assumano tutti i valori desiderati.

![[69 Funzioni Goniometriche Inverse.svg|690]]

## Arcotangente

La tangente ristretta a

$$
\left(-\frac\pi2,\frac\pi2\right)
$$

è strettamente crescente e ha immagine $\mathbb R$. La sua inversa è

$$
\arctan:\mathbb R\to
\left(-\frac\pi2,\frac\pi2\right).
$$

Per ogni $y\in\mathbb R$, tutte le soluzioni di $\tan x=y$ sono

$$
x=\arctan y+k\pi,
\qquad k\in\mathbb Z.
$$

## Arcoseno

Il seno ristretto a $[-\pi/2,\pi/2]$ è strettamente crescente e ha immagine $[-1,1]$. La sua inversa è

$$
\arcsin:[-1,1]\to
\left[-\frac\pi2,\frac\pi2\right].
$$

Per $y\in[-1,1]$, tutte le soluzioni di $\sin x=y$ sono date dalle due famiglie

$$
x=\arcsin y+2k\pi
$$

oppure

$$
x=\pi-\arcsin y+2k\pi,
\qquad k\in\mathbb Z.
$$

Per $y=\pm1$ le due famiglie coincidono.

## Arcocoseno

Il coseno ristretto a $[0,\pi]$ è strettamente decrescente e ha immagine $[-1,1]$. La sua inversa è

$$
\arccos:[-1,1]\to[0,\pi].
$$

Per $y\in[-1,1]$, tutte le soluzioni di $\cos x=y$ sono

$$
x=\arccos y+2k\pi
$$

oppure

$$
x=-\arccos y+2k\pi,
\qquad k\in\mathbb Z.
$$

Anche qui, per $y=\pm1$ le due famiglie coincidono.

## Valore principale e tutte le soluzioni

$\arcsin y$, $\arccos y$ e $\arctan y$ restituiscono un unico **valore principale**, scelto nell'intervallo di invertibilità. Le equazioni goniometriche sull'intera retta richiedono poi di recuperare tutte le soluzioni usando periodicità e simmetrie.

### Da dire all'orale

> Le inverse goniometriche non invertono seno, coseno e tangente su tutto il loro dominio: invertono opportune restrizioni iniettive. I loro codomini sono precisamente gli intervalli scelti per tali restrizioni.

## Errori comuni

- Scrivere $\arcsin:\mathbb R\to\mathbb R$ o $\arccos:\mathbb R\to\mathbb R$.
- Dimenticare che $\arctan y$ è sempre compreso tra $-\pi/2$ e $\pi/2$.
- Usare una sola famiglia di soluzioni per seno o coseno.
- Confondere $\sin^{-1}x$ con $1/\sin x$.
- Dimenticare che la restrizione del coseno è decrescente, non crescente.

## Connessioni

- Sono applicazioni di [[66 Funzione Inversa|funzione inversa]] tramite una restrizione iniettiva.
- La monotonia delle restrizioni usa [[62 Funzioni Monotone|funzioni monotone]].
- Le famiglie di soluzioni dipendono dalla [[63 Funzioni Periodiche|periodicità]].

## Prospettiva d'esame

Per definire correttamente una funzione goniometrica inversa bisogna dichiarare dominio, codominio e restrizione invertita. Per risolvere un'equazione, il valore principale da solo non basta: occorre scrivere tutte le famiglie di soluzioni.
