---
course: Analisi 1
type: concept
status: studied
source: Lezione 01, PDF p. 13
---
# Condizioni necessarie e sufficienti

## Intuizione

Una condizione sufficiente garantisce il risultato; una condizione necessaria deve invece essere presente ogni volta che il risultato si verifica.

## Definizione formale

Se $P\Rightarrow Q$, $P$ è sufficiente per $Q$ e $Q$ è necessaria per $P$.

Se vale anche $Q\Rightarrow P$, allora $P$ e $Q$ sono necessarie e sufficienti l'una per l'altra.

### Da dire all'orale

> Se $P\Rightarrow Q$, $P$ è sufficiente per $Q$ e $Q$ è necessaria per $P$; se valgono entrambe le implicazioni, le due condizioni sono necessarie e sufficienti.

## Esempi

### Esempio svolto: condizione sufficiente ma non necessaria

Siano

$$
P:\ \text{il triangolo è equilatero},
$$

$$
Q:\ \text{il triangolo è isoscele}.
$$

Un triangolo equilatero possiede tre lati uguali e quindi, in particolare, almeno due lati uguali. Pertanto $P\Rightarrow Q$.

Ne segue che:

- essere equilatero è una condizione sufficiente per essere isoscele;
- essere isoscele è una condizione necessaria per essere equilatero.

Il contrario non vale: un triangolo con lati $2$, $2$ e $3$ è isoscele ma non equilatero. Quindi essere equilatero non è una condizione necessaria per essere isoscele.

### Esempio svolto: condizione necessaria e sufficiente

Per un intero $n$, consideriamo:

$$
P:\ n\text{ è pari},
\qquad
Q:\ n+1\text{ è dispari}.
$$

Se $n$ è pari, esiste $k\in\mathbb Z$ tale che $n=2k$; allora

$$
n+1=2k+1,
$$

quindi $n+1$ è dispari.

Viceversa, se $n+1$ è dispari, esiste $k\in\mathbb Z$ tale che

$$
n+1=2k+1.
$$

Sottraendo $1$ da entrambi i membri otteniamo $n=2k$, quindi $n$ è pari. Valgono entrambe le implicazioni e le due condizioni sono necessarie e sufficienti.

## Errori comuni

- Invertire “necessaria” e “sufficiente”.
- Deducendo $P\Rightarrow Q$, affermare senza prova anche $Q\Rightarrow P$.

## Connessioni

La doppia implicazione $P\Leftrightarrow Q$ esprime che ciascuna delle due condizioni è contemporaneamente necessaria e sufficiente per l'altra.
