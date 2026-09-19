---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 01, PDF p. 6
  - Lezione 03, PDF pp. 4-5
  - Libro, cap. 1.8, p. 18
---

# Numeri complessi

## Intuizione

I numeri complessi estendono i reali introducendo l'unità immaginaria $i$, che permette di trattare equazioni come $x^2+1=0$.

Nei numeri reali l'equazione $x^2+1=0$ non ha soluzioni, perché $x^2\geq0$ per ogni $x\in\mathbb{R}$ e quindi $x^2+1\geq1>0$. L'estensione a $\mathbb{C}$ introduce invece un elemento il cui quadrato è $-1$.

## Definizione formale

$$
\mathbb C=\{z=a+ib:a,b\in\mathbb R,\ i^2=-1\}.
$$

### Da dire all'orale

> L'insieme dei numeri complessi è formato dai numeri della forma $a+ib$, dove $a$ e $b$ sono reali e $i$ è l'unità immaginaria definita dalla relazione $i^2=-1$.

## Notazione

In $z=a+ib$, $a$ è la parte reale e $b$ è il coefficiente della parte immaginaria.

Si scrive

$$
\operatorname{Re}z=a,
\qquad
\operatorname{Im}z=b.
$$

La parte immaginaria è il coefficiente reale $b$, non il termine completo $ib$.

$$
4-3i=4+(-3)i,
$$

perciò qui $a=4$ e $b=-3$.

## Esempi

### Perché serve l'unità immaginaria

L'unità immaginaria soddisfa

$$
i^2=-1.
$$

Di conseguenza sia $i$ sia $-i$ risolvono l'equazione

$$
x^2+1=0.
$$

### Esempio svolto: riconoscere parte reale e coefficiente immaginario

Consideriamo

$$
z=-5+7i.
$$

Confrontando questa scrittura con la forma generale $z=a+ib$, otteniamo

$$
a=-5,
\qquad
b=7.
$$

Entrambi i coefficienti sono reali, quindi $z\in\mathbb C$.

Se invece

$$
z=4-3i=4+(-3)i,
$$

allora $a=4$ e $b=-3$: il segno meno appartiene al coefficiente $b$.

### Esempio svolto: un reale visto come complesso

Ogni numero reale può essere scritto con coefficiente immaginario nullo. Per esempio,

$$
-2=-2+0i.
$$

Pertanto $-2\in\mathbb C$ e, più in generale, $\mathbb R\subset\mathbb C$.

## Condizioni e struttura d'ordine

Il campo $\mathbb{C}$ non può essere dotato di un ordine compatibile con le operazioni di campo. Infatti, in ogni campo ordinato il quadrato di un elemento non nullo è positivo; applicando questa proprietà a $i$ si avrebbe $i^2>0$, in contraddizione con $i^2=-1<0$.

## Connessioni

$$
\mathbb N\subset\mathbb Z\subset\mathbb Q\subset\mathbb R\subset\mathbb C.
$$

## Errori comuni

- In $a-bi$, il coefficiente $b$ nella forma $a+ib$ è negativo.
- Non confondere la lettera $C$ con il simbolo di inclusione $\subset$.
- Non dire che $x^2$ “ha soltanto soluzioni positive o nulle”: correttamente, il quadrato di ogni numero reale assume un valore non negativo.
- La parte immaginaria di $a+ib$ è $b$, non $ib$.
