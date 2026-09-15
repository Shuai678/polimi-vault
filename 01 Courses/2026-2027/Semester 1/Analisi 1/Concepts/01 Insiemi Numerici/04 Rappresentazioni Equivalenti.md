---
course: Analisi 1
type: concept
status: studied
source: Lecture 01, PDF p. 3
---

# Rappresentazioni equivalenti dei numeri razionali

## Intuizione

Uno stesso numero razionale può essere scritto mediante frazioni diverse. Per esempio, $\frac{3}{7}$, $\frac{6}{14}$ e $\frac{15}{35}$ rappresentano lo stesso numero.

## Definizione formale

Per $m,n,a,b\in\mathbb Z$, con $n\ne0$ e $b\ne0$,

$$
\frac{m}{n}=\frac{a}{b}
\Longleftrightarrow
mb=na.
$$

### Da dire all'orale

> Due frazioni con denominatori non nulli rappresentano lo stesso numero razionale se e solo se il prodotto incrociato del primo numeratore per il secondo denominatore è uguale al prodotto del primo denominatore per il secondo numeratore.

## Metodo di riconoscimento

Per verificare se $\frac{m}{n}$ e $\frac{a}{b}$ sono equivalenti, calcolare $mb$ e $na$. Le frazioni sono equivalenti esattamente quando i due prodotti coincidono.

## Esempi

### Esempio svolto: frazioni equivalenti

Vogliamo verificare se $\frac37$ e $\frac{15}{35}$ rappresentano lo stesso numero razionale. I denominatori sono entrambi non nulli, quindi possiamo applicare il prodotto incrociato:

$$
3\cdot35=105,
$$

$$
7\cdot15=105.
$$

I due prodotti coincidono; pertanto

$$
\frac37=\frac{15}{35}.
$$

Lo stesso risultato si vede semplificando la seconda frazione:

$$
\frac{15}{35}=\frac{15:5}{35:5}=\frac37.
$$

### Esempio svolto: frazioni non equivalenti

Confrontiamo $\frac23$ e $\frac26$:

$$
2\cdot6=12,
\qquad
3\cdot2=6.
$$

Poiché $12\ne6$, concludiamo che

$$
\frac23\ne\frac26.
$$

Il fatto che i numeratori siano uguali non è sufficiente: cambiando il denominatore cambia il valore della frazione.

## Connessioni

Moltiplicando numeratore e denominatore per lo stesso intero $k\ne0$ non si cambia il valore della frazione:

$$
\frac{m}{n}=\frac{mk}{nk}.
$$

Poiché esistono infiniti valori possibili di $k$, ogni numero razionale ha infinite rappresentazioni frazionarie equivalenti.

## Errori comuni

- Non basta che due frazioni abbiano numeratori o denominatori “simili”: bisogna verificare il prodotto incrociato.
- Una rappresentazione equivalente non può avere denominatore zero.
