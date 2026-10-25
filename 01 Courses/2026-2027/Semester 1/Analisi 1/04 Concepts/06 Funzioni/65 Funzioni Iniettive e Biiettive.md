---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 05, PDF pp. 12-13
  - Libro, §2.1, p. 36
---

# Funzioni iniettive e biiettive

## Iniettività

Una funzione

$$
f:A\to B
$$

è **iniettiva** se elementi distinti del dominio hanno immagini distinte:

$$
x_1\neq x_2
\quad\Longrightarrow\quad
f(x_1)\neq f(x_2).
$$

Per contrapposizione, la stessa proprietà si può scrivere

$$
f(x_1)=f(x_2)
\quad\Longrightarrow\quad
x_1=x_2.
$$

Equivalentemente, ogni $y\in\operatorname{Im}f$ possiede una e una sola controimmagine:

$$
\forall y\in\operatorname{Im}f\quad
\exists!x\in A:f(x)=y.
$$

## Biiettività

La funzione $f:A\to B$ è **biiettiva** o **biunivoca** se è contemporaneamente:

- iniettiva: ogni $y\in B$ ha al massimo una controimmagine;
- [[56 Suriettività|suriettiva]]: ogni $y\in B$ ha almeno una controimmagine.

In conclusione,

$$
f\text{ biiettiva}
\quad\Longleftrightarrow\quad
\forall y\in B\ \exists!x\in A:f(x)=y.
$$

![[65 Iniettivita Suriettivita Biiettivita.svg|644]]

## Lettura tramite l'equazione $f(x)=y$

| Proprietà di $f:A\to B$ | Numero di soluzioni in $A$ per $f(x)=y$, con $y\in B$ |
|---|---|
| Iniettiva | al massimo una |
| Suriettiva | almeno una |
| Biiettiva | esattamente una |

Questa tabella separa due domande diverse:

- **esistenza** della soluzione: suriettività;
- **unicità** della soluzione: iniettività.

### Da dire all'orale

> Una funzione è iniettiva se uguaglianza delle immagini implica uguaglianza degli argomenti. È biiettiva se ogni elemento del codominio è immagine di uno e un solo elemento del dominio.

## Interpretazione grafica

Una funzione è iniettiva se ogni retta orizzontale incontra il grafico al massimo una volta. È suriettiva rispetto al codominio dichiarato se ogni livello orizzontale corrispondente a un elemento del codominio incontra il grafico almeno una volta. Se entrambe le condizioni valgono, ogni livello lo incontra esattamente una volta.

## Esempio: il quadrato

La funzione

$$
f:\mathbb R\to\mathbb R,
\qquad f(x)=x^2,
$$

non è iniettiva, perché

$$
f(1)=f(-1)=1
$$

con $1\neq-1$. Non è neppure suriettiva su $\mathbb R$, perché nessun numero negativo appartiene alla sua immagine.

Restringendo invece il dominio,

$$
h:[0,+\infty)\to\mathbb R,
\qquad h(x)=x^2,
$$

si ottiene una funzione iniettiva, ma non ancora suriettiva sul codominio $\mathbb R$. Per renderla biiettiva bisogna dichiarare

$$
h:[0,+\infty)\to[0,+\infty).
$$

## Come dimostrare le proprietà

### Iniettività

Partire da

$$
f(x_1)=f(x_2)
$$

e dedurre necessariamente $x_1=x_2$. Per confutarla basta trovare $x_1\neq x_2$ con la stessa immagine.

### Suriettività

Fissare $y\in B$ arbitrario e mostrare che l'equazione $f(x)=y$ ha almeno una soluzione $x\in A$.

### Biiettività

Verificare separatamente iniettività e suriettività, oppure mostrare direttamente che $f(x)=y$ ha esattamente una soluzione nel dominio per ogni $y$ del codominio.

## Errori comuni

- Confondere iniettività e suriettività.
- Cercare controimmagini soltanto nell'immagine quando si sta verificando la suriettività sul codominio.
- Credere che l'equazione $f(x)=y$ debba avere una soluzione per ogni $y\in B$ anche nel caso della sola iniettività.
- Dimenticare che dominio e codominio possono cambiare la classificazione della stessa formula.
- Confondere il test delle rette orizzontali con quello delle rette verticali, che controlla se il grafico rappresenta una funzione.

## Connessioni

- Completa [[56 Suriettività|suriettività]].
- Dipende da [[55 Funzioni Dominio Codominio e Immagine|dominio, codominio e immagine]].
- È la condizione che rende possibile una [[66 Funzione Inversa|funzione inversa]] su tutto il codominio.
- La [[62 Funzioni Monotone|stretta monotonia]] è una condizione sufficiente per l'iniettività.

## Prospettiva d'esame

Le prove più affidabili partono dall'equazione $f(x)=y$: “almeno una” corrisponde alla suriettività, “al massimo una” all'iniettività, “esattamente una” alla biiettività.
