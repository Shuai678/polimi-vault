---
course: Analisi 1
type: formula-sheet
exam: Prima prova in itinere
status: Da studiare
updated: 2026-10-30
source:
  - "[[D05 Unicità del Limite]]"
  - "[[D06 Limitatezza delle Successioni Convergenti]]"
  - "[[D07 Teorema di Permanenza del Segno]]"
  - "[[D08 Teorema dei Due Carabinieri]]"
  - "[[D09 Regolarità delle Successioni Monotone]]"
  - "[[D12 Teorema del Confronto Asintotico per le Serie]]"
  - "[[D13 Criterio del Rapporto per le Serie Numeriche]]"
  - "[[80 Algebra dei Limiti di Successioni]]"
  - "[[84 Confronto in Modulo e Prodotto con un Infinitesimo]]"
cssclasses:
  - formulario
---

# Scelta di epsilon nelle dimostrazioni

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

Riepilogo dei valori di $\varepsilon$ e del motivo per cui funzionano nelle dimostrazioni sui limiti e sulle serie. $\varepsilon$ è sempre un numero reale positivo: rappresenta una tolleranza, cioè il raggio dell'intorno

$$
(\ell-\varepsilon,\ell+\varepsilon).
$$

## Quando possiamo scegliere epsilon

- **Se usiamo un limite già noto**, la definizione vale per ogni tolleranza positiva. Possiamo quindi applicarla a un valore comodo, come $1$ oppure $|\ell|/2$.
- **Se dobbiamo dimostrare un limite**, dobbiamo partire da un $\varepsilon>0$ arbitrario e ottenere un errore minore di $\varepsilon$. Verificare soltanto il caso $\varepsilon=1$ non basta.

La scelta di $\varepsilon$ precede quella dell'indice $N$: è $N$ che può dipendere dalla precisione richiesta.

## Scelte nelle dimostrazioni del formulario

| Dimostrazione e caso | Scelta di $\varepsilon$ | Scopo della scelta |
| --- | --- | --- |
| [[D05 Unicità del Limite\|D5 — Unicità]], due limiti finiti con $\ell_1>\ell_2$ | $\displaystyle\varepsilon=\frac{\ell_1-\ell_2}{3}$ | Ottenere intorni disgiunti: $2\varepsilon<\ell_1-\ell_2$, quindi $\ell_2+\varepsilon<\ell_1-\varepsilon$. |
| [[D06 Limitatezza delle Successioni Convergenti\|D6 — Limitatezza]] | $\varepsilon=1$ | Racchiudere la coda nella fascia fissa $\ell-1<a_n<\ell+1$. Poi si controllano anche i primi termini, che sono in numero finito. |
| [[D07 Teorema di Permanenza del Segno\|D7 — Permanenza del segno]], limite finito $\ell\neq0$ | $\displaystyle\varepsilon=\frac{\lvert\ell\rvert}{2}$ | Scegliere un intorno che non attraversi lo zero. Se $\ell>0$, si ottiene $a_n>\ell/2>0$; se $\ell<0$, si ottiene $a_n<\ell/2<0$. |
| [[D08 Teorema dei Due Carabinieri\|D8 — Due carabinieri]], limite finito | **Qualunque** $\varepsilon>0$ | Le due successioni esterne stanno definitivamente nella fascia $(\ell-\varepsilon,\ell+\varepsilon)$; anche quella intermedia deve starci. |
| [[D09 Regolarità delle Successioni Monotone\|D9 — Successioni monotone]], limite finito | **Qualunque** $\varepsilon>0$ | Nel caso crescente, il supremo trova un termine sopra $\ell-\varepsilon$ e la monotonia mantiene i successivi sopra quella soglia. Nel caso decrescente si ragiona con l'infimo e $\ell+\varepsilon$. |
| [[D12 Teorema del Confronto Asintotico per le Serie\|D12 — Confronto asintotico]], $a_n/b_n\to1$ | $\displaystyle\varepsilon=\frac12$ | Ottenere $\frac12<\frac{a_n}{b_n}<\frac32$ e quindi, per $b_n>0$, $\frac12b_n<a_n<\frac32b_n$. |
| [[D13 Criterio del Rapporto per le Serie Numeriche\|D13 — Rapporto]], $0\leq\ell<1$ | $\displaystyle\varepsilon=\frac{1-\ell}{2}$ | Tenere il rapporto sotto $q=\ell+\varepsilon=\frac{1+\ell}{2}<1$, per confrontare con una geometrica convergente. |
| [[D13 Criterio del Rapporto per le Serie Numeriche\|D13 — Rapporto]], $1<\ell<+\infty$ | $\displaystyle\varepsilon=\frac{\ell-1}{2}$ | Tenere il rapporto sopra $q=\ell-\varepsilon=\frac{1+\ell}{2}>1$, per confrontare con una geometrica divergente. |

In D13, $\ell$ è il limite del rapporto $a_{n+1}/a_n$. Per $\ell=1$ queste scelte darebbero $\varepsilon=0$, che non è ammesso: il criterio non decide.

## Perché proprio un terzo o una metà

In [[73 Unicità del Limite di Successione|unicità del limite]], poniamo $d=\ell_1-\ell_2>0$. Ogni intorno ha raggio $d/3$, quindi i due raggi insieme occupano $2d/3<d$: resta uno spazio fra gli intorni. Per esempio, se i presunti limiti fossero $2$ e $5$, sceglieremmo $\varepsilon=1$, ottenendo gli intervalli disgiunti $(1,3)$ e $(4,6)$.

Il $3$ è una scelta comoda: qualsiasi $0<\varepsilon<d/2$ garantisce uno spazio fra i due intorni; anche $d/4$ funzionerebbe.

Nella permanenza del segno, invece, la distanza del limite dallo zero è $|\ell|$. Scegliendone la metà, l'intorno resta dalla stessa parte dello zero. Per esempio:

- Se $\ell=4$, scegliamo $\varepsilon=2$ e otteniamo definitivamente $2<a_n<6$.
- Se $\ell=-4$, scegliamo ancora $\varepsilon=2$ e otteniamo definitivamente $-6<a_n<-2$.

Anche il valore $1$ scelto per la limitatezza non è obbligatorio: basta una qualsiasi tolleranza positiva fissata.

## Precisioni intermedie nelle altre dimostrazioni

Qui la precisione finale $\varepsilon>0$ resta arbitraria. Scegliamo tolleranze più piccole per compensare somme o coefficienti.

| Risultato | Precisione intermedia | Perché funziona |
| --- | --- | --- |
| [[80 Algebra dei Limiti di Successioni\|Somma e differenza]] | $\varepsilon/2$ per ciascuna successione | La disuguaglianza triangolare somma i due errori: $\varepsilon/2+\varepsilon/2=\varepsilon$. |
| [[80 Algebra dei Limiti di Successioni\|Prodotto]], con $a_n\to a$, $b_n\to b$ e $\lvert a_n\rvert\leq M$, $M>0$ | $\displaystyle\delta=\frac{\varepsilon}{M+\lvert b\rvert}$ per entrambi gli errori | La stima è $\lvert a_nb_n-ab\rvert\leq M\lvert b_n-b\rvert+\lvert b\rvert\,\lvert a_n-a\rvert<(M+\lvert b\rvert)\delta=\varepsilon$. |
| [[84 Confronto in Modulo e Prodotto con un Infinitesimo\|Limitata per infinitesima]], con $\lvert c_n\rvert\leq K$, $K>0$, e $b_n\to0$ | $\varepsilon/K$ per l'errore $\lvert b_n\rvert$ | Si ottiene $\lvert c_nb_n\rvert\leq K\lvert b_n\rvert<K(\varepsilon/K)=\varepsilon$. |

Anche nella verifica di $1/n\to0$, in [[72 Limite Finito di una Successione]], $\varepsilon>0$ è arbitrario: scegliamo un intero $N>1/\varepsilon$, così per ogni $n\geq N$ vale $1/n<\varepsilon$.

## Casi con limiti infiniti

Per un limite infinito usiamo soglie $M$, anziché intorni di raggio $\varepsilon$ attorno a un numero reale:

- In [[D07 Teorema di Permanenza del Segno|D7]], scegliamo la soglia $1$: definitivamente $a_n>1$ nel caso $+\infty$, oppure $a_n<-1$ nel caso $-\infty$.
- In [[D13 Criterio del Rapporto per le Serie Numeriche|D13]], se il rapporto tende a $+\infty$, scegliamo $M=2$ per ottenere definitivamente $a_{n+1}/a_n>2>1$.
- In [[D05 Unicità del Limite|D5]], per escludere contemporaneamente un limite finito $\ell$ e $+\infty$, usiamo $\varepsilon=1$ sul limite finito, ottenendo $a_n<\ell+1$, e una soglia $M>\max\{0,\ell+1\}$ sul limite infinito, ottenendo $a_n>M>\ell+1$. Le due condizioni sono incompatibili. Per $-\infty$ si ragiona analogamente con il limite inferiore $\ell-1$.

> [!tip] Come ricordare la scelta
> Parti dalla disuguaglianza che vuoi ottenere: intorni separati, termini dello stesso segno del limite, rapporto sopra o sotto $1$, oppure errore finale minore di $\varepsilon$. Il valore scelto deve garantire proprio quella condizione.
