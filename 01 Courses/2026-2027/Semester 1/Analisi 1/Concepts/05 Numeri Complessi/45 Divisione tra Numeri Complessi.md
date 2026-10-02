---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF p. 12
  - Libro, §1.8, pp. 18-19
---

# Divisione tra numeri complessi

## Intuizione

Per eliminare un numero complesso dal denominatore si moltiplicano numeratore e denominatore per il coniugato del denominatore. Il denominatore diventa così il numero reale $|w|^2$.

## Definizione formale

Per $z,w\in\mathbb C$ con $w\neq0$,

$$
\frac zw
=\frac zw\frac{\overline w}{\overline w}
=\frac{z\overline w}{w\overline w}
=\frac{z\overline w}{|w|^2}.
$$

### Da dire all'orale

> Per dividere $z$ per un complesso non nullo $w$, moltiplico numeratore e denominatore per $\overline w$ e ottengo $z/w=z\overline w/|w|^2$.

## Condizioni

È necessario che $w\neq0$. In tal caso $|w|^2>0$, quindi il denominatore reale ottenuto è diverso da zero.

## Metodo

1. Individuare il denominatore $w$.
2. Calcolare il coniugato $\overline w$.
3. Moltiplicare numeratore e denominatore per $\overline w$.
4. Usare $w\overline w=|w|^2$.
5. Sviluppare e separare parte reale e parte immaginaria.

## Esempio della lezione

Siano

$$
z=3-2i,
\qquad
w=1+7i.
$$

Allora

$$
\frac zw
=\frac{(3-2i)(1-7i)}{1^2+7^2}.
$$

Il numeratore è

$$
(3-2i)(1-7i)
=3-21i-2i+14i^2
=-11-23i.
$$

Pertanto

$$
\frac{3-2i}{1+7i}
=-\frac{11}{50}-\frac{23}{50}i.
$$

## Errori comuni

- Usare il coniugato del numeratore invece di quello del denominatore.
- Moltiplicare soltanto il denominatore per il coniugato.
- Dimenticare che $i^2=-1$.
- Omettere la condizione $w\neq0$.

## Connessioni

- Usa le [[44 Proprietà del Coniugato|proprietà del coniugato]].
- È la versione operativa dell'[[39 Campo Complesso e Inverso Moltiplicativo|inverso moltiplicativo]] in $\mathbb C$.

## Prospettiva d'esame

Potenziale rilevanza d'esame: eseguire divisioni in forma algebrica e giustificare ogni passaggio tramite il coniugato.
