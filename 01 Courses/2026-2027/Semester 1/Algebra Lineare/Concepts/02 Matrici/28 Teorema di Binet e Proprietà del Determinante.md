---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 7, PDF pp. 7-11, stampate 68-72"
---

# Teorema di Binet e proprietà del determinante

Stato: **da studiare**.

## Proprietà di base

Il PDF enuncia normalizzazione, alternanza e multilinearità. Di seguito le proprietà sono sviluppate usando [[22 Determinante e Sviluppo di Laplace|Laplace]].

### Normalizzazione

$$
\det I_n=1,
$$

perché l'identità è triangolare e tutti gli elementi diagonali sono 1.

### Multilinearità

Tenendo fisse le altre righe, il determinante è lineare nella riga scelta:

$$
\det(\ldots,u+\lambda v,\ldots)
=\det(\ldots,u,\ldots)+\lambda\det(\ldots,v,\ldots).
$$

Nello sviluppo su quella riga, i minori non dipendono dalle sue entrate. Ogni entrata compare quindi al primo grado e le somme si separano.

La stessa proprietà vale per ogni colonna. Non significa che il determinante sia lineare rispetto all'intera matrice.

### Due righe uguali

Se due righe sono uguali, il determinante è zero.

Una prova valida su ogni campo procede per induzione sull'ordine. Per ordine 2:

$$
\det\begin{pmatrix}a&b\\a&b\end{pmatrix}=ab-ba=0.
$$

Per ordine $n>2$, si sceglie una riga diversa dalle due uguali e si sviluppa lungo quella. Ogni minore conserva due righe uguali, quindi ha determinante zero per induzione. Tutti gli addendi sono nulli.

Per due colonne uguali si usa lo stesso ragionamento sviluppando su una colonna diversa dalle due.

### Scambio di due righe

Scambiare due righe cambia il segno del determinante.

Per giustificarlo, si considerano due posizioni con righe $u$ e $v$ e si mette $u+v$ in entrambe. Il determinante è zero perché le due righe sono uguali. Espandendo per multilinearità:

$$
0=D(u,u)+D(u,v)+D(v,u)+D(v,v)
=D(u,v)+D(v,u).
$$

Quindi $D(v,u)=-D(u,v)$. La notazione $D$ sottintende tutte le altre righe fisse. Vale analogamente per le colonne.

## Effetto delle operazioni elementari

| Operazione da $A$ a $B$ | Effetto |
|---|---|
| Scambio di due righe | $\det B=-\det A$ |
| Una riga moltiplicata per $\lambda$ | $\det B=\lambda\det A$ |
| $R_i\leftarrow R_i+\lambda R_k$, $i\ne k$ | $\det B=\det A$ |

L'ultima formula segue dalla multilinearità: il termine aggiuntivo ha la riga $k$ ripetuta, quindi è nullo.

La formula del riscalamento vale anche per $\lambda=0$, ma in quel caso l'operazione non è reversibile e non è ammessa nel MEG.

## Una riga oppure tutta la matrice

Moltiplicando una sola riga per $\lambda$ si ottiene un solo fattore $\lambda$. Moltiplicando tutta una matrice $n\times n$, vengono moltiplicate tutte le $n$ righe:

$$
\boxed{\det(\lambda A)=\lambda^n\det A.}
$$

Su $\mathbb R$, per esempio, $\det(2I_2)=4$, mentre $2\det I_2=2$.

Anche $\det(A+B)=\det A+\det B$ è falsa in generale: con $A=B=I_2$, i due membri valgono 4 e 2.

## Teorema di Binet

**Ipotesi:** $A,B\in M_{\mathbb K}(n,n)$, sullo stesso campo e dello stesso ordine.

**Tesi:**

$$
\boxed{\det(AB)=\det A\,\det B.}
$$

Nel primo membro c'è un prodotto matriciale; nel secondo un prodotto fra elementi del campo.

### Dimostrazione del tutor

Siano $A_1,\ldots,A_n$ le colonne di $A$. La colonna $j$ di $AB$ è $\sum_{k=1}^n b_{kj}A_k$.

Espandendo il determinante per multilinearità in tutte le colonne:

$$
\det(AB)=
\sum_{k_1,\ldots,k_n=1}^n
\left(\prod_{j=1}^n b_{k_j,j}\right)
\det(A_{k_1},\ldots,A_{k_n}).
$$

Se due indici $k_j$ coincidono, due colonne sono uguali e il termine è zero. Restano soltanto gli ordinamenti degli indici $1,\ldots,n$, cioè le permutazioni $\sigma$.

Riordinare le colonne di $A$ cambia il determinante per il segno della permutazione. Si indica con $\operatorname{sgn}(\sigma)$ il numero $+1$ o $-1$ corrispondente alla parità degli scambi:

$$
\det(A_{\sigma(1)},\ldots,A_{\sigma(n)})
=\operatorname{sgn}(\sigma)\det A.
$$

Pertanto:

$$
\det(AB)=\det A
\sum_{\sigma}\operatorname{sgn}(\sigma)
\prod_{j=1}^n b_{\sigma(j),j}.
$$

L'ultima somma è $\det B$: si ottiene espandendo le colonne di $B$ nelle colonne dell'identità e ripetendo lo stesso ragionamento, con $\det I_n=1$.

Segue $\det(AB)=\det A\,\det B$. Questa prova è un'integrazione del tutor; nel PDF il teorema è enunciato.

## Conseguenze del teorema

### Determinanti dei prodotti nei due ordini

Per matrici quadrate dello stesso ordine:

$$
\det(AB)=\det A\det B
=\det B\det A=\det(BA).
$$

Questo non implica $AB=BA$. La commutatività usata al centro riguarda i numeri del campo.

### Inversa

Se $A$ è invertibile:

$$
1=\det I_n=\det(AA^{-1})=\det A\det(A^{-1}).
$$

Quindi $\det A\ne0$ e

$$
\det(A^{-1})=(\det A)^{-1}.
$$

### Annullamento e operazioni di riga

Se $B=TA$ con $T$ invertibile, Binet dà

$$
\det B=\det T\det A.
$$

Poiché $\det T\ne0$, segue

$$
\det B=0\iff\det A=0.
$$

L'annullamento del determinante è preservato da tutte le operazioni elementari, anche quando il valore del determinante cambia.

## Precisazione sul campo con due elementi

All'ultima pagina il PDF ricava il determinante nullo di una matrice con due righe uguali da $2\det A=0$.

Quest'ultimo passaggio consente di dividere per 2 soltanto se $2\ne0$ nel campo. In $\mathbb F_2$ non è lecito: $2=0$.

La proprietà «due righe uguali implicano determinante zero» rimane vera anche in $\mathbb F_2$, come dimostra la prova per induzione riportata sopra, che non divide per 2.

## Da dire all'orale

> Il determinante è multilineare nelle singole righe e colonne, si annulla se due di esse coincidono e cambia segno scambiandole. Il teorema di Binet afferma che il determinante del prodotto di due matrici quadrate dello stesso ordine è il prodotto dei determinanti.

## Collegamenti e fonte

- [[22 Determinante e Sviluppo di Laplace]], [[26 Matrici Elementari e Reversibilità del MEG]].
- [[29 Calcolo del Determinante con Gauss]], [[12 Campi Numerici e Campo F2]].
- Fonte: [[GAL 2026-2027 - 20261008 - LEZIONE 7.pdf#page=7|Lezione 7, pp. 7-11, stampate 68-72]].
