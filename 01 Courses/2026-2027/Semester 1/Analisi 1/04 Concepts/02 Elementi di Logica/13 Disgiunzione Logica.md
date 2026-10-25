---
course: Analisi 1
type: concept
status: studied
source: Lezione 01, PDF p. 9
---
# Disgiunzione logica

## Intuizione

La disgiunzione corrisponde all'“oppure” inclusivo: è sufficiente che almeno una delle due proposizioni sia vera e rimane vera anche quando lo sono entrambe.

## Definizione formale

$P\lor Q$ è vera se almeno una tra $P$ e $Q$ è vera; è falsa solo se sono entrambe false.

### Da dire all'orale

> La disgiunzione $P\lor Q$ è vera se almeno una delle due proposizioni è vera, anche quando sono entrambe vere.

## Tabella di verità

| $P$ | $Q$ | $P\lor Q$ |
|---|---|---|
| vera | vera | vera |
| vera | falsa | vera |
| falsa | vera | vera |
| falsa | falsa | falsa |

## Esempi

### Esempio svolto: una sola proposizione vera

Siano

$$
P:\ 5\text{ è pari},
\qquad
Q:\ 5>0.
$$

$P$ è falsa, mentre $Q$ è vera. La disgiunzione $P\lor Q$ è quindi vera, perché almeno una delle due proposizioni è vera.

### Esempio svolto: entrambe vere

Siano

$$
P:\ 6\text{ è pari},
\qquad
Q:\ 6>0.
$$

Entrambe sono vere, quindi anche $P\lor Q$ è vera. Questo caso mostra che l'“oppure” logico non esclude la possibilità che siano vere entrambe.

## Connessioni

La disgiunzione compare spesso quando una conclusione ammette più possibilità alternative, delle quali almeno una deve verificarsi.

## Errori comuni

- L'“oppure” logico è inclusivo.
- La disgiunzione è falsa soltanto quando entrambe le proposizioni sono false.
