---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 3, PDF pp. 2-8, pagine stampate 22-28"
---

# Matrici come funzioni e indici

Stato: **da studiare**.

## Perché il professore introduce le matrici

Una funzione definita su un prodotto cartesiano di due insiemi finiti può essere rappresentata mediante una tabella. Una scelta determina la riga, l'altra la colonna; nella casella si legge il valore della funzione.

Il passaggio concettuale è:

$$
\text{coppia di indici }(i,j)
\longmapsto
\text{valore nella posizione }(i,j).
$$

## Gli esempi che precedono la definizione

### Media dei voti

Il PDF considera gli insiemi $T$ ed $E$ delle valutazioni di teoria ed esercizi e la funzione

$$
V:T\times E\to\mathbb N,\qquad
V(t,e)=\left\lceil\frac{30}{100}t+\frac{70}{100}e\right\rceil.
$$

Le parentesi superiori indicano l'arrotondamento per eccesso al più piccolo intero maggiore o uguale alla media. Per esempio, con $t=16$ ed $e=18$:

$$
0{,}3\cdot16+0{,}7\cdot18
=4{,}8+12{,}6=17{,}4,
\qquad V(16,18)=18.
$$

Nella tabella del PDF, le righe corrispondono alla teoria e le colonne agli esercizi. I valori oltre 30 sono rappresentati nella tabella con l'indicazione 30L; la gestione dell'esame è raccolta in [[01 Courses/2026-2027/Semester 1/Algebra Lineare/02 Exam Book|Preparazione all'esame]].

### Probabilità congiunta di moneta e dado

Per $M=\{T,C\}$ e $D=\{1,\ldots,6\}$ il professore rappresenta in una tabella $2\times6$ la probabilità di ogni coppia:

$$
P:M\times D\to[0,1],\qquad P(m,d)=\frac1{12}.
$$

La prima riga contiene le sei probabilità degli esiti con testa e la seconda quelle con croce.

Per ottenere $1/12$ si assume il modello con moneta e dado equi e lanci indipendenti:

$$
P(m,d)=\frac12\cdot\frac16=\frac1{12}.
$$

La sola equità marginale, senza indipendenza, non basta a determinare tutte le probabilità congiunte. Questa condizione è esplicitata dal tutor.

### Grafico e funzione indicatrice

Per una funzione $f:A\to B$:

$$
\Gamma(f)=\{(a,b)\in A\times B\mid b=f(a)\}.
$$

Si può registrare l'appartenenza al grafico con una funzione a valori numerici:

$$
\nu:A\times B\to\{0,1\},\qquad
\nu(a,b)=
\begin{cases}
1,&(a,b)\in\Gamma(f),\\
0,&(a,b)\notin\Gamma(f).
\end{cases}
$$

Per $f:\mathbb R\to\mathbb R$, $f(x)=x^2$, il dominio di $\nu$ è $\mathbb R^2$. L'indicatrice vale 1 sui punti della parabola e 0 sugli altri punti del piano; questo esempio ha dominio infinito e non dà una matrice finita.

### Iniziali dei frutti

Nell'esempio finito della Lezione 3, $f$ associa ad arancia, limone e lampone la propria iniziale. La tabella del PDF è:

| Lettera \ Frutto | arancia | lampone | limone |
|---|---|---|---|
| $a$ | 1 | 0 | 0 |
| $b$ | 0 | 0 | 0 |
| $l$ | 0 | 1 | 1 |

Qui il professore dispone le lettere sulle righe e i frutti sulle colonne: la casella della riga $b$ e della colonna $a$ contiene $\nu(a,b)$. L'ordine di presentazione della tabella va quindi distinto dall'ordine degli argomenti di $\nu$.

## Definizione 3.1

Per interi positivi $m,n$, si pone

$$
[m]=\{1,\ldots,m\},\qquad [n]=\{1,\ldots,n\}.
$$

Una **matrice di tipo $(m,n)$ a valori in un campo $\mathbb K$** è una funzione

$$
A:[m]\times[n]\longrightarrow\mathbb K.
$$

Il dominio contiene le posizioni, mentre il codominio contiene i valori ammessi. Il significato di campo e gli esempi del PDF sono in [[12 Campi Numerici e Campo F2]].

## Entrate e notazione

Si scrive

$$
a_{ij}=A(i,j),
$$

dove $i$ è l'indice di riga e $j$ l'indice di colonna:

$$
A=
\begin{pmatrix}
a_{11}&a_{12}&\cdots&a_{1n}\\
a_{21}&a_{22}&\cdots&a_{2n}\\
\vdots&\vdots&\ddots&\vdots\\
a_{m1}&a_{m2}&\cdots&a_{mn}
\end{pmatrix}.
$$

Si indica con $M_{\mathbb K}(m,n)$ l'insieme di tutte queste matrici. Il numero delle entrate è $mn$.

![[11 Matrice Righe Colonne e Indici.svg|920]]

Lo schema del tutor evidenzia $a_{23}=6$: si sceglie prima la riga 2, poi la colonna 3. L'indice di riga aumenta verso il basso nella tabella. Non va interpretato come l'ascissa di un punto del piano.

## Casi particolari

| Dimensioni | Nome | Corrispondenza usata nel corso |
|---|---|---|
| $1\times1$ | matrice con una sola entrata | $M_{\mathbb K}(1,1)\leftrightarrow\mathbb K$ |
| $1\times n$ | vettore riga di lunghezza $n$ | $M_{\mathbb K}(1,n)\leftrightarrow\mathbb K^n$ |
| $m\times1$ | vettore colonna di altezza $m$ | $M_{\mathbb K}(m,1)\leftrightarrow\mathbb K^m$ |
| $n\times n$ | matrice quadrata di ordine $n$ | $M_{\mathbb K}(n,n)=M_{\mathbb K}(n)$ |

Per esempio:

$$
\begin{pmatrix}1&2&3\end{pmatrix}\in M_{\mathbb R}(1,3),
\qquad
\begin{pmatrix}1\\2\\3\end{pmatrix}\in M_{\mathbb R}(3,1).
$$

Entrambe possono essere associate alla lista $(1,2,3)$, ma hanno dimensioni diverse. Le identificazioni con $\mathbb K^n$ sono [[09 Biiettività|biiezioni]]; non autorizzano a scambiare righe e colonne durante un'operazione.

## Da dire all'orale

> Una matrice di tipo m per n su un campo K è una funzione dall'insieme delle coppie di indici di riga e colonna a K. La sua entrata a con indici i e j è il valore della funzione nella posizione i, j.

## Collegamenti e fonte

- [[01 Prodotto Cartesiano]], [[05 Funzioni]], [[10 Prodotti Cartesiani di Più Insiemi]].
- [[13 Uguaglianza e Somma di Matrici]] e [[14 Prodotto di una Matrice per uno Scalare]].
- Fonte: [[GAL 2026-2027 - 20260930 - LEZIONE 3.pdf#page=2|Lezione 3, pp. 2-8, stampate 22-28]]; esempi 1-4 e definizione 3.1.
