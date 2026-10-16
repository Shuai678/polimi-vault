---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 7, PDF pp. 5-6, stampate 66-67"
---

# Calcolo del rango con Gauss

Stato: **da studiare**.

## Proposizione del professore

Se $U$ è una matrice a scala ottenuta da $A$ mediante il MEG:

$$
\boxed{r(A)=r(U)=\text{numero dei pivot di }U.}
$$

Il numero dei pivot coincide con il numero delle righe non nulle. Non si contano tutte le entrate non nulle.

## Perché le operazioni non cambiano il rango

Usiamo la [[21 Rango e Prodotti Colonna per Riga|definizione del rango]]:

$$
A=\sum_{\ell=1}^{r(A)}C_\ell R_\ell.
$$

Se $U=TA$, dove $T$ è la matrice invertibile delle operazioni:

$$
U=\sum_{\ell=1}^{r(A)}(TC_\ell)R_\ell.
$$

Questa decomposizione ha al massimo $r(A)$ addendi, quindi $r(U)\le r(A)$.

Poiché $A=T^{-1}U$, ripetendo il ragionamento si ha $r(A)\le r(U)$. Le due disuguaglianze danno l'uguaglianza.

## Perché una matrice a scala con q pivot ha rango q

La prova seguente esplicita il risultato enunciato nel PDF.

### Limite superiore

Le sole $q$ righe non nulle permettono la decomposizione

$$
U=\sum_{i=1}^{q}e_iR_i(U).
$$

Quindi $r(U)\le q$.

### Indipendenza delle righe non nulle

Qui «indipendenti» significa che una loro combinazione con risultato zero può avere soltanto coefficienti tutti nulli.

Supponiamo

$$
\alpha_1R_1(U)+\cdots+\alpha_qR_q(U)=0.
$$

Se un coefficiente fosse non nullo, scegliamo il primo, $\alpha_i$. Nella colonna del pivot della riga $i$:

- le righe precedenti hanno coefficienti $\alpha_1,\ldots,\alpha_{i-1}$ nulli;
- le righe successive hanno entrata zero, perché i loro pivot sono più a destra;
- rimane soltanto $\alpha_i p_i$.

Ma $\alpha_i p_i\ne0$ nel campo: entrambi i fattori sono non nulli. È una contraddizione. Le $q$ righe sono quindi indipendenti.

### Limite inferiore

Se $U$ fosse somma di $s$ prodotti colonna-riga, ciascuna riga di $U$ sarebbe combinazione delle $s$ righe usate nei prodotti.

Il lemma qui sotto mostra che $q$ righe indipendenti non possono essere generate da meno di $q$ righe. Quindi $s\ge q$. Prendendo il minimo: $r(U)\ge q$.

Le due disuguaglianze concludono $r(U)=q$.

### Lemma algebrico usato nella prova

Se $v_1,\ldots,v_q$ sono indipendenti e tutte sono combinazioni di $s$ righe $w_1,\ldots,w_s$, allora $q\le s$.

Si dimostra per induzione su $s$. Per $s=0$ l'unica combinazione è zero e non può esserci una riga indipendente.

Per $s>0$, se $q=0$ la conclusione è immediata. Altrimenti $v_1\ne0$: nella sua espressione almeno un coefficiente è non nullo. Riordinando le righe generatrici, chiamiamo quel coefficiente $c_{11}$ davanti a $w_1$.

Per ogni $i\ge2$ poniamo

$$
v'_i=v_i-\frac{c_{i1}}{c_{11}}v_1.
$$

Le nuove righe sono combinazioni di $w_2,\ldots,w_s$, perché il coefficiente di $w_1$ si annulla. Sono ancora indipendenti: una relazione fra le $v'_i$, espansa, sarebbe una relazione fra $v_1,\ldots,v_q$, e quindi avrebbe tutti i coefficienti nulli.

Per induzione $q-1\le s-1$, da cui $q\le s$.

## Un'ulteriore proprietà utile

Per matrici moltiplicabili:

$$
r(AB)\le\min(r(A),r(B)).
$$

Da una decomposizione di $A$ si ottiene $AB=\sum C_\ell(R_\ell B)$; da una decomposizione di $B$ si ottiene $AB=\sum(AC_\ell)R_\ell$. Ciascuna fornisce uno dei due limiti.

In particolare $r(I_n)=n$, perché l'identità è a scala con $n$ pivot. Questi risultati giustificano i criteri di [[20 Matrici Invertibili|invertibilità]].

## Esempio del professore

Su $\mathbb R$:

$$
A=\begin{pmatrix}
1&0&-1&2\\
2&0&3&1\\
1&0&4&-1
\end{pmatrix}.
$$

La riduzione completa è in [[06 Gauss Rango Determinante e Inversa]]. Si ottiene

$$
U=\begin{pmatrix}1&0&-1&2\\0&0&5&-3\\0&0&0&0\end{pmatrix},
$$

con due pivot, quindi $r(A)=2$.

## Il campo è parte del problema

Esempio del tutor: $\begin{pmatrix}1&1\\1&-1\end{pmatrix}$ ha rango 2 su $\mathbb R$, ma, interpretando le entrate in $\mathbb F_2$, diventa $\begin{pmatrix}1&1\\1&1\end{pmatrix}$ e ha rango 1.

Non si trasferisce una riduzione numerica da un campo a un altro senza rifare i calcoli.

## Da dire all'orale

> Le operazioni elementari di riga preservano il rango perché sono invertibili. Dopo Gauss il rango è il numero delle righe non nulle, cioè il numero dei pivot della matrice a scala.

## Collegamenti e fonte

- [[21 Rango e Prodotti Colonna per Riga]], [[25 Pivot e Matrici a Scala]], [[26 Matrici Elementari e Reversibilità del MEG]].
- Fonte: [[GAL 2026-2027 - 20261008 - LEZIONE 7.pdf#page=5|Lezione 7, pp. 5-6, stampate 66-67]]. La dimostrazione generale e il lemma sono integrazioni del tutor.
