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

# Enunciati — Successioni e Limiti

[[00 Dimostrazioni Prima Prova in Itinere|Indice di teoremi e dimostrazioni]] · [[00 Indice Formulario|Formulario]]

Le prove richieste su unicità, limitatezza, segno, due carabinieri e monotonia sono nelle schede [[D05 Unicità del Limite]], [[D06 Limitatezza delle Successioni Convergenti]], [[D07 Teorema di Permanenza del Segno]], [[D08 Teorema dei Due Carabinieri]] e [[D09 Regolarità delle Successioni Monotone]].

## 1. Definizioni necessarie per gli enunciati

Per $\ell\in\mathbb R$,

$$
a_n\to\ell\iff
\forall\varepsilon>0\ \exists N\ \forall n\geq N:\ |a_n-\ell|<\varepsilon.
$$

Inoltre,

$$
\begin{aligned}
a_n\to+\infty&\iff\forall M>0\ \exists N\ \forall n\geq N:\ a_n>M,\\
a_n\to-\infty&\iff\forall M>0\ \exists N\ \forall n\geq N:\ a_n<-M.
\end{aligned}
$$

Una successione è **regolare** se ha limite finito o infinito; è **convergente** se il limite è finito. Una proprietà è vera **definitivamente** se vale per tutti gli indici da una certa soglia in poi. Cambiare un numero finito di termini non cambia il limite.

Riferimenti: [[71 Proprietà Definitivamente Vere]], [[72 Limite Finito di una Successione]] e [[74 Limiti Infiniti e Regolarità delle Successioni]].

## 2. Algebra dei limiti finiti

Se $a_n\to a\in\mathbb R$, $b_n\to b\in\mathbb R$ e $\lambda,\mu\in\mathbb R$, allora

$$
\lambda a_n+\mu b_n\to\lambda a+\mu b,\qquad
a_nb_n\to ab,\qquad |a_n|\to|a|.
$$

Se $b\neq0$, il denominatore è definitivamente non nullo e

$$
\frac{a_n}{b_n}\to\frac ab.
$$

Se inoltre $a>0$ e $a_n>0$ definitivamente, allora $a_n^{b_n}\to a^b$.

Riferimento: [[80 Algebra dei Limiti di Successioni]].

## 3. Disuguaglianze e passaggio al limite

Se $a_n\leq b_n$ definitivamente e i due limiti esistono nella retta reale estesa, allora

$$
\lim a_n\leq\lim b_n.
$$

La disuguaglianza stretta può diventare non stretta: $0<1/n$, ma entrambi i membri hanno limite zero.

Se $a_n\to a$, $b_n\to b$ e $a<b$, allora $a_n<b_n$ definitivamente. Per limiti finiti segue dalla permanenza del segno applicata a $b_n-a_n$; i casi con infiniti si verificano scegliendo soglie separate.

Riferimento: [[81 Disuguaglianze e Passaggio al Limite]].

## 4. Teorema del confronto per successioni divergenti

- Se $a_n\leq b_n$ definitivamente e $a_n\to+\infty$, allora $b_n\to+\infty$.
- Se $a_n\leq b_n$ definitivamente e $b_n\to-\infty$, allora $a_n\to-\infty$.

Per un limite infinito basta quindi una sola barriera nel verso utile. Sono anche le estensioni del confronto a limiti infiniti.

Riferimento: [[83 Teorema del confronto per successioni divergenti]].

## 5. Confronto in modulo e prodotto con un infinitesimo

Se $|a_n|\leq b_n$ definitivamente e $b_n\to0$, allora $a_n\to0$. In particolare

$$
a_n\to0\iff|a_n|\to0.
$$

Se $a_n$ è limitata, anche soltanto nella coda, e $b_n\to0$, allora $a_nb_n\to0$. Non serve che $a_n$ abbia limite.

Riferimento: [[84 Confronto in Modulo e Prodotto con un Infinitesimo]].

## 6. Limite di una progressione geometrica

Per $q\in\mathbb R$, il carattere della successione $q^n$, con $n\geq1$, è:

| Ragione | Comportamento di $q^n$ |
| --- | --- |
| $\lvert q\rvert<1$ | Tende a $0$ |
| $q=1$ | È costante uguale a $1$ |
| $q>1$ | Tende a $+\infty$ |
| $q\leq-1$ | Non ha limite nella retta reale estesa |

Riferimento: [[78 Limiti di Potenze e Progressioni Geometriche]]. Questa è una successione; la **serie** geometrica è trattata in [[Enunciati 04 Serie Numeriche]].

## 7. Criterio del rapporto per successioni

Sia $a_n>0$ definitivamente e supponiamo che esista $\ell=\lim a_{n+1}/a_n\in[0,+\infty]$.

- Se $\ell<1$, allora $a_n\to0$.
- Se $\ell>1$, incluso $+\infty$, allora $a_n\to+\infty$.
- Se $\ell=1$, il criterio non decide.

Per esempio $1/n$, $1$ e $n$ hanno tutti rapporto tendente a $1$ e limiti diversi.

Riferimento: [[91 Criterio del Rapporto per Successioni]]. La conclusione sulla **serie** richiede [[D13 Criterio del Rapporto per le Serie Numeriche]].

## 8. Aritmetizzazione parziale dell’infinito

Gli infiniti descrivono comportamenti limite; non sono numeri reali su cui eseguire liberamente ogni operazione.

### Somme determinate

Se $a_n\to a\in\mathbb R$ e $b_n\to+\infty$, allora $a_n+b_n\to+\infty$. Se $b_n\to-\infty$, il limite della somma è $-\infty$.

Inoltre, la somma di due successioni che tendono entrambe a $+\infty$ tende a $+\infty$; analogamente, due limiti $-\infty$ danno una somma con limite $-\infty$.

Una somma con infiniti di segno opposto presenta invece la forma indeterminata $+\infty-\infty$.

### Prodotti e segni

Se un fattore tende a un numero reale **non nullo** e l'altro a un infinito, il prodotto diverge con il segno dato dal prodotto dei segni. La stessa regola vale se entrambi i fattori hanno limite infinito.

| Primo limite | Secondo limite | Limite del prodotto |
|---|---|---|
| positivo non nullo, oppure $+\infty$ | $+\infty$ | $+\infty$ |
| positivo non nullo, oppure $+\infty$ | $-\infty$ | $-\infty$ |
| negativo non nullo, oppure $-\infty$ | $+\infty$ | $-\infty$ |
| negativo non nullo, oppure $-\infty$ | $-\infty$ | $+\infty$ |

Se uno dei limiti è zero e l'altro infinito, la regola non decide il risultato.

### Quozienti e segno del denominatore

La notazione

$$
b_n\to0^+\quad\Longleftrightarrow\quad b_n\to0\text{ e }b_n>0\text{ definitivamente}
$$

non indica un nuovo numero: aggiunge il segno con cui ci si avvicina a zero. Analogamente $0^-$ richiede $b_n<0$ definitivamente.

Se $a_n\to a\in\mathbb R\setminus\{0\}$,

| Segno di $a$ | Limite del denominatore | Limite di $a_n/b_n$ |
|---|---|---|
| $a>0$ | $0^+$ | $+\infty$ |
| $a>0$ | $0^-$ | $-\infty$ |
| $a<0$ | $0^+$ | $-\infty$ |
| $a<0$ | $0^-$ | $+\infty$ |

Questi casi restano validi se il numeratore tende rispettivamente a $+\infty$ o $-\infty$. Il denominatore deve essere definitivamente non nullo.

Se invece $a_n\to a\in\mathbb R$ e $b_n\to\pm\infty$, allora

$$
\frac{a_n}{b_n}\to0.
$$

Il semplice dato $b_n\to0$, senza il segno definitivo, non determina un infinito con segno. Per esempio $1/[(-1)^n/n]=(-1)^n n$ non ha limite.

Le forme aritmetiche indeterminate sono

$$
\infty-\infty,\qquad0\cdot\infty,\qquad\frac\infty\infty,\qquad\frac00.
$$

“Indeterminata” significa che i limiti dei pezzi non bastano: il limite dell’espressione concreta può esistere oppure no.

Riferimento: [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate]].

## 9. Potenze con base ed esponente variabili

Con $a_n>0$ definitivamente vale

$$
a_n^{b_n}=e^{b_n\log a_n}.
$$

Supponiamo $a_n\to a\in[0,+\infty]$ e $b_n\to b\in\mathbb R\cup\{-\infty,+\infty\}$. La tabella riassume i casi con limite determinato. In tutte le righe resta l'ipotesi $a_n>0$ definitivamente.

| Limite della base $a$ | $b>0$ finito | $b<0$ finito | $b=0$ | $b=+\infty$ | $b=-\infty$ |
|---|---|---|---|---|---|
| $0$ | $0$ | $+\infty$ | indeterminata | $0$ | $+\infty$ |
| $0<a<1$ | $a^b$ | $a^b$ | $1$ | $0$ | $+\infty$ |
| $a=1$ | $1$ | $1$ | $1$ | indeterminata | indeterminata |
| $1<a<+\infty$ | $a^b$ | $a^b$ | $1$ | $+\infty$ | $0$ |
| $a=+\infty$ | $+\infty$ | $0$ | indeterminata | $+\infty$ | $0$ |

Il caso con $a>0$ e $b$ entrambi finiti è già in [[80 Algebra dei Limiti di Successioni]]. Le altre righe precisano l'estensione trattata nella Lezione 08.

Le forme indeterminate delle potenze sono $0^0$, $(+\infty)^0$ e $1^{\pm\infty}$. Si studia il prodotto $b_n\log a_n$; se tende a $L\in\mathbb R$, la potenza tende a $e^L$; se tende a $+\infty$ tende a $+\infty$, se tende a $-\infty$ tende a zero.

Riferimento: [[89 Limiti di Potenze con Base ed Esponente Variabili]]. Per i limiti esponenziali notevoli: [[Enunciati 03 Equivalenti e Limiti Notevoli]].
