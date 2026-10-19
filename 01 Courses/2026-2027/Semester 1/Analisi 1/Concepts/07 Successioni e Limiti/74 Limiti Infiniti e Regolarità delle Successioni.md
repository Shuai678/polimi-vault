---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF pp. 15-19
  - Libro, §3.2, pp. 82-84
---

# Limiti infiniti e regolarità delle successioni

## Intuizione: dal limite finito al limite infinito

Il ragionamento comune è questo: qualunque condizione di vicinanza al limite si scelga, tutti i termini da un certo indice in poi devono soddisfarla.

Per un limite finito $\ell\in\mathbb R$, la vicinanza si esprime mediante la distanza: scelta una precisione arbitraria $\varepsilon>0$, si richiede che [[71 Proprietà Definitivamente Vere|definitivamente]]

$$
|a_n-\ell|<\varepsilon.
$$

Per un limite infinito si usano invece delle **soglie**. Infatti, $+\infty$ e $-\infty$ non sono numeri reali: la distanza ordinaria tra un numero reale e l'infinito non è definita.

- Per $+\infty$, scelta una soglia $M>0$ grande quanto si vuole, si richiede che [[71 Proprietà Definitivamente Vere|definitivamente]] $a_n>M$.
- Per $-\infty$, scelto $M>0$, si richiede che [[71 Proprietà Definitivamente Vere|definitivamente]] $a_n<-M$. Qui $M$ rappresenta una distanza positiva dallo zero, mentre la soglia $-M$ è negativa.

Per esempio, tra $10$ e $1000$, il numero $1000$ è più avanti nella direzione di $+\infty$, perché è maggiore. Chiamarlo «più vicino a $+\infty$» è solo un'espressione intuitiva, non un confronto tra distanze dall'infinito. La distanza da zero da sola non basta: anche $-1000$ è molto lontano da zero, ma nella direzione opposta.

**Superare una singola soglia non basta per tendere a $+\infty$**: bisogna superare ogni soglia fissata e rimanerci sopra da un certo indice in poi. Analogamente, per tendere a $-\infty$ bisogna stare [[71 Proprietà Definitivamente Vere|definitivamente]] sotto ogni soglia negativa fissata. Non è necessario che la successione sia monotona.


## Limite $+\infty$

Data una successione $(a_n)$, si dice che essa diverge a $+\infty$ e si scrive:

$$
\lim_{n\to+\infty}a_n=+\infty
$$

se

$$
\forall M>0\;\exists N\in\mathbb N\;\forall n\geq N:
a_n>M.
$$

Qualunque sia la soglia positiva $M$, tutti i termini abbastanza avanzati la superano.

## Limite $-\infty$

Data una successione $(a_n)$, si dice che essa diverge a $-\infty$ e si scrive:

$$
\lim_{n\to+\infty}a_n=-\infty
$$

se

$$
\forall M>0\;\exists N\in\mathbb N\;\forall n\geq N:
a_n<-M.
$$

Qualunque sia la soglia negativa $-M$, tutti i termini abbastanza avanzati stanno al di sotto di essa.

![[74 Limiti Infiniti Successioni.svg|668]]


## Esempio: $\log(1/n)\to-\infty$

Fissato $M>0$, si vuole ottenere

$$
\log\frac1n<-M.
$$

Poiché l'esponenziale è crescente,

$$
\log\frac1n<-M
\quad\Longleftrightarrow\quad
\frac1n<e^{-M}
\quad\Longleftrightarrow\quad
n>e^M.
$$

È sufficiente scegliere un indice naturale $N>e^M$.

## Successioni regolari e irregolari

Si introduce la retta reale estesa

$$
\overline{\mathbb R}=\mathbb R\cup\{-\infty,+\infty\}.
$$

Secondo la terminologia della lezione:

* è **regolare** se ammette limite in $\overline{\mathbb R}$, quindi:
	- una successione **converge** se ha limite finito;
	- **diverge a $+\infty$** o **a $-\infty$** se ha il corrispondente limite infinito;
- è **irregolare**, oscillante o indeterminata se non ha né limite finito né limite infinito, cioè se non ammette alcun limite in $\overline{\mathbb R}$.


Esempi di successioni irregolari sono

$$
(-1)^n,
\qquad
(-2)^n,
$$

e la successione

$$
a_n=
\begin{cases}
2^n, & n\text{ pari},\\
1, & n\text{ dispari}.
\end{cases}
$$

La prima è limitata, la seconda è illimitata e la terza presenta una sottosuccessione costante e una che cresce: limitatezza o illimitatezza, da sole, non decidono la regolarità.

Il limite in $\overline{\mathbb R}$, quando esiste, è unico.

## Infinitesimi e infiniti

Una successione si dice:

- **infinitesima** se $a_n\to0$;
- **infinita** se $a_n\to+\infty$ oppure $a_n\to-\infty$.

## Convergenza per eccesso o per difetto

Se $a_n\to\ell\in\mathbb R$ e [[71 Proprietà Definitivamente Vere|definitivamente]]

$$
a_n\geq\ell,
$$

si dice che $a_n$ converge a $\ell$ **per eccesso** e si può scrivere $a_n\to\ell^+$.
Se invece [[71 Proprietà Definitivamente Vere|definitivamente]]

$$
a_n\leq\ell,
$$

si parla di convergenza **per difetto** e si scrive $a_n\to\ell^-$. Per esempio,

$$
2^{1/n}\to1^+,
\qquad
\frac{n}{n+1}\to1^-.
$$

La successione $(-1)^n/n\to0$ non converge né per eccesso né per difetto, perché cambia segno infinite volte.

### Da dire all'orale

> Un limite infinito non significa che i termini siano infiniti: significa che superano [[71 Proprietà Definitivamente Vere|definitivamente]] ogni soglia fissata. Una successione è regolare se ha un comportamento limite, finito o infinito.

## Errori comuni

- Scrivere $a_n=+\infty$ invece di esprimere il superamento di ogni soglia.
- Credere che bastino termini arbitrariamente grandi: devono essere grandi tutti i termini da un certo indice in poi.
- Chiamare “divergente” qualunque successione non convergente, ignorando la terminologia specifica della lezione.
- Confondere una successione illimitata con una successione che tende necessariamente a $+\infty$ o $-\infty$.
- Parlare di convergenza per eccesso o difetto senza la condizione definitiva rispetto al limite.

## Connessioni

- Usa [[71 Proprietà Definitivamente Vere|proprietà definitivamente vere]].
- Estende [[72 Limite Finito di una Successione|il limite finito]] alla retta reale estesa.
- Riprende [[73 Unicità del Limite di Successione|l'unicità del limite]].
- Le successioni monotone risultano sempre regolari per [[76 Teorema del Limite delle Successioni Monotone|il teorema del limite monotono]].

## Prospettiva d'esame

Per dimostrare un limite infinito si parte da una soglia arbitraria $M>0$, si risolve la disuguaglianza richiesta e si ricava una soglia naturale $N=N(M)$ valida per tutti gli indici successivi.
