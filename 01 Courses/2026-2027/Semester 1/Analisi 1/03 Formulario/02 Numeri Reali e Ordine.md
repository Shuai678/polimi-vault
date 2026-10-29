---
course: Analisi 1
type: formula-sheet
updated: 2026-10-29
cssclasses:
  - formulario
---

# Numeri reali e ordine

[[00 Indice Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

**In questa scheda:** [[#Insiemi numerici e campo|Insiemi numerici e campo]] · [[#Ordine, estremi e completezza|Ordine, estremi e completezza]] · [[#Valore assoluto e retta reale|Valore assoluto e retta reale]] · [[#Potenze e logaritmi|Potenze e logaritmi]]

## Insiemi numerici e campo

### Insiemi numerici e reali

[[03 Numeri Razionali|Insiemi numerici]] · [[06 Numeri Reali e Irrazionali|reali]]

$$
\mathbb N\subset\mathbb Z\subset\mathbb Q\subset\mathbb R\subset\mathbb C
$$

$$
\mathbb Q=\left\{\frac pq:p,q\in\mathbb Z,\ q\neq0\right\},
\qquad\text{irrazionali}=\mathbb R\setminus\mathbb Q.
$$

### Campo e campo ordinato

[[22 Campi|Campo]] · [[23 Campi Ordinati|campo ordinato]]

**Campo:** somma e prodotto commutativi e associativi; neutri $0\neq1$; opposti; inversi per gli elementi non nulli; distributività.

**Campo ordinato:** ordine totale compatibile con la somma e con il prodotto di elementi non negativi.

### Irrazionalità di √2 · D1

[[20 Dimostrazione per Assurdo|Irrazionalità di √2]] · [[D01 Irrazionalità della Radice di Due|Dimostrazione D1]]

$$
\sqrt2\notin\mathbb Q.
$$

**Idea della prova:** assurdo, frazione ridotta ai minimi termini e parità di numeratore e denominatore.

### Disuguaglianza di Bernoulli · D2

[[21 Dimostrazione per Induzione|Disuguaglianza di Bernoulli]] · [[D02 Disuguaglianza di Bernoulli|Dimostrazione D2]]

**Ipotesi:** $x>-1$ e $n\in\mathbb N$, incluso $n=0$.

$$
(1+x)^n\geq1+nx.
$$

## Ordine, estremi e completezza

### Maggioranti e minoranti

[[24 Maggioranti Minoranti e Insiemi Limitati|Maggioranti e minoranti]]

$$
\begin{aligned}
M\text{ maggiorante di }E&\iff\forall x\in E,\ x\leq M,\\
m\text{ minorante di }E&\iff\forall x\in E,\ m\leq x.
\end{aligned}
$$

$E$ è **limitato** se possiede entrambi.

### Massimo, minimo, supremo e infimo

[[25 Massimo e Minimo|Massimo e minimo]] · [[26 Estremo Superiore e Inferiore|estremi]]

| Estremo | Definizione |
| --- | --- |
| $\max E$ | Maggiorante **appartenente a $E$**. |
| $\min E$ | Minorante **appartenente a $E$**. |
| $\sup E$ | Minimo dei maggioranti. |
| $\inf E$ | Massimo dei minoranti. |

Se $\sup E\in E$, allora è il massimo.

### Completezza

[[27 Completezza dei Numeri Reali|Completezza]]

Ogni $E\subseteq\mathbb R$ **non vuoto e limitato superiormente** possiede $\sup E\in\mathbb R$.

Analogamente, se è non vuoto e limitato inferiormente, possiede $\inf E\in\mathbb R$.

### Caratterizzazione degli estremi

[[28 Caratterizzazione degli Estremi|Caratterizzazione degli estremi]]

**Supremo:** $s=\sup E$ se e solo se $s$ è maggiorante e

$$
\forall\varepsilon>0\ \exists x\in E:\ s-\varepsilon<x\leq s.
$$

**Infimo:** $m=\inf E$ se e solo se $m$ è minorante e

$$
\forall\varepsilon>0\ \exists x\in E:\ m\leq x<m+\varepsilon.
$$

## Valore assoluto e retta reale

### Valore assoluto e disuguaglianze triangolari

[[29 Valore Assoluto|Valore assoluto]] · [[30 Disuguaglianza Triangolare|triangolare]]

$$
\lvert x\rvert=\max\{x,-x\}.
$$

Per $r\geq0$:

$$
\lvert x\rvert\leq r\iff-r\leq x\leq r.
$$

**Disuguaglianze triangolari**

$$
\begin{aligned}
\lvert x+y\rvert&\leq\lvert x\rvert+\lvert y\rvert,\\
\bigl\lvert\lvert x\rvert-\lvert y\rvert\bigr\rvert&\leq\lvert x-y\rvert.
\end{aligned}
$$

### Intervalli e densità

[[31 Retta Reale e Intervalli|Intervalli]] · [[32 Densità dei Razionali nei Reali|densità]]

**Intervalli:** parentesi quadre per un estremo incluso; tonde per un estremo escluso. Accanto a $\pm\infty$ si usano sempre parentesi tonde.

**Densità dei razionali:** se $x<y$ sono reali,

$$
\exists q\in\mathbb Q:\ x<q<y.
$$

## Potenze e logaritmi

### Radici e potenze razionali

[[33 Radice Ennesima Reale|Radici]] · [[34 Potenze con Esponente Razionale|potenze razionali]]

$\sqrt[n]{y}$ è l'unica radice **non negativa** per $y\geq0$, $n\geq1$.

$$
\sqrt{x^2}=\lvert x\rvert.
$$

Per $a>0$, $n>0$:

$$
a^{m/n}=\sqrt[n]{a^m}.
$$

### Potenze reali

[[35 Potenze con Esponente Reale|Potenze reali]]

**Ipotesi:** $a>0$.

$$
a^{u+v}=a^ua^v,\qquad(a^u)^v=a^{uv},\qquad a^{-u}=\frac1{a^u}.
$$

Per $a>1$:

$$
a^x=\sup\{a^r:r\in\mathbb Q,\ r<x\}.
$$

### Logaritmi

[[36 Logaritmi|Logaritmi]]

**Ipotesi:** $a>0$, $a\neq1$, $y>0$.

$$
\log_a y=x\iff a^x=y.
$$

Per $u,v>0$:

$$
\begin{aligned}
\log_a(uv)&=\log_a u+\log_a v,\\
\log_a(u/v)&=\log_a u-\log_a v,\\
\log_a(u^t)&=t\log_a u.
\end{aligned}
$$

### Cambiamento di base

[[36 Logaritmi|Cambiamento di base]]

**Ipotesi:** $a,b>0$, $a,b\neq1$, $y>0$.

$$
\log_b y=\frac{\log_a y}{\log_a b}.
$$

**Convenzione:** in questa pagina $\log=\ln$.

---

[[01 Linguaggio e Dimostrazioni|← Linguaggio e Dimostrazioni]] · [[00 Indice Formulario#Indice rapido|↑ Indice]] · [[03 Numeri Complessi|Numeri Complessi →]]
