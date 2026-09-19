---
course: Analisi 1
type: concept
status: da-verificare
source:
  - Lezione 02, PDF pp. 26-27
  - Libro, cap. 1.4
---

# Potenze con esponente razionale

## Intuizione

Le radici permettono di estendere la potenza dagli esponenti interi agli esponenti razionali. Il denominatore dell'esponente indica una radice, mentre il numeratore indica una potenza.

## Definizione formale

Sia $a>0$. Per $m\in\mathbb{N}$ si pone

$$
a^0=1,
\qquad
a^m=\underbrace{a\cdot a\cdots a}_{m\text{ volte}}.
$$

Per $n\in\mathbb{N}$, $n\neq0$,

$$
a^{1/n}=\sqrt[n]{a}.
$$

Per $m,n\in\mathbb{N}$, $n\neq0$,

$$
a^{m/n}=\sqrt[n]{a^m}=\left(\sqrt[n]{a}\right)^m.
$$

Per un esponente razionale negativo,

$$
a^{-m/n}=\frac1{a^{m/n}}.
$$

### Da dire all'orale

> Per $a>0$ e $r=\frac mn\in\mathbb{Q}$ con $n>0$, si definisce $a^r$ come la radice $n$-esima di $a^m$; per un esponente negativo si prende il reciproco della corrispondente potenza positiva.

## Notazione

- $a$ è la base positiva.
- $m$ è il numeratore dell'esponente.
- $n$ è il denominatore positivo e indica l'indice della radice.
- Il segno negativo dell'esponente richiede il reciproco.

## Condizioni

- La definizione generale richiede $a>0$.
- Il denominatore dell'esponente deve essere non nullo.
- Per basi negative alcune radici non esistono in $\mathbb{R}$; per $a=0$ gli esponenti negativi richiederebbero una divisione per zero.

## Metodo / Dimostrazione

### Buona definizione

Uno stesso razionale possiede rappresentazioni frazionarie diverse. Supponiamo

$$
\frac mn=\frac pq,
$$

quindi $mq=pn$. Poniamo

$$
u=a^{m/n},
\qquad
v=a^{p/q}.
$$

Allora

$$
u^{nq}=a^{mq},
\qquad
v^{nq}=a^{pn}.
$$

Poiché $mq=pn$, si ha $u^{nq}=v^{nq}$. Essendo $u,v>0$, l'unicità della radice positiva implica $u=v$. La definizione dipende quindi dal numero razionale e non dalla frazione scelta.

## Proprietà

Per $a,b>0$ e $r,s\in\mathbb{Q}$:

$$
a^r a^s=a^{r+s},
$$

$$
\frac{a^r}{a^s}=a^{r-s},
$$

$$
(a^r)^s=a^{rs},
$$

$$
(ab)^r=a^r b^r.
$$

## Esempi

$$
8^{2/3}=\left(\sqrt[3]{8}\right)^2=2^2=4.
$$

$$
16^{-3/4}=\frac1{16^{3/4}}=\frac1{(\sqrt[4]{16})^3}=\frac18.
$$

## Errori comuni

- Interpretare $a^{m/n}$ come $a^m/a^n$.
- Dimenticare il reciproco con un esponente negativo.
- Usare una base negativa senza controllare l'esistenza della radice reale.
- Credere che frazioni equivalenti producano valori diversi.

## Connessioni

- [[33 Radice Ennesima Reale|La radice ennesima]] definisce gli esponenti reciproci.
- La densità di $\mathbb{Q}$ permetterà di approssimare ogni esponente reale con esponenti razionali.

## Prospettiva d'esame

Nel calcolo di $a^{m/n}$ conviene leggere prima il denominatore come indice della radice e poi il numeratore come potenza, controllando sempre il segno dell'esponente e le condizioni sulla base.
