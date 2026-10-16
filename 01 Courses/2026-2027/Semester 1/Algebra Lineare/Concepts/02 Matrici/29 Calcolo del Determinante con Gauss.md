---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 6, PDF pp. 10-12, stampate 54-56"
  - "Lezione 7, PDF pp. 7-10, stampate 68-71"
---

# Calcolo del determinante con Gauss

Stato: **da studiare**.

## Strategia

Per $A\in M_{\mathbb K}(n,n)$, il MEG produce una matrice a scala $U$, quindi triangolare superiore. Il suo determinante è

$$
\det U=u_{11}\cdots u_{nn}.
$$

Per risalire a $\det A$ si registra l'effetto di tutte le operazioni usate. Le sostituzioni non cambiano il determinante, gli scambi cambiano il segno e i riscalamenti moltiplicano il valore.

## Formula con il registro delle operazioni

Supponiamo di avere eseguito $s$ scambi e riscalamenti per scalari non nulli $\lambda_1,\ldots,\lambda_t$, oltre a eventuali sostituzioni. Allora

$$
\det U=(-1)^s\left(\prod_{\ell=1}^{t}\lambda_\ell\right)\det A,
$$

quindi

$$
\boxed{
\det A=
\frac{(-1)^s}{\prod_{\ell=1}^{t}\lambda_\ell}
\prod_{i=1}^{n}u_{ii}.
}
$$

Se non si usano riscalamenti, il denominatore è 1. In caratteristica 2, $-1=1$: la formula si interpreta sempre nel campo scelto.

## Collegamento con la codifica del MEG

Scrivendo

$$
U=TA,\qquad A=ZU,\qquad Z=T^{-1},
$$

il [[28 Teorema di Binet e Proprietà del Determinante|teorema di Binet]] dà

$$
\det A=\det Z\det U
=\det Z\,u_{11}\cdots u_{nn}.
$$

Questo è il collegamento presentato dal professore: il registro dei fattori è un modo pratico per calcolare $\det Z$ senza moltiplicare tutte le matrici elementari.

## Esempio completo del tutor

Su $\mathbb R$, sia

$$
A=\begin{pmatrix}0&2&1\\1&1&0\\2&3&4\end{pmatrix}.
$$

### 1 Scambio

$$
R_1\leftrightarrow R_2:
\quad
A_1=\begin{pmatrix}1&1&0\\0&2&1\\2&3&4\end{pmatrix},
\qquad \det A_1=-\det A.
$$

### 2 Eliminazione sotto il primo pivot

$$
R_3\leftarrow R_3-2R_1:
\quad
A_2=\begin{pmatrix}1&1&0\\0&2&1\\0&1&4\end{pmatrix}.
$$

La terza riga diventa $(2-2,\ 3-2,\ 4-0)=(0,1,4)$. Il determinante non cambia.

### 3 Riscalamento

$$
R_2\leftarrow\frac12R_2:
\quad
A_3=\begin{pmatrix}1&1&0\\0&1&\frac12\\0&1&4\end{pmatrix}.
$$

Ora $\det A_3=\frac12\det A_2=-\frac12\det A$.

### 4 Eliminazione sotto il secondo pivot

$$
R_3\leftarrow R_3-R_2:
\quad
U=\begin{pmatrix}1&1&0\\0&1&\frac12\\0&0&\frac72\end{pmatrix}.
$$

Il determinante rimane invariato in questo passo. Quindi

$$
\frac72=\det U=-\frac12\det A
\quad\Longrightarrow\quad \det A=-7.
$$

Il solo prodotto dei pivot avrebbe dato $7/2$: occorre recuperare scambio e riscalamento.

## Verifica indipendente

Sviluppando la matrice iniziale sulla prima riga:

$$
\det A
=-2\det\begin{pmatrix}1&0\\2&4\end{pmatrix}
+\det\begin{pmatrix}1&1\\2&3\end{pmatrix}
=-8+1=-7.
$$

## Interpretazione geometrica in dimensione due

Integrazione del tutor: per una matrice reale $2\times2$, le due colonne sono vettori del piano. Il valore assoluto del determinante è l'area del loro parallelogramma; il segno distingue le due orientazioni.

![[29 Determinante Area e Operazioni di Riga.svg|1040]]

Il disegno è in scala. Per $A=\begin{pmatrix}2&1\\0&2\end{pmatrix}$ l'area è 4:

- sostituire $R_1$ con $R_1+R_2$ manda $(x,y)$ in $(x+y,y)$ e conserva area e segno;
- scambiare le righe scambia le coordinate dei vettori, conservando l'area ma invertendo l'orientazione: il determinante passa da 4 a $-4$.

La figura illustra le proprietà; le giustificazioni algebriche sono in [[28 Teorema di Binet e Proprietà del Determinante]].

## Rango determinante e invertibilità

Per una matrice quadrata $n\times n$:

$$
\boxed{
\det A\ne0
\iff r(A)=n
\iff A\text{ è invertibile}.
}
$$

La prima equivalenza segue da Gauss: una matrice a scala quadrata ha $n$ pivot esattamente quando tutti gli elementi diagonali sono non nulli. Le operazioni preservano il rango e l'annullamento del determinante.

Se $A$ è invertibile, Binet impone $\det A\ne0$.

Viceversa, se $r(A)=n$, dopo Gauss ogni posizione diagonale ha un pivot non nullo. Si possono normalizzare i pivot e annullare le entrate sopra di essi, ottenendo $I_n$ con altre operazioni invertibili. Se $P$ è la matrice di queste operazioni e $U=TA$, si ha $(PT)A=I_n$. Poiché $PT$ è invertibile, $A=(PT)^{-1}$ e l'inversa di $A$ è $PT$.

Questa dimostrazione completa del criterio è un'integrazione del tutor ai risultati delle lezioni.

## Matrici rettangolari

Gauss e il rango si usano anche per matrici rettangolari. Il determinante qui definito, invece, riguarda soltanto le matrici quadrate.

Per una $3\times4$ con tre pivot, il rango è 3; non si forma un determinante della matrice intera e non si conclude che abbia un'inversa bilatera.

## Da dire all'orale

> Per calcolare il determinante con Gauss si riduce la matrice a triangolare, si moltiplicano le entrate diagonali e si corregge il risultato per scambi e riscalamenti. Le somme di multipli di altre righe non modificano il determinante.

## Collegamenti e fonti

- [[23 Matrici Diagonali e Triangolari]], [[24 Operazioni Elementari e Metodo di Gauss]], [[27 Calcolo del Rango con Gauss]].
- [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=10|Lezione 6, pp. 10-12, stampate 54-56]].
- [[GAL 2026-2027 - 20261008 - LEZIONE 7.pdf#page=7|Lezione 7, pp. 7-10, stampate 68-71]].

## Conferma e sviluppo nella Lezione 10

Il criterio $A$ invertibile $\iff r(A)=n\iff\det A\ne0$ è enunciato come **Teorema 10.3** nella [[GAL 2026-2027 - 20261014 - LEZIONE 10.pdf#page=12|Lezione 10, pp. 12-14, stampate 93-95]]. La dimostrazione del professore passa da Binet ai pivot e poi ai sistemi con termini noti canonici.

[[35 Ricerca della Matrice Inversa con Gauss]] riporta anche il passaggio che rende bilatera l'inversa costruita inizialmente a destra, senza duplicare la presente nota. [[34 Teorema di Cramer e Soluzione Unica]] collega il rango massimo all'unicità delle soluzioni.
