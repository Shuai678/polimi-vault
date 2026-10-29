---
course: Analisi 1
type: formula-sheet
updated: 2026-10-29
cssclasses:
  - formulario
---

# Equivalenti e limiti notevoli

[[00 Indice Formulario|Indice del formulario]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map/00 Course Map|Corso]]

**In questa scheda:** [[#Notazione e numero di Nepero|Notazione e numero di Nepero]] · [[#Equivalenti per argomento infinitesimo|Equivalenti per argomento infinitesimo]] · [[#Gerarchia e termini dominanti|Gerarchia e termini dominanti]] · [[#Razionalizzazione e cautele|Razionalizzazione e cautele]]

> [!info] Ipotesi della scheda
> $t=t_n\to0$, con $t_n\neq0$ definitivamente. Nei rapporti il denominatore deve essere non nullo definitivamente; gli angoli sono in **radianti**.

## Notazione e numero di Nepero

### o-piccolo ed equivalenza

[[93 Notazione o-Piccolo|o-piccolo]] · [[94 Equivalenza Asintotica|equivalenza]]

$$
a_n=o(b_n)\iff\frac{a_n}{b_n}\to0.
$$

$$
a_n\sim b_n\iff\frac{a_n}{b_n}\to1\iff a_n=b_n+o(b_n).
$$

**Equivalenza:** errore relativo che tende a zero.

### Numero di Nepero

[[90 Numero di Nepero e Limiti di Tipo Esponenziale|Numero di Nepero]]

$$
e=\lim_{n\to\infty}\left(1+\frac1n\right)^n.
$$

Per $a\in\mathbb R$ fissato:

$$
\left(1+\frac an\right)^n\to e^a.
$$

Più in generale, se $c_n\to\pm\infty$:

$$
\left(1+\frac1{c_n}\right)^{c_n}\to e.
$$

## Equivalenti per argomento infinitesimo

### Seno e arcotangente

[[95 Equivalenti e Sviluppi Asintotici Notevoli|Seno e arcotangente]]

$$
\sin t\sim t,\qquad\arctan t\sim t.
$$

Quindi:

$$
\frac{\sin t}{t}\to1,\qquad\frac{\arctan t}{t}\to1.
$$

### Coseno

[[95 Equivalenti e Sviluppi Asintotici Notevoli|Coseno]]

$$
1-\cos t\sim\frac{t^2}{2}.
$$

**Sviluppo con resto**

$$
\cos t=1-\frac{t^2}{2}+o(t^2).
$$

### Esponenziale e logaritmo

[[95 Equivalenti e Sviluppi Asintotici Notevoli|Esponenziale e logaritmo]]

$$
e^t-1\sim t,\qquad\log(1+t)\sim t.
$$

**Sviluppi con resto**

$$
\begin{aligned}
e^t&=1+t+o(t),\\
\log(1+t)&=t+o(t).
\end{aligned}
$$

### Potenza con incremento piccolo

[[95 Equivalenti e Sviluppi Asintotici Notevoli|Potenza con incremento piccolo]]

**Ipotesi:** $\alpha\neq0$ fissato; la base è positiva definitivamente.

$$
(1+t)^\alpha-1\sim\alpha t.
$$

**Sviluppo con resto**

$$
(1+t)^\alpha=1+\alpha t+o(t).
$$

## Gerarchia e termini dominanti

### Gerarchia degli infiniti

[[85 Gerarchia degli Infiniti|Gerarchia degli infiniti]]

**Ipotesi:** $a>1$, $\alpha,\beta>0$ fissati.

$$
\begin{aligned}
(\log_a n)^\beta&=o(n^\alpha),\\
n^\alpha&=o(a^n),\\
a^n&=o(n!),\\
n!&=o(n^n).
\end{aligned}
$$

### Termini dominanti

[[86 Termine Dominante nei Rapporti di Successioni|Termini dominanti]]

**Ipotesi:** $P_n\sim An^p$, $Q_n\sim Bn^q$, $A,B\neq0$.

$$
\frac{P_n}{Q_n}\sim\frac AB n^{p-q}.
$$

## Razionalizzazione e cautele

### Razionalizzazione e cancellazioni

[[88 Razionalizzazione e Differenze di Radicali|Razionalizzazione]] · [[97 Cancellazioni e Precisione del Resto Asintotico|cancellazioni]]

**Ipotesi:** $A,B\geq0$, non entrambi nulli.

$$
\sqrt A-\sqrt B=\frac{A-B}{\sqrt A+\sqrt B}.
$$

> [!warning] Differenze e cancellazioni
> Gli equivalenti dei singoli termini possono non bastare. Conservare i resti alla scala necessaria.

### Calcolo con equivalenti e composizioni

[[96 Calcolo dei Limiti con Equivalenti Asintotici|Calcolo con equivalenti]] · [[98 Equivalenti Asintotici nelle Funzioni Composte|composizioni]]

- **Prodotti e quozienti:** sostituire verificando i domini.
- **Composizioni:** controllare dove tende ogni argomento.
- **Somme, differenze e potenze variabili:** serve un controllo ulteriore.

---

[[05 Successioni e Limiti|← Successioni e Limiti]] · [[00 Indice Formulario#Indice rapido|↑ Indice]] · [[07 Serie Numeriche|Serie Numeriche →]]
