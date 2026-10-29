---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D1
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 1"
  - "20 Dimostrazione per Assurdo"
cssclasses:
  - formulario
---

# D1 — Irrazionalità della Radice di Due

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D1** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Il numero reale $\sqrt2$ è irrazionale:

$$
\sqrt2\notin\mathbb Q.
$$

## Idea della dimostrazione

Supponiamo di poter scrivere la radice come una frazione ridotta ai minimi termini. L’uguaglianza obbliga numeratore e denominatore a essere entrambi pari.

## Dimostrazione

Supponiamo per assurdo che $\sqrt2\in\mathbb Q$. Possiamo allora scrivere

$$
\sqrt2=\frac mn,
\qquad m,n\in\mathbb Z,\quad n\neq0,\quad\gcd(m,n)=1.
$$

Elevando al quadrato e moltiplicando per $n^2$ otteniamo

$$
m^2=2n^2.
$$

Quindi $m^2$ è pari e anche $m$ è pari. Infatti, se $m$ fosse dispari, $m=2k+1$ darebbe $m^2=2(2k^2+2k)+1$, che è dispari.

Scriviamo dunque $m=2k$ e sostituiamo:

$$
4k^2=2n^2
\quad\Longrightarrow\quad n^2=2k^2.
$$

Anche $n^2$, e quindi $n$, è pari. Allora $m$ e $n$ hanno il divisore comune $2$: contraddizione con $\gcd(m,n)=1$.

La supposizione iniziale è falsa, quindi $\sqrt2\notin\mathbb Q$.

## Da ricordare

La contraddizione usa il fatto che la frazione è stata scelta **ridotta ai minimi termini**. Senza questa scelta, trovare due interi pari non basterebbe.

## Note di riferimento

[[20 Dimostrazione per Assurdo]]
