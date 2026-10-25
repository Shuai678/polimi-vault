---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF p. 12
  - Libro, §1.8, p. 19
---

# Proprietà del coniugato

## Intuizione

Il coniugato di $z=x+iy$ è $\overline z=x-iy$: riflette il punto rispetto all'asse reale. Algebricamente è utile perché il prodotto tra un numero complesso e il suo coniugato elimina la parte immaginaria.

## Definizione formale

Per $z=x+iy$ si definisce

$$
\overline z=x-iy.
$$

Valgono, per ogni $z,w\in\mathbb C$,

$$
z\overline z=|z|^2,
\qquad
|\overline z|=|z|,
$$

$$
\overline{z+w}=\overline z+\overline w,
\qquad
\overline{zw}=\overline z\,\overline w,
$$

$$
\overline{\overline z}=z,
\qquad
z+\overline z=2\operatorname{Re}z,
\qquad
z-\overline z=2i\operatorname{Im}z.
$$

### Da dire all'orale

> Il coniugato di $z=x+iy$ è $\overline z=x-iy$. La coniugazione rispetta somma e prodotto, è involutiva e soddisfa $z\overline z=|z|^2$.

## Metodo / Dimostrazione

Per la proprietà fondamentale,

$$
z\overline z=(x+iy)(x-iy)
=x^2-ixy+ixy-i^2y^2
=x^2+y^2
=|z|^2.
$$

I termini misti si cancellano e si usa $i^2=-1$.

Per la somma, se $w=a+ib$,

$$
\overline{z+w}
=\overline{(x+a)+i(y+b)}
=(x+a)-i(y+b)
=\overline z+\overline w.
$$

## Condizioni

Le identità precedenti valgono per tutti i numeri complessi. La condizione di non nullità compare soltanto quando il coniugato viene usato per un inverso o una divisione.

## Esempi

Per $z=3-2i$,

$$
\overline z=3+2i,
\qquad
z\overline z=(3-2i)(3+2i)=13=|z|^2.
$$

## Errori comuni

- Confondere $\overline z$ con $-z$: nel coniugato cambia soltanto il segno della parte immaginaria.
- Scrivere $z\overline z=|z|$ invece di $z\overline z=|z|^2$.
- Distribuire il coniugato cambiando il segno della parte reale.

## Connessioni

- Riprende [[41 Coniugato e Modulo dei Numeri Complessi|coniugato e modulo]].
- L'identità $z\overline z=|z|^2$ è lo strumento centrale della [[45 Divisione tra Numeri Complessi|divisione tra numeri complessi]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: manipolare rapidamente coniugati, riconoscere quantità reali e motivare la formula dell'inverso.
