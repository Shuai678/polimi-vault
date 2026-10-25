---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 02, PDF pp. 7-10
  - Libro, cap. 1.3
---

# Maggioranti, minoranti e insiemi limitati

## Intuizione

Un maggiorante è una barriera posta al di sopra di tutti gli elementi di un insieme; un minorante è una barriera posta al di sotto di tutti gli elementi. Le barriere non devono necessariamente appartenere all'insieme.

## Definizione formale

Sia $E\subseteq X$ non vuoto, dove $X$ è un campo ordinato.

Un elemento $k\in X$ è un **maggiorante** di $E$ se

$$
x\leq k \qquad \forall x\in E.
$$

L'insieme $E$ è **limitato superiormente** se possiede almeno un maggiorante:

$$
\exists k\in X:\ \forall x\in E,\ x\leq k.
$$

Un elemento $h\in X$ è un **minorante** di $E$ se

$$
h\leq x \qquad \forall x\in E.
$$

L'insieme $E$ è **limitato inferiormente** se possiede almeno un minorante:

$$
\exists h\in X:\ \forall x\in E,\ h\leq x.
$$

L'insieme $E$ è **limitato** se è limitato sia superiormente sia inferiormente, cioè se esistono $h,k\in X$ tali che

$$
h\leq x\leq k \qquad \forall x\in E.
$$

### Da dire all'orale

> Un insieme non vuoto è limitato superiormente se possiede un maggiorante, cioè un elemento maggiore o uguale a ogni elemento dell'insieme; è limitato inferiormente se possiede un minorante. È limitato se valgono entrambe le proprietà.

## Notazione

- $E$ è l'insieme studiato.
- $X$ è l'ambiente ordinato nel quale si cercano maggioranti e minoranti.
- $k$ indica un maggiorante.
- $h$ indica un minorante.
- $\forall$ significa “per ogni”.
- $\exists$ significa “esiste almeno un”.

## Condizioni

- Nella lezione $E$ è assunto non vuoto.
- Un maggiorante o un minorante deve appartenere all'ambiente $X$, ma non necessariamente a $E$.
- Un insieme può avere molti maggioranti e molti minoranti.

## Metodo / Dimostrazione

Per dimostrare che $E$ non è limitato superiormente bisogna negare correttamente la definizione:

$$
\forall k\in X,\ \exists x\in E:\ x>k.
$$

Occorre quindi prendere un candidato maggiorante arbitrario $k$ e costruire un elemento di $E$ che lo superi.

Analogamente, $E$ non è limitato inferiormente se

$$
\forall h\in X,\ \exists x\in E:\ x<h.
$$

### Esempio: $\mathbb{R}$ non è limitato superiormente

Sia $k\in\mathbb{R}$ un candidato maggiorante arbitrario. Il numero

$$
x=k+1
$$

appartiene a $\mathbb{R}$ e soddisfa $x>k$. Quindi $k$ non è un maggiorante. Poiché il ragionamento vale per ogni $k\in\mathbb{R}$, l'insieme $\mathbb{R}$ non è limitato superiormente.

## Esempi

Per $E=(-2,3)$:

- $3$ e $4$ sono maggioranti, benché non appartengano a $E$;
- $-2$ e $-3$ sono minoranti;
- $E$ è limitato.

L'insieme $\mathbb{N}$ è limitato inferiormente da $0$, ma non è limitato superiormente.

## Errori comuni

- Credere che un maggiorante o un minorante debba appartenere all'insieme.
- Confondere “limitato superiormente” con “avere massimo”.
- Affermare soltanto che non esiste un maggiorante senza mostrare come superare ogni candidato.
- Usare un esempio particolare al posto di una costruzione valida per un candidato arbitrario.

## Connessioni

- La negazione della limitatezza usa i quantificatori e la loro corretta inversione.
- Maggioranti e minoranti permettono di definire massimo, minimo, estremo superiore ed estremo inferiore.
- Il fatto che una barriera appartenga o meno a $E$ sarà decisivo per distinguere massimo ed estremo superiore.

## Prospettiva d'esame

Per provare che un insieme è limitato basta esibire barriere valide. Per provare che non è limitato superiormente o inferiormente bisogna partire da un candidato arbitrario e costruire un elemento che lo superi o che gli sia inferiore.
