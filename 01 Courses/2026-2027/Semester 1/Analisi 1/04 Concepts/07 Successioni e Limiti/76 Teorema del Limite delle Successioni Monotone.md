---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF pp. 20-25
  - Lezione 07, PDF pp. 2-4
  - Libro, §3.4, p. 90
---

# Teorema del limite delle successioni monotone

## [[Enunciato]] nel caso di limite finito

Ogni successione [[75 Successioni Monotone|monotona]] e [[70 Grafico e Limitatezza delle Successioni|limitata]] ammette limite finito.

Indichiamo con $n_0$ l'indice iniziale della successione, per esempio $0$ oppure $1$: $a_{n_0}$ è il suo primo termine.

### Caso crescente: convergenza per difetto

Se $(a_n)$ è **crescente e limitata superiormente**, allora

$$
\lim_{n\to+\infty}a_n=\ell^-,
\qquad
\ell=\sup\{a_n:n\geq n_0\}\in\mathbb R.
$$

La convergenza è **per difetto**, perché tutti i termini stanno sotto il limite o coincidono con esso:

$$
a_n\leq\ell
\qquad\text{per ogni }n\geq n_0.
$$

### Caso decrescente: convergenza per eccesso

Se $(a_n)$ è **decrescente e limitata inferiormente**, allora

$$
\lim_{n\to+\infty}a_n=\ell^+,
\qquad
\ell=\inf\{a_n:n\geq n_0\}\in\mathbb R.
$$

La convergenza è **per eccesso**, perché tutti i termini stanno sopra il limite o coincidono con esso:

$$
a_n\geq\ell
\qquad\text{per ogni }n\geq n_0.
$$

Le notazioni $\ell^-$ e $\ell^+$ indicano il [[74 Limiti Infiniti e Regolarità delle Successioni#Convergenza per eccesso o per difetto|verso di avvicinamento]]: il valore del limite è sempre il numero reale $\ell$. Qui le disuguaglianze valgono **per ogni indice**, quindi anche [[71 Proprietà Definitivamente Vere|definitivamente]]. Si ammette l'uguaglianza: una successione costante è monotona e converge sia per difetto sia per eccesso secondo queste definizioni.

### Perché basta una sola limitazione

- Una successione **crescente** è automaticamente limitata **inferiormente** dal primo termine, perché $a_{n_0}\leq a_n$ per ogni $n\geq n_0$. Per applicare il teorema basta quindi richiedere che sia limitata **superiormente**.
- Una successione **decrescente** è automaticamente limitata **superiormente** dal primo termine, perché $a_n\leq a_{n_0}$ per ogni $n\geq n_0$. Basta quindi richiedere che sia limitata **inferiormente**.

## Dimostrazione nel caso crescente

Sia $(a_n)$ crescente e limitata superiormente. L'insieme dei suoi valori

$$
A=\{a_n:n\geq n_0\}
$$

è non vuoto e limitato superiormente. Per la completezza di $\mathbb R$ esiste

$$
\ell=\sup A.
$$

Fissiamo $\varepsilon>0$. Il numero $\ell-\varepsilon$ non può essere un maggiorante di $A$, altrimenti sarebbe un maggiorante più piccolo del minimo maggiorante $\ell$. Esiste quindi un indice $n_\varepsilon$ tale che

$$
\ell-\varepsilon<a_{n_\varepsilon}\leq\ell.
$$

Per la monotonia, se $n\geq n_\varepsilon$ allora

$$
a_{n_\varepsilon}\leq a_n.
$$

Poiché $\ell$ è un maggiorante di $A$, vale anche $a_n\leq\ell$. Pertanto, per ogni $n\geq n_\varepsilon$,

$$
\ell-\varepsilon<a_n\leq\ell<\ell+\varepsilon.
$$

Ponendo $N=n_\varepsilon$, questa è esattamente la definizione di $a_n\to\ell$. Inoltre $a_n\leq\ell$ per ogni indice: la convergenza è per difetto, cioè $a_n\to\ell^-$.

![[76 Successione Monotona e Supremo.svg|592]]

Il caso decrescente si dimostra in modo analogo usando l'estremo inferiore.

## Ruolo della completezza

Il passaggio decisivo è l'esistenza del supremo di un insieme non vuoto e limitato superiormente. Questa proprietà vale in $\mathbb R$ ma non in $\mathbb Q$: perciò il teorema dipende dalla completezza dei numeri reali.

## Forma estesa

Ogni successione monotona ammette limite in $\overline{\mathbb R}$. Infatti:

- se è crescente e limitata superiormente, converge al proprio estremo superiore;
- se è crescente e non è limitata superiormente, tende a $+\infty$;
- se è decrescente e limitata inferiormente, converge al proprio estremo inferiore;
- se è decrescente e non è limitata inferiormente, tende a $-\infty$.

In forma compatta, per una successione **crescente**,

$$
\lim_{n\to+\infty}a_n=
\sup\{a_n:n\geq n_0\}
\in\mathbb R\cup\{+\infty\}.
$$

Per una successione **decrescente**,

$$
\lim_{n\to+\infty}a_n=
\inf\{a_n:n\geq n_0\}
\in\mathbb R\cup\{-\infty\}.
$$

Si intende il supremo uguale a $+\infty$ nel caso non limitato superiormente e l'infimo uguale a $-\infty$ nel caso non limitato inferiormente.

Ne segue che ogni successione monotona è [[74 Limiti Infiniti e Regolarità delle Successioni|regolare]].

### Da dire all'orale

> Una successione crescente e limitata superiormente converge per difetto al supremo dei suoi valori; una decrescente e limitata inferiormente converge per eccesso all'infimo. Nel caso crescente, la proprietà caratteristica del supremo permette di trovare un termine sopra $\ell-\varepsilon$; la monotonia mantiene tutti i termini successivi sopra quella soglia, mentre $\ell$ li maggiora.


## Completamento della Lezione 07: caso illimitato

> [!note] Da studiare
> Questa dimostrazione e le osservazioni seguenti sono state aggiunte il 2026-10-05. Il materiale preparato resta distinto dal progresso di apprendimento.

Sia $(a_n)$ crescente e non limitata superiormente, con indice iniziale $n_0$. È automaticamente limitata inferiormente da $a_{n_0}$, perché $a_n\geq a_{n_0}$ per ogni $n\geq n_0$.

Fissiamo una soglia arbitraria $M>0$. La non limitatezza superiore significa che $M$ non è un maggiorante: esiste quindi un indice $k\geq n_0$ tale che $a_k>M$. Per la monotonia, per ogni $n\geq k$ vale

$$
a_n\geq a_k>M.
$$

Abbiamo così verificato

$$
\forall M>0\;\exists k\;\forall n\geq k:\ a_n>M,
$$

cioè $a_n\to+\infty$. Il passaggio decisivo trasforma l'esistenza di **un** termine oltre la soglia nel superamento della soglia da parte di **tutti** i successivi.

Nel caso decrescente non limitato inferiormente, dato $M>0$ si trova $k$ con $a_k<-M$ e per ogni $n\geq k$ si ha $a_n\leq a_k<-M$: dunque $a_n\to-\infty$.

## Il viceversa è falso

Il teorema afferma che

$$
(a_n)\ \text{monotona}\ \implies\ (a_n)\ \text{regolare}.
$$

**Il viceversa non vale in generale**: sapere che una successione è regolare non basta per concludere che sia monotona. Una successione regolare può essere monotona oppure non esserlo.

Per esempio, per $n\geq1$,

$$
a_n=\frac{(-1)^n}{n}
$$

converge a zero perché $|a_n|=1/n\to0$, ma non è monotona: $a_1=-1<a_2=1/2$ e $a_2=1/2>a_3=-1/3$.

### Da dire all'orale

> Una successione crescente illimitata superiormente tende a più infinito: per ogni soglia esiste un termine che la supera, e la monotonia mantiene sopra la soglia tutti i termini successivi. Per una successione decrescente illimitata inferiormente il ragionamento è analogo verso meno infinito.

## Errori comuni

- Credere che la monotonia da sola garantisca un limite finito.
- Confondere il verso di monotonia con quello di avvicinamento: nel caso di limite finito, una successione crescente converge per difetto e una decrescente converge per eccesso.
- Usare il supremo senza aver verificato la limitatezza superiore.
- Confondere il supremo dell'insieme dei valori con il massimo: il limite può non essere mai raggiunto.
- Omettere il punto in cui la monotonia estende la stima da un termine a tutti i successivi.
- Dimenticare che la forma estesa ammette anche $+\infty$ o $-\infty$.

## Connessioni

- Combina [[75 Successioni Monotone|monotonia]] e [[70 Grafico e Limitatezza delle Successioni|limitatezza]].
- Usa [[26 Estremo Superiore e Inferiore|supremo e infimo]] e [[27 Completezza dei Numeri Reali|completezza di $\mathbb R$]].
- Conclude la [[74 Limiti Infiniti e Regolarità delle Successioni|regolarità]] di ogni successione monotona.

## Prospettiva d'esame

Occorre conoscere sia l'enunciato con le ipotesi direzionali corrette e il verso di avvicinamento (crescente per difetto, decrescente per eccesso), sia la dimostrazione: definizione del supremo, scelta di $n_\varepsilon$, uso della monotonia e verifica finale della condizione $\varepsilon$-$N$.
