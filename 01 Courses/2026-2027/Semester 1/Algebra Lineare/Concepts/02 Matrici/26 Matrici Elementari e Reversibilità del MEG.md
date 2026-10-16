---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 7, PDF pp. 2-4, stampate 63-65"
---

# Matrici elementari e reversibilità del MEG

Stato: **da studiare**.

## Reversibilità delle operazioni

Ogni [[24 Operazioni Elementari e Metodo di Gauss|operazione elementare di riga]] si può annullare:

- lo scambio si annulla ripetendo lo stesso scambio;
- il riscalamento per $\lambda\ne0$ si annulla con $\lambda^{-1}$;
- $R_i\leftarrow R_i+\lambda R_k$ si annulla con $R_i\leftarrow R_i-\lambda R_k$.

Per annullare una sequenza si applicano le operazioni inverse in ordine cronologico inverso.

## La codifica a sinistra

Una matrice elementare $E$ si ottiene applicando una singola operazione alla matrice identità $I_m$. Per ogni matrice $A$ con $m$ righe, il prodotto $EA$ esegue proprio quell'operazione su $A$.

Il fattore è a sinistra perché si combinano le righe. La moltiplicazione a destra riguarda invece le colonne e non rappresenta lo stesso intervento.

## Esempi della Lezione 7

### Scambio delle due righe

$$
S=\begin{pmatrix}0&1\\1&0\end{pmatrix},
\qquad
S\begin{pmatrix}0&1&-1\\1&2&3\end{pmatrix}
=\begin{pmatrix}1&2&3\\0&1&-1\end{pmatrix}.
$$

$S^2=I_2$, quindi $S^{-1}=S$.

### Moltiplicazione della seconda riga

$$
D=\begin{pmatrix}1&0\\0&10^4\end{pmatrix},
\qquad D^{-1}=\begin{pmatrix}1&0\\0&10^{-4}\end{pmatrix}.
$$

Queste matrici eseguono e annullano il riscalamento. Nella Lezione 7 l'esempio usa una seconda riga con entrate $(10^{-8},3,7)$; nella Lezione 6 l'analogo esempio aveva $(10^{-8},4,7)$.

### Sostituzione della seconda riga

$$
E=\begin{pmatrix}1&0\\-4&1\end{pmatrix},
\qquad E^{-1}=\begin{pmatrix}1&0\\4&1\end{pmatrix}.
$$

$$
E\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}
=\begin{pmatrix}1&2&3\\0&-3&-6\end{pmatrix}.
$$

Il coefficiente $-4$ nella posizione $(2,1)$ significa «alla riga 2 somma $-4$ volte la riga 1».

## Forme generali e verifica delle inverse

Per un riscalamento si sostituisce un elemento diagonale di $I_m$ con $\lambda\ne0$; l'inversa ha $\lambda^{-1}$ nella stessa posizione.

Per $i\ne k$, sia $N_{ik}$ la matrice con una sola entrata 1 in posizione $(i,k)$. Allora

$$
E=I_m+\lambda N_{ik}
$$

realizza $R_i\leftarrow R_i+\lambda R_k$. Poiché $N_{ik}^2=0$:

$$
(I_m+\lambda N_{ik})(I_m-\lambda N_{ik})=I_m.
$$

Il prodotto nell'altro ordine dà la stessa identità. Questa verifica vale anche su $\mathbb F_2$.

## Una sequenza completa

Se si eseguono prima $E_1$, poi $E_2$, fino a $E_s$:

$$
U=E_s\cdots E_2E_1A=TA.
$$

Le inverse esplicite danno

$$
T^{-1}=E_1^{-1}E_2^{-1}\cdots E_s^{-1}.
$$

Perciò, ponendo $Z=T^{-1}$:

$$
A=ZU,\qquad ZT=TZ=I_m.
$$

Non si sta affermando che $A$ sia invertibile: le matrici invertibili sono $T$ e $Z$, anche se $A$ è rettangolare o nulla.

## Precisazione sul passaggio a p. 4

Il PDF usa il ragionamento $A=(ZT)A$ per giungere a $ZT=I_m$. Per una sola matrice $A$ fissata questa cancellazione non basta: se $A=0$, qualsiasi prodotto $ZT$ soddisferebbe l'uguaglianza.

La conclusione corretta si giustifica costruendo le matrici inverse delle singole operazioni, come sopra. Si ottengono $ZT=TZ=I_m$ indipendentemente dalla particolare matrice su cui si opera.

## Da dire all'orale

> Ogni operazione elementare di riga è una moltiplicazione a sinistra per una matrice elementare invertibile. Il prodotto di queste matrici codifica il MEG e le inverse, applicate in ordine inverso, ricostruiscono la matrice iniziale.

## Collegamenti e fonte

- [[20 Matrici Invertibili]], [[27 Calcolo del Rango con Gauss]], [[29 Calcolo del Determinante con Gauss]].
- Fonte: [[GAL 2026-2027 - 20261008 - LEZIONE 7.pdf#page=2|Lezione 7, pp. 2-4, stampate 63-65]]. Le forme generali e la precisazione sulla cancellazione sono sviluppate dal tutor.
