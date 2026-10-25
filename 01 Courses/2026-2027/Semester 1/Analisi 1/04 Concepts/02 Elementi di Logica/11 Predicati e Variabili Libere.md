---
course: Analisi 1
type: concept
status: studied
source: Lezione 01, PDF pp. 7-12
---

# Predicati e variabili libere

## Intuizione

Un predicato è una frase matematica con uno spazio da riempire. Quando assegniamo un valore alla variabile, lo spazio viene riempito e otteniamo una proposizione vera o falsa.

## Definizione formale

Un predicato è un enunciato contenente variabili libere, il cui valore di verità dipende dai valori assegnati a tali variabili. Per ogni assegnazione ammessa, il predicato diventa una proposizione vera oppure falsa.

### Da dire all'orale

> Un predicato è un enunciato contenente variabili libere, il cui valore di verità dipende dai valori assegnati alle variabili; una volta fissati tali valori, diventa una proposizione.

## Esempi

### Esempio svolto: saturare una variabile libera

$$
P(x):x>0,
\qquad x\in\mathbb R.
$$

$P(x)$ è un predicato, perché il valore di verità dipende dal valore assegnato a $x$.

Assegniamo prima $x=-2$:

$$
P(-2):-2>0
$$

La variabile libera è stata sostituita e abbiamo ottenuto una proposizione falsa.

Assegniamo poi $x=3$:

$$
P(3):3>0.
$$

Questa volta otteniamo una proposizione vera.

### Esempio svolto: il dominio fa parte del predicato

Consideriamo

$$
Q(n):\frac1n\text{ è definito}.
$$

Se dichiariamo $n\in\mathbb N\setminus\{0\}$, allora $Q(n)$ è vera per ogni valore ammesso. Se invece dichiariamo $n\in\mathbb N$, il valore $n=0$ è ammesso e produce $\frac10$, che non è definito. Il dominio modifica quindi le assegnazioni possibili e non può essere omesso.

## Condizioni

L'insieme in cui varia la variabile, cioè il dominio del predicato, fa parte della sua definizione e stabilisce i valori che possono essere assegnati.

## Quantificatori

Un predicato può essere trasformato in una proposizione assegnando un valore alla variabile oppure legando la variabile mediante un quantificatore.

- $\forall$ si legge “per ogni”.
- $\exists$ si legge “esiste almeno un”.
- $\exists!$ si legge “esiste ed è unico”.
- $\nexists$ si legge “non esiste”.

### Esempio svolto: quantificare un predicato

Consideriamo

$$
P(n):\ n\text{ è pari},
\qquad n\in\mathbb N.
$$

Il solo simbolo $P(n)$ indica un predicato. Vediamo che cosa accade usando diversi quantificatori.

1. La proposizione

   $$
   \forall n\in\mathbb N,\quad P(n)
   $$

   significa “ogni naturale è pari” ed è falsa; per esempio, $1$ è naturale ma non è pari.

2. La proposizione

   $$
   \exists n\in\mathbb N:\ P(n)
   $$

   significa “esiste almeno un naturale pari” ed è vera; per esempio, $0$ è naturale ed è pari.

3. La proposizione

   $$
   \exists! n\in\mathbb N:\ P(n)
   $$

   significa “esiste un unico naturale pari” ed è falsa, perché esistono molti naturali pari, come $0$, $2$ e $4$.

4. La proposizione

   $$
   \nexists n\in\mathbb N:\ P(n)
   $$

   significa “non esiste alcun naturale pari” ed è falsa, perché $0$ è un esempio di naturale pari.

In tutti e quattro i casi la variabile $n$ non è più libera: è legata dal quantificatore, quindi l'enunciato completo è una proposizione.

### Da dire all'orale

> Un quantificatore lega una variabile libera e trasforma il predicato in una proposizione: il quantificatore universale richiede che la proprietà valga per ogni elemento del dominio, mentre quello esistenziale richiede che valga per almeno un elemento.

## Errori comuni

- Dopo la sostituzione $x=a$, $P(a)$ non contiene più la variabile libera $x$: è una proposizione, non un predicato.
- Non confondere il dominio del predicato con il denominatore di una frazione.
- Non confondere $\exists$ con $\exists!$: il primo richiede almeno un elemento, il secondo esattamente uno.
- Il dominio deve essere dichiarato anche quando si usano i quantificatori.
