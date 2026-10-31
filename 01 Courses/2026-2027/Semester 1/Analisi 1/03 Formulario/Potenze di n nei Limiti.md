---
course: Analisi 1
type: formula-sheet
updated: 2026-10-30
cssclasses:
  - formulario
---

# Potenze di n nei limiti

[[00 Indice Formulario|Indice del formulario]] · [[05 Successioni e Limiti|Successioni e limiti]] · [[Guida agli Esercizi su Successioni e Limiti|Scelta del metodo]]

**Ipotesi:** $n\geq1$, $n\to+\infty$; esponenti $\alpha,a,b$ fissati, salvo indicazioni diverse. $\log=\ln$.

## Comportamento delle potenze di n

| Esponente | Limite di $n^\alpha$ |
| --- | --- |
| $\alpha<0$ | $0$ |
| $\alpha=0$ | $1$ |
| $\alpha>0$ | $+\infty$ |

**Anche se $0<\alpha<1$, la potenza cresce senza limite:** cresce più lentamente di $n$, ma non tende a zero.

## Proprietà algebriche delle potenze

Per $n>0$ e $a,b\in\mathbb R$:

| Proprietà | Formula |
| --- | --- |
| Prodotto | $n^a n^b=n^{a+b}$ |
| Quoziente | $\dfrac{n^a}{n^b}=n^{a-b}$ |
| Potenza di potenza | $(n^a)^b=n^{ab}$ |
| Esponente negativo | $n^{-a}=\dfrac1{n^a}$ |
| Esponente frazionario | $n^{p/q}=\sqrt[q]{n^p}$, $p\in\mathbb Z$, $q\geq1$ intero |
| Esponente zero | $n^0=1$ |

## Confronto tra due potenze

$$
\frac{n^a}{n^b}=n^{a-b}.
$$

| Confronto | Limite del rapporto |
| --- | --- |
| $a>b$ | $+\infty$ |
| $a=b$ | $1$ |
| $a<b$ | $0$ |

La regola vale anche con esponenti nulli, negativi o frazionari: **sottrarre gli esponenti e guardare il segno**.

## Gerarchia degli infiniti

Per $0<a<b$ e $c>1$ fissati:

$$
\boxed{\log n\ll n^a\ll n^b\ll c^n},
\qquad
f_n\ll g_n\iff\frac{f_n}{g_n}\to0.
$$

Qualunque potenza positiva di $n$ domina il logaritmo. Gerarchia completa in [[06 Equivalenti e Limiti Notevoli#Gerarchia degli infiniti|Equivalenti e limiti notevoli]].

## Distinguere base ed esponente

$$
n^{1/2}=\sqrt n\to+\infty,
\qquad
\left(\frac12\right)^n\to0.
$$

Nel primo caso è fisso l'esponente; nel secondo è fissa la base: valgono le regole delle [[78 Limiti di Potenze e Progressioni Geometriche|progressioni geometriche]].

**Esponente variabile:** la tabella iniziale non basta. Scrivere $n^{b_n}=e^{b_n\log n}$ e studiare l'esponente; vedi [[89 Limiti di Potenze con Base ed Esponente Variabili]].

---

[[Guida agli Esercizi su Successioni e Limiti|← Scelta del metodo]] · [[00 Indice Formulario#Indice rapido|↑ Indice]]
