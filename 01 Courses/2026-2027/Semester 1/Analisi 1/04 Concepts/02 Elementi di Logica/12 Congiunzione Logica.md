---
course: Analisi 1
type: concept
status: studied
source: Lezione 01, PDF p. 9
---

# Congiunzione logica

## Intuizione

La congiunzione corrisponde alla parola “e”: richiede che entrambe le condizioni siano soddisfatte nello stesso momento.

## Definizione formale

Date due proposizioni $P$ e $Q$, la congiunzione $P\land Q$ è vera se e solo se $P$ e $Q$ sono entrambe vere; è falsa in tutti gli altri casi.

### Da dire all'orale

> Date due proposizioni $P$ e $Q$, la congiunzione $P\land Q$ è vera se e solo se $P$ e $Q$ sono entrambe vere.

## Tabella di verità

| $P$ | $Q$ | $P\land Q$ |
|---|---|---|
| vera | vera | vera |
| vera | falsa | falsa |
| falsa | vera | falsa |
| falsa | falsa | falsa |

## Esempi

### Esempio svolto: congiunzione vera

Siano

$$
P:\ 6\text{ è pari},
\qquad
Q:\ 6>0.
$$

$P$ è vera e $Q$ è vera. Di conseguenza anche

$$
P\land Q:\ 6\text{ è pari e }6>0
$$

è vera.

### Esempio svolto: congiunzione falsa

Siano

$$
P:\ 6\text{ è pari},
\qquad
Q:\ 6<0.
$$

$P$ è vera, ma $Q$ è falsa. Poiché una delle due proposizioni è falsa, la congiunzione $P\land Q$ è falsa.

## Connessioni

Quando un teorema richiede più ipotesi collegate da “e”, tutte devono essere verificate per poterlo applicare.

## Errori comuni

- Basta che una delle due proposizioni sia falsa perché $P\land Q$ sia falsa.
- Verificare una sola delle due condizioni non basta a rendere vera la congiunzione.
