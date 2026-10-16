---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 9, PDF pp. 4-9, stampate 76-81"
  - "Lezione 10, PDF pp. 2-3, stampate 83-84"
---

# Risoluzione dei sistemi con Gauss e parametri

Stato: **da studiare**.

## Perché Gauss si applica alla matrice completa

Partiamo da $Ax=b$, con $A:m\times n$. Un'operazione elementare di riga è una trasformazione reversibile delle equazioni:

- scambiare due equazioni;
- moltiplicarne una per uno scalare non nullo;
- sommare a un'equazione un multiplo di un'altra.

Deve agire su **tutta la riga di $[A\mid b]$**, compreso il termine noto. Così il nuovo sistema ha esattamente le stesse soluzioni.

Formalmente, se $E$ è una [[26 Matrici Elementari e Reversibilità del MEG|matrice elementare]] invertibile,

$$
Ax=b\iff EAx=Eb.
$$

Il verso inverso usa $E^{-1}$. Ripetendo le operazioni:

$$
[A\mid b]\longrightarrow[U\mid c],\qquad U=TA,\quad c=Tb,
$$

con $T$ invertibile. Una trasformazione di colonna, invece, non è una trasformazione delle sole equazioni e non si esegue senza gestire le incognite.

## Algoritmo operativo

1. Fissare campo e ordine delle incognite.
2. Ridurre la matrice completa a scala.
3. Cercare righe $[0\ \cdots\ 0\mid c_i]$ con $c_i\ne0$: significano $0=c_i$, quindi nessuna soluzione.
4. In assenza di contraddizioni, ignorare le righe interamente nulle.
5. Le colonne con pivot **in $U$** individuano le variabili dipendenti, dette anche variabili pivot.
6. Le altre $n-r$ variabili sono libere: assegnare a ciascuna un parametro arbitrario.
7. Ricavare le variabili pivot con sostituzione all'indietro.

Un pivot nell'ultima colonna di $[U\mid c]$ non corrisponde a un'incognita: segnala incompatibilità.

## Esempio con due parametri del professore

Su $\mathbb R$:

$$
\begin{cases}
3x-2y=1,\\
6x+ay=b.
\end{cases}
\qquad
\begin{bmatrix}3&-2&1\\6&a&b\end{bmatrix}
\xrightarrow{R_2\leftarrow R_2-2R_1}
\begin{bmatrix}3&-2&1\\0&a+4&b-2\end{bmatrix}.
$$

Non dividiamo subito per $a+4$: potrebbe essere zero.

### Caso 1: $a\ne-4$

$$
y=\frac{b-2}{a+4},\qquad
x=\frac{1+2y}{3}=\frac{a+2b}{3(a+4)}.
$$

Entrambe le variabili sono pivot: una sola soluzione per ogni $b$.

### Caso 2: $a=-4$, $b=2$

L'ultima riga è nulla. Rimane $3x-2y=1$; ponendo $y=t$:

$$
\begin{pmatrix}x\\y\end{pmatrix}
=
\begin{pmatrix}1/3\\0\end{pmatrix}
+t\begin{pmatrix}2/3\\1\end{pmatrix},
\qquad t\in\mathbb R.
$$

Le soluzioni sono infinite perché il parametro varia in $\mathbb R$.

### Caso 3: $a=-4$, $b\ne2$

L'ultima equazione è $0=b-2\ne0$: l'insieme delle soluzioni è vuoto.

![[31 Sistemi Lineari e Intersezioni di Rette.svg|1040]]

**Figura del tutor, in scala:** i tre pannelli scelgono rispettivamente $(a,b)=(2,2),(-4,2),(-4,4)$. Le due rette si intersecano in un punto, coincidono oppure sono parallele distinte. I colori distinguono le due equazioni; nel caso coincidente la linea tratteggiata è sovrapposta.

## Perché i parametri descrivono tutte e sole le soluzioni

Se le colonne pivot hanno indici $j_1<\cdots<j_r$, la riga $i$ ha la forma

$$
u_{i,j_i}x_{j_i}+\sum_{j>j_i}u_{ij}x_j=c_i,
\qquad u_{i,j_i}\ne0.
$$

Partendo dall'ultima riga non nulla:

$$
x_{j_i}=\frac{c_i-\sum_{j>j_i}u_{ij}x_j}{u_{i,j_i}}.
$$

Ogni variabile libera può essere assegnata arbitrariamente; la sostituzione determina univocamente le altre. Viceversa, ogni soluzione ha valori per quelle variabili, quindi viene riprodotta dalla costruzione.

Le variabili libere **non devono essere necessariamente le ultime**: nel PDF sono collocate alla fine per semplificare lo schema della dimostrazione.

### Esempio del tutor con colonne pivot non iniziali

$$
\begin{bmatrix}
1&2&0&-1&3\\
0&0&1&4&2\\
0&0&0&0&0
\end{bmatrix}.
$$

Ci sono quattro incognite. I pivot sono nelle colonne 1 e 3, perciò $x_2=s$ e $x_4=t$ sono libere:

$$
x_3=2-4t,\qquad x_1=3-2s+t.
$$

Quindi

$$
x=
\begin{pmatrix}3\\0\\2\\0\end{pmatrix}
+s\begin{pmatrix}-2\\1\\0\\0\end{pmatrix}
+t\begin{pmatrix}1\\0\\-4\\1\end{pmatrix}.
$$

Non si scambia $x_2$ con $x_3$ per comodità: si mantiene l'ordine delle coordinate.

## Campo finito e numero di soluzioni

Se il sistema è compatibile e ha $n-r$ variabili libere, la parametrizzazione mediante le loro coordinate è biiettiva.

- Su un campo infinito: una soluzione se $r=n$, infinite se $r<n$.
- Su un campo finito con $q$ elementi: esattamente $q^{n-r}$ soluzioni.

In particolare, su $\mathbb F_2$ un parametro libero dà due soluzioni, non infinite. È una precisazione del tutor alla formulazione geometrica su $\mathbb R$.

## Da dire all'orale

> Si applica Gauss alla matrice completa. Le operazioni reversibili conservano le soluzioni; una riga con coefficienti nulli e termine noto non nullo rende il sistema impossibile. Altrimenti si assegnano parametri alle colonne non pivot e si determinano le variabili pivot per sostituzione all'indietro.

## Collegamenti e fonti

- [[24 Operazioni Elementari e Metodo di Gauss]], [[25 Pivot e Matrici a Scala]], [[32 Teorema di Rouché-Capelli]].
- [[07 Sistemi Lineari Gauss e Rouché-Capelli]].
- [[GAL 2026-2027 - 20261012 - LEZIONE 9.pdf#page=4|Lezione 9, pp. 4-9, stampate 76-81]].
- [[GAL 2026-2027 - 20261014 - LEZIONE 10.pdf#page=2|Lezione 10, pp. 2-3, stampate 83-84]].
