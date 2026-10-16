---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 10, PDF pp. 6-14, stampate 87-95"
---

# Ricerca della matrice inversa con Gauss

Stato: **da studiare**.

## Invertire significa risolvere più sistemi

Per $A\in M_{\mathbb K}(n,n)$ cerchiamo $X$ tale che $AX=I_n$. Se $X=[x^{(1)}\mid\cdots\mid x^{(n)}]$:

$$
AX=I_n\iff Ax^{(j)}=e_j\quad\text{per ogni }j,
$$

dove $e_j$ è la colonna con 1 al posto $j$ e 0 altrove.

Sono $n$ sistemi con la **stessa matrice dei coefficienti** e termini noti diversi. Invece di ripetere Gauss, affianchiamo l'identità:

$$
\boxed{[A\mid I_n]\longrightarrow[I_n\mid A^{-1}].}
$$

Si compie l'eliminazione sotto e sopra i pivot e li si normalizza a 1: questa prosecuzione di Gauss viene detta anche Gauss-Jordan.

## Perché il blocco destro è davvero l'inversa

Ogni operazione agisce su entrambi i blocchi. Se il prodotto delle matrici elementari è $T$:

$$
[A\mid I_n]\longrightarrow[TA\mid T].
$$

Se a sinistra si arriva a $I_n$, allora $TA=I_n$. Poiché $T$ è invertibile, $A=T^{-1}$, quindi anche $AT=I_n$. Il blocco destro è l'inversa bilatera.

Se il rango di $A$ è minore di $n$, nessuna sequenza di operazioni invertibili può trasformare il blocco sinistro in $I_n$. Non si dichiara allora inversa il blocco destro di una forma incompleta.

## Derivazione generale per una matrice due per due

Siano

$$
A=\begin{pmatrix}a&b\\c&d\end{pmatrix},
\qquad \Delta=ad-bc.
$$

Supponiamo dapprima $a\ne0$:

$$
\begin{bmatrix}a&b&1&0\\c&d&0&1\end{bmatrix}
\xrightarrow{R_1\leftarrow a^{-1}R_1}
\begin{bmatrix}1&b/a&1/a&0\\c&d&0&1\end{bmatrix}
$$

$$
\xrightarrow{R_2\leftarrow R_2-cR_1}
\begin{bmatrix}1&b/a&1/a&0\\0&\Delta/a&-c/a&1\end{bmatrix}.
$$

Se $\Delta=0$, il sistema corrispondente alla seconda colonna dell'identità contiene $0=1$: non esiste inversa.

Se $\Delta\ne0$, si normalizza la seconda riga e si elimina sopra il secondo pivot:

$$
\begin{bmatrix}1&b/a&1/a&0\\0&1&-c/\Delta&a/\Delta\end{bmatrix}
\xrightarrow{R_1\leftarrow R_1-(b/a)R_2}
\begin{bmatrix}1&0&d/\Delta&-b/\Delta\\0&1&-c/\Delta&a/\Delta\end{bmatrix}.
$$

L'entrata in alto a destra del primo blocco di soluzione si semplifica così:

$$
\frac1a+\frac{bc}{a\Delta}
=\frac{\Delta+bc}{a\Delta}
=\frac{ad}{a\Delta}
=\frac d\Delta.
$$

Quindi

$$
\boxed{A^{-1}=\frac1{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}}
\qquad\text{se }ad-bc\ne0.
$$

### Caso $a=0$, esplicitato dal tutor

Se $\Delta\ne0$, allora $-bc\ne0$, dunque sia $b$ sia $c$ sono non nulli. Si scambiano le righe: il primo pivot diventa $c\ne0$ e l'algoritmo procede.

La formula finale vale anche con $a=0$, come conferma il prodotto nei due ordini:

$$
\begin{pmatrix}a&b\\c&d\end{pmatrix}
\begin{pmatrix}d&-b\\-c&a\end{pmatrix}
=
\begin{pmatrix}\Delta&0\\0&\Delta\end{pmatrix},
$$

$$
\begin{pmatrix}d&-b\\-c&a\end{pmatrix}
\begin{pmatrix}a&b\\c&d\end{pmatrix}
=
\begin{pmatrix}\Delta&0\\0&\Delta\end{pmatrix}.
$$

Se invece $a=0$ e $\Delta=0$, il criterio del determinante esclude l'invertibilità.

## Matrici rettangolari: inverse laterali

Per $A:m\times n$, una candidata inversa laterale è $X:n\times m$.

- Inversa destra: $AX=I_m$, cioè $m$ sistemi $Ax^{(j)}=e_j$. Scritti insieme sono $m^2$ equazioni nelle $nm$ entrate di $X$.
- Inversa sinistra: $XA=I_n$, cioè $n^2$ equazioni nelle stesse $nm$ entrate.

Il conteggio delle equazioni suggerisce possibilità ma **non dimostra l'esistenza**: le equazioni possono essere ridondanti o incompatibili.

Precisazione del tutor con criteri esatti:

$$
A\text{ ha un'inversa destra}\iff r(A)=m,
\qquad
A\text{ ha un'inversa sinistra}\iff r(A)=n.
$$

Per la prima sufficienza, se $r(A)=m$, ogni sistema $Ax=e_j$ è compatibile per Rouché-Capelli; si affiancano le soluzioni. Per la seconda, se $r(A)=n$, Gauss-Jordan dà

$$
PA=\begin{bmatrix}I_n\\0\end{bmatrix}
$$

con $P:m\times m$ invertibile. Prendendo le prime $n$ righe di $P$ si ottiene $L$ con $LA=I_n$.

Per la necessità si usa $r(BC)\le\min(r(B),r(C))$: ogni decomposizione colonna-riga di uno dei fattori induce una decomposizione con al più altrettanti termini del prodotto. Da $AX=I_m$ segue $m\le r(A)\le m$, e analogamente per $XA=I_n$.

Pertanto occorre $m\le n$ per un'inversa destra e $n\le m$ per una sinistra. Averle entrambe forza $m=n$, coerentemente con [[20 Matrici Invertibili]].

## Esempio rettangolare del PDF completato dal tutor

$$
A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}.
$$

Il minore sulle prime due colonne è $5-8=-3\ne0$, quindi $r(A)=2$. Le inverse destre sono

$$
X=
\begin{pmatrix}
-5/3+s&2/3+t\\
4/3-2s&-1/3-2t\\
s&t
\end{pmatrix},
\qquad s,t\in\mathbb R.
$$

Ogni colonna risolve rispettivamente $Ax=e_1$ o $Ax=e_2$, e il prodotto dà $AX=I_2$. I parametri sono indipendenti perché appartengono a due sistemi distinti.

Non esiste un'inversa sinistra. Infatti $h=(1,-2,1)^{\mathsf T}\ne0$ soddisfa $Ah=0$; se $LA=I_3$, avremmo

$$
h=I_3h=LAh=L0=0,
$$

contraddizione.

## Il Teorema 10.3 e la sua dimostrazione

Il ciclo del professore è:

$$
A\text{ invertibile}\Longrightarrow\det A\ne0
\Longrightarrow r(A)=n\Longrightarrow A\text{ invertibile}.
$$

Le prime due implicazioni usano Binet e i pivot della forma triangolare. Per l'ultima, Cramer costruisce $B$ con $AB=I_n$. Da Binet $\det B\ne0$, quindi anche $B$ ha rango $n$ e Cramer costruisce $C$ con $BC=I_n$. Per associatività:

$$
A=A(BC)=(AB)C=C.
$$

Quindi $BA=BC=I_n$: $B$ è l'inversa bilatera di $A$. Il criterio e il collegamento con Gauss sono anche in [[29 Calcolo del Determinante con Gauss]].

## Da dire all'orale

> Le colonne dell'inversa sono le soluzioni dei sistemi che hanno come termini noti le colonne dell'identità. Applicando le stesse operazioni a tutti i sistemi si trasforma $[A\mid I]$ in $[I\mid A^{-1}]$, quando $A$ è quadrata di rango massimo.

## Fonti ed esempi

- [[08 Nucleo Struttura Cramer e Inverse]]: calcoli completi e caso con primo pivot nullo.
- [[GAL 2026-2027 - 20261014 - LEZIONE 10.pdf#page=6|Lezione 10, pp. 6-11, stampate 87-92]].
- [[GAL 2026-2027 - 20261014 - LEZIONE 10.pdf#page=12|Lezione 10, pp. 12-14, stampate 93-95]].
