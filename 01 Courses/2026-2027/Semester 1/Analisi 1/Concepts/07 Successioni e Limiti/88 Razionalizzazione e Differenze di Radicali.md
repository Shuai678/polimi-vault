---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 08, PDF pp. 9-10
  - Libro, §3.5.4, p. 99 (razionalizzazione)
---

# Razionalizzazione e differenze di radicali

## Quando si usa e idea del metodo

Una differenza di radicali può presentare la forma $\infty-\infty$. I due termini crescono, ma la loro differenza può tendere a zero, a un valore finito non nullo o a infinito.

La razionalizzazione trasforma una **differenza** difficile in un **rapporto** studiabile. Per le radici quadrate si usa

$$
(A-B)(A+B)=A^2-B^2.
$$

Moltiplicare e dividere per $A+B$ è lecito quando questa somma è non nulla. Il dominio delle radici si controlla prima della trasformazione.

## Esempio 1: differenza di radici quadrate

### Testo

Calcolare il limite di

$$
d_n=\sqrt{n^2+n}-\sqrt{n^2-n},\qquad n\geq1.
$$

### Idea

Entrambi i radicali tendono a $+\infty$. Il coniugato $\sqrt{n^2+n}+\sqrt{n^2-n}$ è positivo e permette di eliminare i radicali dal numeratore.

### Svolgimento passo per passo

$$
\begin{aligned}
d_n
&=\frac{(\sqrt{n^2+n}-\sqrt{n^2-n})(\sqrt{n^2+n}+\sqrt{n^2-n})}
{\sqrt{n^2+n}+\sqrt{n^2-n}}\\
&=\frac{(n^2+n)-(n^2-n)}{\sqrt{n^2+n}+\sqrt{n^2-n}}\\
&=\frac{2n}{n\sqrt{1+1/n}+n\sqrt{1-1/n}}\\
&=\frac2{\sqrt{1+1/n}+\sqrt{1-1/n}}.
\end{aligned}
$$

Si è usato $\sqrt{n^2}=|n|=n$ perché $n\geq1$. I due radicali del denominatore tendono a $1$; il denominatore tende a $2\neq0$. Dunque

$$
\boxed{d_n\to1.}
$$

**Cosa imparare:** sostituire entrambi i radicali con $n$ avrebbe cancellato proprio l'informazione che determina il limite della differenza.

## Esempio 2: radici settime

### Testo

Il PDF propone di usare la differenza di potenze per

$$
h_n=(n^2+n)^{1/7}-(n^2-n)^{1/7}.
$$

### Identità utile

Per ogni intero $m\geq1$,

$$
A^m-B^m=(A-B)\sum_{k=0}^{m-1}A^{m-1-k}B^k.
$$

Il prodotto si verifica distribuendo: i termini intermedi si cancellano e restano $A^m-B^m$. Per $m=7$ poniamo $A=(n^2+n)^{1/7}$ e $B=(n^2-n)^{1/7}$. Per $n\geq2$ entrambi sono positivi, perciò la somma al denominatore è positiva.

### Svolgimento passo per passo

$$
h_n=\frac{A^7-B^7}{\sum_{k=0}^{6}A^{6-k}B^k}
=\frac{2n}{\sum_{k=0}^{6}A^{6-k}B^k}.
$$

Scriviamo

$$
A=n^{2/7}(1+1/n)^{1/7},\qquad
B=n^{2/7}(1-1/n)^{1/7}.
$$

Ogni prodotto $A^{6-k}B^k$ contiene il fattore $n^{12/7}$. Quindi

$$
h_n=\frac{2n^{-5/7}}
{\displaystyle\sum_{k=0}^{6}(1+1/n)^{(6-k)/7}(1-1/n)^{k/7}}.
$$

Ciascuno dei sette addendi del denominatore tende a $1$, anche per $k=0$ e $k=6$. Il denominatore tende a $7$ e il numeratore a zero:

$$
\boxed{h_n\to0.}
$$

## Esempio 3: esponente irrazionale

### Testo

Nel PDF il limite seguente è lasciato aperto. Qui lo risolviamo:

$$
f_n=(n^2+n)^{1/\sqrt2}-(n^2-n)^{1/\sqrt2}.
$$

### Idea

L'identità precedente richiede un esponente intero dopo l'elevamento a potenza; non si applica direttamente a questo esponente irrazionale. Possiamo però confrontare la differenza con quella di radici quadrate appena calcolata.

### Svolgimento passo per passo

Poniamo $r=1/\sqrt2>1/2$, $X=n^2+n$ e $Y=n^2-n$. Per $n\geq2$, $X>Y>0$. Aggiungendo e sottraendo $X^{r-1/2}\sqrt Y$ si ha l'identità

$$
X^r-Y^r
=X^{r-1/2}(\sqrt X-\sqrt Y)
+\sqrt Y\bigl(X^{r-1/2}-Y^{r-1/2}\bigr).
$$

Il secondo addendo è non negativo: $r-1/2>0$ e la potenza di esponente positivo è crescente. Pertanto

$$
f_n\geq(n^2+n)^{r-1/2}\,d_n.
$$

Sappiamo che $d_n\to1$, quindi $d_n\geq1/2$ definitivamente. Inoltre

$$
(n^2+n)^{r-1/2}\geq(n^2)^{r-1/2}=n^{2r-1}\to+\infty,
$$

poiché $2r-1=\sqrt2-1>0$. Si ottiene definitivamente

$$
f_n\geq\frac12 n^{\sqrt2-1}\to+\infty.
$$

Per [[83 Teorema del Confronto per Limiti Infiniti]],

$$
\boxed{f_n\to+\infty.}
$$

### Cosa imparare

Quando una razionalizzazione algebrica non è disponibile, una stima dal basso può bastare per dimostrare un limite infinito. Qui sono sufficienti monotonia delle potenze, permanenza del segno e confronto.

## Errori comuni

- Scrivere $\sqrt{x-y}=\sqrt x-\sqrt y$.
- Usare il coniugato senza controllare che il denominatore introdotto sia non nullo.
- Raccogliere $n^2$ da una radice come se uscisse invariato: da una radice quadrata esce $n$, da una radice settima $n^{2/7}$.
- Trattare due termini con la stessa crescita principale come se la loro differenza fosse automaticamente zero.

### Da dire all'orale

> La razionalizzazione usa la differenza di potenze per trasformare una differenza di radicali in un rapporto equivalente. Bisogna controllare il dominio e il denominatore introdotto. Se l'identità non è disponibile, si può cercare un confronto con una differenza già studiata.

## Connessioni e prospettiva d'esame

Si usano [[33 Radice Ennesima Reale]], [[35 Potenze con Esponente Reale]], [[80 Algebra dei Limiti di Successioni]] e [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate]]. La cautela sulle cancellazioni diventerà fondamentale in [[94 Equivalenza Asintotica]]. Potenziale rilevanza d'esame: riconoscere una differenza indeterminata e scegliere tra identità esatta e confronto.
