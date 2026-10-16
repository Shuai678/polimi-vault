---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 1, PDF pp. 2-3, pagine stampate 12-13"
---

# Relazioni di ordine

Stato: **da studiare**.

## L'esempio dell'inclusione

La Lezione 1 riprende le relazioni attraverso l'inclusione tra insiemi:

$$
A\subseteq B
\iff
\forall x\in A,\ x\in B.
$$

L'inclusione non è simmetrica in generale. Per esempio:

$$
\{1\}\subseteq\{1,2\},\qquad
\{1,2\}\not\subseteq\{1\}.
$$

Per formulare l'esempio rigorosamente, fissiamo un insieme universo $U$ e consideriamo i suoi sottoinsiemi, raccolti nell'insieme delle parti $\mathcal P(U)$. Questa precisazione del tutor evita di usare «l'insieme di tutti gli insiemi», espressione informale presente nel PDF.

## Antisimmetria

Una relazione $R$ su $S$ è **antisimmetrica** se

$$
\forall a,b\in S,\qquad
(aRb\ \text{e}\ bRa)\implies a=b.
$$

Due elementi distinti non possono essere collegati in entrambi i versi. I collegamenti di un elemento con se stesso sono consentiti.

L'antisimmetria non è la negazione della simmetria. L'uguaglianza è, per esempio, sia simmetrica sia antisimmetrica.

## Definizione

Una relazione su $S$ è una **relazione d'ordine** se è riflessiva, antisimmetrica e transitiva.

Qui «ordine» indica un ordine non stretto; non si sostituisce la riflessività con la condizione $a<a$.

## Dimostrazione per l'inclusione

Siano $A,B,C\subseteq U$.

### Riflessività

Ogni elemento di $A$ appartiene ad $A$. Dunque $A\subseteq A$.

### Antisimmetria

Supponiamo $A\subseteq B$ e $B\subseteq A$.

- La prima inclusione afferma che ogni elemento di $A$ appartiene a $B$.
- La seconda afferma che ogni elemento di $B$ appartiene ad $A$.

I due insiemi hanno esattamente gli stessi elementi, quindi $A=B$.

### Transitività

Supponiamo $A\subseteq B$ e $B\subseteq C$. Preso un qualunque $x\in A$, la prima inclusione dà $x\in B$; la seconda dà $x\in C$. Poiché questo vale per ogni $x\in A$, segue $A\subseteq C$.

Quindi l'inclusione è una relazione d'ordine su $\mathcal P(U)$.

## Confronto con l'equivalenza

| Tipo | Riflessiva | Simmetrica | Antisimmetrica | Transitiva |
|---|---|---|---|---|
| Equivalenza | richiesta | richiesta | non richiesta | richiesta |
| Ordine | richiesta | non richiesta | richiesta | richiesta |

«Non richiesta» non significa «vietata».

### Precisazione del tutor sugli elementi confrontabili

Una relazione d'ordine non impone che ogni coppia sia confrontabile. Per esempio, $\{1\}$ e $\{2\}$ non sono inclusi l'uno nell'altro. L'ordine dell'inclusione è quindi parziale; non occorre che sia totale.

## Da dire all'orale

> Una relazione d'ordine è una relazione riflessiva, antisimmetrica e transitiva. L'inclusione tra i sottoinsiemi di un insieme fissato ne è un esempio.

## Collegamenti e fonte

- [[02 Relazioni Binarie]] e [[03 Relazioni di Equivalenza]].
- Fonte: [[GAL 2026-2027 - 20260917 - LEZIONE 1.pdf#page=2|Lezione 1, pp. 2-3, stampate 12-13]].
