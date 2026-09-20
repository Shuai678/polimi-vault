---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF pp. 4-5
  - Libro, cap. 1.8, p. 18
---

# Unità immaginaria e forma algebrica

## Intuizione

Nei numeri reali l'equazione $x^2+1=0$ non ha soluzioni, perché $x^2\geq0$ per ogni $x\in\mathbb R$ e quindi $x^2+1\geq1>0$. I numeri complessi estendono i reali introducendo un elemento il cui quadrato è $-1$.

## Definizione formale

L'unità immaginaria $i$ è definita dalla relazione

$$
i^2=-1.
$$

L'insieme dei numeri complessi è

$$
\mathbb C=\{z=a+ib:a,b\in\mathbb R\}.
$$

### Da dire all'orale

> L'insieme dei numeri complessi è formato dai numeri della forma $a+ib$, dove $a$ e $b$ sono reali e $i$ è l'unità immaginaria definita dalla relazione $i^2=-1$.

## Notazione

In $z=a+ib$, $a$ è la parte reale e $b$ è la parte immaginaria. Si scrive

$$
\operatorname{Re}z=a,
\qquad
\operatorname{Im}z=b.
$$

La parte immaginaria è il coefficiente reale $b$, non il termine completo $ib$.

## Condizioni

I coefficienti $a$ e $b$ devono essere numeri reali. Il campo $\mathbb C$ non può essere dotato di un ordine compatibile con le operazioni di campo: in un campo ordinato il quadrato di un elemento non nullo è positivo, mentre $i^2=-1$.

## Esempi

L'equazione

$$
x^2+1=0
$$

ha in $\mathbb C$ le soluzioni $i$ e $-i$, perché entrambe hanno quadrato uguale a $-1$.

Per

$$
z=4-3i=4+(-3)i
$$

si ha

$$
\operatorname{Re}z=4,
\qquad
\operatorname{Im}z=-3.
$$

Ogni numero reale è anche complesso: per esempio,

$$
-6=-6+0i.
$$

Quindi $\mathbb R\subset\mathbb C$.

## Errori comuni

- In $a-bi$, la parte immaginaria è il numero reale $-b$.
- La parte immaginaria di $a+ib$ è $b$, non $ib$.
- Non dire che $x^2$ “ha soltanto soluzioni positive o nulle”: correttamente, il quadrato di ogni numero reale assume un valore non negativo.
- Non confondere un numero immaginario puro con la parte immaginaria di un numero complesso.

## Connessioni

- Questa nota sviluppa l'introduzione contenuta in [[01 Insiemi Numerici/07 Numeri Complessi|Numeri complessi]].
- La forma $a+ib$ sarà usata per definire le operazioni tra numeri complessi.

## Prospettiva d'esame

È importante saper motivare perché l'equazione $x^2+1=0$ non ha soluzioni reali, definire correttamente $i$ e riconoscere parte reale e parte immaginaria.
