---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 6, PDF pp. 2-3, stampate 46-47"
  - "Lezione 7, PDF pp. 2-4, stampate 63-65"
---

# Matrici invertibili

Stato: **da studiare**.

## Definizione 6.1

Per $A\in M_{\mathbb K}(m,n)$:

- una inversa destra è una matrice $B\in M_{\mathbb K}(n,m)$ tale che $AB=I_m$;
- una inversa sinistra è una matrice $C\in M_{\mathbb K}(n,m)$ tale che $CA=I_n$;
- $A$ è invertibile se possiede sia una inversa destra sia una inversa sinistra.

Le dimensioni delle identità sono imposte dai prodotti. Un'inversa destra da sola non coincide con la definizione di invertibilità bilatera per matrici rettangolari.

## Proposizione 6.2 e dimostrazione

**Ipotesi:** $A$ ha una inversa destra $B$ e una sinistra $C$.

**Tesi:** le due inverse coincidono e l'inversa è unica.

Si usano esclusivamente identità e associatività:

$$
\begin{aligned}
B&=I_nB\\
&=(CA)B &&\text{poiché }CA=I_n,\\
&=C(AB) &&\text{per associatività},\\
&=CI_m &&\text{poiché }AB=I_m,\\
&=C.
\end{aligned}
$$

Se esistessero due inverse bilatere $B$ e $D$, si potrebbe considerare $B$ come inversa destra e $D$ come inversa sinistra. Lo stesso argomento darebbe $B=D$.

L'unica inversa si indica con $A^{-1}$. Non è la matrice ottenuta prendendo il reciproco delle singole entrate.

## Il ruolo della forma quadrata

Una matrice con inversa bilatera deve essere quadrata. Usando i risultati sul [[27 Calcolo del Rango con Gauss|rango]]:

$$
m=r(I_m)=r(AB)\le r(A)\le n,
$$

e analogamente $n=r(CA)\le r(A)\le m$. Quindi $m=n$.

Questa conseguenza è un'integrazione del tutor, da leggere dopo le proprietà del rango. Per matrici quadrate su un campo, l'esistenza di una sola inversa laterale implica anche quella dell'altra; il criterio equivalente è il rango massimo.

## Esempio rettangolare

$$
A=\begin{pmatrix}1&0\end{pmatrix},
\qquad B=\begin{pmatrix}1\\0\end{pmatrix}.
$$

Allora $AB=I_1$, ma

$$
BA=\begin{pmatrix}1&0\\0&0\end{pmatrix}\ne I_2.
$$

$B$ è un'inversa destra di $A$. Non è un'inversa bilatera.

## Esempio quadrato verificato dal tutor

$$
A=\begin{pmatrix}1&1\\0&1\end{pmatrix},
\qquad B=\begin{pmatrix}1&-1\\0&1\end{pmatrix}.
$$

$$
AB=\begin{pmatrix}1&-1+1\\0&1\end{pmatrix}=I_2,
\qquad
BA=\begin{pmatrix}1&1-1\\0&1\end{pmatrix}=I_2.
$$

Quindi $B=A^{-1}$.

## Cancellazione con ipotesi

Se $A$ è invertibile e $AX=AY$, moltiplicare a sinistra per $A^{-1}$ dà $X=Y$.

Se $XA=YA$, occorre moltiplicare a destra. Invertire l'ordine dei fattori non è consentito.

Per una matrice $A$ arbitraria, da $XA=A$ non si può concludere $X=I$: se $A=0$, l'uguaglianza vale per ogni $X$.

## Calcolo tramite operazioni elementari

Le operazioni di riga sono reversibili e si rappresentano mediante matrici invertibili. Se una sequenza porta $A$ a $I_n$, il prodotto $T$ delle matrici delle operazioni soddisfa $TA=I_n$ ed è l'inversa.

Un esempio completo con la matrice affiancata all'identità è in [[06 Gauss Rango Determinante e Inversa]]. È un'integrazione operativa del tutor alla codifica spiegata nella Lezione 7.

## Da dire all'orale

> Una matrice è invertibile se ammette un'inversa per il prodotto sia a destra sia a sinistra. Le due inverse coincidono per associatività e l'inversa bilatera è unica.

## Collegamenti e fonti

- [[19 Proprietà del Prodotto e Matrice Identità]].
- [[26 Matrici Elementari e Reversibilità del MEG]], [[29 Calcolo del Determinante con Gauss]].
- [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=2|Lezione 6, pp. 2-3, stampate 46-47]].
- [[GAL 2026-2027 - 20261008 - LEZIONE 7.pdf#page=2|Lezione 7, pp. 2-4, stampate 63-65]].

## Seguito nella Lezione 10

[[35 Ricerca della Matrice Inversa con Gauss]] sviluppa il calcolo per colonne, il caso $2\times2$ anche con primo elemento nullo e le inverse laterali rettangolari. Per una matrice quadrata, il Teorema 10.3 collega invertibilità, rango massimo e determinante non nullo; il criterio è in [[29 Calcolo del Determinante con Gauss]].

Fonte aggiuntiva: [[GAL 2026-2027 - 20261014 - LEZIONE 10.pdf#page=6|Lezione 10, pp. 6-14, stampate 87-95]].
