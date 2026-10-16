---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 0, PDF pp. 9-10"
---

# Relazioni di equivalenza

Stato: **da studiare**.

## Intuizione e definizione

Una relazione di equivalenza esprime quando due elementi possono essere considerati uguali rispetto a una caratteristica scelta.

Una [[02 Relazioni Binarie|relazione]] $R\subseteq A\times A$ è di **equivalenza** se soddisfa tutte e tre le proprietà:

$$
\begin{aligned}
&\forall a\in A,\quad aRa &&\text{riflessività},\\
&\forall a,b\in A,\quad aRb\implies bRa &&\text{simmetria},\\
&\forall a,b,c\in A,\quad
(aRb\ \text{e}\ bRc)\implies aRc &&\text{transitività}.
\end{aligned}
$$

Le formule descrivono tre condizioni diverse: ciascuna deve essere verificata.

## Esempio del professore con dimostrazione esplicitata

Su un insieme di persone, consideriamo la relazione «avere la maglia dello stesso colore», assumendo assegnato un unico colore a ciascuna maglia.

Indichiamo con $c(a)$ il colore della maglia di $a$. Allora:

$$
aRb\iff c(a)=c(b).
$$

1. **Riflessività:** $c(a)=c(a)$; quindi $aRa$.
2. **Simmetria:** se $c(a)=c(b)$, allora $c(b)=c(a)$; quindi $aRb\implies bRa$.
3. **Transitività:** se $c(a)=c(b)$ e $c(b)=c(c)$, allora $c(a)=c(c)$; quindi $aRb$ e $bRc$ implicano $aRc$.

La relazione identifica persone rispetto al colore della maglia, senza affermare che siano la stessa persona.

## Controesempio del tutor

La relazione $\leq$ su $\mathbb R$ è riflessiva e transitiva, ma non simmetrica:

$$
1\leq2,\qquad 2\not\leq1.
$$

Non è quindi una relazione di equivalenza. Una sola proprietà mancante è sufficiente per escludere l'equivalenza.

## Come riconoscerla

Si scrive anzitutto la condizione che definisce $aRb$. Si dimostrano poi separatamente le tre proprietà per elementi arbitrari di $A$. Un esempio favorevole non dimostra una proprietà universale.

## Da dire all'orale

> Una relazione di equivalenza su un insieme è una relazione binaria riflessiva, simmetrica e transitiva.

## Collegamenti e fonte

- Prerequisito: [[02 Relazioni Binarie]].
- Confronto: [[04 Relazioni di Ordine]], dove si richiede antisimmetria al posto della simmetria.
- Esempio numerico svolto: [[01 Prodotti Cartesiani e Relazioni]].
- Fonte: [[GAL 2026-2027 - 20260916 - LEZIONE 0.pdf#page=9|Lezione 0, pp. 9-10]]. I passaggi simbolici della dimostrazione sono esplicitati dal tutor.
