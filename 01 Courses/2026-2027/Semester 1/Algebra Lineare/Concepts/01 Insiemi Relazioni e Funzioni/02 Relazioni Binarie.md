---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 0, PDF pp. 8-10"
---

# Relazioni binarie

Stato: **da studiare**.

## Dalle possibilità alla selezione

Il [[01 Prodotto Cartesiano|prodotto cartesiano]] $A\times B$ contiene tutte le coppie ammesse. Una relazione seleziona quelle che soddisfano una condizione.

## Definizione 0.2

Una relazione binaria tra $A$ e $B$ è un sottoinsieme

$$
R\subseteq A\times B.
$$

Scrivere $aRb$ equivale a scrivere $(a,b)\in R$. La relazione è l'insieme delle coppie selezionate; la condizione in parole serve a descrivere quali coppie appartengono a quell'insieme.

### Esempio del professore

Siano $A$ l'insieme delle persone in aula e $B$ un insieme di colori. La relazione

$$
R=\{(a,b)\in A\times B\mid
\text{la maglia di }a\text{ ha colore }b\}
$$

contiene soltanto gli abbinamenti persona-colore che si verificano.

Se si assume che ogni persona abbia una maglia di un unico colore considerato, questa relazione è anche una [[05 Funzioni|funzione]]. Questa unicità è un'ipotesi dell'esempio.

## Relazioni su uno stesso insieme

Per studiare riflessività, simmetria e transitività si considera una relazione su $A$:

$$
R\subseteq A\times A.
$$

Nel PDF due persone sono in relazione quando hanno la maglia dello stesso colore.

## Tre proprietà

### Riflessività

Ogni elemento è in relazione con se stesso:

$$
\forall a\in A,\qquad (a,a)\in R.
$$

Per confutarla basta trovare un elemento $a\in A$ per il quale $(a,a)\notin R$.

### Simmetria

Ogni coppia presente può essere invertita:

$$
\forall a,b\in A,\qquad
(a,b)\in R\implies(b,a)\in R.
$$

Per confutarla occorre una coppia presente $(a,b)$ la cui inversa $(b,a)$ sia assente.

### Transitività

Due collegamenti consecutivi impongono il collegamento diretto:

$$
\forall a,b,c\in A,\qquad
\bigl((a,b)\in R\ \text{e}\ (b,c)\in R\bigr)
\implies(a,c)\in R.
$$

Per confutarla servono due coppie presenti $(a,b)$ e $(b,c)$ e una coppia assente $(a,c)$. Gli elementi $a,b,c$ non devono necessariamente essere distinti.

## Esempio numerico del tutor

Su $A=\{1,2,3\}$ consideriamo

$$
R=\{(1,1),(2,2),(3,3),(1,2),(2,1)\}.
$$

- È riflessiva: contiene le tre coppie diagonali.
- È simmetrica: le due coppie non diagonali sono una l'inversa dell'altra.
- È transitiva: all'interno di $\{1,2\}$ sono presenti tutte le coppie; l'elemento $3$ è collegato soltanto a se stesso.

Questa relazione è quindi una [[03 Relazioni di Equivalenza|relazione di equivalenza]].

## Errori da evitare

- Confondere $(a,b)\in R$ con $R\subseteq A\times B$.
- Dichiarare falsa la transitività soltanto perché manca una coppia: devono essere presenti anche le due coppie dell'ipotesi.
- Considerare la simmetria sufficiente per l'equivalenza.
- Confondere simmetria e [[04 Relazioni di Ordine|antisimmetria]].

## Da dire all'orale

> Una relazione binaria tra due insiemi è un sottoinsieme del loro prodotto cartesiano. Le proprietà di una relazione su un insieme si verificano traducendo le rispettive condizioni in condizioni sulle coppie.

## Collegamenti e fonte

- [[03 Relazioni di Equivalenza]] e [[04 Relazioni di Ordine]].
- [[06 Implicazione e Contrapposizione]] per leggere correttamente le proprietà.
- Fonte: [[GAL 2026-2027 - 20260916 - LEZIONE 0.pdf#page=8|Lezione 0, pp. 8-10]]; definizione 0.2 e proprietà.
