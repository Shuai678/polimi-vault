---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF p. 11
---

# Distanza nel piano complesso

## Intuizione

Il modulo $|z|$ misura la distanza di $z$ dall'origine. Per misurare la distanza tra due numeri complessi $z$ e $w$, si considera il vettore differenza $z-w$ e se ne calcola la lunghezza.

## Definizione formale

Siano

$$
z=x+iy,
\qquad
w=a+ib.
$$

La distanza tra i punti associati a $z$ e $w$ è

$$
d(z,w)=|z-w|.
$$

Poiché

$$
z-w=(x-a)+i(y-b),
$$

si ottiene

$$
|z-w|=\sqrt{(x-a)^2+(y-b)^2}.
$$

### Da dire all'orale

> Dati $z=x+iy$ e $w=a+ib$, la distanza tra i punti che li rappresentano nel piano complesso è $|z-w|$, cioè $\sqrt{(x-a)^2+(y-b)^2}$.

## Notazione

- $z-w$ è un numero complesso e rappresenta il vettore che va da $w$ a $z$.
- $|z-w|$ è un numero reale non negativo e rappresenta la lunghezza di quel vettore.
- $d(z,w)$ indica la distanza tra $z$ e $w$.

## Condizioni

La formula vale per ogni $z,w\in\mathbb C$. I due numeri possono coincidere; in tal caso la distanza è nulla.

## Metodo / Dimostrazione

Le differenze tra le coordinate dei punti sono

$$
\Delta x=x-a,
\qquad
\Delta y=y-b.
$$

Il segmento che unisce i punti è l'ipotenusa di un triangolo rettangolo avente cateti di lunghezza $|x-a|$ e $|y-b|$. Per il teorema di Pitagora,

$$
d(z,w)^2=(x-a)^2+(y-b)^2,
$$

da cui, prendendo la radice non negativa,

$$
d(z,w)=|z-w|.
$$

## Rappresentazione geometrica

![[Assets/42 Distanza nel Piano Complesso.svg|689]]

Nel grafico, le differenze tra ascisse e ordinate formano i cateti del triangolo, mentre il segmento verde è la distanza $|z-w|$.

## Proprietà

Per ogni $z,w\in\mathbb C$:

$$
|z-w|\geq0,
$$

$$
|z-w|=0\Longleftrightarrow z=w,
$$

$$
|z-w|=|w-z|.
$$

La simmetria segue da

$$
w-z=-(z-w)
$$

e dal fatto che un vettore e il suo opposto hanno la stessa lunghezza.

## Esempi

Siano

$$
z=1+2i,
\qquad
w=-2-2i.
$$

Allora

$$
z-w=(1+2i)-(-2-2i)=3+4i
$$

e quindi

$$
|z-w|=\sqrt{3^2+4^2}=5.
$$

## Errori comuni

- Calcolare $|z|-|w|$ invece di $|z-w|$.
- Dimenticare che sottrarre $w$ cambia il segno di entrambe le sue parti.
- Confondere il numero complesso $z-w$ con la distanza reale $|z-w|$.
- Ottenere una distanza negativa.

## Connessioni

- La distanza generalizza il [[41 Coniugato e Modulo dei Numeri Complessi|modulo]]: ponendo $w=0$ si ottiene $|z-0|=|z|$.
- L'equazione $|z-w|=\rho$ descriverà i punti posti a distanza costante $\rho$ da $w$.

## Prospettiva d'esame

Potenziale rilevanza d'esame: riconoscere che $|z-w|$ è una distanza, tradurre correttamente la differenza nelle coordinate e distinguere $|z-w|$ da $|z|-|w|$.
