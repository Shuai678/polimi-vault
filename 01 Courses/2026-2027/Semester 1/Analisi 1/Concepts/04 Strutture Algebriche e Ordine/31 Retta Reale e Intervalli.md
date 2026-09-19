---
course: Analisi 1
type: concept
status: da-verificare
source:
  - Lezione 02, PDF pp. 19-24
  - Libro, cap. 1.1.4-1.1.5
---

# Retta reale e intervalli

## Intuizione

I numeri reali possono essere rappresentati come punti di una retta orientata. Il valore assoluto misura la distanza dall'origine e gli intervalli descrivono porzioni consecutive della retta.

## Definizione formale

Fissati $a,b\in\mathbb{R}$ con $a<b$:

$$
(a,b)=\{x\in\mathbb{R}:a<x<b\},
$$

$$
[a,b]=\{x\in\mathbb{R}:a\leq x\leq b\},
$$

$$
(a,b]=\{x\in\mathbb{R}:a<x\leq b\},
$$

$$
[a,b)=\{x\in\mathbb{R}:a\leq x<b\}.
$$

Gli intervalli illimitati principali sono

$$
(-\infty,b),\quad(-\infty,b],\quad(a,+\infty),\quad[a,+\infty).
$$

Inoltre,

$$
\mathbb{R}=(-\infty,+\infty).
$$

### Da dire all'orale

> Un intervallo è un sottoinsieme della retta reale che contiene, insieme a due suoi punti, tutti i punti compresi tra essi. Le parentesi quadre includono l'estremo, mentre le parentesi tonde lo escludono.

## Notazione

- Una parentesi quadra indica che l'estremo appartiene all'intervallo.
- Una parentesi tonda indica che l'estremo è escluso.
- I simboli $+\infty$ e $-\infty$ non sono numeri reali e sono sempre accompagnati da parentesi tonde.
- La distanza tra i punti associati ad $a$ e $b$ è $|a-b|$.

## Condizioni

Per gli intervalli limitati scritti con estremi distinti si assume $a<b$.

Gli estremi infiniti non possono essere massimo o minimo e non appartengono mai all'intervallo.

## Estremi, massimo e minimo

| Intervallo | Estremo inferiore | Minimo | Estremo superiore | Massimo |
|---|---:|---:|---:|---:|
| $(a,b)$ | $a$ | non esiste | $b$ | non esiste |
| $[a,b]$ | $a$ | $a$ | $b$ | $b$ |
| $(a,b]$ | $a$ | non esiste | $b$ | $b$ |
| $[a,b)$ | $a$ | $a$ | $b$ | non esiste |

Per gli intervalli illimitati:

- $(-\infty,b)$ ha estremo superiore $b$ ma non massimo;
- $(-\infty,b]$ ha estremo superiore e massimo uguali a $b$;
- $(a,+\infty)$ ha estremo inferiore $a$ ma non minimo;
- $[a,+\infty)$ ha estremo inferiore e minimo uguali ad $a$.

## Esempi

Per

$$
E=[-1,2)
$$

si ha

$$
\inf E=\min E=-1,
\qquad
\sup E=2,
$$

mentre il massimo non esiste.

La condizione $x\geq3$ si rappresenta mediante

$$
[3,+\infty).
$$

## Errori comuni

- Usare una parentesi quadra accanto a $+\infty$ o $-\infty$.
- Confondere parentesi tonde e quadre.
- Affermare che un intervallo aperto non possiede estremo superiore o inferiore.
- Confondere estremo superiore con massimo.
- Credere che “aperto” significhi necessariamente “illimitato”.

## Connessioni

- [[29 Valore Assoluto|Il valore assoluto]] fornisce la distanza sulla retta reale.
- [[25 Massimo e Minimo|Massimo e minimo]] dipendono dall'inclusione degli estremi.
- [[26 Estremo Superiore e Inferiore|Estremo superiore e inferiore]] dipendono dalla posizione delle barriere, non dalla loro appartenenza.
- Il punto della retta associato a $\sqrt2$ mostra geometricamente perché $\mathbb{Q}$ non esaurisce la retta reale.

## Prospettiva d'esame

Nel passaggio da una disuguaglianza a un intervallo bisogna controllare separatamente ciascun estremo e stabilire se sia incluso. Per ogni intervallo conviene saper riconoscere immediatamente limitatezza, estremi, massimo e minimo.
