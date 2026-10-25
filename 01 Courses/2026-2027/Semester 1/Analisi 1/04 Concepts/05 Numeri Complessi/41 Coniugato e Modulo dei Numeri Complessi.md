---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF pp. 10-11
  - Libro, cap. 1.8, pp. 18-19
---

# Coniugato e modulo dei numeri complessi

## Intuizione

Il coniugato descrive una simmetria rispetto all'asse reale. Il modulo misura invece la distanza del punto associato al numero complesso dall'origine del piano.

## Complesso coniugato

### Definizione formale

Dato

$$
z=x+iy,
$$

si chiama **complesso coniugato** di $z$ il numero

$$
\overline z=x-iy.
$$

### Da dire all'orale

> Dato $z=x+iy$, il suo complesso coniugato è $\overline z=x-iy$. Geometricamente, $\overline z$ è il simmetrico di $z$ rispetto all'asse reale.

### Significato geometrico

Il punto associato a $z$ ha coordinate $(x,y)$, mentre quello associato a $\overline z$ ha coordinate $(x,-y)$. La parte reale rimane invariata e la parte immaginaria cambia segno.

## Modulo

### Definizione formale

Dato $z=x+iy$, si chiama **modulo** di $z$ il numero reale

$$
|z|=\sqrt{x^2+y^2}.
$$

### Da dire all'orale

> Il modulo del numero complesso $z=x+iy$ è il numero reale non negativo $\sqrt{x^2+y^2}$ e rappresenta la distanza del punto associato a $z$ dall'origine del piano complesso.

### Significato geometrico

![[Assets/41 Coniugato e Modulo.svg|662]]

Il segmento che unisce l'origine a $(x,y)$ è l'ipotenusa di un triangolo rettangolo con cateti di lunghezza $|x|$ e $|y|$. Per il teorema di Pitagora,

$$
|z|^2=x^2+y^2.
$$

I punti associati a $z$ e $\overline z$ hanno la stessa distanza dall'origine, quindi

$$
|z|=|\overline z|.
$$

## Notazione

- $\overline z$ si legge «coniugato di $z$».
- $|z|$ si legge «modulo di $z$».
- Il modulo è un numero reale non negativo.
- Il coniugato è ancora un numero complesso.

## Condizioni

Il coniugato e il modulo sono definiti per ogni $z\in\mathbb C$. Non è richiesta la condizione $z\neq0$.

Poiché $x^2+y^2\geq0$, la radice reale che definisce il modulo esiste sempre.

## Proprietà

Per ogni $z\in\mathbb C$:

$$
|z|\geq0,
$$

$$
|z|=0\Longleftrightarrow z=0,
$$

$$
|z|=|\overline z|,
$$

$$
z=\overline z\Longleftrightarrow z\in\mathbb R.
$$

L'ultima equivalenza segue dal fatto che

$$
x+iy=x-iy
$$

se e solo se $y=0$.

## Approfondimento dal libro

Moltiplicando un numero complesso per il suo coniugato si ottiene il quadrato del modulo:

$$
z\overline z=(x+iy)(x-iy)=x^2+y^2=|z|^2.
$$

Per $z\neq0$, questa relazione permette di riscrivere l'inverso come

$$
z^{-1}=\frac{\overline z}{|z|^2}.
$$

## Metodo

Per calcolare il coniugato:

1. si mantiene invariata la parte reale;
2. si cambia soltanto il segno della parte immaginaria.

Per calcolare il modulo:

1. si identificano parte reale e parte immaginaria;
2. si elevano entrambe al quadrato;
3. si sommano i risultati;
4. si prende la radice quadrata non negativa.

## Esempi

Se

$$
z=-2+3i,
$$

allora

$$
\overline z=-2-3i.
$$

Se

$$
z=3-4i,
$$

allora

$$
|z|=\sqrt{3^2+(-4)^2}=\sqrt{25}=5.
$$

## Errori comuni

- Cambiare anche il segno della parte reale nel coniugato.
- Confondere il coniugato $\overline z$ con l'opposto $-z$.
- Scrivere $\sqrt{x^2-y^2}$ al posto di $\sqrt{x^2+y^2}$.
- Dimenticare le parentesi quando la parte immaginaria è negativa.
- Attribuire al modulo un valore negativo.

## Connessioni

- Il coniugato formalizza l'espressione già usata nell'[[39 Campo Complesso e Inverso Moltiplicativo|inverso moltiplicativo]].
- Il modulo è la lunghezza del vettore studiato nel [[40 Piano Complesso e Interpretazione Vettoriale|piano complesso]].
- Il modulo permette di definire la [[42 Distanza nel Piano Complesso|distanza tra due numeri complessi]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: saper calcolare coniugato e modulo, spiegarne il significato geometrico e collegare la formula dell'inverso alla relazione $z\overline z=|z|^2$.
