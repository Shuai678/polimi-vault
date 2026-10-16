---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 10, PDF pp. 3-5, stampate 84-86"
---

# Nucleo e struttura delle soluzioni

Stato: **da studiare**.

## Separare la posizione dalle direzioni

Nella parametrizzazione $x=v_0+\sum_i t_iv_i$:

- $v_0$ è una soluzione particolare: dipende da $A$ e da $b$, oltre che dalla scelta effettuata;
- la parte variabile descrive le soluzioni del sistema **omogeneo associato** $Ax=0$, che dipende soltanto da $A$.

Cambiare i termini noti, quando il sistema resta compatibile, cambia la posizione dell'insieme delle soluzioni ma non le sue direzioni.

## Definizione di nucleo

Per $A\in M_{\mathbb K}(m,n)$:

$$
\boxed{\ker(A)=\{h\in\mathbb K^n:Ah=0\}.}
$$

Lo zero a destra è la colonna nulla di $\mathbb K^m$. Gli elementi del nucleo sono colonne di $\mathbb K^n$: non si confondono questi due ambienti.

Il sistema $Ax=0$ è sempre compatibile, perché $A0=0$. La soluzione nulla è detta anche banale. Il nucleo può contenere solo quella oppure anche vettori non nulli.

Da [[32 Teorema di Rouché-Capelli|Rouché-Capelli]] il nucleo si descrive con $n-r(A)$ parametri liberi.

## Teorema 10.1: struttura delle soluzioni

Supponiamo che $Ax=b$ sia compatibile e fissiamo **una** sua soluzione $v_0$. Allora

$$
\boxed{\{x:Ax=b\}=v_0+\ker(A)
=\{v_0+h:h\in\ker(A)\}.}
$$

La notazione $v_0+\ker(A)$ indica un insieme ottenuto sommando $v_0$ a ciascun elemento del nucleo.

### Dimostrazione per doppia inclusione

**Ogni soluzione è di quella forma.** Se $Ax=b$, poniamo $h=x-v_0$. Per distributività:

$$
Ah=A(x-v_0)=Ax-Av_0=b-b=0.
$$

Quindi $h\in\ker(A)$ e $x=v_0+h$.

**Ogni vettore di quella forma è soluzione.** Se $h\in\ker(A)$:

$$
A(v_0+h)=Av_0+Ah=b+0=b.
$$

Le due inclusioni dimostrano l'uguaglianza degli insiemi.

## Esempio del professore

Per

$$
A=\begin{pmatrix}5&2&1\\2&2&-2\\1&-2&5\end{pmatrix},
\qquad b=\begin{pmatrix}1\\0\\1\end{pmatrix},
$$

il calcolo della Lezione 10 dà

$$
v_0=\begin{pmatrix}1/3\\-1/3\\0\end{pmatrix},\qquad
v_1=\begin{pmatrix}-1\\2\\1\end{pmatrix},
\qquad
x=v_0+tv_1.
$$

Controlli esplicitati dal tutor:

$$
Av_0=
\begin{pmatrix}5/3-2/3\\2/3-2/3\\1/3+2/3\end{pmatrix}
=b,
$$

$$
Av_1=
\begin{pmatrix}-5+4+1\\-2+4-2\\-1-4+5\end{pmatrix}
=0.
$$

Poiché il rango è 2 e ci sono tre incognite, una sola direzione parametrizza tutto il nucleo:

$$
\ker(A)=\{t(-1,2,1)^{\mathsf T}:t\in\mathbb R\}.
$$

Il calcolo completo al variare di $k$ è in [[08 Nucleo Struttura Cramer e Inverse]].

## Due proprietà che chiariscono il teorema

1. La differenza di due soluzioni dello **stesso** sistema è nel nucleo.
2. La somma di due soluzioni di $Ax=b$ soddisfa $A(x+y)=2b$, non necessariamente $b$.

Se $b\ne0$ e ci sono soluzioni, non sono chiuse rispetto alla somma: $2b=b$ implicherebbe $b=0$. Invece il nucleo è chiuso:

$$
h_1,h_2\in\ker(A)\implies A(h_1+h_2)=0,
\qquad A(\lambda h_1)=\lambda Ah_1=0.
$$

Questa è la porta d'ingresso ai [[41 Sottospazi Vettoriali e Criterio di Chiusura|sottospazi vettoriali]].

![[33 Nucleo e Traslazione delle Soluzioni.svg|1040]]

**Esempio geometrico del tutor, in scala:** per $A=\begin{pmatrix}1&-1\end{pmatrix}$, il nucleo è la retta $x-y=0$ e il sistema $x-y=2$ ha soluzioni $(2,0)+t(1,1)$. La retta arancione è la traslazione di quella blu. I punti $p=(2,0)$ e $q=(3,1)$ sono soluzioni; la differenza $q-p=(1,1)$ è nel nucleo.

Il disegno non identifica punto e vettore come oggetti concettualmente uguali: rappresenta le colonne tramite coordinate e i vettori tramite frecce.

## Unicità e scelta della soluzione particolare

Se $v_0'$ è un'altra soluzione particolare, $v_0'-v_0\in\ker(A)$. Perciò

$$
v_0+\ker(A)=v_0'+\ker(A).
$$

La descrizione può cambiare senza cambiare l'insieme.

Se $\ker(A)=\{0\}$, un sistema compatibile ha una sola soluzione. Viceversa, se il nucleo contiene $h\ne0$, da una soluzione $v_0$ si ottengono almeno le due soluzioni distinte $v_0$ e $v_0+h$.

## Da dire all'orale

> Il nucleo di una matrice è l'insieme delle soluzioni del sistema omogeneo associato. Se un sistema è compatibile, tutte e sole le sue soluzioni sono una soluzione particolare più un elemento del nucleo; lo si dimostra sottraendo la soluzione particolare e usando la distributività.

## Collegamenti e fonte

- [[32 Teorema di Rouché-Capelli]], [[36 Spazi Affini ed Equazioni Cartesiane e Parametriche]], [[41 Sottospazi Vettoriali e Criterio di Chiusura]].
- [[GAL 2026-2027 - 20261014 - LEZIONE 10.pdf#page=3|Lezione 10, pp. 3-5, stampate 84-86]].
