---
course: Algebra Lineare
type: summary
status: da studiare
mastery: non verificata
created: 2026-11-03
updated: 2026-11-03
aliases:
  - Riassunto GAL
  - Mega riassunto GAL
---

# Riassunto completo di GAL

Riassunto dei **49 concetti di Geometria e Algebra Lineare**, fino alla **Lezione 15 del 28 ottobre 2026**, comprese basi, dimensione, estrazione e completamento.

Il percorso del corso è questo: **insiemi e funzioni → matrici → Gauss, rango e determinante → sistemi lineari → spazi vettoriali e affini → basi e dimensione**. Ogni parte dà un linguaggio più generale a quella precedente.

Indice di riferimento: [[01 Courses/2026-2027/Semester 1/Algebra Lineare/Concepts/00 Concept Index|Indice dei concetti di GAL]].

**1. Il prodotto cartesiano costruisce tutte le combinazioni ordinate.**

Dati due insiemi $A$ e $B$:

$$
A\times B=\{(a,b):a\in A,\ b\in B\}.
$$

Gli elementi sono **coppie ordinate**: la posizione delle componenti conta.

$$
(a,b)=(c,d)\iff a=c\ \text{e}\ b=d.
$$

Per esempio, se $A=\{1,2\}$ e $B=\{a,b\}$:

$$
A\times B=\{(1,a),(1,b),(2,a),(2,b)\}.
$$

Da ricordare:

- In generale $A\times B\ne B\times A$.
- Se uno dei due insiemi è vuoto, il prodotto è vuoto.
- Per insiemi finiti, $\#(A\times B)=\#A\cdot\#B$.

Con più insiemi si ottengono terne, quadruple e liste ordinate:

$$
A_1\times\cdots\times A_n
=\{(a_1,\ldots,a_n):a_i\in A_i\}.
$$

In particolare, $\mathbb K^n$ è l'insieme delle liste ordinate di $n$ elementi del campo $\mathbb K$.

La coppia annidata $((a,b),c)$ e la terna $(a,b,c)$ hanno forme diverse, ma esiste una biiezione naturale che associa l'una all'altra.

Riferimenti: [[01 Prodotto Cartesiano]], [[10 Prodotti Cartesiani di Più Insiemi]].

**2. Una relazione seleziona alcune coppie del prodotto cartesiano.**

Una **relazione binaria** tra $A$ e $B$ è un sottoinsieme:

$$
R\subseteq A\times B.
$$

Scrivere $aRb$ significa che $(a,b)\in R$.

Quando $R\subseteq A\times A$, possiamo studiare queste proprietà:

| Proprietà | Significato |
|---|---|
| Riflessività | Ogni elemento è in relazione con sé stesso: $aRa$. |
| Simmetria | Da $aRb$ segue $bRa$. |
| Antisimmetria | Da $aRb$ e $bRa$ segue $a=b$. |
| Transitività | Da $aRb$ e $bRc$ segue $aRc$. |

Una relazione è di **equivalenza** se è riflessiva, simmetrica e transitiva. Per esempio, su $\mathbb Z$, «avere la stessa parità» è un'equivalenza.

Una relazione è di **ordine** se è riflessiva, antisimmetrica e transitiva. Esempi sono $\le$ sui reali e $\subseteq$ tra insiemi.

L'antisimmetria permette collegamenti nei due versi soltanto tra elementi uguali. **Non è la negazione della simmetria**: l'uguaglianza soddisfa entrambe.

Un ordine può essere **parziale**: non tutti gli elementi devono essere confrontabili. Per esempio, né $\{1\}\subseteq\{2\}$ né $\{2\}\subseteq\{1\}$.

Per dimostrare una proprietà si ragiona su elementi arbitrari; per smentirla basta un controesempio.

Riferimenti: [[02 Relazioni Binarie]], [[03 Relazioni di Equivalenza]], [[04 Relazioni di Ordine]].

**3. Un'implicazione distingue condizioni necessarie e sufficienti.**

La scrittura

$$
P\implies Q
$$

significa che ogni volta che vale $P$, deve valere $Q$.

- $P$ è una condizione **sufficiente** per $Q$.
- $Q$ è una condizione **necessaria** per $P$.

La **contrapposta** è logicamente equivalente:

$$
(P\implies Q)\iff(\neg Q\implies\neg P).
$$

L'implicazione inversa $Q\implies P$, invece, richiede una dimostrazione separata.

Esempio: se una relazione è una funzione con dominio finito $A$, il suo grafico ha $\#A$ coppie. Avere $\#A$ coppie, però, non garantisce che sia una funzione: un ingresso potrebbe comparire due volte e un altro mai.

Riferimento: [[06 Implicazione e Contrapposizione]].

**4. Una funzione assegna esattamente un risultato a ogni ingresso.**

Una funzione $f:A\to B$ è una relazione tale che:

$$
\forall a\in A,\qquad \exists!b\in B:\ f(a)=b.
$$

Le due richieste sono:

- **Esistenza:** ogni elemento del dominio deve avere un'immagine.
- **Unicità:** lo stesso ingresso non può avere due immagini diverse.

Si distinguono:

$$
\begin{aligned}
A&=\text{dominio},\\
B&=\text{codominio},\\
\operatorname{Im}f&=\{f(a):a\in A\}=\text{immagine}.
\end{aligned}
$$

L'immagine è un sottoinsieme del codominio e può essere più piccola.

Il grafico è:

$$
\Gamma(f)=\{(a,f(a)):a\in A\}\subseteq A\times B.
$$

Riferimento: [[05 Funzioni]].

**5. Iniettività, suriettività e biiettività descrivono come vengono raggiunti gli elementi del codominio.**

| Proprietà | Definizione | Intuizione |
|---|---|---|
| Iniettiva | $f(a_1)=f(a_2)\implies a_1=a_2$ | Ogni risultato proviene da **al massimo un ingresso**. |
| Suriettiva | $\forall b\in B,\ \exists a\in A:f(a)=b$ | Ogni elemento del codominio viene raggiunto. |
| Biiettiva | $\forall b\in B,\ \exists!a\in A:f(a)=b$ | Ogni elemento del codominio proviene da **esattamente un ingresso**. |

Per smentire l'iniettività trovi due ingressi distinti con la stessa immagine. Per smentire la suriettività trovi un elemento del codominio mai raggiunto.

La funzione $x\mapsto x^2$ mostra quanto contino dominio e codominio:

- $\mathbb R\to\mathbb R$: non è iniettiva e non è suriettiva.
- $\mathbb R\to[0,+\infty)$: è suriettiva, ma non iniettiva.
- $[0,+\infty)\to[0,+\infty)$: è biiettiva.

Una biiezione ammette una **funzione inversa** $f^{-1}:B\to A$.

L'insieme delle controimmagini

$$
f^{-1}(\{b\})=\{a\in A:f(a)=b\}
$$

si può invece definire anche senza biiettività: può essere vuoto oppure contenere più elementi.

Riferimenti: [[07 Iniettività]], [[08 Suriettività]], [[09 Biiettività]].

**6. Una matrice è una funzione su una coppia di indici.**

Una matrice con $m$ righe e $n$ colonne a valori in $\mathbb K$ è formalmente una funzione:

$$
A:[m]\times[n]\to\mathbb K,
\qquad A(i,j)=a_{ij}.
$$

Si scrive $A\in M_{\mathbb K}(m,n)$.

Nell'entrata $a_{ij}$:

- $i$ indica la **riga**;
- $j$ indica la **colonna**.

Una matrice $m\times n$ ha $mn$ entrate. I casi particolari sono vettori riga $1\times n$, vettori colonna $m\times1$ e matrici quadrate $n\times n$.

Il **campo** stabilisce quali scalari utilizziamo e le regole del calcolo. Negli appunti compaiono $\mathbb Q$, $\mathbb R$, $\mathbb C$ e $\mathbb F_2$.

In un campo ogni scalare diverso da zero ha un inverso moltiplicativo. Per questo si può dividere per un pivot non nullo.

Nel campo $\mathbb F_2=\{0,1\}$ si calcola modulo $2$:

$$
1+1=0,\qquad 1\cdot1=1.
$$

La somma corrisponde a XOR e il prodotto ad AND. Inoltre:

$$
-A=A,\qquad A+A=0.
$$

**Il campo può cambiare il risultato di un esercizio**, compresi rango e indipendenza.

Riferimenti: [[11 Matrici come Funzioni e Indici]], [[12 Campi Numerici e Campo F2]].

**7. Somma e prodotto per scalare si calcolano entrata per entrata.**

Due matrici sono uguali se hanno le stesse dimensioni e tutte le entrate corrispondenti uguali.

Per matrici dello stesso tipo:

$$
(A+B)_{ij}=a_{ij}+b_{ij},
\qquad
(\lambda A)_{ij}=\lambda a_{ij}.
$$

La somma è associativa e commutativa; la matrice nulla è il neutro e $-A$ è l'opposta.

Per il prodotto per scalare valgono:

$$
\begin{aligned}
\lambda(A+B)&=\lambda A+\lambda B,\\
(\lambda+\mu)A&=\lambda A+\mu A,\\
(\lambda\mu)A&=\lambda(\mu A),\\
1A&=A.
\end{aligned}
$$

Queste proprietà permettono anche di scegliere procedure meno costose. Per matrici $m\times n$:

- Calcolare $\lambda(A+B)$ richiede $mn$ somme e $mn$ prodotti.
- Calcolare separatamente $\lambda A+\lambda B$ richiede $mn$ somme e $2mn$ prodotti.

Il risultato coincide; cambia il lavoro necessario per ottenerlo.

Riferimenti: [[13 Uguaglianza e Somma di Matrici]], [[14 Prodotto di una Matrice per uno Scalare]], [[15 Proprietà e Costo dei Calcoli Matriciali]].

**8. Il prodotto matriciale combina righe e colonne.**

Se $A$ è $m\times n$ e $B$ è $n\times p$, allora:

$$
AB\in M_{\mathbb K}(m,p),
\qquad
(AB)_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}.
$$

La regola delle dimensioni è:

$$
(m\times n)(n\times p)\longrightarrow m\times p.
$$

Per ottenere l'entrata $(i,j)$ moltiplichi le componenti corrispondenti della riga $i$ di $A$ e della colonna $j$ di $B$, poi sommi.

Attenzione all'ordine:

- Riga per colonna: risultato $1\times1$.
- Colonna per riga: risultato generalmente con più righe e colonne.

Il prodotto è associativo e distributivo:

$$
(AB)C=A(BC),\qquad
A(B+C)=AB+AC,\qquad
(A+B)C=AC+BC.
$$

La matrice identità soddisfa:

$$
I_mA=A=AI_n.
$$

**In generale il prodotto non è commutativo:** $AB$ può essere diverso da $BA$, oppure uno dei due può non essere definito.

Inoltre possono esistere matrici non nulle con prodotto nullo:

$$
\begin{pmatrix}1&0\\0&0\end{pmatrix}
\begin{pmatrix}0&0\\0&1\end{pmatrix}
=0.
$$

Di conseguenza, da $AB=AC$ non puoi cancellare automaticamente $A$: servono ulteriori ipotesi.

Riferimenti: [[16 Prodotto Matriciale Righe per Colonne]], [[19 Proprietà del Prodotto e Matrice Identità]].

**9. Il prodotto rappresenta operazioni successive e percorsi.**

Nella convenzione del corso, le **colonne rappresentano le partenze** e le **righe gli arrivi**.

Se $A$ rappresenta $f$ e $B$ rappresenta $g$, la composizione $g\circ f$ è rappresentata da:

$$
BA.
$$

Prima agisce la matrice più a destra:

$$
B(Ax)=(BA)x.
$$

Nelle matrici di transizione:

$$
g_{ij}=\Pr(\text{arrivare in }i\mid\text{partire da }j).
$$

Le entrate sono non negative e ogni colonna somma a $1$:

$$
g_{ij}\ge0,\qquad \sum_i g_{ij}=1.
$$

L'entrata $(G^2)_{ij}$ somma le probabilità di tutti i percorsi in due passi $j\to k\to i$:

$$
(G^2)_{ij}=\sum_k g_{ik}g_{kj}.
$$

Se $x^{(0)}$ è la distribuzione iniziale:

$$
x^{(q)}=G^q x^{(0)}.
$$

Nel modello didattico di PageRank:

$$
G=pT+(1-p)K,
$$

dove $T$ descrive la navigazione tramite collegamenti e $K$ la scelta uniforme di una pagina. Le potenze descrivono le visite dopo più passi; le questioni sulla stabilizzazione richiedono un'analisi ulteriore.

Riferimenti: [[17 Prodotto Matriciale e Composizione]], [[18 PageRank e Matrici di Transizione]].

**10. L'inversa permette di annullare l'effetto di una matrice.**

Per $A$ di tipo $m\times n$:

- Un'inversa destra $B$ soddisfa $AB=I_m$.
- Un'inversa sinistra $C$ soddisfa $CA=I_n$.

Se esistono entrambe, coincidono:

$$
C=C(AB)=(CA)B=B.
$$

L'inversa bilatera è quindi unica e si indica con $A^{-1}$. Una matrice con inversa bilatera deve essere quadrata.

Per matrici quadrate su un campo, basta l'esistenza di una sola inversa laterale: vale anche l'altra uguaglianza.

Per matrici rettangolari può invece esistere soltanto un'inversa laterale:

$$
\begin{aligned}
A\text{ ha inversa destra}&\iff r(A)=m,\\
A\text{ ha inversa sinistra}&\iff r(A)=n.
\end{aligned}
$$

L'inversa **non** si ottiene prendendo il reciproco di ogni entrata.

Riferimento: [[20 Matrici Invertibili]].

**11. Il rango misura quanta informazione indipendente contiene una matrice.**

Negli appunti il rango viene introdotto come il minimo numero di prodotti **colonna per riga** necessari per scrivere la matrice:

$$
r(A)=\min\left\{q:A=\sum_{\ell=1}^{q}C_\ell R_\ell\right\}.
$$

Per esempio:

$$
\begin{pmatrix}1&2\\2&4\end{pmatrix}
=
\begin{pmatrix}1\\2\end{pmatrix}
\begin{pmatrix}1&2\end{pmatrix}
$$

ha rango $1$: basta un prodotto, e la matrice non è nulla.

Per ogni matrice $m\times n$:

$$
0\le r(A)\le\min(m,n),
\qquad
r(A)=0\iff A=0.
$$

Le interpretazioni che si collegano durante il corso sono:

$$
\boxed{
\begin{aligned}
r(A)
&=\text{numero di pivot dopo Gauss}\\
&=\dim\operatorname{Span}(\text{colonne})\\
&=\dim\operatorname{Span}(\text{righe}).
\end{aligned}
}
$$

Per matrici moltiplicabili:

$$
r(AB)\le\min(r(A),r(B)).
$$

Nell'applicazione alle probabilità, una tabella congiunta reale, non negativa e normalizzata ha rango $1$ esattamente quando le due variabili sono indipendenti: la tabella fattorizza nel prodotto delle marginali.

Riferimenti: [[21 Rango e Prodotti Colonna per Riga]], [[27 Calcolo del Rango con Gauss]].

**12. Il determinante associa uno scalare a una matrice quadrata.**

Per una matrice $2\times2$:

$$
\det\begin{pmatrix}a&b\\c&d\end{pmatrix}=ad-bc.
$$

Per ordini maggiori si usa lo **sviluppo di Laplace**. Fissando una riga $i$:

$$
\det A=\sum_{j=1}^{n}a_{ij}(-1)^{i+j}\det\widehat A_{ij}.
$$

Qui:

- $\widehat A_{ij}$ si ottiene eliminando la riga $i$ e la colonna $j$.
- $\det\widehat A_{ij}$ è il minore.
- $(-1)^{i+j}\det\widehat A_{ij}$ è il cofattore.

Si può sviluppare lungo qualsiasi riga o colonna; conviene sceglierne una con molti zeri. I segni seguono lo schema:

$$
\begin{pmatrix}
+&-&+\\
-&+&-\\
+&-&+
\end{pmatrix}.
$$

Una matrice è **diagonale** se tutte le entrate fuori dalla diagonale principale sono nulle. È triangolare superiore se ha zeri sotto la diagonale, inferiore se li ha sopra.

Per ogni matrice triangolare:

$$
\boxed{\det T=t_{11}t_{22}\cdots t_{nn}.}
$$

Per matrici reali $2\times2$, $|\det A|$ è anche l'area del parallelogramma formato dalle colonne.

Riferimenti: [[22 Determinante e Sviluppo di Laplace]], [[23 Matrici Diagonali e Triangolari]].

**13. Le proprietà del determinante spiegano come cambia durante i calcoli.**

Il determinante è **lineare rispetto a una singola riga o colonna**, tenendo ferme le altre.

Le proprietà principali sono:

$$
\det I_n=1,
\qquad
\det(AB)=\det A\,\det B.
$$

La seconda è il **teorema di Binet**, per matrici quadrate dello stesso ordine.

Inoltre:

- Due righe o due colonne uguali implicano determinante nullo.
- Una riga o colonna nulla implica determinante nullo.
- Se le righe o le colonne sono dipendenti, il determinante è nullo.

Moltiplicando tutta una matrice $n\times n$ per $\lambda$:

$$
\det(\lambda A)=\lambda^n\det A.
$$

Il determinante non è lineare rispetto all'intera matrice: in generale,

$$
\det(A+B)\ne\det A+\det B.
$$

Se $A$ è invertibile:

$$
\det(A^{-1})=\frac1{\det A}.
$$

Riferimento: [[28 Teorema di Binet e Proprietà del Determinante]].

**14. Gauss trasforma la matrice in una forma da cui si leggono le informazioni essenziali.**

Le operazioni elementari sono:

| Operazione | Condizione | Effetto sul determinante |
|---|---|---|
| Scambiare due righe | — | Cambia segno. |
| Moltiplicare una riga per $\lambda$ | $\lambda\ne0$ | Moltiplica il determinante per $\lambda$. |
| Sommare a una riga un multiplo di un'altra | Righe diverse | Lascia invariato il determinante. |

Sono tutte **reversibili** e conservano il rango.

Il **pivot** di una riga non nulla è il suo primo elemento non nullo. Una matrice è **a scala** quando i pivot si spostano strettamente verso destra scendendo tra le righe, e le righe nulle sono tutte in fondo.

I pivot non devono necessariamente essere $1$.

Gauss procede scegliendo un pivot non nullo, portandolo nella posizione utile e annullando gli elementi sotto di esso:

$$
R_i\leftarrow R_i-\frac{a}{p}R_{\text{pivot}}.
$$

Si ripete sulla parte rimanente. Alla fine:

$$
r(A)=\text{numero di pivot}.
$$

Ogni operazione si può rappresentare con una **matrice elementare** moltiplicata a sinistra:

$$
U=E_s\cdots E_1A=TA,
$$

con $T$ invertibile. Questa reversibilità spiega perché il rango viene conservato.

Se $A$ è quadrata, $U$ è triangolare. Per ricostruire il determinante originale bisogna registrare scambi e riscalamenti. Con $s$ scambi e riscalamenti $\lambda_1,\ldots,\lambda_t$:

$$
\det A=
\frac{(-1)^s}{\lambda_1\cdots\lambda_t}
\prod_{i=1}^{n}u_{ii}.
$$

Si arriva così al collegamento centrale, per $A$ quadrata $n\times n$:

$$
\boxed{
A\text{ invertibile}
\iff r(A)=n
\iff\det A\ne0.
}
$$

Riferimenti: [[24 Operazioni Elementari e Metodo di Gauss]], [[25 Pivot e Matrici a Scala]], [[26 Matrici Elementari e Reversibilità del MEG]], [[29 Calcolo del Determinante con Gauss]].

**15. Un sistema lineare cerca una combinazione delle colonne uguale al termine noto.**

Un sistema con $m$ equazioni e $n$ incognite si scrive:

$$
Ax=b,
\qquad
A\in M_{\mathbb K}(m,n),\quad
x\in\mathbb K^n,\quad b\in\mathbb K^m.
$$

Se $C_1,\ldots,C_n$ sono le colonne di $A$:

$$
Ax=b
\iff
x_1C_1+\cdots+x_nC_n=b.
$$

Le incognite sono quindi i coefficienti di una combinazione lineare.

Per risolverlo si applica Gauss alla **matrice completa**:

$$
[A\mid b]\longrightarrow[U\mid c].
$$

Ogni operazione deve coinvolgere anche il termine noto.

Una riga

$$
[0\ \cdots\ 0\mid c],\qquad c\ne0,
$$

significa $0=c$, quindi il sistema è impossibile.

Se non ci sono contraddizioni:

- Le colonne pivot di $U$ individuano le variabili da ricavare.
- Le altre variabili sono libere.
- Si assegnano parametri alle variabili libere e si risale per sostituzione.

Le colonne delle variabili libere possono essere intercalate a quelle pivot: non sono necessariamente le ultime.

Con parametri nei coefficienti, bisogna separare i casi **prima di dividere per un'espressione che potrebbe annullarsi**.

Riferimenti: [[30 Sistemi Lineari e Rappresentazioni Matriciali]], [[31 Risoluzione dei Sistemi con Gauss e Parametri]].

**16. Rouché-Capelli stabilisce esistenza e numero dei parametri liberi.**

Il teorema afferma:

$$
\boxed{
Ax=b\text{ è compatibile}
\iff r(A)=r([A\mid b]).
}
$$

Con $n$ incognite:

| Ranghi | Conseguenza |
|---|---|
| $r(A)<r([A\mid b])$ | Nessuna soluzione. |
| $r(A)=r([A\mid b])=n$ | Una sola soluzione. |
| $r(A)=r([A\mid b])=r<n$ | Soluzioni con $n-r$ parametri liberi. |

Il numero di parametri è **numero delle incognite meno rango**.

Su $\mathbb R$, se ci sono parametri liberi, le soluzioni sono infinite. Su un campo finito con $q$ elementi, invece, sono esattamente:

$$
q^{n-r}.
$$

Per esempio, su $\mathbb F_2$, due parametri liberi danno quattro soluzioni.

Contare soltanto equazioni e incognite non basta a stabilire la compatibilità: bisogna considerare anche termini noti e ridondanze.

Riferimento: [[32 Teorema di Rouché-Capelli]].

**17. Il nucleo contiene le direzioni lungo cui puoi muoverti senza cambiare il risultato.**

Il **nucleo** di $A:m\times n$ è:

$$
\ker A=\{x\in\mathbb K^n:Ax=0\}.
$$

È l'insieme delle soluzioni del sistema omogeneo associato, che è sempre compatibile perché contiene $0$.

La sua dimensione è:

$$
\boxed{\dim\ker A=n-r(A).}
$$

Se $Ax=b$ è compatibile e $x_p$ è una soluzione particolare, tutte le soluzioni sono:

$$
\boxed{x=x_p+h,\qquad h\in\ker A.}
$$

La ragione è:

$$
Ax=Ax_p=b\implies A(x-x_p)=0.
$$

Viceversa, $A(x_p+h)=b$ per ogni $h\in\ker A$.

Per esempio:

$$
x+y+z=1
$$

ha soluzioni

$$
\begin{pmatrix}x\\y\\z\end{pmatrix}
=
\begin{pmatrix}1\\0\\0\end{pmatrix}
+s\begin{pmatrix}-1\\1\\0\end{pmatrix}
+t\begin{pmatrix}-1\\0\\1\end{pmatrix}.
$$

Il primo vettore sceglie una posizione; gli altri due descrivono le direzioni del nucleo.

Un sistema compatibile ha soluzione unica esattamente quando $\ker A=\{0\}$.

Riferimento: [[33 Nucleo e Struttura delle Soluzioni]].

**18. Cramer e Gauss permettono di trovare soluzioni e inverse.**

Se $A$ è quadrata con $\det A\ne0$, il sistema $Ax=b$ ha una sola soluzione per ogni $b$:

$$
x=A^{-1}b.
$$

La formula di Cramer è:

$$
x_j=\frac{\det A_j(b)}{\det A},
$$

dove $A_j(b)$ si ottiene sostituendo la **colonna $j$** di $A$ con $b$.

Per calcolare l'inversa si affianca l'identità e si applicano le stesse operazioni a entrambi i blocchi:

$$
\boxed{
[A\mid I_n]\longrightarrow[I_n\mid A^{-1}].
}
$$

Per arrivare all'identità bisogna normalizzare i pivot e annullare anche le entrate sopra di essi.

Per una matrice $2\times2$:

$$
\boxed{
\begin{pmatrix}a&b\\c&d\end{pmatrix}^{-1}
=
\frac1{ad-bc}
\begin{pmatrix}d&-b\\-c&a\end{pmatrix}
}
$$

purché $ad-bc\ne0$.

Riferimenti: [[34 Teorema di Cramer e Soluzione Unica]], [[35 Ricerca della Matrice Inversa con Gauss]].

**19. Gli insiemi affini sono descritti da vincoli oppure da un punto e delle direzioni.**

Un sistema compatibile descrive un insieme:

$$
S=\{x:Ax=b\}=P+\ker A.
$$

Le **equazioni cartesiane** impongono vincoli alle coordinate. Le **equazioni parametriche** costruiscono i punti:

$$
x=P+t_1v_1+\cdots+t_dv_d.
$$

Se le direzioni sono una base del nucleo, $d$ è il numero effettivo dei parametri:

$$
d=n-r(A).
$$

Una retta ha forma

$$
x=P+tv,\qquad v\ne0.
$$

Un piano ha forma

$$
x=P+sv+tw,
$$

con $v,w$ indipendenti. Se sono proporzionali e almeno uno è non nullo, i due parametri descrivono soltanto una retta.

In $\mathbb R^3$ una retta richiede due vincoli lineari indipendenti; un piano ne richiede uno.

Esempio:

$$
\begin{cases}
x+y+z=2,\\
x-y+z=0
\end{cases}
\iff
\begin{pmatrix}x\\y\\z\end{pmatrix}
=
\begin{pmatrix}1\\1\\0\end{pmatrix}
+t\begin{pmatrix}-1\\0\\1\end{pmatrix}.
$$

Equivalentemente, la retta è descritta da $y=1$ e $x+z=1$.

Un insieme affine $P+H$ è un sottospazio vettoriale quando contiene l'origine, cioè quando $P\in H$. Guardare soltanto se il punto scelto $P$ è nullo non basta.

Riferimenti: [[36 Spazi Affini ed Equazioni Cartesiane e Parametriche]], [[37 Rette e Piani tra Parametri e Vincoli]].

**20. Uno spazio vettoriale raccoglie oggetti che si sommano e si moltiplicano per scalari con le stesse regole.**

Uno spazio vettoriale $V$ su $\mathbb K$ possiede operazioni:

$$
+:V\times V\to V,
\qquad
\cdot:\mathbb K\times V\to V.
$$

Gli otto assiomi richiedono:

1. Associatività della somma.
2. Commutatività della somma.
3. Esistenza del vettore nullo.
4. Esistenza dell'opposto di ogni vettore.
5. $\lambda(u+v)=\lambda u+\lambda v$.
6. $(\lambda+\mu)v=\lambda v+\mu v$.
7. $(\lambda\mu)v=\lambda(\mu v)$.
8. $1v=v$.

Da questi seguono:

$$
0v=0_V,\qquad
\lambda0_V=0_V,\qquad
(-1)v=-v.
$$

Inoltre:

$$
\lambda v=0_V
\iff
\lambda=0\ \text{oppure}\ v=0_V.
$$

Questa proprietà riguarda il prodotto di **uno scalare per un vettore**; per il prodotto tra matrici abbiamo visto che la situazione è diversa.

I vettori possono essere:

- Liste di numeri in $\mathbb K^n$.
- Matrici in $M_{\mathbb K}(m,n)$.
- Polinomi.
- Funzioni su uno stesso dominio, con operazioni puntuali.
- Successioni, con operazioni termine per termine.
- Vettori geometrici liberi.

Per parlare di spazio vettoriale devi specificare **insieme, campo e operazioni**. Gli assiomi, da soli, non definiscono lunghezze, angoli o distanze.

Riferimenti: [[38 Spazi Vettoriali e Assiomi]], [[39 Esempi di Spazi Vettoriali]], [[40 Proprietà Elementari degli Spazi Vettoriali]].

**21. Un sottospazio deve contenere lo zero ed essere chiuso rispetto alle operazioni.**

Un sottoinsieme $H\subseteq V$ è un sottospazio se:

$$
\begin{aligned}
&0_V\in H,\\
&u,v\in H\implies u+v\in H,\\
&v\in H,\ \lambda\in\mathbb K\implies\lambda v\in H.
\end{aligned}
$$

Equivalentemente, $H$ deve essere non vuoto e contenere ogni combinazione $\alpha u+\beta v$ dei propri elementi.

Esempi:

- $\ker A$.
- Rette e piani per l'origine.
- Polinomi di grado al massimo $d$.
- Funzioni continue su un intervallo fissato.

**Contenere lo zero è necessario, ma non sufficiente.**

L'unione dei due assi cartesiani contiene lo zero, però:

$$
(1,0),(0,1)\in H,
\qquad
(1,0)+(0,1)=(1,1)\notin H.
$$

Quindi non è un sottospazio.

Anche «grado al massimo $d$» va distinto da «grado esattamente $d$»: quest'ultimo insieme non contiene il polinomio nullo e non è un sottospazio.

Riferimento: [[41 Sottospazi Vettoriali e Criterio di Chiusura]].

**22. Lo span raccoglie tutte le combinazioni lineari; i generatori devono produrre tutto lo spazio dichiarato.**

Una combinazione lineare di $v_1,\ldots,v_s$ è:

$$
\lambda_1v_1+\cdots+\lambda_sv_s.
$$

Lo **span** è l'insieme di tutte queste combinazioni:

$$
\operatorname{Span}(v_1,\ldots,v_s)
=
\left\{\sum_{i=1}^{s}\lambda_iv_i:\lambda_i\in\mathbb K\right\}.
$$

È sempre un sottospazio ed è il più piccolo sottospazio che contiene i vettori dati.

I vettori sono **generatori di $V$** quando:

$$
V=\operatorname{Span}(v_1,\ldots,v_s).
$$

La proprietà dipende dall'ambiente: un vettore non nullo genera la propria retta, ma non tutto $\mathbb R^3$.

Mettendo vettori di $\mathbb K^m$ come colonne:

$$
A=[v_1\mid\cdots\mid v_s],
$$

otteniamo:

$$
b\in\operatorname{Span}(v_1,\ldots,v_s)
\iff
A\lambda=b\text{ è compatibile}.
$$

Per generare tutto $\mathbb K^m$ serve:

$$
\boxed{r(A)=m.}
$$

Lo stesso metodo vale per polinomi e matrici: prima li scrivi mediante coefficienti dei monomi oppure entrate, poi risolvi un sistema scalare.

Riferimenti: [[42 Combinazioni Lineari e Span]], [[43 Generatori e Sistemi Lineari]].

**23. L'indipendenza lineare esclude rappresentazioni ridondanti.**

Una famiglia $v_1,\ldots,v_s$ è indipendente se:

$$
\boxed{
\lambda_1v_1+\cdots+\lambda_sv_s=0
\implies
\lambda_1=\cdots=\lambda_s=0.
}
$$

È dipendente se esiste una relazione nulla con coefficienti **non tutti nulli**.

Se nella relazione $\lambda_j\ne0$, puoi isolare:

$$
v_j=-\sum_{i\ne j}\frac{\lambda_i}{\lambda_j}v_i.
$$

Quel vettore è quindi ricostruibile dagli altri e può essere eliminato senza cambiare lo span.

Per $A=[v_1\mid\cdots\mid v_s]$:

$$
\boxed{
v_1,\ldots,v_s\text{ indipendenti}
\iff
\ker A=\{0\}
\iff
r(A)=s.
}
$$

Da ricordare:

- Una famiglia che contiene il vettore nullo è dipendente.
- Un solo vettore è indipendente se e solo se è non nullo.
- Due vettori sono dipendenti quando uno è multiplo dell'altro.
- Tre vettori possono essere dipendenti anche senza coppie proporzionali.

Per esempio:

$$
(1,0)+(0,1)-(1,1)=0.
$$

Riferimento: [[44 Dipendenza e Indipendenza Lineare]].

**24. Una base garantisce esistenza e unicità delle rappresentazioni.**

Una famiglia è una **base di $V$** quando genera $V$ ed è indipendente.

| Proprietà | Che cosa garantisce |
|---|---|
| Generazione | Ogni vettore di $V$ ha una rappresentazione. |
| Indipendenza | Ogni vettore dello span ha al massimo una rappresentazione. |
| Base | Ogni vettore di $V$ ha esattamente una rappresentazione. |

Fissata una base ordinata $\mathcal B=(b_1,\ldots,b_d)$:

$$
v=\lambda_1b_1+\cdots+\lambda_db_d.
$$

Le coordinate sono:

$$
[v]_{\mathcal B}
=
\begin{pmatrix}\lambda_1\\\vdots\\\lambda_d\end{pmatrix}.
$$

Sono uniche **rispetto alla base scelta**. Cambiando base, generalmente cambiano le coordinate.

Per esempio, in $\mathbb R^2$:

$$
(3,1)=2(1,1)+(1,-1).
$$

Quindi rispetto alla base $\mathcal B=((1,1),(1,-1))$:

$$
[(3,1)]_{\mathcal B}=
\begin{pmatrix}2\\1\end{pmatrix}.
$$

Il vettore resta lo stesso; cambia il modo di descriverlo.

Riferimento: [[45 Basi e Unicità delle Coordinate]].

**25. La dimensione è il numero di elementi di una base, indipendentemente dalla base scelta.**

Il **lemma fondamentale** afferma, per famiglie finite dello stesso spazio:

$$
\boxed{
\#(\text{famiglia indipendente})
\le
\#(\text{famiglia generatrice}).
}
$$

Se uno spazio è generato da $m$ vettori, ogni famiglia con più di $m$ vettori è dipendente.

Applicando il lemma a due basi, una volta in un verso e una volta nell'altro, si dimostra che hanno lo stesso numero di elementi. Perciò è ben definita:

$$
\dim_{\mathbb K}V=\text{numero di vettori di una base}.
$$

Se $\dim V=d<\infty$:

- Più di $d$ vettori sono necessariamente dipendenti.
- Meno di $d$ vettori non possono generare $V$.
- Esattamente $d$ vettori sono una base se sono indipendenti **oppure** se sono generatori.

Le basi canoniche principali sono:

| Spazio | Base canonica | Dimensione |
|---|---|---|
| $\mathbb K^n$ | $e_1,\ldots,e_n$ | $n$ |
| $M_{\mathbb K}(m,n)$ | Matrici $E_{ij}$ con un solo $1$ | $mn$ |
| $\mathbb K[t]_{\le d}$ | $1,t,\ldots,t^d$ | $d+1$ |
| $\{0\}$ | Famiglia vuota | $0$ |

La dimensione conta i coefficienti indipendenti necessari per descrivere un vettore, non il numero di elementi dello spazio. $\mathbb R^2$ ha infiniti elementi e dimensione $2$.

Uno spazio è **finitamente generato** se ammette una famiglia finita di generatori.

Tutti i polinomi $\mathbb K[t]$ non sono finitamente generati: fissati finitissimi polinomi, esiste un limite superiore finito dei loro gradi e nessuna loro combinazione può produrre un monomio di grado superiore.

Riferimenti: [[46 Lemma Fondamentale e Teorema della Dimensione]], [[47 Basi Canoniche e Spazi Finitamente Generati]].

**26. Estrarre una base significa eliminare le ridondanze conservando lo span.**

Ci sono due metodi da distinguere:

| Metodo | Risultato |
|---|---|
| Vettori per righe, poi Gauss | Le righe non nulle finali sono una base dello stesso span. |
| Vettori per colonne, poi Gauss di riga | Le colonne **originali** con gli indici dei pivot sono una base estratta dai dati. |

Nel metodo delle righe potresti ottenere vettori nuovi, diversi da quelli iniziali.

Nel metodo delle colonne:

1. Formi $A=[v_1\mid\cdots\mid v_s]$.
2. Applichi Gauss.
3. Individui gli indici delle colonne pivot.
4. Prendi le colonne corrispondenti della matrice **iniziale**.

Le operazioni di riga conservano le relazioni tra colonne, ma possono cambiarne lo spazio generato. Per questo le colonne trasformate non sostituiscono automaticamente quelle originali nella risposta.

Esempio degli appunti:

$$
w_1=\begin{pmatrix}0\\2\\1\end{pmatrix},\quad
w_2=\begin{pmatrix}4\\1\\2\end{pmatrix},\quad
w_3=\begin{pmatrix}4\\-3\\0\end{pmatrix}.
$$

Poiché $w_3=w_2-2w_1$, e i primi due sono indipendenti, $(w_1,w_2)$ è una base dello span, che ha dimensione $2$.

Riferimento: [[48 Estrazione di una Base con Gauss]].

**27. Completare una base significa aggiungere le direzioni mancanti.**

Se $\dim V=d<\infty$ e hai $k$ vettori indipendenti, puoi completarli a una base aggiungendo esattamente $d-k$ vettori.

Ogni nuovo vettore deve stare **fuori dallo span di quelli già scelti**. Essere semplicemente diverso dagli altri non basta.

In $\mathbb K^n$ puoi procedere così:

$$
A=[v_1\mid\cdots\mid v_k\mid e_1\mid\cdots\mid e_n].
$$

Applichi Gauss senza scambiare colonne e scegli le colonne originali con indici pivot. I vettori iniziali indipendenti vengono conservati; i pivot successivi indicano quali canonici aggiungere.

Esempio:

$$
v_1=(1,0,1),\qquad v_2=(0,1,1).
$$

Generano il piano $z=x+y$. Il vettore $e_1=(1,0,0)$ è fuori da quel piano, quindi:

$$
(v_1,v_2,e_1)
$$

è una base di $\mathbb R^3$.

Una famiglia iniziale dipendente non può essere completata a una base conservandone tutti i vettori: la relazione di dipendenza rimarrebbe.

Riferimento: [[49 Completamento di Vettori Indipendenti a una Base]].

**28. Il fac-simile combina prodotti, sistemi, sottospazi e basi nello stesso problema.**

In [[01 Fac-simile Matrici e Sottospazi del 28 ottobre 2026]] è fissata:

$$
B=\begin{pmatrix}1&2\\3&6\end{pmatrix}.
$$

Si considera:

$$
V=\{A\in M_{\mathbb R}(2,2):BA=0\}.
$$

Scrivendo $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, la condizione diventa:

$$
a+2c=0,\qquad b+2d=0.
$$

Quindi:

$$
A=
s\begin{pmatrix}-2&0\\1&0\end{pmatrix}
+t\begin{pmatrix}0&-2\\0&1\end{pmatrix}.
$$

Le due matrici sono indipendenti: formano una base e $\dim V=2$.

Per

$$
W=\operatorname{Span}(BE_{11},BE_{12},BE_{21},BE_{22}),
$$

si eliminano i generatori ridondanti e si trova:

$$
W=
\left\{
\begin{pmatrix}u&v\\3u&3v\end{pmatrix}:u,v\in\mathbb R
\right\},
\qquad \dim W=2.
$$

Infine, imporre $A_1+A_2=I_2$, con $A_1\in V$ e $A_2\in W$, significa risolvere un sistema sulle quattro entrate. Si ottiene:

$$
I_2=
\underbrace{\frac17
\begin{pmatrix}6&-2\\-3&1\end{pmatrix}}_{\in V}
+
\underbrace{\frac17
\begin{pmatrix}1&2\\3&6\end{pmatrix}}_{\in W}.
$$

Il metodo da riconoscere negli esercizi è:

| Richiesta | Operazione da fare |
|---|---|
| Verificare che un insieme sia un sottospazio | Controllare zero e chiusura per combinazioni lineari. |
| Stabilire se $b$ appartiene a uno span | Risolvere $A\lambda=b$. |
| Verificare l'indipendenza | Risolvere $A\lambda=0$ e cercare soluzioni non nulle. |
| Trovare base e dimensione di un nucleo | Risolvere $Ax=0$ e leggere le direzioni dei parametri liberi. |
| Estrarre una base dai vettori dati | Scegliere le colonne originali con indici pivot. |
| Completare una famiglia indipendente | Aggiungere vettori che aumentano il rango. |
| Trovare coordinate in una base | Risolvere $[b_1\mid\cdots\mid b_d]\lambda=v$. |
| Decomporre un vettore tra due sottospazi | Scrivere una combinazione delle rispettive basi e confrontare le coordinate. |
