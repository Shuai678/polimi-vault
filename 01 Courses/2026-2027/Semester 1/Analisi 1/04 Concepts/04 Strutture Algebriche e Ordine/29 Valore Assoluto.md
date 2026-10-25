---
course: Analisi 1
type: concept
status: da-verificare
source:
  - Lezione 02, PDF pp. 18-20
  - Libro, cap. 1.7
---

# Valore assoluto

## Intuizione

Il valore assoluto di un numero reale rappresenta la sua distanza da zero. Per questo motivo è sempre non negativo e non dipende dal lato della retta reale sul quale si trova il numero.

## Definizione formale

Per ogni $a\in\mathbb{R}$ si definisce

$$
|a|=
\begin{cases}
a, & \text{se }a\geq0,\\
-a, & \text{se }a<0.
\end{cases}
$$

### Da dire all'orale

> Il valore assoluto di un numero reale $a$ è $a$ se $a$ è non negativo e $-a$ se $a$ è negativo; geometricamente rappresenta la distanza di $a$ dall'origine.

## Notazione

- $|a|$ indica il valore assoluto o modulo di $a$.
- $|a-b|$ indica la distanza tra i punti reali $a$ e $b$.
- Le barre non possono essere eliminate senza conoscere il segno dell'espressione interna.

## Condizioni

Per $r\geq0$ valgono

$$
|a|\leq r \Longleftrightarrow -r\leq a\leq r
$$

e

$$
|a|<r \Longleftrightarrow -r<a<r.
$$

Per $r\geq0$ vale inoltre

$$
|a|>r \Longleftrightarrow a<-r\ \lor\ a>r.
$$

Se $r<0$, la disuguaglianza $|a|\leq r$ non ha soluzioni.

## Metodo / Dimostrazione

Dalla definizione per casi segue che

$$
|a|\geq0
$$

per ogni $a\in\mathbb{R}$ e che

$$
|a|=0 \Longleftrightarrow a=0.
$$

Inoltre,

$$
|-a|=|a|.
$$

La distanza tra due numeri reali è

$$
d(a,b)=|a-b|=|b-a|.
$$

## Esempi

$$
|-4|=-(-4)=4.
$$

La distanza tra $-2$ e $5$ è

$$
|-2-5|=|-7|=7.
$$

La disuguaglianza

$$
|x|\leq3
$$

equivale a

$$
-3\leq x\leq3.
$$

## Errori comuni

- Scrivere $|-4|=-4$.
- Eliminare le barre senza controllare il segno dell'espressione interna.
- Usare una disgiunzione per $|x|\leq r$, che richiede invece due condizioni simultanee.
- Usare una congiunzione per $|x|>r$, che richiede invece due possibilità alternative.

## Connessioni

- Il valore assoluto traduce algebricamente la distanza sulla retta reale.
- La distanza $|x-x_0|$ sarà centrale nelle definizioni di limite e continuità.
- La disuguaglianza triangolare controlla il valore assoluto di una somma.

## Prospettiva d'esame

Prima di risolvere una disuguaglianza con valore assoluto bisogna riconoscere se descrive punti interni o esterni a un intervallo e controllare il segno del termine a destra.
