---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 08, PDF pp. 20-22
  - Lezione 09, PDF pp. 2-3, 14-16
  - Libro, §3.8, pp. 102-103
---

# Notazione o-piccolo

## Intuizione

Dire che un termine è piccolo ha senso soltanto rispetto a una scala. $n$ cresce senza limite, ma è trascurabile rispetto a $n^2$ perché $n/n^2\to0$. La notazione $o$-piccolo esprime questa **trascurabilità relativa**.

## Definizione formale

Siano $(a_n)$ e $(b_n)$ due successioni reali, con $b_n\neq0$ definitivamente. Si scrive, per $n\to+\infty$,

$$
\boxed{a_n=o(b_n)\quad\Longleftrightarrow\quad\frac{a_n}{b_n}\to0.}
$$

Non occorre che entrambe tendano a zero o a infinito. Per esempio

$$
n=o(n^2),\qquad1/n^2=o(1/n),\qquad\sin n=o(n).
$$

Nel terzo caso basta $|\sin n/n|\leq1/n\to0$; il numeratore non ha limite.

### Da dire all'orale

> Una successione è un o-piccolo di un'altra, definitivamente non nulla, quando il rapporto fra la prima e la seconda tende a zero. La notazione indica una quantità trascurabile rispetto alla scala scelta, non necessariamente una quantità che tende a zero in valore assoluto.

## Come leggere una scrittura con resto

La scrittura

$$
a_n=c\,b_n+o(b_n)
$$

significa che esiste un resto $r_n$ tale che

$$
a_n=c\,b_n+r_n,\qquad\frac{r_n}{b_n}\to0.
$$

Il simbolo $o(b_n)$ descrive una **classe di possibili resti**: due occorrenze non rappresentano necessariamente la stessa successione. In particolare non si possono cancellare due simboli $o(b_n)$ come se fossero quantità identiche.

Una forma equivalente e spesso utile è

$$
a_n=o(b_n)\quad\Longleftrightarrow\quad a_n=\varepsilon_n b_n
\text{ con }\varepsilon_n\to0.
$$

Basta porre $\varepsilon_n=a_n/b_n$ nella coda in cui $b_n\neq0$.

## Collegamento con gli ordini

Da [[92 Confronto di Infiniti e Infinitesimi]]:

- per due infiniti, $a_n=o(b_n)$ significa che $a_n$ ha ordine inferiore;
- per due infinitesimi, significa che $a_n$ ha ordine superiore.

Se $a_n/b_n\to\pm\infty$, allora $a_n\neq0$ definitivamente e $b_n/a_n\to0$: si scrive $b_n=o(a_n)$.

## Gerarchia nella notazione del PDF

Per $a>1$, $\alpha>0$ e $\beta>0$ fissati,

$$
(\log_a n)^\beta=o(n^\alpha),\qquad
n^\alpha=o(a^n),\qquad
a^n=o(n!),\qquad
n!=o(n^n).
$$

Queste sono le stesse affermazioni di [[85 Gerarchia degli Infiniti]], formulate come confronti relativi.

## Operazioni utili sui resti

> [!info] Approfondimento dal libro
> Le proprietà dei resti in §3.8, pp. 102-103, si giustificano direttamente dividendo per la scala. Qui si esplicitano le operazioni utili negli esempi della lezione.

Se $r_n=o(b_n)$ e $s_n=o(b_n)$, allora

$$
r_n+s_n=o(b_n),\qquad r_n-s_n=o(b_n),
$$

perché $(r_n\pm s_n)/b_n=r_n/b_n\pm s_n/b_n\to0$. Anche $c\,r_n=o(b_n)$ per ogni costante reale fissata $c$.

Se $r_n=o(b_n)$ e $b_n=o(c_n)$, con le scale definitivamente non nulle,

$$
\frac{r_n}{c_n}=\frac{r_n}{b_n}\frac{b_n}{c_n}\to0,
$$

quindi $r_n=o(c_n)$. Infine, moltiplicando per $d_n\neq0$ definitivamente,

$$
\frac{d_nr_n}{d_nb_n}=\frac{r_n}{b_n}\to0,
$$

ossia $d_nr_n=o(d_nb_n)$. Le condizioni di non nullità servono a definire i rapporti.

## Integrazione della Lezione 09 — Da studiare

Le pp. 14-15 del PDF L9 riprendono le operazioni sui resti presentate sopra. Le nuove identità precisano come leggere le **classi di resti** e come cambiarne la scala.

### $o(1)$ significa infinitesimo

$$
b_n=o(1)\quad\Longleftrightarrow\quad\frac{b_n}{1}\to0
\quad\Longleftrightarrow\quad b_n\to0.
$$

Per una scala $a_n\neq0$ definitivamente,

$$
\boxed{o(a_n)=a_n\,o(1).}
$$

Infatti $r_n=o(a_n)$ equivale a $r_n=a_n\varepsilon_n$ con $\varepsilon_n=r_n/a_n\to0$. Viceversa, ogni prodotto di questa forma è un $o(a_n)$. L'uguaglianza descrive le classi, non identifica un resto particolare.

### Moltiplicare e cambiare la scala

Se $a_n,b_n\neq0$ definitivamente,

$$
\boxed{a_n\,o(b_n)=o(a_nb_n).}
$$

Un verso segue da $(a_nr_n)/(a_nb_n)=r_n/b_n\to0$. Viceversa, se $s_n=o(a_nb_n)$, allora $r_n=s_n/a_n$ soddisfa $r_n/b_n\to0$ e $s_n=a_nr_n$. È quindi un'uguaglianza fra classi.

In particolare, per $c\neq0$ fissato, $c\,o(a_n)=o(a_n)$, e $-o(a_n)=o(a_n)$. Per $c=0$ ogni resto viene annullato: $0\,o(a_n)$ contiene soltanto la successione nulla e non è l'intera classe $o(a_n)$. Resta invece vero che $0r_n=o(a_n)$ per ogni resto $r_n$.

### Assorbimento di resti con scale diverse

Se $b_n=o(a_n)$, allora ogni $r_n=o(b_n)$ è anche $o(a_n)$:

$$
\frac{r_n}{a_n}=\frac{r_n}{b_n}\frac{b_n}{a_n}\to0.
$$

Perciò il resto con la scala più piccola si può assorbire nell'altro. Gli esempi del PDF sono

$$
o(1/n)+o(1/n^2)=o(1/n),\qquad
o(n)+o(n^2)=o(n^2).
$$

Nel primo, $1/n^2=o(1/n)$; nel secondo, $n=o(n^2)$. La somma di due resti nella stessa classe vi appartiene ancora. Queste uguaglianze fra classi ammettono anche il verso opposto: qualunque resto della classe a destra si scrive come sé stesso più il resto nullo dell'altra classe.

### Scale equivalenti producono la stessa classe

Se $a_n\sim b_n$, allora

$$
\boxed{o(a_n)=o(b_n).}
$$

Se $r_n=o(a_n)$, si ha $r_n/b_n=(r_n/a_n)(a_n/b_n)\to0$. Scambiando $a_n$ e $b_n$ si prova il viceversa. Per esempio, da [[95 Equivalenti e Sviluppi Asintotici Notevoli]],

$$
o\!\left(\sin\frac1n\right)=o(1/n).
$$

Queste regole servono per normalizzare i resti negli esercizi di [[96 Calcolo dei Limiti con Equivalenti Asintotici]]. Il fatto che un resto sia $o(n^2)$ non ne determina il limite: il caso conclusivo del PDF è spiegato in [[97 Cancellazioni e Precisione del Resto Asintotico]].

## Esempio del PDF: descrivere il resto di una somma

### Testo

Per $n\geq2$ consideriamo

$$
a_n=7n^{47}+\log n+\log\log n+(\log n)^{18}
+\sin n+n^{18}-1+\arctan(n^2).
$$

### Idea e svolgimento passo per passo

Poniamo $r_n=a_n-7n^{47}$ e controlliamo **ogni** addendo di $r_n/n^{47}$.

$$
\frac{\log n}{n^{47}}\to0,\qquad
\frac{(\log n)^{18}}{n^{47}}
=\left(\frac{\log n}{n^{47/18}}\right)^{18}\to0,
\qquad
\frac{n^{18}}{n^{47}}=\frac1{n^{29}}\to0.
$$

Per $n$ grande, $0\leq\log\log n\leq\log n$, quindi anche il relativo rapporto tende a zero. Infine

$$
\left|\frac{\sin n-1+\arctan(n^2)}{n^{47}}\right|
\leq\frac{2+\pi/2}{n^{47}}\to0.
$$

La somma di questi rapporti tende a zero: $r_n=o(n^{47})$. Dunque

$$
\boxed{a_n=7n^{47}+o(n^{47}).}
$$

### Cosa imparare

La notazione condensa controlli già giustificati. Il resto può essere grande in valore assoluto: contiene $n^{18}$, ma è piccolo rispetto a $n^{47}$.

## Errori comuni e prospettiva d'esame

- Leggere $o(n^{47})$ come “qualcosa che tende a zero”. È il **rapporto con $n^{47}$** a tendere a zero.
- Scrivere $a_n=o(0)$: la scala deve essere definitivamente non nulla.
- Cancellare o dividere due resti senza conoscerne la relazione.
- Concludere $r_n=o(s_n)$ soltanto perché entrambi sono $o(b_n)$: per esempio $1/n$ e $1/n^2$ sono entrambi $o(1)$, ma il rapporto del primo con il secondo diverge.

Potenziale rilevanza d'esame: definizione pronunciabile, controllo del resto e passaggio alla [[94 Equivalenza Asintotica|equivalenza asintotica]].
