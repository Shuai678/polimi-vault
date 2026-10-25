---
course: Analisi 1
type: method
status: da-studiare
source:
  - Lezione 01, PDF pp. 15-16
  - Libro, cap. 1.1, p. 2
---
# Dimostrazione per contrapposizione

## Intuizione

Invece di partire direttamente dall'ipotesi $P$ per raggiungere la tesi $Q$, si parte dalla negazione della tesi e si dimostra la negazione dell'ipotesi. Questo è possibile perché un'implicazione e la sua contrapposta hanno sempre lo stesso valore di verità.

## Metodo

Per dimostrare $P\Rightarrow Q$, si può dimostrare l'implicazione logicamente equivalente:

$$
\neg Q\Rightarrow\neg P.
$$

### Da dire all'orale

> Per dimostrare un'implicazione $P\Rightarrow Q$ per contrapposizione, dimostro l'implicazione equivalente $\neg Q\Rightarrow\neg P$.

## Condizioni

- Bisogna identificare correttamente ipotesi $P$ e tesi $Q$.
- Bisogna negare entrambe senza scambiarle.
- La contrapposta di $P\Rightarrow Q$ è $\neg Q\Rightarrow\neg P$, non $Q\Rightarrow P$.

## Esempio svolto passo per passo

Vogliamo dimostrare:

> Per ogni $n\in\mathbb N$, se $n^2$ è pari, allora $n$ è pari.

Definiamo

$$
P(n):\ n^2\text{ è pari},
\qquad
Q(n):\ n\text{ è pari}.
$$

La proposizione da dimostrare è $P(n)\Rightarrow Q(n)$. La sua contrapposta è

$$
\neg Q(n)\Rightarrow\neg P(n),
$$

cioè:

> Se $n$ è dispari, allora $n^2$ è dispari.

Questa implicazione si dimostra direttamente. Se $n$ è dispari, esiste $k\in\mathbb N$ tale che

$$
n=2k+1.
$$

Allora

$$
\begin{aligned}
n^2
&=(2k+1)^2\\
&=4k^2+4k+1\\
&=2(2k^2+2k)+1.
\end{aligned}
$$

Poiché $2k^2+2k\in\mathbb N$, $n^2$ è dispari. Abbiamo quindi dimostrato la contrapposta. Essendo la contrapposta logicamente equivalente all'implicazione iniziale, concludiamo che

$$
n^2\text{ pari}\Rightarrow n\text{ pari}.
$$

## Errori comuni

- Dimostrare l'inversa $Q\Rightarrow P$ invece della contrapposta $\neg Q\Rightarrow\neg P$.
- Negare “pari” senza dichiarare che il dominio è costituito da interi: soltanto in tale dominio “non pari” equivale a “dispari”.
- Concludere l'implicazione originaria senza ricordare l'equivalenza logica con la contrapposta.

## Connessioni

- La prova usa la dimostrazione diretta già svolta in [[17 Dimostrazione Diretta]].
- Il risultato viene utilizzato nella dimostrazione per assurdo dell'irrazionalità di $\sqrt2$.

## Prospettiva d'esame

Prima dei calcoli conviene scrivere esplicitamente $P$, $Q$, $\neg Q$ e $\neg P$: questo riduce il rischio di dimostrare l'implicazione sbagliata.
