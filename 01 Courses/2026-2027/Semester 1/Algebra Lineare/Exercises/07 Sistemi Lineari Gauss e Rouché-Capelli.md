---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 9, PDF pp. 2-9, stampate 74-81"
  - "Esempi aggiuntivi del tutor, indicati nelle sezioni"
---

# Sistemi lineari: Gauss e Rouché-Capelli

Stato: **da studiare**. Soluzioni preparate dal tutor, non svolgimenti attribuiti allo studente.

## 1 Dalle equazioni alla soluzione

**Fonte:** sistema della Lezione 9, p. 2; calcolo della soluzione esplicitato dal tutor.

$$
\begin{cases}x-3y=2,\\4x+5y=1.\end{cases}
$$

La matrice completa e l'eliminazione sono

$$
\begin{bmatrix}1&-3&2\\4&5&1\end{bmatrix}
\xrightarrow{R_2\leftarrow R_2-4R_1}
\begin{bmatrix}1&-3&2\\0&17&-7\end{bmatrix}.
$$

L'ultima riga dà $y=-7/17$. La prima dà

$$
x=2+3y=2-\frac{21}{17}=\frac{13}{17}.
$$

Entrambe le matrici, dei coefficienti e completa, hanno rango 2. Non ci sono parametri liberi. La verifica nelle due equazioni è in [[30 Sistemi Lineari e Rappresentazioni Matriciali]].

## 2 Discussione completa dei due parametri

**Fonte:** Lezione 9, pp. 4-5.

$$
\begin{bmatrix}3&-2&1\\6&a&b\end{bmatrix}
\longrightarrow
\begin{bmatrix}3&-2&1\\0&a+4&b-2\end{bmatrix}.
$$

La seconda riga si ottiene sottraendo due volte la prima a **tutte** le entrate della seconda.

| Condizione | $r(A)$ | $r([A\mid b])$ | Soluzioni |
|---|---|---|---|
| $a\ne-4$ | 2 | 2 | $y=(b-2)/(a+4)$, $x=(a+2b)/(3(a+4))$ |
| $a=-4,\ b=2$ | 1 | 1 | $(x,y)=(1/3,0)+t(2/3,1)$ |
| $a=-4,\ b\ne2$ | 1 | 2 | nessuna |

Nel caso compatibile con rango 1, $t\in\mathbb R$. Nel caso impossibile la riga finale è $0=b-2$ con membro destro non nullo.

Per il caso $a\ne-4$ la sostituzione nell'equazione generale controlla entrambe le formule:

$$
3x-2y
=\frac{a+2b-2(b-2)}{a+4}=1,
$$

$$
6x+ay
=\frac{2(a+2b)+a(b-2)}{a+4}
=\frac{b(a+4)}{a+4}=b.
$$

Geometria e passaggi sono in [[31 Risoluzione dei Sistemi con Gauss e Parametri]].

## 3 Colonne pivot non consecutive

**Fonte:** esempio del tutor.

Risolvere il sistema già a scala rappresentato da

$$
\begin{bmatrix}
1&2&0&-1&3\\
0&0&1&4&2\\
0&0&0&0&0
\end{bmatrix}.
$$

I coefficienti occupano quattro colonne. I pivot sono nelle colonne 1 e 3, quindi $r=2$ e le incognite libere sono $x_2=s$, $x_4=t$.

$$
x_3=2-4t,\qquad x_1=3-2s+t.
$$

La soluzione generale è

$$
x=
\begin{pmatrix}3\\0\\2\\0\end{pmatrix}
+s\begin{pmatrix}-2\\1\\0\\0\end{pmatrix}
+t\begin{pmatrix}1\\0\\-4\\1\end{pmatrix}.
$$

Controllo diretto: $x_1+2x_2-x_4=3-2s+t+2s-t=3$ e $x_3+4x_4=2-4t+4t=2$.

Ogni coppia $(s,t)$ dà una soluzione e ogni soluzione si ritrova scegliendo i suoi valori di $x_2,x_4$.

## 4 Più equazioni che incognite non significa impossibile

**Fonte:** esempio del tutor.

$$
\begin{cases}x+y=1,\\2x+2y=2,\\x-y=0.\end{cases}
$$

$$
\begin{bmatrix}1&1&1\\2&2&2\\1&-1&0\end{bmatrix}
\xrightarrow{\substack{R_2\leftarrow R_2-2R_1\\R_3\leftarrow R_3-R_1}}
\begin{bmatrix}1&1&1\\0&0&0\\0&-2&-1\end{bmatrix}.
$$

Si scambiano le ultime due righe. Il rango comune è 2, uguale al numero delle incognite. Quindi $y=1/2$ e $x=1/2$.

Le tre equazioni sono soddisfatte: $1/2+1/2=1$, il doppio vale 2 e la differenza vale 0. La seconda equazione era ridondante.

## 5 Meno equazioni che incognite non garantisce esistenza

**Fonte:** esempio del tutor.

$$
\begin{cases}x+y+z=0,\\2x+2y+2z=1.\end{cases}
$$

La seconda riga meno due volte la prima dà $0=1$. I ranghi sono $r(A)=1$ e $r([A\mid b])=2$: nessuna soluzione, nonostante ci siano tre incognite e due equazioni.

## 6 Campo finito: un parametro non significa infinite soluzioni

**Fonte:** esempio del tutor, su $\mathbb F_2$.

$$
x+y=1.
$$

Poniamo $y=t\in\{0,1\}$. In questo campo $-t=t$, quindi $x=1+t$.

- $t=0$: $(x,y)=(1,0)$.
- $t=1$: $(x,y)=(0,1)$, perché $1+1=0$.

Sono esattamente due soluzioni, cioè $2^{2-1}$. La struttura con un parametro resta valida, ma cambia il numero di valori che il parametro può assumere.

## Teoria e fonte

- [[30 Sistemi Lineari e Rappresentazioni Matriciali]], [[31 Risoluzione dei Sistemi con Gauss e Parametri]], [[32 Teorema di Rouché-Capelli]].
- [[GAL 2026-2027 - 20261012 - LEZIONE 9.pdf#page=2|Lezione 9, pp. 2-9, stampate 74-81]].
