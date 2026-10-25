---
course: Analisi 1
type: concept
status: studied
source: Lezione 01, PDF pp. 9-10
---
# Implicazione logica

## Intuizione

L'implicazione $P\Rightarrow Q$ afferma che ogni volta che l'ipotesi $P$ è vera deve essere vera anche la tesi $Q$.

## Definizione formale

$P\Rightarrow Q$ è falsa solo quando $P$ è vera e $Q$ è falsa.

### Da dire all'orale

> Nell'implicazione $P\Rightarrow Q$, $P$ è l'ipotesi e $Q$ è la tesi; l'implicazione è falsa solo se l'ipotesi è vera e la tesi è falsa.

## Tabella di verità

| $P$ | $Q$ | $P\Rightarrow Q$ |
|---|---|---|
| vera | vera | vera |
| vera | falsa | falsa |
| falsa | vera | vera |
| falsa | falsa | vera |

## Esempi

### Esempio svolto: verificare un'implicazione

Consideriamo l'affermazione:

> Se un intero è multiplo di $4$, allora è pari.

Per $n=8$, l'ipotesi “$8$ è multiplo di $4$” è vera e la tesi “$8$ è pari” è vera. Questo caso è coerente con l'implicazione.

Per $n=6$, l'ipotesi è falsa perché $6$ non è multiplo di $4$. Il numero $6$ non può quindi essere un controesempio, indipendentemente dal fatto che la tesi sia vera.

Un controesempio dovrebbe essere un multiplo di $4$ che non sia pari. Un tale intero non esiste, perché se $n=4k$, allora

$$
n=4k=2(2k),
$$

e dunque $n$ è pari.

## Condizioni

Per confutare un'implicazione bisogna trovare un caso in cui l'ipotesi sia vera e la tesi sia falsa.

## Errori comuni

- Considerare falsa l'implicazione soltanto perché l'ipotesi è falsa.
- Confondere l'implicazione $P\Rightarrow Q$ con la sua inversa $Q\Rightarrow P$.

## Connessioni

- La dimostrazione diretta assume $P$ e deduce $Q$.
- Il controesempio rende $P$ vera e $Q$ falsa.
- La contrapposizione dimostra l'implicazione equivalente $\neg Q\Rightarrow\neg P$.
