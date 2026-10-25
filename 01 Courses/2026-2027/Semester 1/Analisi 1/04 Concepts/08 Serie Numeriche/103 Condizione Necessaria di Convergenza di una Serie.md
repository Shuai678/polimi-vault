---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 10, PDF pp. 18-19
  - Libro, §4.1, p. 115; teorema 4.4 e osservazioni 4.5-4.7
---

# Condizione necessaria di convergenza di una serie

## Intuizione

Se le somme parziali si stabilizzano verso un numero reale, l'effetto dell'aggiunta di un solo nuovo termine deve diventare arbitrariamente piccolo. Questo impone che il termine generale tenda a zero.

È una condizione **necessaria**, non sufficiente: tanti contributi sempre più piccoli possono continuare ad accumularsi senza limite. La [[104 Serie Armonica|serie armonica]] fornisce il controesempio richiesto dal docente.

## Teorema

Se la serie reale $\sum_{n=0}^{+\infty}a_n$ converge, allora

$$
\boxed{\lim_{n\to+\infty}a_n=0.}
$$

### Ipotesi e tesi

- **Ipotesi:** le somme parziali $S_N=\sum_{n=0}^{N}a_n$ convergono a $S\in\mathbb R$.
- **Tesi:** la successione dei termini $(a_n)$ è infinitesima.

Il limite $S$ deve essere **finito**. La sola regolarità della serie, che include la divergenza, non basta per questa conclusione.

## Strategia della dimostrazione

Esprimiamo il nuovo termine come differenza di due somme parziali consecutive. Entrambe tendono allo stesso limite finito; la loro differenza tende a zero.

## Dimostrazione passo per passo

Per ogni $N\geq1$,

$$
S_N=\sum_{n=0}^{N-1}a_n+a_N=S_{N-1}+a_N,
\qquad a_N=S_N-S_{N-1}.
$$

Per ipotesi $S_N\to S\in\mathbb R$. Anche $S_{N-1}\to S$: togliere o spostare un numero finito di indici non cambia il limite. L'[[80 Algebra dei Limiti di Successioni|algebra dei limiti finiti]] dà

$$
\lim_{N\to+\infty}a_N
=\lim_{N\to+\infty}(S_N-S_{N-1})
=S-S=0.
$$

Non possiamo ripetere lo stesso ragionamento con $S=+\infty$ o $S=-\infty$, perché la differenza degli infiniti è una forma indeterminata.

## Corollario: come escludere la convergenza

Per [[18 Dimostrazione per Contrapposizione]], se $a_n$ **non tende a zero**, la serie non converge. Questo include:

- il limite di $a_n$ esiste ed è reale non nullo;
- il limite è $+\infty$ o $-\infty$;
- il limite non esiste.

La conclusione è “non convergente”. Per distinguere divergenza e irregolarità serve un ulteriore studio delle somme parziali.

### Esempi già disponibili

- $\sum_{n=0}^{+\infty}1$ non converge perché $a_n\to1\neq0$; le somme $N+1$ mostrano più precisamente divergenza a $+\infty$.
- $\sum_{n=0}^{+\infty}(-1)^n$ non converge perché il termine non ha limite; le somme $1,0,1,0,\ldots$ mostrano irregolarità.
- Per una geometrica con $|q|\geq1$, $q^n$ non tende a zero: la condizione esclude la convergenza, coerentemente con [[100 Serie Geometrica e Rappresentazioni Decimali]].

## Il converso è falso

$$
a_n\to0\quad\not\Longrightarrow\quad
\sum_{n=0}^{+\infty}a_n\text{ converge}.
$$

La serie armonica parte dall'indice $1$ e ha termini $a_n=1/n\to0$, ma

$$
\sum_{n=1}^{+\infty}\frac1n=+\infty.
$$

La prova completa, con la disuguaglianza logaritmica del PDF, è in [[104 Serie Armonica]]. Per confronto, i termini $1/[n(n+1)]$ tendono anch'essi a zero e la [[102 Serie Telescopiche e Serie di Mengoli|serie di Mengoli]] converge a $1$. Lo stesso limite dei termini è compatibile con caratteri diversi.

## Uso negli esercizi

Il limite del termine generale è un controllo iniziale: se non è zero, si può già escludere la convergenza. Se è zero, il controllo è superato ma il problema resta aperto. Si cerca allora un'identità per le somme parziali o uno strumento ulteriore già disponibile nel corso.

## Errori comuni e prospettiva d'esame

- Chiamare questa condizione “criterio sufficiente di convergenza”.
- Concludere che la serie diverge necessariamente a $+\infty$ quando il termine non tende a zero.
- Confondere la somma $S$ con il limite zero del termine generale.
- Usare $S-S=0$ con $S$ infinito.

Potenziale rilevanza d'esame: enunciato con ipotesi di convergenza finita, dimostrazione, contrapposizione e controesempio al converso.

### Da dire all'orale

> Condizione necessaria perché una serie converga è che il termine generale tenda a zero. Infatti il termine è la differenza di due somme parziali consecutive, che in caso di convergenza tendono allo stesso numero reale. La condizione non è sufficiente: la serie armonica diverge pur avendo termine generale infinitesimo.
