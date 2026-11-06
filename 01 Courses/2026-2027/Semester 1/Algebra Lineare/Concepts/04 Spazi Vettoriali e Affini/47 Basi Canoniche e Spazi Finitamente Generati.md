---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 15, PDF pp. 4-8, stampate 122-126"
---

# Basi canoniche e spazi finitamente generati

Stato: **da studiare**.

## Finitamente generato non significa insieme finito

$V$ è **finitamente generato** se esiste una famiglia finita $v_1,\ldots,v_s$ tale che

$$
V=\operatorname{Span}(v_1,\ldots,v_s).
$$

Da una famiglia finita di generatori si possono rimuovere successivamente i vettori ridondanti, ottenendo una base: la procedura è in [[48 Estrazione di una Base con Gauss]]. Quindi per questi spazi la dimensione è finita.

Per esempio $\mathbb R^2$ ha infiniti elementi, ma è generato da due vettori. La cardinalità dello spazio non è la sua dimensione.

Uno spazio non finitamente generato non ammette nessuna famiglia **finita** di generatori.

## Base canonica di colonne

In $\mathbb K^n$ siano $e_1,\ldots,e_n$ le colonne con un'unica entrata 1, rispettivamente nelle posizioni $1,\ldots,n$.

Ogni $x=(x_1,\ldots,x_n)^{\mathsf T}$ si scrive

$$
x=x_1e_1+\cdots+x_ne_n.
$$

Quindi i vettori canonici generano. Inoltre $\sum_i\lambda_ie_i=0$ impone, confrontando ogni entrata, $\lambda_i=0$ per tutti gli indici. Sono indipendenti:

$$
\boxed{\mathcal E=(e_1,\ldots,e_n)\text{ è una base},\qquad
\dim_{\mathbb K}\mathbb K^n=n.}
$$

Le coordinate rispetto a questa base sono proprio le entrate della colonna.

## Base canonica delle matrici

In $M_{\mathbb K}(m,n)$, $E_{ij}$ è la matrice con 1 nella posizione $(i,j)$ e 0 altrove.

$$
A=(a_{ij})=\sum_{i=1}^{m}\sum_{j=1}^{n}a_{ij}E_{ij}.
$$

Le $mn$ matrici generano. Se la somma è nulla, confrontando l'entrata $(i,j)$ si ottiene che il coefficiente di $E_{ij}$ è zero: sono indipendenti.

$$
\boxed{\dim_{\mathbb K}M_{\mathbb K}(m,n)=mn.}
$$

Per matrici $2\times2$, nell'ordine del PDF:

$$
\mathcal E=(E_{11},E_{12},E_{21},E_{22}),\qquad
\left[\begin{pmatrix}a&b\\c&d\end{pmatrix}\right]_{\mathcal E}
=\begin{pmatrix}a\\b\\c\\d\end{pmatrix}.
$$

I vettori della base sono **matrici**, mentre le loro coordinate sono liste di scalari.

## Base canonica dei polinomi di grado limitato

Per $d\ge0$ intero:

$$
\mathcal P=(1,t,t^2,\ldots,t^d)
$$

genera $\mathbb K[t]_{\le d}$. Se $\sum_{j=0}^{d}a_jt^j$ è il polinomio nullo, tutti i coefficienti sono zero: la famiglia è indipendente.

$$
\boxed{\dim_{\mathbb K}\mathbb K[t]_{\le d}=d+1.}
$$

Si conta anche il monomio costante $1=t^0$. Per esempio $\mathbb R[t]_{\le2}$ ha dimensione 3, non 2.

Qui i polinomi sono formali: l'uguaglianza significa uguaglianza dei coefficienti, anche su campi finiti.

## Perché tutti i polinomi non sono finitamente generati

Il PDF considera la catena

$$
\operatorname{Span}(1)\subsetneq
\operatorname{Span}(1,t)\subsetneq
\operatorname{Span}(1,t,t^2)\subsetneq\cdots.
$$

Dimostrazione esplicitata dal tutor: supponiamo che un numero finito di polinomi $p_1,\ldots,p_s$ generi $\mathbb K[t]$. Sia $D$ un limite superiore finito dei loro gradi; se sono tutti nulli si può prendere $D=0$.

Ogni combinazione $\sum_i\lambda_ip_i$ ha potenze al massimo $D$. Non può quindi essere $t^{D+1}$. È una contraddizione.

Si può anche osservare che per ogni $d$ i monomi $1,t,\ldots,t^d$ sono indipendenti: non esiste un limite finito alla lunghezza delle famiglie indipendenti.

**Precisazione:** non significa che «le combinazioni lineari non bastano». Ogni singolo polinomio è una combinazione **finita** di monomi. Non basta una famiglia finita fissata una volta per tutte. Non si introducono somme infinite negli assiomi di spazio vettoriale.

## L'esempio delle funzioni continue

Il PDF colloca $C^0(I)$ fra gli spazi non finitamente generati.

Per un intervallo aperto non vuoto $I\subseteq\mathbb R$, esplicitazione del tutor: per ogni $d$, le funzioni $1,x,\ldots,x^d$ sono continue e indipendenti su $I$. Una loro combinazione nulla su tutto $I$ sarebbe un polinomio con infiniti zeri, quindi il polinomio nullo. Si usa il fatto algebrico che un polinomio non nullo di grado $d$ ha al massimo $d$ radici distinte, ottenuto dividendo successivamente per i fattori delle radici.

Il lemma fondamentale esclude dunque un numero finito di generatori. Non si estende questa affermazione senza controlli a domini vuoti o finiti.

## Famiglie infinite: significato dello span

Integrazione del tutor: per una famiglia infinita, lo span contiene tutte le combinazioni che usano solo un numero **finito** di vettori della famiglia. Per esempio $\{1,t,t^2,\ldots\}$ genera $\mathbb K[t]$ in questo senso.

La teoria delle dimensioni infinite non è sviluppata nei PDF forniti: qui serve soltanto riconoscere l'assenza di generatori finiti.

## Da dire all'orale

> Uno spazio è finitamente generato se tutte le sue componenti si ottengono da un numero finito di vettori. Le basi canoniche danno dimensione $n$ per $\mathbb K^n$, $mn$ per le matrici e $d+1$ per i polinomi di grado al massimo $d$. Lo spazio di tutti i polinomi non è finitamente generato perché i gradi non sono limitati.

## Collegamenti e fonte

- [[39 Esempi di Spazi Vettoriali]], [[45 Basi e Unicità delle Coordinate]], [[46 Lemma Fondamentale e Teorema della Dimensione]].
- [[GAL 2026-2027 - 20261028 - LEZIONE 15.pdf#page=4|Lezione 15, pp. 4-8, stampate 122-126]].
