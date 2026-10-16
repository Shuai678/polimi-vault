---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 11, PDF pp. 8-9 e 11, stampate 103-104 e 106"
---

# Esempi di spazi vettoriali

Stato: **da studiare**.

## Un'unica struttura su oggetti diversi

Gli esempi della Lezione 11 condividono gli [[38 Spazi Vettoriali e Assiomi|otto assiomi]], ma cambia la natura dei vettori. In questa nota gli esempi del PDF sono accompagnati da verifiche e calcoli del tutor.

## Colonne e matrici

$\mathbb K^n$ e $M_{\mathbb K}(m,n)$ sono spazi vettoriali su $\mathbb K$ con operazioni per componenti.

$$
(A+B)_{ij}=a_{ij}+b_{ij},\qquad
(\lambda A)_{ij}=\lambda a_{ij}.
$$

Lo zero è la colonna o matrice nulla. L'opposta si ottiene cambiando segno a tutte le componenti. Gli assiomi sono quelli del campo applicati a ogni entrata.

Il prodotto tra matrici non è necessario per definirne lo spazio vettoriale. In $M_{\mathbb K}(2,3)$ il prodotto tra due elementi non è neppure definito, ma somma e prodotto per scalare lo sono.

## Vettori geometrici liberi

I vettori geometrici liberi del piano o dello spazio, con somma e prodotto per scalare usuali, sono spazi vettoriali su $\mathbb R$.

«Libero» significa che il vettore non è legato a un punto di applicazione: rappresenta lo stesso spostamento quando viene traslato parallelamente. Fissando un riferimento, gli spostamenti sono descritti da coordinate.

Il vettore nullo è lo spostamento nullo; l'opposto ha verso contrario. Non si confondono vettori liberi e punti: per sommare posizioni come vettori si sta usando un'origine scelta.

## Soluzioni di un sistema omogeneo

Per $A:m\times n$:

$$
\ker(A)=\{x\in\mathbb K^n:Ax=0\}.
$$

Questo insieme contiene lo zero ed è chiuso:

$$
A(x+y)=Ax+Ay=0,\qquad A(\lambda x)=\lambda Ax=0.
$$

Gli altri assiomi sono ereditati da $\mathbb K^n$. Il nucleo è quindi uno spazio vettoriale e, più precisamente, un [[41 Sottospazi Vettoriali e Criterio di Chiusura|sottospazio]].

## Successioni numeriche

Una successione reale è una funzione $\mathbb N\to\mathbb R$, indicata con $(a_n)_{n\in\mathbb N}$. Le parentesi evidenziano l'ordine dei termini: non è il semplice insieme dei valori assunti.

Lo spazio di **tutte** le successioni reali usa

$$
(a_n)+(b_n)=(a_n+b_n),\qquad
\lambda(a_n)=(\lambda a_n).
$$

La successione nulla ha tutti i termini zero. L'opposta di $(a_n)$ è $(-a_n)$. Gli assiomi valgono indice per indice.

Per esempio, per $a_n=n$ e $b_n=(-1)^n$:

$$
(a+2b)_n=n+2(-1)^n.
$$

Non si stanno sommando serie infinite: si sommano due successioni termine a termine. Non è richiesta la convergenza.

## Funzioni su un dominio fissato

Per $I\subseteq\mathbb R$ fissato:

$$
V(I)=\mathcal F(I,\mathbb R)=\{f:I\to\mathbb R\}
$$

è uno spazio vettoriale su $\mathbb R$ con operazioni puntuali:

$$
(f+g)(x)=f(x)+g(x),\qquad
(\lambda f)(x)=\lambda f(x).
$$

Lo zero è la funzione costantemente nulla; $(-f)(x)=-f(x)$.

Esempio: $f(x)=x^2$, $g(x)=1-x$ sullo stesso $I$ danno

$$
(2f-g)(x)=2x^2+x-1.
$$

Per V1, a ogni $x\in I$:

$$
((f+g)+h)(x)=(f(x)+g(x))+h(x)
=f(x)+(g(x)+h(x))=(f+(g+h))(x).
$$

L'uguaglianza delle funzioni segue dall'uguaglianza per ogni argomento.

**Precisazione di lettura:** nel manoscritto della p. 8 l'ultimo addendo della formula della somma può leggersi come una ripetizione di $f(x)$. La definizione corretta è $f(x)+g(x)$, coerente con l'operazione fra le due funzioni.

La somma di funzioni non è la loro composizione.

### Funzioni continue

Per un intervallo aperto $I$, il PDF cita

$$
C^0(I)=\{f:I\to\mathbb R:f\text{ continua}\}\subseteq V(I).
$$

La funzione nulla è continua; somma e multiplo scalare di funzioni continue sono continui. Quindi è un sottospazio con le operazioni puntuali. Le proprietà analitiche della continuità sono qui un prerequisito dell'esempio, non una dimostrazione svolta nel corso di GAL.

## Polinomi

$$
\mathbb K[t]=
\left\{\sum_{j=0}^{d}a_jt^j:d\ge0,\ a_j\in\mathbb K\right\}.
$$

Ogni polinomio ha solo un numero finito di coefficienti non nulli. Per sommare polinomi di grado diverso si aggiungono coefficienti zero dove mancano:

$$
p(t)+q(t)=\sum_j(a_j+b_j)t^j,
\qquad
\lambda p(t)=\sum_j(\lambda a_j)t^j.
$$

Esempio su $\mathbb R$:

$$
p(t)=1+2t-t^2,\qquad q(t)=-1+t^2+t^3,
$$

$$
p(t)+q(t)=2t+t^3,\qquad -2p(t)=-2-4t+2t^2.
$$

I vettori sono i polinomi; $t$ è un'indeterminata; gli scalari sono elementi di $\mathbb K$. Il prodotto fra due polinomi non è l'operazione esterna richiesta dagli assiomi.

Precisazione del tutor: su un campo finito polinomio formale e funzione polinomiale non coincidono necessariamente come oggetti. In $\mathbb F_2[t]$, $t^2-t$ è un polinomio non nullo, pur assumendo valore zero per ogni elemento di $\mathbb F_2$.

### Grado al massimo $d$

Per $d\ge0$ intero:

$$
\mathbb K[t]_{\le d}=
\{a_0+a_1t+\cdots+a_dt^d:a_j\in\mathbb K\}.
$$

Contiene il polinomio nullo; somma e prodotto per scalare non introducono potenze maggiori di $d$. È quindi un sottospazio di $\mathbb K[t]$.

La condizione è **grado al massimo $d$**, non grado esattamente $d$: due termini principali possono cancellarsi. L'insieme dei polinomi di grado esattamente $d$ non contiene lo zero e non è un sottospazio.

## Inclusione e identificazione

Il PDF mette in relazione vettori del piano e dello spazio. In coordinate, $\mathbb R^2$ e $\mathbb R^3$ contengono rispettivamente coppie e terne: non sono letteralmente uno sottoinsieme dell'altro.

Si identifica $\mathbb R^2$ con il piano $\{(x,y,0)\}\subseteq\mathbb R^3$ tramite $(x,y)\mapsto(x,y,0)$. Questa identificazione conserva somma e prodotto per scalare.

## Da dire all'orale

> Matrici, successioni, funzioni e polinomi sono spazi vettoriali perché le operazioni definite per componenti o punto per punto ereditano gli assiomi dal campo. Occorre specificare il dominio delle funzioni, le dimensioni delle matrici e il campo degli scalari.

## Fonte e collegamenti

- [[38 Spazi Vettoriali e Assiomi]], [[41 Sottospazi Vettoriali e Criterio di Chiusura]].
- [[GAL 2026-2027 - 20261015 - LEZIONE 11.pdf#page=8|Lezione 11, pp. 8-9, stampate 103-104]].
- [[GAL 2026-2027 - 20261015 - LEZIONE 11.pdf#page=11|Lezione 11, p. 11, stampata 106]].
