---
course: Analisi 1
type: exam-proof
exam: Prima prova in itinere
proof_id: D4
status: Da studiare
updated: 2026-10-29
source:
  - "AM1-regolamento26-27.pdf, p. 2, voce 4"
  - "53 Radici Ennesime Complesse"
cssclasses:
  - formulario
---

# D4 — Radici Ennesime di un Numero Complesso

[[00 Dimostrazioni Prima Prova in Itinere|Indice delle dimostrazioni]] · [[00 Indice Formulario|Formulario]]

> [!info] Dimostrazione richiesta per lo scritto
> Voce **D4** dell’elenco nel [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.

## Enunciato e ipotesi

Siano $w=Re^{i\varphi}\neq0$ e $n\geq1$ intero. L’equazione $z^n=w$ ha esattamente $n$ radici distinte:

$$
z_k=R^{1/n}e^{i(\varphi+2k\pi)/n},
\qquad k=0,\ldots,n-1.
$$

Se $w=0$, l’unica radice distinta è $z=0$.

## Idea della dimostrazione

Uguagliamo moduli e argomenti dopo aver applicato De Moivre. Poi controlliamo che i candidati siano tutti e non si ripetano.

## Dimostrazione

Cerchiamo un numero

$$
z=\rho e^{i\theta},
\qquad \rho>0,
$$

tale che

$$
z^n=w.
$$

### 1. Applicare la formula di De Moivre per le potenze

Si ha

$$
z^n=\rho^n e^{in\theta}.
$$

L'equazione diventa quindi

$$
\rho^n e^{in\theta}=Re^{i\varphi}.
$$

### 2. Uguagliare i moduli

I moduli devono soddisfare

$$
\rho^n=R.
$$

Poiché $R>0$ e $\rho$ è un modulo, cioè $\rho>0$, esiste un'unica soluzione reale positiva:

$$
\rho=R^{1/n}.
$$

### 3. Uguagliare gli argomenti

Due numeri complessi non nulli con lo stesso modulo coincidono quando i loro argomenti differiscono per un multiplo intero di $2\pi$. Pertanto

$$
n\theta=\varphi+2h\pi,
\qquad h\in\mathbb{Z}.
$$

Dividendo per $n$,

$$
\theta=\frac{\varphi+2h\pi}{n},
\qquad h\in\mathbb{Z}.
$$

Si ottengono quindi i candidati

$$
z_h
=R^{1/n}e^{i(\varphi+2h\pi)/n},
\qquad h\in\mathbb{Z}.
$$

### 4. Verificare che ogni candidato sia una radice

Elevando $z_h$ alla potenza $n$,

$$
\begin{aligned}
z_h^n
&=\left(R^{1/n}e^{i(\varphi+2h\pi)/n}\right)^n\\
&=Re^{i(\varphi+2h\pi)}\\
&=Re^{i\varphi}e^{i2h\pi}\\
&=Re^{i\varphi}\\
&=w,
\end{aligned}
$$

perché $e^{i2h\pi}=1$ per ogni $h\in\mathbb{Z}$.

### 5. Eliminare le ripetizioni

Ogni intero $h$ può essere scritto mediante la divisione con resto come

$$
h=qn+k,
$$

con

$$
q\in\mathbb{Z},
\qquad
k\in\{0,1,\ldots,n-1\}.
$$

Allora

$$
\begin{aligned}
\frac{\varphi+2h\pi}{n}
&=\frac{\varphi+2(qn+k)\pi}{n}\\
&=\frac{\varphi+2k\pi}{n}+2q\pi.
\end{aligned}
$$

L'aggiunta di $2q\pi$ non cambia il numero complesso. Quindi ogni valore intero di $h$ produce una delle soluzioni corrispondenti ai soli resti

$$
k=0,1,\ldots,n-1.
$$

### 6. Dimostrare che le n radici sono distinte

Supponiamo che due indici $k_1,k_2\in\{0,1,\ldots,n-1\}$ producano la stessa radice. I loro argomenti dovrebbero differire per un multiplo intero di $2\pi$:

$$
\frac{\varphi+2k_2\pi}{n}
-\frac{\varphi+2k_1\pi}{n}
=2m\pi
$$

per qualche $m\in\mathbb{Z}$. Semplificando,

$$
\frac{2(k_2-k_1)\pi}{n}=2m\pi.
$$

Quindi

$$
k_2-k_1=mn.
$$

Ma $k_1$ e $k_2$ appartengono entrambi a $\{0,\ldots,n-1\}$, perciò

$$
-(n-1)\leq k_2-k_1\leq n-1.
$$

L'unico multiplo di $n$ in questo intervallo è $0$. Ne segue

$$
k_2-k_1=0,
$$

e quindi $k_1=k_2$. Le $n$ radici elencate sono dunque tutte distinte.

### Il caso $w=0$

Se $z^n=0$, allora $|z|^n=0$ e dunque $|z|=0$: necessariamente $z=0$. Viceversa $0^n=0$ per $n\geq1$.

## Da ricordare

La prova deve spiegare **esistenza, completezza dell’elenco e distinzione delle radici**. Il modulo è $R^{1/n}$; non è $R/n$.

## Note di riferimento

[[53 Radici Ennesime Complesse]]
