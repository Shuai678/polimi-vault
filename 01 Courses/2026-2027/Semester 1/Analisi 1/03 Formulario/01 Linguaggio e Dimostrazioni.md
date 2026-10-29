---
course: Analisi 1
type: formula-sheet
updated: 2026-10-29
cssclasses:
  - formulario
---

# Linguaggio e dimostrazioni

[[00 Indice Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

**In questa scheda:** [[#Insiemi e proposizioni|Insiemi e proposizioni]] · [[#Quantificatori e negazioni|Quantificatori e negazioni]] · [[#Metodi di dimostrazione|Metodi di dimostrazione]]

## Insiemi e proposizioni

### Differenza e inclusione

[[08 Differenza tra Insiemi|Differenza]] · [[09 Sottoinsiemi e Inclusione|inclusione]]

$$
\begin{aligned}
A\setminus B&=\{x\in A:x\notin B\},\\
A\subseteq B&\iff\forall x\,(x\in A\Rightarrow x\in B).
\end{aligned}
$$

### Congiunzione e disgiunzione

[[12 Congiunzione Logica|Congiunzione]] · [[13 Disgiunzione Logica|disgiunzione]]

| Connettivo | Quando è vero |
| --- | --- |
| $P\land Q$ | Entrambe le proposizioni sono vere. |
| $P\lor Q$ | Almeno una è vera, anche entrambe. |

### Implicazione

[[15 Implicazione Logica|Implicazione]] · [[16 Condizioni Necessarie e Sufficienti|condizioni]]

$$
P\Rightarrow Q
$$

È **falsa solo** quando $P$ è vera e $Q$ è falsa.

- $P$ è una condizione **sufficiente** per $Q$.
- $Q$ è una condizione **necessaria** per $P$.
- $P\Leftrightarrow Q$ richiede **entrambe** le implicazioni.

## Quantificatori e negazioni

### Regole di negazione

[[11 Predicati e Variabili Libere|Quantificatori]] · [[14 Negazione Logica|negazioni]]

**Negare i quantificatori**

$$
\begin{aligned}
\neg(\forall x\,P)&=\exists x\,\neg P,\\
\neg(\exists x\,P)&=\forall x\,\neg P.
\end{aligned}
$$

**Leggi di De Morgan**

$$
\begin{aligned}
\neg(P\land Q)&=\neg P\lor\neg Q,\\
\neg(P\lor Q)&=\neg P\land\neg Q.
\end{aligned}
$$

## Metodi di dimostrazione

### Diretta e contrapposizione

[[17 Dimostrazione Diretta|Diretta]] · [[18 Dimostrazione per Contrapposizione|contrapposizione]]

**Diretta:** partire dalle ipotesi e arrivare alla tesi.

**Contrapposizione:** dimostrare l'implicazione equivalente

$$
P\Rightarrow Q\iff\neg Q\Rightarrow\neg P.
$$

### Controesempio e assurdo

[[19 Controesempio|Controesempio]] · [[20 Dimostrazione per Assurdo|assurdo]]

**Controesempio:** per confutare $P\Rightarrow Q$ basta un caso con **$P$ vera e $Q$ falsa**.

**Assurdo:** le ipotesi, insieme alla **negazione della tesi**, devono portare a una contraddizione.

### Induzione

[[21 Dimostrazione per Induzione|Induzione]]

1. **Base:** verificare $P(n_0)$.
2. **Passo induttivo:** per ogni $n\geq n_0$, provare

$$
P(n)\Rightarrow P(n+1).
$$

**Conclusione:** $P(n)$ vale per ogni $n\geq n_0$.

---

[[00 Indice Formulario#Indice rapido|↑ Indice]] · [[02 Numeri Reali e Ordine|Numeri Reali e Ordine →]]
