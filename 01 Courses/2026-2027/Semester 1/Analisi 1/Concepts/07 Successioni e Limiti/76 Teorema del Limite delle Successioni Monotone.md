---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF pp. 20-25
  - Libro, §3.4, p. 90
---

# Teorema del limite delle successioni monotone

## Enunciato finito

Ogni successione monotona e limitata ammette limite finito. Più precisamente:

- se $(a_n)$ è crescente e limitata superiormente, allora

$$
\lim_{n\to+\infty}a_n=\sup\{a_n:n\geq n_0\};
$$

- se $(a_n)$ è decrescente e limitata inferiormente, allora

$$
\lim_{n\to+\infty}a_n=\inf\{a_n:n\geq n_0\}.
$$

Per una successione crescente basta dunque un maggiorante; per una decrescente basta un minorante.

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

Questa è esattamente la definizione di $a_n\to\ell$.

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

In forma compatta,

$$
\lim_{n\to+\infty}a_n=
\sup\{a_n:n\geq n_0\}
$$

per una successione crescente, ammettendo il valore $+\infty$, e analogamente il limite è l'infimo per una successione decrescente, ammettendo $-\infty$.

Ne segue che ogni successione monotona è regolare.

### Da dire all'orale

> Nel caso crescente il candidato limite è il supremo dei valori. La proprietà caratteristica del supremo permette di trovare un termine sopra $\ell-\varepsilon$; la monotonia mantiene tutti i termini successivi sopra quella soglia, mentre $\ell$ li maggiora.

## Errori comuni

- Credere che la monotonia da sola garantisca un limite finito.
- Usare il supremo senza aver verificato la limitatezza superiore.
- Confondere il supremo dell'insieme dei valori con il massimo: il limite può non essere mai raggiunto.
- Omettere il punto in cui la monotonia estende la stima da un termine a tutti i successivi.
- Dimenticare che la forma estesa ammette anche $+\infty$ o $-\infty$.

## Connessioni

- Combina [[75 Successioni Monotone|monotonia]] e [[70 Grafico e Limitatezza delle Successioni|limitatezza]].
- Usa [[26 Estremo Superiore e Inferiore|supremo e infimo]] e [[27 Completezza dei Numeri Reali|completezza di $\mathbb R$]].
- Conclude la [[74 Limiti Infiniti e Regolarità delle Successioni|regolarità]] di ogni successione monotona.

## Prospettiva d'esame

Occorre conoscere sia l'enunciato con le ipotesi direzionali corrette sia la dimostrazione: definizione del supremo, scelta di $n_\varepsilon$, uso della monotonia e verifica finale della condizione $\varepsilon$-$N$.
