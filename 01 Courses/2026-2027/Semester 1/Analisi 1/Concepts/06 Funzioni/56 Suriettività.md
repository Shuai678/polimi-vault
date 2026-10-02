---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 04, PDF p. 20
  - Libro, §2.1, p. 36
---

# Suriettività

## Perché serve

Per una funzione $f:A\to B$ vale sempre $\operatorname{Im}f\subseteq B$. La suriettività distingue il caso in cui la funzione raggiunge **tutto** il codominio: nessun elemento di $B$ resta escluso.

## Intuizione

Una funzione è suriettiva quando ogni possibile valore dichiarato nel codominio viene effettivamente prodotto da almeno un elemento del dominio.

Non è richiesto che l'elemento del dominio sia unico: un valore del codominio può avere più antecedenti.

## Definizione formale

Una funzione

$$
f:A\to B
$$

si dice **suriettiva** se

$$
\operatorname{Im}f=B.
$$

Equivalentemente,

$$
\forall y\in B\;\exists x\in A:\ f(x)=y.
$$

### Da dire all'orale

> Una funzione $f:A\to B$ è suriettiva se ogni elemento del codominio è immagine di almeno un elemento del dominio; equivalentemente, $\operatorname{Im}f=B$.

## Il ruolo del codominio

Consideriamo la legge $x\mapsto x^2$.

La funzione

$$
f:\mathbb{R}\to\mathbb{R},
\qquad
f(x)=x^2,
$$

non è suriettiva, perché nessun numero reale negativo è il quadrato di un reale. Per esempio,

$$
-1\in\mathbb{R}
$$

ma non esiste $x\in\mathbb{R}$ tale che $x^2=-1$.

Invece

$$
g:\mathbb{R}\to[0,+\infty),
\qquad
g(x)=x^2,
$$

è suriettiva. Infatti, dato un qualunque $y\in[0,+\infty)$, si può scegliere

$$
x=\sqrt y\in\mathbb{R},
$$

e allora

$$
g(x)=(\sqrt y)^2=y.
$$

La formula è la stessa, ma la suriettività cambia perché cambia il codominio.

## Come si dimostra la suriettività

Per dimostrare che $f:A\to B$ è suriettiva:

1. prendere un elemento arbitrario $y\in B$;
2. risolvere l'equazione $f(x)=y$ rispetto a $x$;
3. mostrare che almeno una soluzione appartiene ad $A$;
4. concludere che ogni $y\in B$ possiede almeno un antecedente.

Il punto logico è che $y$ deve essere arbitrario: verificare soltanto alcuni valori non dimostra la suriettività.

## Come si dimostra che una funzione non è suriettiva

Per negare

$$
\forall y\in B\;\exists x\in A:\ f(x)=y,
$$

basta trovare un elemento $y_0\in B$ che non sia immagine di alcun elemento del dominio:

$$
\exists y_0\in B\;\forall x\in A:\ f(x)\neq y_0.
$$

Nell'esempio $f(x)=x^2$ con codominio $\mathbb{R}$, si può scegliere $y_0=-1$.

## Esempio svolto

### Testo

Stabilire se la funzione

$$
f:\mathbb{R}\to\mathbb{R},
\qquad
f(x)=2x-3,
$$

è suriettiva.

### Idea

Fissiamo un generico $y\in\mathbb{R}$ e cerchiamo un $x\in\mathbb{R}$ tale che $2x-3=y$.

### Svolgimento passo per passo

$$
2x-3=y
$$

equivale a

$$
2x=y+3,
$$

quindi

$$
x=\frac{y+3}{2}.
$$

Per ogni $y\in\mathbb{R}$, il numero $(y+3)/2$ è reale e soddisfa

$$
f\left(\frac{y+3}{2}\right)
=2\frac{y+3}{2}-3
=y.
$$

### Risultato

La funzione è suriettiva.

### Cosa imparare dall'esercizio

Per una dimostrazione di suriettività bisogna costruire un antecedente valido per un elemento arbitrario del codominio.

## Errori comuni

- Controllare soltanto alcuni valori del codominio.
- Confondere suriettività con unicità dell'antecedente.
- Dimenticare che il valore da raggiungere deve appartenere al codominio dichiarato.
- Risolvere $f(x)=y$ senza verificare che la soluzione appartenga al dominio.
- Decidere la suriettività guardando soltanto la formula e ignorando il codominio.

## Connessioni

- Richiede la distinzione tra dominio, codominio e immagine di [[55 Funzioni Dominio Codominio e Immagine|una funzione]].
- Nel [[57 Grafico di una Funzione|grafico]], la suriettività può essere letta mediante le rette orizzontali corrispondenti ai valori del codominio.
- La negazione della suriettività usa la stessa logica del [[19 Controesempio|controesempio]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: tradurre la suriettività in quantificatori, dimostrarla risolvendo $f(x)=y$ per un $y$ arbitrario oppure confutarla esibendo un valore del codominio non raggiunto.
