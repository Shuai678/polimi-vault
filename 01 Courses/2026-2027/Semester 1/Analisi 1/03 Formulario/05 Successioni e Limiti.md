---
course: Analisi 1
type: formula-sheet
updated: 2026-10-29
cssclasses:
  - formulario
---

# Successioni e limiti

[[00 Indice Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

**In questa scheda:** [[#Definizioni di limite|Definizioni di limite]] · [[#Teoremi fondamentali|Teoremi fondamentali]] · [[#Algebra e confronti|Algebra e confronti]] · [[#Geometriche e rapporto|Geometriche e rapporto]] · [[#Forme indeterminate|Forme indeterminate]]

## Definizioni di limite

### Successione e proprietà definitive

[[58 Successioni di Numeri Reali|Successione]] · [[71 Proprietà Definitivamente Vere|definitivamente]]

**Successione reale:** funzione $n\mapsto a_n\in\mathbb R$, per interi $n\geq n_0$.

**Proprietà definitivamente vera**

$$
\exists N\ \forall n\geq N:\ P(n).
$$

### Limite finito

[[72 Limite Finito di una Successione|Limite finito]]

Per $\ell\in\mathbb R$:

$$
a_n\to\ell\iff
\forall\varepsilon>0\ \exists N\ \forall n\geq N:
\lvert a_n-\ell\rvert<\varepsilon.
$$

> [!warning] Ordine dei quantificatori
> Prima si fissa $\varepsilon>0$, poi si sceglie $N$: l'ordine è essenziale.

### Limiti infiniti e regolarità

[[74 Limiti Infiniti e Regolarità delle Successioni|Limiti infiniti e regolarità]]

$$
\begin{aligned}
a_n\to+\infty&\iff\forall M>0\ \exists N\ \forall n\geq N:\ a_n>M,\\
a_n\to-\infty&\iff\forall M>0\ \exists N\ \forall n\geq N:\ a_n<-M.
\end{aligned}
$$

**Regolare:** ammette limite finito o infinito.

## Teoremi fondamentali

### Unicità del limite · D5

[[73 Unicità del Limite di Successione|Unicità del limite]] · [[D05 Unicità del Limite|Dimostrazione D5]]

**Se esiste, il limite è unico.**

La nota dimostra il caso finito; l'estensione ai limiti infiniti è in [[74 Limiti Infiniti e Regolarità delle Successioni|limiti infiniti]].

### Convergenza e limitatezza · D6

[[77 Limitatezza delle Successioni Convergenti|Convergenza e limitatezza]] · [[D06 Limitatezza delle Successioni Convergenti|Dimostrazione D6]]

$$
a_n\to\ell\in\mathbb R\Rightarrow(a_n)\text{ limitata}.
$$

**Il viceversa è falso:** $(-1)^n$ è limitata ma non converge.

### Permanenza del segno · D7

[[79 Teorema di Permanenza del Segno|Permanenza del segno]] · [[D07 Teorema di Permanenza del Segno|Dimostrazione D7]]

Se $a_n\to\ell>0$, anche per $\ell=+\infty$:

$$
a_n>0\quad\text{definitivamente}.
$$

Vale l'analogo per il segno negativo.

**Passaggio al limite:** se $a_n\geq0$ definitivamente e il limite esiste, allora $\ell\geq0$.

### Due carabinieri · D8

[[82 Teorema dei Due Carabinieri|Due carabinieri]] · [[D08 Teorema dei Due Carabinieri|Dimostrazione D8]]

**Ipotesi:** $a_n\leq b_n\leq c_n$ definitivamente e $a_n,c_n\to\ell\in\mathbb R$.

$$
b_n\to\ell.
$$

### Monotonia e limite monotono · D9

[[75 Successioni Monotone|Monotonia]] · [[76 Teorema del Limite delle Successioni Monotone|limite monotono]] · [[D09 Regolarità delle Successioni Monotone|Dimostrazione D9]]

| Monotonia | Limite |
| --- | --- |
| Crescente: $a_{n+1}\geq a_n$ | $\sup\{a_n\}$: finito se limitata superiormente, altrimenti $+\infty$. |
| Decrescente: $a_{n+1}\leq a_n$ | $\inf\{a_n\}$, eventualmente $-\infty$. |

## Algebra e confronti

### Algebra dei limiti

[[80 Algebra dei Limiti di Successioni|Algebra dei limiti]]

**Ipotesi:** $a_n\to a$ e $b_n\to b$, con $a,b$ finiti.

$$
a_n+b_n\to a+b,\qquad a_nb_n\to ab.
$$

Se $b\neq0$:

$$
\frac{a_n}{b_n}\to\frac ab.
$$

Se $a>0$ e le basi sono definitivamente positive:

$$
a_n^{b_n}\to a^b.
$$

### Disuguaglianze e confronto infinito

[[81 Disuguaglianze e Passaggio al Limite|Disuguaglianze]] · [[83 Teorema del confronto per successioni divergenti|confronto infinito]]

**Ipotesi:** $a_n\leq b_n$ definitivamente e limiti esistenti.

$$
\lim a_n\leq\lim b_n.
$$

**Confronto infinito:** se $a_n\to+\infty$, allora anche $b_n\to+\infty$. Analogamente, una successione con maggiorante che tende a $-\infty$ tende a $-\infty$.

### Limitata × infinitesima

[[84 Confronto in Modulo e Prodotto con un Infinitesimo|Limitata × infinitesima]]

**Ipotesi:** $\lvert a_n\rvert\leq M$ definitivamente e $b_n\to0$.

$$
a_nb_n\to0.
$$

Vale anche se $a_n$ **non ha limite**.

## Geometriche e rapporto

### Progressione geometrica

[[78 Limiti di Potenze e Progressioni Geometriche|Progressione geometrica]]

| Ragione | Comportamento di $q^n$ |
| --- | --- |
| $\lvert q\rvert<1$ | Tende a $0$. |
| $q=1$ | Vale $1$. |
| $q>1$ | Tende a $+\infty$. |
| $q\leq-1$ | È irregolare. |

### Rapporto per successioni

[[91 Criterio del Rapporto per Successioni|Rapporto per successioni]]

**Ipotesi:** $a_n>0$ definitivamente e

$$
\frac{a_{n+1}}{a_n}\to L\in[0,+\infty].
$$

| Valore di $L$ | Conclusione |
| --- | --- |
| $L<1$ | $a_n\to0$ |
| $L>1$ | $a_n\to+\infty$ |
| $L=1$ | **Non decide.** |

## Forme indeterminate

### Forme indeterminate e potenze variabili

[[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate|Forme indeterminate]] · [[89 Limiti di Potenze con Base ed Esponente Variabili|potenze variabili]]

Richiedono uno studio specifico:

$$
\frac00,\quad\frac\infty\infty,\quad0\cdot\infty,\quad
\infty-\infty,\quad1^{\pm\infty},\quad0^0,\quad\infty^0.
$$

**Potenze variabili**, con $a_n>0$:

$$
a_n^{b_n}=e^{b_n\log a_n}.
$$

---

[[04 Funzioni|← Funzioni]] · [[00 Indice Formulario#Indice rapido|↑ Indice]] · [[06 Equivalenti e Limiti Notevoli|Equivalenti e Limiti Notevoli →]]
