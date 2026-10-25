---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 01, PDF pp. 3-5
  - Libro, cap. 1.1.1, pp. 3-4
---

# Rappresentazioni decimali dei numeri razionali

## Intuizione

Una frazione e una scrittura decimale possono rappresentare lo stesso numero. Le cifre decimali possono terminare oppure ripetersi per sempre secondo uno stesso schema.

## Definizione formale

Un numero $x$ è razionale se e solo se la sua rappresentazione decimale è finita oppure infinita periodica.

### Da dire all'orale

> Un numero è razionale se e solo se ammette una rappresentazione decimale finita oppure infinita periodica.

## Terminologia

- Una rappresentazione è **finita** se, dopo un certo numero di cifre decimali, le cifre successive sono tutte nulle.
- Una rappresentazione è **infinita periodica** se, da un certo punto in poi, una sequenza finita di cifre si ripete indefinitamente.
- La sequenza ripetuta si chiama **periodo**.

## Esempi

### Esempio svolto: rappresentazione finita

Eseguendo la divisione $3:2$ otteniamo

$$
\frac32=1{,}5.
$$

La scrittura può essere prolungata aggiungendo zeri senza cambiare il numero:

$$
1{,}5=1{,}5000\ldots
$$

La rappresentazione è finita perché, dopo la prima cifra decimale, tutte le cifre successive sono nulle.

### Esempio svolto: rappresentazione periodica

Eseguendo la divisione $1:3$, il resto torna sempre uguale a $1$ e la cifra $3$ continua a ripetersi:

$$
\frac13=0{,}3333\ldots=0{,}\overline3.
$$

Il periodo è formato dalla sola cifra $3$. Analogamente,

$$
0{,}272727\ldots=0{,}\overline{27}
$$

ha periodo $27$ ed è quindi un numero razionale.

### Esempio svolto: due scritture per lo stesso numero

La lezione osserva che

$$
0{,}\overline9=1.
$$

Per verificarlo, poniamo $x=0{,}\overline9$. Moltiplicando per $10$ otteniamo $10x=9{,}\overline9$. Sottraendo la prima uguaglianza dalla seconda:

$$
10x-x=9{,}\overline9-0{,}\overline9,
$$

quindi

$$
9x=9
$$

e pertanto $x=1$. Non si tratta di un'approssimazione: le due scritture rappresentano esattamente lo stesso numero.

### Approfondimento dal libro

Per evitare doppie rappresentazioni si preferiscono gli allineamenti decimali propri, nei quali il periodo non è costituito dalla cifra $9$. Per esempio si usa $1{,}000\ldots$ invece di $0{,}\overline9$.

## Connessioni

- Le [[03 Numeri Razionali|frazioni]] possono essere convertite in rappresentazioni decimali mediante divisione.
- La notazione $\overline{27}$ segnala che il blocco $27$ si ripete indefinitamente.

## Errori comuni

- Una scrittura infinita non è necessariamente irrazionale: può essere periodica e quindi razionale.
- Non confondere una scrittura finita con un'approssimazione: $1{,}5$ e $1{,}5000\ldots$ sono esattamente lo stesso numero.
