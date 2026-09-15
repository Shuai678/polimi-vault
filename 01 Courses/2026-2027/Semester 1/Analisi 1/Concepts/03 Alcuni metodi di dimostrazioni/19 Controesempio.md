---
course: Analisi 1
type: method
status: studied
source: Lezione 01, PDF pp. 17-18
---
# Controesempio

## Intuizione

Un'affermazione universale sostiene che una proprietà vale per tutti gli elementi del dominio. Per dimostrare che è falsa basta trovare un solo elemento che rispetti l'ipotesi ma non la tesi.

## Metodo

Per confutare un'implicazione universale:

$$
\forall x\in A,\;P(x)\Rightarrow Q(x),
$$

basta trovare un elemento $x_0\in A$ per cui $P(x_0)$ è vera e $Q(x_0)$ è falsa.

### Da dire all'orale

> Un controesempio a un'implicazione universale è un elemento del dominio per cui l'ipotesi è vera e la tesi è falsa.

## Condizioni

Un controesempio $x_0$ deve soddisfare contemporaneamente:

- $x_0\in A$;
- $P(x_0)$ vera;
- $Q(x_0)$ falsa.

Un elemento che rende falsa anche l'ipotesi non confuta l'implicazione.

## Esempio

L'enunciato “ogni numero primo è dispari” è falso: $2$ è primo ma non è dispari.

Invece $4$ non è un controesempio: è pari, ma non soddisfa l'ipotesi di essere primo.

## Errori comuni

- Controllare soltanto che la tesi sia falsa e dimenticare di verificare l'ipotesi.
- Usare un elemento esterno al dominio.
- Pensare che molti esempi favorevoli dimostrino un'affermazione universale: un numero finito di esempi non sostituisce una dimostrazione.

## Connessioni

- Un'implicazione è falsa esattamente quando l'ipotesi è vera e la tesi è falsa.
- Un solo controesempio valido confuta un'affermazione universale, mentre esempi favorevoli non bastano a dimostrarla.

## Prospettiva d'esame

Per presentare un controesempio bisogna indicare esplicitamente il dominio e verificare separatamente che l'ipotesi sia vera e che la tesi sia falsa.
