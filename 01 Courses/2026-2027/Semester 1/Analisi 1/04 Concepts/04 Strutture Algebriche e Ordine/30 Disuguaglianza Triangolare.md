---
course: Analisi 1
type: theorem
status: da-verificare
source:
  - Lezione 02, PDF pp. 18-19
  - Libro, cap. 1.7
---

# Disuguaglianza triangolare

## Teorema

Per ogni $x,y\in\mathbb{R}$ vale

$$
|x+y|\leq|x|+|y|.
$$

## In parole semplici

Il valore assoluto di una somma non supera la somma dei valori assoluti. Termini con segno opposto possono compensarsi, quindi in generale non vale l'uguaglianza.

## Condizioni

- $x,y\in\mathbb{R}$.
- Non sono richieste condizioni sui segni di $x$ e $y$.

## Conclusione

$$
|x+y|\leq|x|+|y|.
$$

## Perché è utile

La disuguaglianza triangolare consente di stimare il valore assoluto di una somma mediante quantità più semplici. Sarà usata nello studio di limiti, successioni, continuità e approssimazioni.

## Intuizione

Se $x$ e $y$ hanno lo stesso segno, le loro grandezze si sommano completamente. Se hanno segni opposti, avviene una compensazione e il valore assoluto della somma diminuisce.

## Strategia della dimostrazione

Si usano le disuguaglianze $-|x|\leq x\leq|x|$ e $-|y|\leq y\leq|y|$, sommandole membro a membro.

## Dimostrazione passo per passo

Per la definizione di [[29 Valore Assoluto|valore assoluto]],

$$
-|x|\leq x\leq|x|
$$

e

$$
-|y|\leq y\leq|y|.
$$

Sommando membro a membro si ottiene

$$
-(|x|+|y|)\leq x+y\leq|x|+|y|.
$$

Poiché $|x|+|y|\geq0$, la caratterizzazione del valore assoluto fornisce

$$
|x+y|\leq|x|+|y|.
$$

## Interpretazione geometrica

Per $a,b,c\in\mathbb{R}$,

$$
a-b=(a-c)+(c-b).
$$

Applicando la disuguaglianza triangolare,

$$
|a-b|\leq|a-c|+|c-b|.
$$

La distanza diretta tra $a$ e $b$ non supera la distanza del percorso che passa per $c$.

## Esempi

Per $x=3$ e $y=-5$:

$$
|x+y|=|-2|=2<8=|3|+|-5|.
$$

Per $x=2$ e $y=3$:

$$
|x+y|=5=|2|+|3|.
$$

## Uso all'esame

La struttura tipica è

$$
|A+B|\leq|A|+|B|,
$$

dove $A$ e $B$ rappresentano espressioni reali.

## Errore comune

- Scrivere sempre $|x+y|=|x|+|y|$.
- Dimenticare che l'uguaglianza, nel caso reale, richiede termini concordi oppure un termine nullo.

## Da dire all'orale

> Per ogni $x,y\in\mathbb{R}$, il valore assoluto della somma è minore o uguale alla somma dei valori assoluti.
