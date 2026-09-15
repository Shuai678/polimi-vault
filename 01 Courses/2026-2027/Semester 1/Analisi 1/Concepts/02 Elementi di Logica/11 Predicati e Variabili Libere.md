---
course: Analisi 1
type: concept
status: studied
source: Lezione 01, PDF pp. 7-8
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

## Errori comuni

- Dopo la sostituzione $x=a$, $P(a)$ non contiene più la variabile libera $x$: è una proposizione, non un predicato.
- Non confondere il dominio del predicato con il denominatore di una frazione.
