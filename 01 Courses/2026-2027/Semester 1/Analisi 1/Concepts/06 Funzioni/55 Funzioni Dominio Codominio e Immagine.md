---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 04, PDF pp. 17-20
  - Libro, §2.1, p. 35
---

# Funzioni, dominio, codominio e immagine

## Perché si introducono

Una funzione formalizza una dipendenza: a ogni dato ammesso associa un risultato ben determinato. Questo linguaggio sarà usato per descrivere funzioni reali, successioni, limiti, derivate e integrali.

La parte essenziale non è soltanto la formula. Bisogna sapere:

- quali valori possono essere inseriti;
- in quale insieme devono cadere i risultati;
- quali valori vengono effettivamente prodotti.

Queste tre informazioni corrispondono a **dominio**, **codominio** e **immagine**.

## Intuizione

Si può pensare a una funzione come a una regola che riceve un elemento $x$ e restituisce un unico elemento $f(x)$:

$$
x\longmapsto f(x).
$$

La parola “unico” è decisiva. Uno stesso elemento del dominio non può avere due immagini diverse. È invece possibile che due elementi distinti del dominio abbiano la stessa immagine.

## Definizione formale

Siano $A$ e $B$ due insiemi. Una funzione

$$
f:A\to B
$$

è una legge che associa a ogni $x\in A$ uno e un solo elemento $y\in B$.

Si scrive

$$
y=f(x).
$$

- $A$ è il **dominio** di $f$;
- $B$ è il **codominio** di $f$;
- $f(x)$ è l'**immagine di $x$ tramite $f$**.

In simboli, la condizione caratteristica è:

$$
\forall x\in A\;\exists!\,y\in B:\ y=f(x),
$$

dove $\exists!$ significa “esiste ed è unico”.

### Da dire all'orale

> Dati due insiemi $A$ e $B$, una funzione $f:A\to B$ è una legge che associa a ogni elemento $x$ del dominio $A$ uno e un solo elemento $f(x)$ del codominio $B$.

## Immagine della funzione

L'**immagine** di $f$ è l'insieme dei valori del codominio che la funzione assume effettivamente:

$$
\operatorname{Im}f
=f(A)
=\{y\in B:\exists x\in A\text{ tale che }f(x)=y\}.
$$

Vale sempre

$$
\operatorname{Im}f\subseteq B,
$$

ma non necessariamente $\operatorname{Im}f=B$.

### Da dire all'orale

> L'immagine di una funzione $f:A\to B$ è l'insieme degli elementi del codominio che sono immagini di almeno un elemento del dominio: $\operatorname{Im}f=\{y\in B:\exists x\in A, f(x)=y\}$.

## Dominio, codominio e immagine non sono la stessa cosa

Consideriamo

$$
f:\mathbb{R}\to\mathbb{R},
\qquad
f(x)=x^2.
$$

Il dominio è $\mathbb{R}$ e il codominio è $\mathbb{R}$. Tuttavia un quadrato reale non può essere negativo, mentre ogni numero non negativo è il quadrato di almeno un reale. Quindi

$$
\operatorname{Im}f=[0,+\infty).
$$

Per esempio,

$$
f(2)=4,
\qquad
f(-2)=4.
$$

Il valore $4$ appartiene all'immagine; il valore $-1$ appartiene al codominio ma non all'immagine.

Questo esempio mostra anche che una funzione può assegnare la stessa immagine a due elementi diversi: l'unicità richiesta dalla definizione riguarda il risultato associato a un **singolo** ingresso.

## La stessa formula può determinare funzioni diverse

Le seguenti funzioni hanno tutte la legge $x\mapsto x^2$, ma non sono la stessa funzione:

$$
\begin{aligned}
f&:\mathbb{R}\to\mathbb{R}, & f(x)&=x^2,\\
g&:\mathbb{R}\to[0,+\infty), & g(x)&=x^2,\\
h&:[0,+\infty)\to[0,+\infty), & h(x)&=x^2,\\
u&:[0,+\infty)\to\mathbb{R}, & u(x)&=x^2.
\end{aligned}
$$

Cambiare dominio o codominio cambia la funzione e può cambiarne le proprietà. Per questo non basta conoscere soltanto la formula.

> [!info] Approfondimento dal libro
> Una funzione è determinata dalla terna formata da dominio, codominio e legge di associazione. Due scritture con la stessa formula possono quindi rappresentare funzioni diverse se hanno dominio o codominio diversi.

## Condizioni da controllare

Perché la scrittura $f:A\to B$ definisca una funzione, bisogna verificare che:

1. la regola sia definita per ogni $x\in A$;
2. per ogni $x\in A$ venga prodotto un solo valore;
3. il valore prodotto appartenga a $B$.

Per esempio,

$$
f:\mathbb{R}\to\mathbb{R},
\qquad
f(x)=\frac1x
$$

non è una funzione con dominio $\mathbb{R}$, perché la legge non è definita in $x=0$. La stessa legge definisce invece una funzione

$$
f:\mathbb{R}\setminus\{0\}\to\mathbb{R}.
$$

## Metodo di lettura di una funzione

Quando compare una funzione $f:A\to B$:

1. identificare il dominio $A$;
2. identificare il codominio $B$;
3. leggere la legge $x\mapsto f(x)$;
4. verificare dove la legge è definita;
5. determinare, se richiesto, l'insieme immagine $f(A)$;
6. non confondere un valore $f(x)$ con l'intera immagine $\operatorname{Im}f$.

## Errori comuni

- Confondere dominio e codominio.
- Identificare automaticamente codominio e immagine.
- Pensare che due elementi diversi non possano avere la stessa immagine.
- Descrivere una funzione dando soltanto la formula e ignorando dominio e codominio.
- Dimenticare di verificare che la legge sia definita per ogni elemento del dominio.
- Confondere l'immagine del singolo elemento $x$, cioè $f(x)$, con l'immagine della funzione, cioè $f(A)$.

## Connessioni

- Usa il linguaggio di [[09 Sottoinsiemi e Inclusione|sottoinsiemi e inclusione]].
- La condizione “uno e un solo” usa il linguaggio di [[11 Predicati e Variabili Libere|predicati e variabili]].
- Prepara [[56 Suriettività|suriettività]] e [[57 Grafico di una Funzione|grafico di una funzione]].
- Una [[58 Successioni di Numeri Reali|successione]] sarà una particolare funzione con dominio contenuto in $\mathbb{N}$.

## Prospettiva d'esame

Potenziale rilevanza d'esame: dichiarare correttamente dominio, codominio e immagine; stabilire se una legge definisce davvero una funzione; riconoscere che una stessa formula può produrre funzioni diverse quando cambiano dominio o codominio.
