---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 3, PDF pp. 5-7, pagine stampate 25-27"
---

# Campi numerici e campo F2

Stato: **da studiare**.

## Ruolo del campo

Il campo $\mathbb K$ stabilisce quali valori possono comparire nelle matrici e quali regole si usano nei calcoli. Il professore cita

$$
\mathbb Q,\qquad \mathbb R,\qquad \mathbb C,\qquad \mathbb F_2.
$$

Le entrate delle matrici e gli scalari devono appartenere al campo specificato.

## Richiamo del tutor sulla definizione

Un campo è un insieme dotato di somma e prodotto, entrambi interni all'insieme, con queste proprietà:

- la somma è associativa e commutativa;
- esiste lo zero, neutro per la somma, e ogni elemento ha un opposto;
- il prodotto è associativo e commutativo;
- esiste l'unità $1\ne0$, neutra per il prodotto;
- ogni elemento diverso da zero ha un inverso moltiplicativo;
- il prodotto è distributivo rispetto alla somma.

L'inverso moltiplicativo di $a\ne0$ soddisfa $aa^{-1}=1$. Non si richiede un inverso per zero.

Questo richiamo esplicita il termine «campo»; il PDF introduce soprattutto esempi e le operazioni in $\mathbb F_2$.

## Il campo con due elementi

$$
\mathbb F_2=\{0,1\}.
$$

Somma e prodotto sono quelli indicati dalle seguenti tabelle:

$$
\begin{array}{c|cc}
+&0&1\\ \hline
0&0&1\\
1&1&0
\end{array}
\qquad
\begin{array}{c|cc}
\cdot&0&1\\ \hline
0&0&0\\
1&0&1
\end{array}.
$$

In particolare:

$$
1+1=0,\qquad 1\cdot1=1.
$$

Si possono calcolare somme e prodotti interi e poi prendere il resto modulo 2. Questo spiega perché il risultato appartiene ancora a $\{0,1\}$.

## Interpretazione logica ed elettrica del PDF

Si associa 0 a falso e 1 a vero.

- La somma corrisponde a **XOR**: vero quando è vero esattamente uno dei due ingressi.
- Il prodotto corrisponde a **AND**: vero quando sono veri entrambi gli ingressi.

La somma non è OR inclusivo: in $\mathbb F_2$, due ingressi veri danno somma 0.

Il professore illustra XOR con due deviatori e AND con due interruttori in serie. I circuiti servono a visualizzare le rispettive tabelle di verità.

## Conseguenze per le matrici

In $\mathbb F_2$ ogni elemento coincide con il proprio opposto:

$$
0+0=0,\qquad1+1=0.
$$

Quindi, per ogni matrice $A$ su $\mathbb F_2$,

$$
-A=A,\qquad A+A=0_{m,n}.
$$

Esempio del tutor:

$$
\begin{pmatrix}1&0\\1&1\end{pmatrix}
+
\begin{pmatrix}1&0\\1&1\end{pmatrix}
=
\begin{pmatrix}0&0\\0&0\end{pmatrix}.
$$

Le dimensioni si gestiscono come negli altri campi; cambiano le operazioni sulle entrate.

## Errori da evitare

- Calcolare $1+1=2$ all'interno di $\mathbb F_2$.
- Usare OR al posto di XOR.
- Confondere i due elementi di $\mathbb F_2$ con i reali senza specificare le operazioni.
- Chiamare campo qualsiasi insieme di numeri: per esempio $\mathbb Z$ non è un campo con le operazioni usuali, perché $2$ non ha inverso intero.

## Da dire all'orale

> Il campo F due contiene zero e uno, con somma e prodotto modulo due. La somma di uno con uno è zero; somma e prodotto corrispondono rispettivamente a XOR e AND.

## Collegamenti e fonte

- [[11 Matrici come Funzioni e Indici]].
- [[13 Uguaglianza e Somma di Matrici]] e [[14 Prodotto di una Matrice per uno Scalare]].
- Fonte: [[GAL 2026-2027 - 20260930 - LEZIONE 3.pdf#page=5|Lezione 3, pp. 5-7, stampate 25-27]]. La definizione generale del campo e le conseguenze sulle matrici sono esplicitazioni del tutor.
