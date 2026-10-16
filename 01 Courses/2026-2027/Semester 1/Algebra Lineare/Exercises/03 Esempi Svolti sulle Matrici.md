---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-10-16
source: esempi originali del tutor
---

# Esempi svolti sulle matrici

Stato: **da studiare**. Tutti i calcoli sono svolgimenti del tutor, non esercizi completati dallo studente.

## 1 Dimensioni indici e combinazione di matrici

### Problema

Siano

$$
A=\begin{pmatrix}1&-2&0\\3&1&4\end{pmatrix},
\qquad
B=\begin{pmatrix}0&2&1\\-1&3&2\end{pmatrix}.
$$

Leggere $a_{23}$ e calcolare $3A-2B$.

### Svolgimento

Entrambe le matrici appartengono a $M_{\mathbb R}(2,3)$: hanno due righe e tre colonne.

$a_{23}$ è l'entrata della seconda riga e terza colonna, dunque $a_{23}=4$.

Si calcolano prima i prodotti per scalare:

$$
3A=\begin{pmatrix}3&-6&0\\9&3&12\end{pmatrix},
\qquad
2B=\begin{pmatrix}0&4&2\\-2&6&4\end{pmatrix}.
$$

Poi si sottraggono le entrate corrispondenti:

$$
\begin{aligned}
3A-2B
&=\begin{pmatrix}
3-0&-6-4&0-2\\
9-(-2)&3-6&12-4
\end{pmatrix}\\
&=\begin{pmatrix}3&-10&-2\\11&-3&8\end{pmatrix}.
\end{aligned}
$$

Il risultato è ancora $2\times3$. Nella posizione $(2,1)$ si sottrae un numero negativo: $9-(-2)=11$.

Prerequisiti: [[11 Matrici come Funzioni e Indici]], [[13 Uguaglianza e Somma di Matrici]], [[14 Prodotto di una Matrice per uno Scalare]].

## 2 Stesso numero di entrate e somma non definita

### Problema

Confrontare

$$
C=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix},
\qquad
D=\begin{pmatrix}1&2\\3&4\\5&6\end{pmatrix}.
$$

### Svolgimento

$C$ è di tipo $(2,3)$ e $D$ è di tipo $(3,2)$. Entrambe hanno sei entrate, ma i domini degli indici sono diversi.

La somma di matrici definita nel corso non consente quindi di formare $C+D$.

Prerequisito: [[13 Uguaglianza e Somma di Matrici]].

## 3 Somma nel campo F2

### Problema

Su $\mathbb F_2$, calcolare la somma di

$$
P=\begin{pmatrix}1&0\\1&1\end{pmatrix},
\qquad
Q=\begin{pmatrix}1&1\\0&1\end{pmatrix}.
$$

### Svolgimento

Si sommano le posizioni corrispondenti usando $1+1=0$:

$$
\begin{aligned}
P+Q
&=\begin{pmatrix}1+1&0+1\\1+0&1+1\end{pmatrix}\\
&=\begin{pmatrix}0&1\\1&0\end{pmatrix}.
\end{aligned}
$$

In questo campo $-P=P$, perché ogni entrata è opposta a se stessa. Inoltre $P+P=0_{2,2}$.

Prerequisito: [[12 Campi Numerici e Campo F2]].

## 4 Contare le operazioni

### Problema

Per due matrici reali $2\times3$ e uno scalare generico $\lambda$, confrontare i calcoli diretti di $\lambda(A+B)$ e $\lambda A+\lambda B$.

### Svolgimento

Ogni matrice ha $2\cdot3=6$ entrate.

- $\lambda(A+B)$: 6 somme per $A+B$, poi 6 prodotti per applicare $\lambda$.
- $\lambda A+\lambda B$: 6 prodotti per ciascuna matrice, poi 6 somme; in totale 12 prodotti e 6 somme.

La prima procedura risparmia 6 prodotti. La distributività garantisce lo stesso risultato.

Prerequisito: [[15 Proprietà e Costo dei Calcoli Matriciali]].
