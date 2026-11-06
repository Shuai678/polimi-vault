---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 13, PDF pp. 10-11, stampate 117-118"
---

# Basi e unicità delle coordinate

Stato: **da studiare**.

## Definizione 13.4

Una famiglia $v_1,\ldots,v_d$ è una **base di $V$** quando:

1. genera $V$;
2. è linearmente indipendente.

Le due condizioni hanno ruoli diversi: i generatori danno l'esistenza della rappresentazione; l'indipendenza dà l'unicità.

Per le coordinate si fissa un **ordine** e si scrive $\mathcal B=(v_1,\ldots,v_d)$. Il PDF usa anche parentesi da insieme: l'ordine va reso esplicito quando i coefficienti diventano una lista.

## Teorema 13.5 di unicità della rappresentazione

Se $\mathcal B$ è una base di $V$, allora per ogni $v\in V$ esiste una e una sola lista $(\lambda_1,\ldots,\lambda_d)$ tale che

$$
v=\lambda_1v_1+\cdots+\lambda_dv_d.
$$

### Dimostrazione

Poiché i $v_i$ generano $V$, almeno una lista di coefficienti esiste.

Supponiamo che ci siano due espressioni:

$$
v=\sum_i\lambda_iv_i,\qquad
v=\sum_i\mu_iv_i.
$$

Sottraendo e usando le proprietà delle operazioni:

$$
0=v-v=\sum_i(\lambda_i-\mu_i)v_i.
$$

Per indipendenza, $\lambda_i-\mu_i=0$ per ogni $i$, cioè $\lambda_i=\mu_i$. La lista è unica.

Vale anche il viceversa: se ogni vettore di $V$ ha una rappresentazione unica tramite la famiglia, allora essa genera $V$ e lo zero ha solo la rappresentazione banale, dunque è una base.

## Coordinate rispetto alla base

Integrazione notazionale del tutor:

$$
\boxed{[v]_{\mathcal B}=
\begin{pmatrix}\lambda_1\\\vdots\\\lambda_d\end{pmatrix}.}
$$

$v$ è un elemento di $V$, mentre $[v]_{\mathcal B}$ è una colonna di $\mathbb K^d$. Se $V$ è uno spazio di matrici, le coordinate sono comunque una colonna di scalari, non la matrice originaria.

La corrispondenza $v\mapsto[v]_{\mathcal B}$ è biiettiva: ogni colonna costruisce un vettore, e colonne diverse non possono costruire lo stesso vettore.

## Stesso vettore, coordinate differenti

Esempio del tutor in $\mathbb R^2$:

$$
\mathcal E=((1,0),(0,1)),\qquad
\mathcal B=((1,1),(1,-1)).
$$

I vettori di $\mathcal B$ sono indipendenti, perché

$$
\alpha(1,1)+\beta(1,-1)=0
\implies
\begin{cases}\alpha+\beta=0,\\\alpha-\beta=0,\end{cases}
\implies\alpha=\beta=0.
$$

Ogni $(x,y)$ è ottenuto ponendo $\alpha=(x+y)/2$, $\beta=(x-y)/2$, quindi sono anche generatori.

Per $v=(3,1)$:

$$
v=3(1,0)+1(0,1)=2(1,1)+1(1,-1).
$$

Dunque

$$
[v]_{\mathcal E}=\begin{pmatrix}3\\1\end{pmatrix},
\qquad
[v]_{\mathcal B}=\begin{pmatrix}2\\1\end{pmatrix}.
$$

![[45 Coordinate rispetto a Due Basi.svg|1040]]

**Figura del tutor, in scala:** la freccia verde rappresenta sempre lo stesso $v$. Cambia la coppia di direzioni usata per costruirlo; i tratti ausiliari mostrano rispettivamente $3e_1+e_2$ e $2b_1+b_2$.

Le formule con divisione per 2 valgono qui su $\mathbb R$. Su $\mathbb F_2$ i due vettori della seconda famiglia coincidono: non sarebbe una base.

## Esempio del professore in dimensione tre

La famiglia

$$
\mathcal B=
\left(
\begin{pmatrix}1\\0\\0\end{pmatrix},
\begin{pmatrix}-2\\1\\0\end{pmatrix},
\begin{pmatrix}0\\1\\1\end{pmatrix}
\right)
$$

è una base di $\mathbb R^3$. Dalla formula generale di [[43 Generatori e Sistemi Lineari]]:

$$
[(a,b,c)^{\mathsf T}]_{\mathcal B}
=\begin{pmatrix}a+2b-2c\\b-c\\c\end{pmatrix}.
$$

Per $(0,1,3)^{\mathsf T}$ le coordinate sono $(-4,-2,3)^{\mathsf T}$: eliminato il quarto generatore ridondante, le due rappresentazioni iniziali diventano una sola.

## Dimensione: il punto lasciato alla lezione successiva

La Definizione 13.6 chiama dimensione il numero di elementi di una base. Perché la definizione sia ben posta bisogna dimostrare che basi diverse abbiano la stessa lunghezza. È il contenuto del [[46 Lemma Fondamentale e Teorema della Dimensione|Teorema 15.2]], non una conseguenza della sola unicità delle coordinate rispetto a una base fissata.

## Da dire all'orale

> Una base è una famiglia indipendente che genera lo spazio. Ogni vettore ammette allora una rappresentazione unica: l'esistenza segue dalla generazione e l'unicità dall'indipendenza, sottraendo due rappresentazioni.

## Collegamenti e fonte

- [[42 Combinazioni Lineari e Span]], [[43 Generatori e Sistemi Lineari]], [[44 Dipendenza e Indipendenza Lineare]].
- [[47 Basi Canoniche e Spazi Finitamente Generati]], [[48 Estrazione di una Base con Gauss]], [[49 Completamento di Vettori Indipendenti a una Base]].
- [[GAL 2026-2027 - 20261019 - LEZIONE 13.pdf#page=10|Lezione 13, pp. 10-11, stampate 117-118]].
