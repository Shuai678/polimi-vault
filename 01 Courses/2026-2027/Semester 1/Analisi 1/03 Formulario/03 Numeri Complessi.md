---
course: Analisi 1
type: formula-sheet
updated: 2026-10-30
cssclasses:
  - formulario
---

# Numeri complessi

[[00 Indice Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

> [!tip] Goniometria di supporto
> [[09 Goniometria per i Numeri Complessi]] — angoli notevoli, segni nei quadranti, formule e applicazioni a potenze e radici.

**In questa scheda:** [[#Forma algebrica e operazioni|Forma algebrica e operazioni]] · [[#Geometria e rappresentazioni|Geometria e rappresentazioni]] · [[#De Moivre, radici e polinomi|De Moivre, radici e polinomi]]

## Forma algebrica e operazioni

### Forma algebrica e operazioni

[[37 Unità Immaginaria e Forma Algebrica|Forma algebrica]] · [[38 Operazioni con i Numeri Complessi|operazioni]]

$$
z=x+iy,\qquad i^2=-1,\qquad\operatorname{Re}z=x,\quad\operatorname{Im}z=y.
$$

$$
(x+iy)(u+iv)=(xu-yv)+i(xv+yu).
$$

### Coniugato, modulo e proprietà

[[41 Coniugato e Modulo dei Numeri Complessi|Coniugato e modulo]] · [[44 Proprietà del Coniugato|proprietà]]

$$
\bar z=x-iy,\qquad\lvert z\rvert=\sqrt{x^2+y^2},\qquad z\bar z=\lvert z\rvert^2.
$$

$$
\overline{z+w}=\bar z+\bar w,\qquad\overline{zw}=\bar z\bar w.
$$

### Inverso e divisione

[[39 Campo Complesso e Inverso Moltiplicativo|Inverso]] · [[45 Divisione tra Numeri Complessi|divisione]]

$$
z^{-1}=\frac{\bar z}{\lvert z\rvert^2}\quad(z\neq0),
\qquad\frac zw=\frac{z\bar w}{\lvert w\rvert^2}\quad(w\neq0).
$$

## Geometria e rappresentazioni

### Distanza e luoghi geometrici

[[42 Distanza nel Piano Complesso|Distanza]] · [[43 Luoghi Geometrici nel Piano Complesso|luoghi geometrici]]

$$
d(z,w)=\lvert z-w\rvert.
$$

| Equazione | Luogo geometrico |
| --- | --- |
| $\lvert z-z_0\rvert=r$, $r>0$ | Circonferenza di centro $z_0$ e raggio $r$. |
| $\operatorname{Re}z=c$ | Retta verticale. |
| $\operatorname{Im}z=c$ | Retta orizzontale. |

### Argomento e quadranti

[[47 Modulo e Argomento dei Numeri Complessi|Argomento]] · [[49 Determinazione dell'Argomento per Quadranti|quadranti]]

**Ipotesi:** $z\neq0$. L'argomento $\theta$ è definito modulo $2\pi$.

$$
\cos\theta=\frac x{\lvert z\rvert},\qquad\sin\theta=\frac y{\lvert z\rvert}.
$$

> [!warning] Controllare il quadrante
> $\arctan(y/x)$ da sola non distingue i quadranti. Il numero zero non ha argomento.

### Forma trigonometrica ed esponenziale

[[48 Forma Trigonometrica dei Numeri Complessi|Forma trigonometrica]] · [[50 Forma Esponenziale e Identità di Eulero|esponenziale]]

**Ipotesi:** $r=\lvert z\rvert>0$.

$$
z=r(\cos\theta+i\sin\theta)=re^{i\theta}.
$$

**Identità di Eulero**

$$
e^{i\theta}=\cos\theta+i\sin\theta.
$$

## De Moivre, radici e polinomi

### De Moivre: prodotto e quoziente · D3

[[51 Formule di De Moivre - Prodotto e Quoziente|De Moivre: prodotto e quoziente]] · [[D03 Formule di De Moivre per Prodotti e Potenze|Dimostrazione D3]]

**Ipotesi:** moduli $r,R>0$.

$$
\begin{aligned}
re^{i\theta}Re^{i\varphi}&=rRe^{i(\theta+\varphi)},\\
\frac{re^{i\theta}}{Re^{i\varphi}}&=\frac rR e^{i(\theta-\varphi)}.
\end{aligned}
$$

**Per D3:** sono richiesti il prodotto e le potenze.

### De Moivre: potenze · D3

[[52 Formula di De Moivre per le Potenze Complesse|De Moivre: potenze]] · [[D03 Formule di De Moivre per Prodotti e Potenze|Dimostrazione D3]]

**Ipotesi:** $r>0$, $n\in\mathbb N$, $n\geq1$.

$$
(re^{i\theta})^n=r^ne^{in\theta}.
$$

### Radici n-esime · D4

[[53 Radici Ennesime Complesse|Radici n-esime]] · [[D04 Radici Ennesime di un Numero Complesso|Dimostrazione D4]]

**Ipotesi:** $w=Re^{i\varphi}\neq0$, $n\geq1$.

$$
z^n=w\iff z=z_k=R^{1/n}e^{i(\varphi+2k\pi)/n},
\qquad k=0,\ldots,n-1.
$$

**Caso $w=0$:** l'unica soluzione è $z=0$.

### Teorema fondamentale dell'algebra

[[54 Equazioni Polinomiali Complesse e Teorema Fondamentale dell'Algebra|Teorema fondamentale dell'algebra]]

Un polinomio complesso **non costante**, di grado $n$, ha esattamente **$n$ radici complesse contate con molteplicità**.

---

[[02 Numeri Reali e Ordine|← Numeri Reali e Ordine]] · [[00 Indice Formulario#Indice rapido|↑ Indice]] · [[04 Funzioni|Funzioni →]]
