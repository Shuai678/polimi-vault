---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 10, PDF p. 5, stampata 86"
  - "Lezione 10, PDF pp. 12-14, stampate 93-95"
---

# Teorema di Cramer e soluzione unica

Stato: **da studiare**.

## Enunciato effettivamente riportato nel PDF

**Teorema 10.2.** Un sistema con $n$ equazioni e $n$ incognite, con matrice dei coefficienti $A$ di rango $n$, ha una e una sola soluzione per ogni $b\in\mathbb K^n$.

$$
A\in M_{\mathbb K}(n,n),\quad r(A)=n
\quad\Longrightarrow\quad
\forall b\in\mathbb K^n,\ \exists!\,x\in\mathbb K^n:Ax=b.
$$

La pagina lo chiama **teorema di Cramer**. Nella pagina consultata viene enunciata l'esistenza e unicità, non viene scritta la formula dei determinanti sostituiti. Tale formula è presentata più sotto come integrazione del tutor.

## Dimostrazione con Rouché-Capelli

La matrice completa ha $n$ righe, quindi rango al massimo $n$. Contiene $A$, il cui rango è già $n$:

$$
n=r(A)\le r([A\mid b])\le n.
$$

La prima disuguaglianza può essere letta anche contando i pivot dopo le stesse operazioni di Gauss: aggiungere l'ultima colonna non elimina i pivot dei coefficienti.

I ranghi sono uguali, quindi il sistema è compatibile. I parametri liberi sono $n-r(A)=0$, dunque la soluzione è unica.

Questo dimostra l'enunciato per **ogni** termine noto, non soltanto per un esempio.

## Rango, determinante e inversa

Il Teorema 10.3 della stessa lezione stabilisce per $A$ quadrata:

$$
\boxed{
A\text{ invertibile}\iff r(A)=n\iff\det A\ne0.
}
$$

La dimostrazione completa, già raccolta senza duplicarla in una nuova nota, è in [[29 Calcolo del Determinante con Gauss]]. La [[35 Ricerca della Matrice Inversa con Gauss|costruzione dell'inversa]] risolve simultaneamente i sistemi $Ax=e_j$.

Se $A$ è invertibile, moltiplicando $Ax=b$ a sinistra per $A^{-1}$:

$$
x=A^{-1}b.
$$

Viceversa, questo vettore è soluzione perché $AA^{-1}b=b$.

Una matrice rettangolare può avere sistemi compatibili con soluzione unica per alcuni termini noti; non si applica però la conclusione «per ogni $b\in\mathbb K^m$» dell'enunciato quadrato senza altre condizioni.

## Formula di Cramer: integrazione dimostrata del tutor

Se $\det A\ne0$, sia $A_j(b)$ la matrice ottenuta da $A$ sostituendo **la colonna $j$** con $b$. Allora

$$
\boxed{x_j=\frac{\det A_j(b)}{\det A},\qquad j=1,\ldots,n.}
$$

### Dimostrazione

Dalla rappresentazione per colonne:

$$
b=x_1C_1(A)+\cdots+x_nC_n(A).
$$

Per multilinearità nella colonna sostituita,

$$
\det A_j(b)=
\sum_{k=1}^n x_k
\det\big(C_1(A),\ldots,C_{j-1}(A),C_k(A),C_{j+1}(A),\ldots,C_n(A)\big).
$$

Se $k\ne j$, due colonne sono uguali e il termine è zero. Per $k=j$ rimane $x_j\det A$. Quindi $\det A_j(b)=x_j\det A$; si divide per $\det A\ne0$.

La formula usa proprietà del [[28 Teorema di Binet e Proprietà del Determinante|determinante]] già dimostrate e resta valida in qualsiasi campo.

## Esempio del tutor

$$
\begin{cases}2x+y=5,\\x-y=1.\end{cases}
\qquad
A=\begin{pmatrix}2&1\\1&-1\end{pmatrix},
\quad \det A=-3.
$$

Sostituendo la prima e la seconda colonna:

$$
\det A_1(b)=
\det\begin{pmatrix}5&1\\1&-1\end{pmatrix}=-6,
\qquad
\det A_2(b)=
\det\begin{pmatrix}2&5\\1&1\end{pmatrix}=-3.
$$

Dunque $x=2$ e $y=1$. Verifica: $2\cdot2+1=5$ e $2-1=1$.

## Errori da evitare

- Il solo fatto che $A$ sia quadrata non garantisce una soluzione unica.
- $\det A=0$ non implica automaticamente impossibilità: possono esserci più soluzioni oppure nessuna.
- Non si divide per un determinante nullo.
- Nella formula si sostituisce una colonna, non una riga scelta arbitrariamente.
- Gauss rimane un metodo risolutivo anche nei casi in cui Cramer non si applica.

## Da dire all'orale

> Per una matrice quadrata di rango massimo, il rango della completa coincide necessariamente con quello dei coefficienti per ogni termine noto. Non ci sono variabili libere, quindi la soluzione è unica. Equivalentemente la matrice è invertibile e ha determinante non nullo.

## Fonti e collegamenti

- [[32 Teorema di Rouché-Capelli]], [[20 Matrici Invertibili]], [[35 Ricerca della Matrice Inversa con Gauss]].
- [[GAL 2026-2027 - 20261014 - LEZIONE 10.pdf#page=5|Lezione 10, p. 5, stampata 86]]: Teorema 10.2.
- [[GAL 2026-2027 - 20261014 - LEZIONE 10.pdf#page=12|Lezione 10, pp. 12-14, stampate 93-95]]: Teorema 10.3.
