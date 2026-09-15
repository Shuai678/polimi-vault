---
course: Analisi 1
type: method
status: studied
source: Lezione 01, PDF pp. 14-15
---
# Dimostrazione diretta

## Intuizione

Una dimostrazione diretta parte dalle informazioni contenute nell'ipotesi e le trasforma, mediante passaggi giustificati, fino a ottenere esattamente la tesi.

## Metodo

Per dimostrare un'implicazione universale

$$
\forall n\in\mathbb N,\qquad P(n)\Rightarrow Q(n),
$$

si sceglie un $n\in\mathbb N$ arbitrario, si assume vera $P(n)$ e, usando definizioni e risultati già noti, si deduce $Q(n)$. Il fatto che $n$ sia arbitrario consente di concludere che l'implicazione vale per ogni $n$ del dominio.

### Da dire all'orale

> In una dimostrazione diretta considero un elemento arbitrario del dominio, assumo vera l'ipotesi e deduco la tesi attraverso una catena di passaggi logici giustificati.

## Condizioni

- L'elemento scelto deve appartenere al dominio indicato dal teorema.
- Ogni passaggio deve derivare da una definizione, da una proprietà o da un risultato già noto.
- La conclusione deve dimostrare la tesi, non limitarsi a ripetere l'ipotesi.

## Esempio

Per dimostrare che, per ogni $n\in\mathbb N$, se $n$ è dispari allora $n^2$ è dispari, partiamo dalla definizione di numero dispari:

$$
n=2k+1
$$

per un opportuno $k\in\mathbb N$. Quindi:

$$
n^2=(2k+1)^2=4k^2+4k+1=2(2k^2+2k)+1,
$$

e $2k^2+2k\in\mathbb N$. Pertanto $n^2$ ha la forma $2h+1$, con $h\in\mathbb N$, e quindi è dispari.

## Errori comuni

- Verificare soltanto alcuni esempi numerici non dimostra un'affermazione universale.
- La formula $n=2k+1$ traduce l'ipotesi che $n$ sia dispari; non dimostra ancora che $n^2$ sia dispari.
- Per concludere bisogna riscrivere proprio $n^2$ nella forma $2h+1$ e verificare che $h$ appartenga al dominio corretto.

## Connessioni

- La stessa proprietà verrà usata per dimostrare per contrapposizione che, se $n^2$ è pari, allora $n$ è pari.
- Le definizioni di numero pari e dispari trasformano una proprietà verbale in una forma algebrica utilizzabile nella dimostrazione.

## Prospettiva d'esame

In una dimostrazione sulla parità conviene dichiarare subito il dominio, tradurre l'ipotesi mediante la definizione e concludere mostrando esplicitamente la forma $2h$ oppure $2h+1$.
