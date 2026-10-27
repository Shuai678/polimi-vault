---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 10, PDF pp. 19-21
  - Libro, §4.1, pp. 115-116; soltanto serie armonica e richiamo alla condizione necessaria
---

# Serie armonica

## Definizione e intuizione

La **serie armonica** è

$$
\sum_{n=1}^{+\infty}\frac1n
=1+\frac12+\frac13+\frac14+\cdots.
$$

Il termine generale $a_n=1/n$ tende a zero; le somme parziali

$$
H_N=\sum_{n=1}^{N}\frac1n
$$

continuano però a crescere senza limite. È il controesempio fondamentale al converso della [[103 Condizione Necessaria di Convergenza di una Serie]].

## Teorema

$$
\boxed{\lim_{N\to+\infty}H_N=+\infty,\qquad
\sum_{n=1}^{+\infty}\frac1n=+\infty.}
$$

La serie è divergente positivamente, sebbene $1/n\to0$.

## Strategia della dimostrazione

Confrontiamo $1/n$ con $\log(1+1/n)$. La somma finita di questi logaritmi è telescopica e vale $\log(N+1)$, che diverge. Il [[83 Teorema del confronto per successioni divergenti|confronto per successioni]] trasferisce la divergenza a $H_N$.

Questa prova lavora direttamente sulle somme parziali e usa teoremi già studiati sulle successioni; non richiede un nuovo criterio generale sulle serie.

## Dimostrazione passo per passo

### 1. La disuguaglianza logaritmica

Da [[90 Numero di Nepero e Limiti di Tipo Esponenziale]],

$$
e=\sup_{n\geq1}\left(1+\frac1n\right)^n.
$$

Quindi per ogni $n\geq1$, essendo tutte le quantità positive,

$$
\left(1+\frac1n\right)^n\leq e.
$$

Il logaritmo naturale è crescente; possiamo applicarlo senza invertire la disuguaglianza. Dalle sue proprietà,

$$
n\log\!\left(1+\frac1n\right)\leq\log e=1,
\qquad
\boxed{\log\!\left(1+\frac1n\right)\leq\frac1n.}
$$

La proprietà del supremo dà una disuguaglianza valida per **ogni** indice. La sola convergenza della successione a $e$ non basterebbe a dedurla termine per termine.

### 2. Il confronto fra somme finite

Sommando la disuguaglianza per $n=1,\ldots,N$,

$$
H_N\geq\sum_{n=1}^{N}\log\!\left(1+\frac1n\right).
$$

Poiché $1+1/n=(n+1)/n>0$, le proprietà di [[36 Logaritmi]] danno

$$
\log\!\left(1+\frac1n\right)=\log(n+1)-\log n.
$$

La somma a destra è quindi [[102 Serie Telescopiche e Serie di Mengoli|telescopica]]:

$$
\begin{aligned}
\sum_{n=1}^{N}\log\!\left(1+\frac1n\right)
&=(\log2-\log1)+(\log3-\log2)+\cdots\\
&\quad +(\log(N+1)-\log N)\\
&=\log(N+1)-\log1=\log(N+1).
\end{aligned}
$$

Abbiamo ottenuto la stima esatta

$$
\boxed{H_N\geq\log(N+1)\qquad\text{per ogni }N\geq1.}
$$

### 3. Il passaggio al limite

Poiché $\log(N+1)\to+\infty$, il teorema del confronto per limiti infiniti implica $H_N\to+\infty$. Per la definizione di somma di una serie, la serie armonica diverge a $+\infty$.

![[104 Divergenza della Serie Armonica.svg|1000]]

Il grafico illustra la crescita delle somme e il minorante logaritmico. La dimostrazione precedente vale per tutti gli indici, non soltanto per quelli disegnati.

## Che cosa insegna questo esempio

La piccolezza del singolo termine e la limitatezza dell'accumulo sono proprietà diverse. Nella serie armonica ogni nuovo contributo si riduce, ma la somma supera qualunque soglia prefissata.

Per esempio $1/n\to0$ e anche $1/[n(n+1)]\to0$. La prima serie diverge; la seconda, di Mengoli, converge a $1$. Il solo limite del termine generale non decide il carattere.

Si deve inoltre distinguere la **successione armonica** $(1/n)$ dalla **serie armonica** $\sum1/n$: la prima converge a zero, la seconda diverge positivamente.

## Errori comuni e prospettiva d'esame

- Usare $1/n\to0$ come prova della convergenza della serie.
- Cercare una somma reale finita dopo aver dimostrato che $H_N$ supera un minorante divergente.
- Sostituire senza giustificazione una disuguaglianza per ogni $n$ con una semplice equivalenza asintotica.
- Confondere la somma di logaritmi con il logaritmo della somma: qui si usa il logaritmo del **quoziente** $(n+1)/n$ e poi una cancellazione telescopica.

Potenziale rilevanza d'esame: controesempio al converso della condizione necessaria e dimostrazione mediante $e$, logaritmo e confronto di successioni.

### Da dire all'orale

> La serie armonica diverge positivamente pur avendo termine generale infinitesimo. Dal fatto che e è il supremo di uno più uno su n elevato a n ricavo logaritmo di uno più uno su n minore o uguale a uno su n. Sommando, ottengo che la somma armonica parziale è almeno logaritmo di N più uno. Questo minorante tende a più infinito, quindi anche le somme armoniche divergono.
