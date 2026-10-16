---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 10, PDF pp. 2-14, stampate 83-95"
  - "Esempi aggiuntivi del tutor, indicati nelle sezioni"
---

# Nucleo, struttura, Cramer e inverse

Stato: **da studiare**. Soluzioni preparate dal tutor, non svolgimenti attribuiti allo studente.

## 1 Sistema della lezione al variare di $k$

**Fonte:** Lezione 10, pp. 2-3. Operazioni e controlli esplicitati dal tutor.

$$
[A\mid b_k]=
\begin{bmatrix}
5&2&1&1+k\\
2&2&-2&k\\
1&-2&5&1+2k
\end{bmatrix},\qquad k\in\mathbb R.
$$

Scambiamo $R_1$ e $R_3$:

$$
\begin{bmatrix}
1&-2&5&1+2k\\
2&2&-2&k\\
5&2&1&1+k
\end{bmatrix}.
$$

Poi $R_2\leftarrow R_2-2R_1$ e $R_3\leftarrow R_3-5R_1$:

$$
\begin{bmatrix}
1&-2&5&1+2k\\
0&6&-12&-2-3k\\
0&12&-24&-4-9k
\end{bmatrix}.
$$

I nuovi termini noti sono $k-2(1+2k)=-2-3k$ e $1+k-5(1+2k)=-4-9k$.

Infine $R_3\leftarrow R_3-2R_2$:

$$
\begin{bmatrix}
1&-2&5&1+2k\\
0&6&-12&-2-3k\\
0&0&0&-3k
\end{bmatrix}.
$$

Il rango di $A$ è sempre 2. La matrice completa ha rango 2 se $k=0$ e 3 se $k\ne0$.

### $k\ne0$

Compare $0=-3k\ne0$: nessuna soluzione.

### $k=0$

Poniamo $z=t$. La seconda equazione dà

$$
6y-12t=-2\implies y=-\frac13+2t.
$$

La prima dà

$$
x=1+2y-5t
=1-\frac23+4t-5t
=\frac13-t.
$$

Quindi

$$
\boxed{x=
\begin{pmatrix}1/3\\-1/3\\0\end{pmatrix}
+t\begin{pmatrix}-1\\2\\1\end{pmatrix},\qquad t\in\mathbb R.}
$$

### Verifica nell'ordine originale delle equazioni

$$
5(1/3-t)+2(-1/3+2t)+t=1,
$$

$$
2(1/3-t)+2(-1/3+2t)-2t=0,
$$

$$
(1/3-t)-2(-1/3+2t)+5t=1.
$$

La prima parte è una soluzione particolare; la direzione è nel nucleo.

## 2 Calcolare il nucleo della stessa matrice

**Fonte:** matrice dell'esempio precedente; svolgimento del tutor.

Con termine noto zero, la stessa eliminazione dà

$$
\begin{cases}x-2y+5z=0,\\6y-12z=0.\end{cases}
$$

Ponendo $z=t$, si ha $y=2t$ e $x=2y-5z=-t$. Pertanto

$$
\ker(A)=\{t(-1,2,1)^{\mathsf T}:t\in\mathbb R\}.
$$

La direzione non dipende da $k$: varia soltanto la compatibilità del termine noto. Questo è il significato operativo del [[33 Nucleo e Struttura delle Soluzioni|teorema di struttura]].

## 3 Cramer, Gauss e inversa sullo stesso sistema

**Fonte:** esempio del tutor; la formula dei determinanti è un'integrazione rispetto all'enunciato della p. 5.

$$
A=\begin{pmatrix}2&1\\1&-1\end{pmatrix},
\qquad b=\begin{pmatrix}5\\1\end{pmatrix}.
$$

Con Cramer, $\det A=-3$, $\det A_1(b)=-6$, $\det A_2(b)=-3$: $x=2$, $y=1$.

Con Gauss:

$$
\begin{bmatrix}2&1&5\\1&-1&1\end{bmatrix}
\xrightarrow{R_1\leftrightarrow R_2}
\begin{bmatrix}1&-1&1\\2&1&5\end{bmatrix}
\xrightarrow{R_2\leftarrow R_2-2R_1}
\begin{bmatrix}1&-1&1\\0&3&3\end{bmatrix}.
$$

Si ottengono $y=1$, $x=2$.

Con l'inversa:

$$
A^{-1}=-\frac13\begin{pmatrix}-1&-1\\-1&2\end{pmatrix}
=\begin{pmatrix}1/3&1/3\\1/3&-2/3\end{pmatrix},
$$

$$
A^{-1}b=
\begin{pmatrix}5/3+1/3\\5/3-2/3\end{pmatrix}
=\begin{pmatrix}2\\1\end{pmatrix}.
$$

I tre metodi danno la stessa soluzione perché risolvono lo stesso problema; Gauss ha il vantaggio di gestire anche i casi singolari.

## 4 Inversa con primo elemento nullo

**Fonte:** esempio del tutor che completa il caso $a=0$ discusso alle pp. 9-11.

$$
A=\begin{pmatrix}0&2\\1&3\end{pmatrix},\qquad\det A=-2\ne0.
$$

$$
\begin{bmatrix}0&2&1&0\\1&3&0&1\end{bmatrix}
\xrightarrow{R_1\leftrightarrow R_2}
\begin{bmatrix}1&3&0&1\\0&2&1&0\end{bmatrix}
\xrightarrow{R_2\leftarrow R_2/2}
\begin{bmatrix}1&3&0&1\\0&1&1/2&0\end{bmatrix}
$$

$$
\xrightarrow{R_1\leftarrow R_1-3R_2}
\begin{bmatrix}1&0&-3/2&1\\0&1&1/2&0\end{bmatrix}.
$$

Quindi

$$
A^{-1}=\begin{pmatrix}-3/2&1\\1/2&0\end{pmatrix}.
$$

Verifica nei due ordini:

$$
AA^{-1}=
\begin{pmatrix}1&0\\-3/2+3/2&1\end{pmatrix}=I_2,
$$

$$
A^{-1}A=
\begin{pmatrix}1&-3+3\\0&1\end{pmatrix}=I_2.
$$

Non era lecito dividere per l'elemento iniziale $a=0$; era lecito scambiare le righe.

## 5 Tutte le inverse destre della matrice rettangolare

**Fonte:** matrice delle pp. 6-7; calcolo completo del tutor.

$$
A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}.
$$

Con due colonne di termini noti:

$$
\begin{bmatrix}1&2&3&1&0\\4&5&6&0&1\end{bmatrix}
\xrightarrow{R_2\leftarrow R_2-4R_1}
\begin{bmatrix}1&2&3&1&0\\0&-3&-6&-4&1\end{bmatrix}
$$

$$
\xrightarrow{R_2\leftarrow-R_2/3}
\begin{bmatrix}1&2&3&1&0\\0&1&2&4/3&-1/3\end{bmatrix}
\xrightarrow{R_1\leftarrow R_1-2R_2}
\begin{bmatrix}1&0&-1&-5/3&2/3\\0&1&2&4/3&-1/3\end{bmatrix}.
$$

La terza incognita è libera **in ognuno** dei due sistemi. Usiamo $s$ per la prima colonna e $t$ per la seconda:

$$
X=
\begin{pmatrix}
-5/3+s&2/3+t\\
4/3-2s&-1/3-2t\\
s&t
\end{pmatrix}.
$$

Controllo della prima colonna:

$$
(-5/3+s)+2(4/3-2s)+3s=1,
$$

$$
4(-5/3+s)+5(4/3-2s)+6s=0.
$$

Controllo della seconda:

$$
(2/3+t)+2(-1/3-2t)+3t=0,
$$

$$
4(2/3+t)+5(-1/3-2t)+6t=1.
$$

Dunque $AX=I_2$ per tutti $s,t\in\mathbb R$.

Non esiste inversa sinistra perché $h=(1,-2,1)^{\mathsf T}\ne0$ è nel nucleo; una matrice $L$ con $LA=I_3$ darebbe $h=LAh=0$. La motivazione è rigorosa, non il semplice conteggio «9 equazioni contro 6 incognite».

## Teoria e fonte

- [[33 Nucleo e Struttura delle Soluzioni]], [[34 Teorema di Cramer e Soluzione Unica]], [[35 Ricerca della Matrice Inversa con Gauss]].
- [[GAL 2026-2027 - 20261014 - LEZIONE 10.pdf#page=2|Lezione 10, pp. 2-14, stampate 83-95]].
