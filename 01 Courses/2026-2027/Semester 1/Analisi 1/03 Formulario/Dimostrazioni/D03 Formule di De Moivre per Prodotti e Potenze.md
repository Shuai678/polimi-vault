---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D3
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 3"
  - "51 Formule di De Moivre - Prodotto e Quoziente"
  - "52 Formula di De Moivre per le Potenze Complesse"
cssclasses:
  - formulario
---

# D3 — Formule di De Moivre per Prodotti e Potenze

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D3** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Siano $z=r(\cos\theta+i\sin\theta)$ e $w=R(\cos\varphi+i\sin\varphi)$, con $r,R>0$.

**Prodotto:**

$$
zw=rR\bigl[\cos(\theta+\varphi)+i\sin(\theta+\varphi)\bigr].
$$

**Potenze:** per ogni intero $n\geq1$,

$$
z^n=r^n\bigl[\cos(n\theta)+i\sin(n\theta)\bigr].
$$

Gli argomenti sono intesi modulo $2\pi$.

## Idea della dimostrazione

Per il prodotto sviluppiamo le parentesi e riconosciamo le formule di addizione. Per le potenze applichiamo la regola del prodotto tramite induzione.

## Dimostrazione

### A. Formula del prodotto

Partiamo dalle forme trigonometriche:

$$
zw
=r(\cos\theta+i\sin\theta)
 R(\cos\varphi+i\sin\varphi).
$$

#### 1. Raccogliere i moduli reali

Poiché $r$ e $R$ sono reali, si può scrivere

$$
zw
=rR(\cos\theta+i\sin\theta)
(\cos\varphi+i\sin\varphi).
$$

#### 2. Sviluppare il prodotto

Applicando la proprietà distributiva,

$$
\begin{aligned}
zw
=rR\bigl(&\cos\theta\cos\varphi
+i\cos\theta\sin\varphi\\
&+i\sin\theta\cos\varphi
+i^2\sin\theta\sin\varphi\bigr).
\end{aligned}
$$

#### 3. Usare l'unità immaginaria

Dato che $i^2=-1$,

$$
\begin{aligned}
zw
=rR\bigl[&\cos\theta\cos\varphi
-\sin\theta\sin\varphi\\
&+i(\sin\theta\cos\varphi
+\cos\theta\sin\varphi)\bigr].
\end{aligned}
$$

#### 4. Riconoscere le formule di addizione

Si usano le identità

$$
\cos(\theta+\varphi)
=\cos\theta\cos\varphi-\sin\theta\sin\varphi,
$$

$$
\sin(\theta+\varphi)
=\sin\theta\cos\varphi+\cos\theta\sin\varphi.
$$

Pertanto

$$
zw=rR\bigl(\cos(\theta+\varphi)+i\sin(\theta+\varphi)\bigr).
$$

La stessa conclusione si legge immediatamente usando la [[50 Forma Esponenziale e Identità di Eulero|forma esponenziale]]:

$$
zw=(re^{i\theta})(Re^{i\varphi})
=rRe^{i(\theta+\varphi)}.
$$

### B. Formula delle potenze

#### Caso base

Per $n=1$,

$$
z^1
=r\bigl(\cos\theta+i\sin\theta\bigr),
$$

che coincide con la forma trigonometrica di $z$. Il caso base è quindi verificato.

#### Ipotesi induttiva

Supponiamo che, per un certo $n\geq1$, valga

$$
z^n
=r^n\bigl(\cos(n\theta)+i\sin(n\theta)\bigr).
$$

Questa è l'ipotesi induttiva.

#### Passo da n a n più uno

Per definizione di potenza,

$$
z^{n+1}=z^n z.
$$

Sostituendo l'ipotesi induttiva e la forma trigonometrica di $z$,

$$
\begin{aligned}
z^{n+1}
&=r^n\bigl(\cos(n\theta)+i\sin(n\theta)\bigr)
  r(\cos\theta+i\sin\theta).
\end{aligned}
$$

La formula del prodotto moltiplica i moduli e somma gli argomenti:

$$
\begin{aligned}
z^{n+1}
&=r^{n+1}
\bigl(\cos(n\theta+\theta)+i\sin(n\theta+\theta)\bigr)\\
&=r^{n+1}
\bigl(\cos((n+1)\theta)+i\sin((n+1)\theta)\bigr).
\end{aligned}
$$

Abbiamo così dimostrato la formula per $n+1$. Per il principio di induzione, la tesi vale per ogni $n\in\mathbb{N}$ con $n\geq1$.

### Esponenti zero e negativi

Se $z\neq0$, per $n=0$ entrambi i membri valgono $1$. Se $n=-m<0$, l’inverso di $z$ ha modulo $1/r$ e argomento $-\theta$; applicando la formula positiva a $(z^{-1})^m$ si ottiene ancora $z^n=r^ne^{in\theta}$.

## Da ricordare

D3 richiede **sia il prodotto sia le potenze**. Per il prodotto i moduli si moltiplicano e gli angoli si sommano; per una potenza il modulo si eleva a $n$ e l’angolo si moltiplica per $n$.

## Note di riferimento

[[51 Formule di De Moivre - Prodotto e Quoziente]] · [[52 Formula di De Moivre per le Potenze Complesse]]
