---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF pp. 19-20
  - Libro, §3.1, p. 77
---

# Successioni monotone

## Definizioni

Una successione $(a_n)$ è:

- **crescente** se $a_n\leq a_{n+1}$ per ogni indice ammesso;
- **strettamente crescente** se $a_n<a_{n+1}$ per ogni indice ammesso;
- **decrescente** se $a_n\geq a_{n+1}$ per ogni indice ammesso;
- **strettamente decrescente** se $a_n>a_{n+1}$ per ogni indice ammesso.

Una successione crescente o decrescente si dice **monotona**.

## Formulazione equivalente

La successione è crescente se e solo se

$$
m\leq n
\quad\Longrightarrow\quad
a_m\leq a_n.
$$

Analogamente, è decrescente se e solo se

$$
m\leq n
\quad\Longrightarrow\quad
a_m\geq a_n.
$$

Il confronto tra termini consecutivi implica quello tra termini qualunque tramite una catena di disuguaglianze.

## Esempi

La successione

$$
a_n=2^n
$$

è strettamente crescente, mentre

$$
b_n=\frac1{2^n}
$$

è strettamente decrescente.

Una successione costante è sia crescente sia decrescente nel senso non stretto.

### Da dire all'orale

> La monotonia confronta i valori seguendo l'ordine degli indici. Le definizioni non strette ammettono uguaglianze, quindi includono anche successioni con tratti costanti.

## Come si verifica

Secondo la forma della successione, si può studiare:

$$
a_{n+1}-a_n,
$$

oppure, quando i termini sono positivi,

$$
\frac{a_{n+1}}{a_n}.
$$

Questi sono strumenti di confronto; la conclusione deve sempre essere ricondotta alla definizione.

## Errori comuni

- Confondere crescente con strettamente crescente.
- Controllare soltanto i primi termini e concludere per tutti gli indici.
- Dimenticare il dominio degli indici nel confronto tra $a_n$ e $a_{n+1}$.
- Pensare che ogni successione monotona debba essere limitata.

## Connessioni

- È la versione discreta di [[62 Funzioni Monotone|monotonia delle funzioni]].
- Unita alla limitatezza conduce al [[76 Teorema del Limite delle Successioni Monotone|teorema del limite monotono]].
- Usa l'ordine reale studiato in [[23 Campi Ordinati|campi ordinati]].

## Prospettiva d'esame

Una prova di monotonia deve produrre una disuguaglianza valida per ogni indice ammesso. Un elenco numerico di termini può suggerire il risultato, ma non lo dimostra.
