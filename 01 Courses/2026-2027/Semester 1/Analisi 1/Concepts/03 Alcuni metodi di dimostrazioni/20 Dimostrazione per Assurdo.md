---
course: Analisi 1
type: method
status: studied
source:
  - Lezione 01, PDF pp. 18-19
  - Libro, cap. 1.1.5, p. 6
---

# Dimostrazione per assurdo

## Intuizione

Per dimostrare una tesi si assume temporaneamente che essa sia falsa. Se questa supposizione conduce a una contraddizione, la negazione della tesi non può essere vera e quindi la tesi è vera.

## Metodo

Per dimostrare una tesi $Q$ per assurdo:

1. si assume vera la negazione $\neg Q$;
2. si deducono conseguenze usando le ipotesi e risultati già noti;
3. si ottiene una contraddizione, cioè una proposizione $S$ insieme alla sua negazione $\neg S$;
4. si conclude che $\neg Q$ è falsa e quindi che $Q$ è vera.

Per dimostrare un'implicazione $P\Rightarrow Q$, si assumono contemporaneamente $P$ e $\neg Q$ e si cerca una contraddizione.

### Da dire all'orale

> In una dimostrazione per assurdo assumo vera la negazione della tesi e mostro che questa supposizione conduce a una contraddizione. Concludo quindi che la negazione della tesi è falsa e che la tesi è vera.

## Condizioni

- La negazione della tesi deve essere formulata correttamente.
- La contraddizione deve derivare dalla supposizione introdotta e dalle altre ipotesi.
- Bisogna indicare esplicitamente quali due affermazioni incompatibili sono state ottenute.

## Esempio

Vogliamo dimostrare che non esiste un massimo numero naturale. Supponiamo per assurdo che esista $M\in\mathbb N$ maggiore o uguale a ogni naturale. Allora $M+1\in\mathbb N$ e $M+1>M$, in contraddizione con la scelta di $M$ come massimo. Pertanto un massimo naturale non esiste.

## Errori comuni

- Assumere la tesi invece della sua negazione.
- Ottenere una contraddizione senza precisare quali affermazioni siano incompatibili.
- Concludere che il teorema è falso: è falsa la supposizione introdotta per assurdo.

## Connessioni

- Nella dimostrazione dell'irrazionalità di $\sqrt{2}$ si suppone che $\sqrt{2}$ sia razionale e si conclude che numeratore e denominatore di una frazione ridotta sono entrambi pari.
- La dimostrazione per assurdo usa la negazione logica e il principio di non contraddizione.

## Prospettiva d'esame

All'orale conviene dichiarare subito la supposizione per assurdo, indicare il punto preciso in cui nasce la contraddizione e spiegare perché essa rende falsa la supposizione iniziale.
