---
course: Analisi 1
type: exam-theorems
exam: Prima prova in itinere
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 1: enunciati, comprensione e applicazione dei teoremi"
  - "Lezioni 01-12 e note dei concetti richiamate nelle singole sezioni"
cssclasses:
  - formulario
---

# Enunciati — Numeri Reali Complessi e Funzioni

[[00 Dimostrazioni Prima Prova in Itinere|Indice di teoremi e dimostrazioni]] · [[00 Indice Formulario|Formulario]]

Le prove D1–D4 sono nelle schede [[D01 Irrazionalità della Radice di Due]], [[D02 Disuguaglianza di Bernoulli]], [[D03 Formule di De Moivre per Prodotti e Potenze]] e [[D04 Radici Ennesime di un Numero Complesso]]. Qui trovi gli ulteriori enunciati e le proprietà da saper usare.

## 1. Principio di induzione

Sia $P(n)$ una proprietà per interi $n\geq n_0$. Se $P(n_0)$ è vera e, per ogni $n\geq n_0$, $P(n)\Rightarrow P(n+1)$, allora $P(n)$ è vera per ogni $n\geq n_0$.

Riferimento: [[21 Dimostrazione per Induzione]].

## 2. Completezza dei reali e caratterizzazione degli estremi

Ogni insieme non vuoto $A\subseteq\mathbb R$ limitato superiormente ha un estremo superiore reale. Analogamente, se è limitato inferiormente, ha un estremo inferiore reale.

Per un insieme non vuoto $A$:

$$
s=\sup A
\iff
\begin{cases}
x\leq s&\text{per ogni }x\in A,\\
\text{per ogni }\varepsilon>0\text{ esiste }x\in A:\ s-\varepsilon<x.
\end{cases}
$$

Analogamente,

$$
m=\inf A
\iff
\begin{cases}
m\leq x&\text{per ogni }x\in A,\\
\text{per ogni }\varepsilon>0\text{ esiste }x\in A:\ x<m+\varepsilon.
\end{cases}
$$

Se il supremo appartiene ad $A$ è il massimo; se l’infimo appartiene ad $A$ è il minimo. L’appartenenza non è automatica.

Riferimenti: [[27 Completezza dei Numeri Reali]] e [[28 Caratterizzazione degli Estremi]].

## 3. Disuguaglianza triangolare e triangolare inversa

Per ogni $x,y\in\mathbb R$,

$$
|x+y|\leq|x|+|y|,
\qquad
\bigl||x|-|y|\bigr|\leq|x-y|.
$$

In particolare, $-|x|\leq x\leq|x|$ e, per $r\geq0$, $|x|\leq r\iff-r\leq x\leq r$.

Riferimenti: [[29 Valore Assoluto]] e [[30 Disuguaglianza Triangolare]].

## 4. Densità dei razionali

Per ogni coppia $x<y$ di numeri reali esiste $q\in\mathbb Q$ tale che $x<q<y$. Fra due reali distinti c’è quindi sempre un numero razionale.

Riferimento: [[32 Densità dei Razionali nei Reali]].

## 5. Esistenza e unicità della radice reale non negativa

Per ogni $y\geq0$ e ogni intero $n\geq1$ esiste un unico $x\geq0$ tale che $x^n=y$; si indica con $x=\sqrt[n]{y}$.

Per un indice pari la radice reale principale è non negativa; in particolare $\sqrt{x^2}=|x|$.

Riferimento: [[33 Radice Ennesima Reale]].

## 6. Proprietà delle potenze e dei logaritmi

Per $a,b>0$ e $u,v\in\mathbb R$,

$$
a^{u+v}=a^ua^v,\qquad (a^u)^v=a^{uv},\qquad a^{-u}=\frac1{a^u},\qquad (ab)^u=a^ub^u.
$$

Se $a>1$, $x\mapsto a^x$ è strettamente crescente; se $0<a<1$ è strettamente decrescente.

Per $a>0$, $a\neq1$ e $x,y>0$,

$$
\log_a(xy)=\log_a x+\log_a y,\qquad
\log_a\frac xy=\log_a x-\log_a y,\qquad
\log_a(x^u)=u\log_a x.
$$

Per $b>0$, $b\neq1$, vale il cambiamento di base:

$$
\log_b x=\frac{\log_a x}{\log_a b}.
$$

L’esponenziale di base $a$ e il logaritmo di base $a$ sono inversi; il logaritmo ha lo stesso verso di monotonia dell’esponenziale.

Riferimenti: [[34 Potenze con Esponente Razionale]], [[35 Potenze con Esponente Reale]] e [[36 Logaritmi]].

## 7. Coniugato, modulo e distanza complessa

Per $z,w\in\mathbb C$,

$$
\overline{z+w}=\bar z+\bar w,\qquad
\overline{zw}=\bar z\bar w,\qquad
z\bar z=|z|^2,\qquad
|zw|=|z|\,|w|.
$$

Se $w\neq0$,

$$
z^{-1}=\frac{\bar z}{|z|^2}\quad(z\neq0),\qquad
\left|\frac zw\right|=\frac{|z|}{|w|}.
$$

La distanza è $d(z,w)=|z-w|$; è non negativa, vale zero esattamente quando $z=w$, è simmetrica e soddisfa la disuguaglianza triangolare. In particolare

$$
|z+w|\leq|z|+|w|,\qquad
\bigl||z|-|w|\bigr|\leq|z-w|.
$$

Per numeri non nulli, $\arg(zw)=\arg z+\arg w$ e $\arg(z/w)=\arg z-\arg w$ modulo $2\pi$. La formula del quoziente segue da quella del prodotto applicata a $w^{-1}$.

Riferimenti: [[41 Coniugato e Modulo dei Numeri Complessi]], [[42 Distanza nel Piano Complesso]], [[44 Proprietà del Coniugato]], [[45 Divisione tra Numeri Complessi]] e [[51 Formule di De Moivre - Prodotto e Quoziente]].

## 8. Teorema fondamentale dell’algebra

Ogni polinomio a coefficienti complessi di grado $n\geq1$ possiede esattamente $n$ radici complesse **contate con molteplicità**. Se $a_n\neq0$ è il coefficiente principale,

$$
p(z)=a_n\prod_{k=1}^{n}(z-z_k).
$$

Le radici non sono necessariamente distinte. Una radice $\alpha$ ha molteplicità $m$ se $p(z)=(z-\alpha)^m q(z)$ con $q(\alpha)\neq0$.

Riferimento: [[54 Equazioni Polinomiali Complesse e Teorema Fondamentale dell'Algebra]].

## 9. Invertibilità e composizione

Una funzione $f:A\to B$ ammette un’inversa $f^{-1}:B\to A$ se e solo se è biiettiva. Se è soltanto iniettiva, è invertibile come funzione $f:A\to\operatorname{Im}f$.

Le identità inverse sono

$$
f^{-1}\circ f=\operatorname{id}_A,\qquad
f\circ f^{-1}=\operatorname{id}_{\operatorname{Im}f}.
$$

La composizione è associativa quando è definita; in generale non è commutativa.

Riferimenti: [[64 Composizione di Funzioni]], [[65 Funzioni Iniettive e Biiettive]] e [[66 Funzione Inversa]].

## 10. Monotonia e funzione inversa

Se $f:A\subseteq\mathbb R\to\mathbb R$ è strettamente monotona, è iniettiva e la sua inversa $f^{-1}:\operatorname{Im}f\to A$ è strettamente monotona nello stesso verso.

La caratterizzazione mediante rapporto incrementale è:

$$
f\text{ crescente}\iff\frac{f(x_2)-f(x_1)}{x_2-x_1}\geq0
\quad\text{per ogni }x_1\neq x_2\text{ in }A.
$$

Per la crescita stretta si usa $>0$; per la decrescita si invertono i segni.

Riferimenti: [[62 Funzioni Monotone]] e [[67 Monotonia e Funzione Inversa]]. Per domini, parità, periodicità e inverse goniometriche: [[04 Funzioni]].
