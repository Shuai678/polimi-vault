---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D2
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 2"
  - "21 Dimostrazione per Induzione"
cssclasses:
  - formulario
---

# D2 — Disuguaglianza di Bernoulli

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D2** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Per ogni $x>-1$ e per ogni intero $n\geq0$,

$$
(1+x)^n\geq1+nx.
$$

## Idea della dimostrazione

Fissiamo $x$ e facciamo induzione sull’esponente. Nel passo induttivo compare il termine aggiuntivo $nx^2$, che è non negativo.

## Dimostrazione

Fissiamo un numero reale arbitrario $x>-1$ e poniamo $P(n): (1+x)^n\geq1+nx$.

### 1. Caso base

Per $n=0$ entrambi i membri valgono $1$. La base è positiva, quindi non compare $0^0$.

### 2. Passo induttivo

Sia $n\geq0$ arbitrario e supponiamo vera $P(n)$. Dobbiamo ottenere $P(n+1)$.

Poiché $1+x>0$, moltiplichiamo l’ipotesi induttiva per $1+x$ conservando il verso:

$$
\begin{aligned}
(1+x)^{n+1}
&=(1+x)^n(1+x)\\
&\geq(1+nx)(1+x)\\
&=1+(n+1)x+nx^2\\
&\geq1+(n+1)x.
\end{aligned}
$$

L’ultima disuguaglianza vale perché $n\geq0$ e $x^2\geq0$.

### 3. Conclusione

Il caso base è vero e $P(n)\Rightarrow P(n+1)$ per ogni $n\geq0$. Per induzione la disuguaglianza vale per tutti questi interi; poiché $x>-1$ era arbitrario, vale per ogni $x>-1$.

## Da ricordare

Devi dichiarare **caso base, ipotesi induttiva e tesi del passo**. La condizione $x>-1$ permette di moltiplicare per $1+x$ senza invertire la disuguaglianza.

## Note di riferimento

[[21 Dimostrazione per Induzione]]
