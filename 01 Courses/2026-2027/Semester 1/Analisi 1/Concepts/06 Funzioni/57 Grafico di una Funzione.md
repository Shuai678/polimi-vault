---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 04, PDF pp. 20-22
  - Libro, §2.1, p. 35 e §2.3.1, pp. 37-38
---

# Grafico di una funzione

## Perché serve

Il grafico trasforma la legge di una funzione in un insieme di punti. In questo modo dominio, immagine e proprietà della funzione possono essere letti geometricamente.

## Definizione formale

Sia

$$
f:A\to B.
$$

Il **grafico** di $f$ è il sottoinsieme del prodotto cartesiano $A\times B$ definito da

$$
G(f)
=\{(x,y)\in A\times B:x\in A,\ y=f(x)\}.
$$

Equivalentemente,

$$
G(f)=\{(x,f(x)):x\in A\}.
$$

Ogni elemento del grafico registra contemporaneamente un ingresso $x$ e la sua immagine $f(x)$.

### Da dire all'orale

> Il grafico di una funzione $f:A\to B$ è l'insieme delle coppie $(x,f(x))$ al variare di $x$ nel dominio, ed è quindi un sottoinsieme di $A\times B$.

## Interpretazione per funzioni reali

Quando

$$
A,B\subseteq\mathbb{R},
$$

il grafico è un sottoinsieme di $\mathbb{R}^2$ e può essere rappresentato nel piano cartesiano.

Per ogni $x_0\in A$ esiste un unico punto del grafico con ascissa $x_0$:

$$
(x_0,f(x_0)).
$$

Perciò la retta verticale

$$
x=x_0
$$

interseca il grafico esattamente una volta quando $x_0\in A$, e non lo interseca quando $x_0\notin A$.

Questa è la lettura geometrica della condizione “a ogni elemento del dominio corrisponde uno e un solo valore”.

## Test della retta verticale

Un sottoinsieme del piano può rappresentare il grafico di una funzione reale di variabile reale soltanto se ogni retta verticale lo incontra al più una volta.

Se una stessa retta verticale incontra la curva in due punti distinti, allo stesso valore $x_0$ corrisponderebbero due ordinate diverse. La relazione non definirebbe quindi una funzione di $x$.

## Dominio come proiezione sull'asse delle ascisse

Il dominio è formato dalle ascisse dei punti del grafico:

$$
A
=\{x\in\mathbb{R}:\exists y\in\mathbb{R}\text{ tale che }(x,y)\in G(f)\}.
$$

Geometricamente, si può pensare di proiettare il grafico sull'asse $x$ mediante rette parallele all'asse $y$.

## Immagine come proiezione sull'asse delle ordinate

L'immagine è formata dalle ordinate dei punti del grafico:

$$
\operatorname{Im}f
=\{y\in\mathbb{R}:\exists x\in A\text{ tale che }(x,y)\in G(f)\}.
$$

Geometricamente, si ottiene proiettando il grafico sull'asse $y$ mediante rette parallele all'asse $x$.

In particolare,

$$
y_0\in\operatorname{Im}f
$$

se e solo se la retta orizzontale

$$
y=y_0
$$

interseca il grafico in almeno un punto.

## Lettura grafica della suriettività

Se $f:A\to B$ con $A,B\subseteq\mathbb{R}$, allora $f$ è [[56 Suriettività|suriettiva]] se e solo se, per ogni $y_0\in B$, la retta orizzontale $y=y_0$ incontra il grafico almeno una volta.

La richiesta è “almeno una volta”, non “esattamente una volta”: la suriettività non vieta che uno stesso valore abbia più antecedenti.

## Esempio: il grafico di x al quadrato

Per

$$
f:\mathbb{R}\to\mathbb{R},
\qquad
f(x)=x^2,
$$

il grafico è

$$
G(f)=\{(x,x^2):x\in\mathbb{R}\}.
$$

- ogni retta verticale lo incontra esattamente una volta;
- una retta orizzontale $y=y_0$ con $y_0<0$ non lo incontra;
- la retta $y=0$ lo incontra una volta;
- una retta $y=y_0$ con $y_0>0$ lo incontra due volte.

Si legge quindi dal grafico che

$$
\operatorname{Im}f=[0,+\infty)
$$

e che $f:\mathbb{R}\to\mathbb{R}$ non è suriettiva.

> [!info] Approfondimento dal libro
> Il libro usa la stessa lettura per collegare il grafico alle proprietà di una funzione: le rette verticali verificano che a ogni ingresso corrisponda un solo valore; le rette orizzontali permettono di leggere quali valori appartengono all'immagine.

## Errori comuni

- Scambiare le coordinate e scrivere $(f(x),x)$ invece di $(x,f(x))$.
- Confondere il grafico, che è un sottoinsieme di $A\times B$, con l'immagine, che è un sottoinsieme di $B$.
- Usare il test della retta orizzontale per stabilire se una relazione è una funzione.
- Dire che una retta verticale deve intersecare il grafico per ogni numero reale, anche quando il dominio non è tutto $\mathbb{R}$.
- Confondere “almeno un'intersezione” con “una sola intersezione” nella verifica della suriettività.

## Connessioni

- Richiede [[55 Funzioni Dominio Codominio e Immagine|dominio, codominio e immagine]].
- Traduce geometricamente la [[56 Suriettività|suriettività]].
- Usa il prodotto cartesiano e la rappresentazione nel piano.

## Prospettiva d'esame

Potenziale rilevanza d'esame: definire il grafico come insieme di coppie, ricavare dominio e immagine da una rappresentazione grafica e distinguere correttamente il criterio verticale dal criterio orizzontale.
