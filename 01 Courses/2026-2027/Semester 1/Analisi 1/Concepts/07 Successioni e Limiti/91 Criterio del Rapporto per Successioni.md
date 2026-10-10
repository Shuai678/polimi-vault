---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 08, PDF pp. 15-17
  - Libro, §3.6, p. 99 e §3.7, p. 100
---

# Criterio del rapporto per successioni

## Quando si usa e intuizione

Il criterio è utile quando $a_n$ contiene fattoriali, potenze o prodotti che si semplificano nel rapporto tra due termini consecutivi. Si studia **$a_{n+1}/a_n$**, non il rapporto tra due successioni diverse.

Se il rapporto resta definitivamente sotto un numero minore di $1$, ogni termine si riduce almeno come in una progressione geometrica. Se resta sopra un numero maggiore di $1$, la successione cresce senza limite.

## Teorema

Sia $a_n>0$ definitivamente e supponiamo che esista

$$
\ell=\lim_{n\to+\infty}\frac{a_{n+1}}{a_n}\in[0,+\infty].
$$

Allora

$$
\boxed{
\begin{aligned}
0\leq\ell<1&\quad\Longrightarrow\quad a_n\to0,\\
\ell>1&\quad\Longrightarrow\quad a_n\to+\infty.
\end{aligned}}
$$

La seconda riga include $\ell=+\infty$. Il limite del rapporto, quando esiste, non può essere negativo perché i termini sono positivi nella coda. Con **$\ell=1$ il criterio non dà conclusioni**.

### Da dire all'orale

> Per una successione definitivamente positiva, se il rapporto tra il termine successivo e quello corrente tende a un valore minore di uno, la successione tende a zero; se tende a un valore maggiore di uno, diverge a più infinito. Quando il rapporto tende a uno, il criterio non è conclusivo.

## Dimostrazione di supporto e collegamento con il libro

Il PDF enuncia il criterio e rinvia la dimostrazione alla successiva trattazione delle serie. Qui non si introducono serie; il caso sotto $1$ può già essere giustificato con successioni monotone e algebra dei limiti.

> [!info] Approfondimento dal libro
> La dimostrazione del caso $\ell<1$ segue §3.6, p. 99. Il caso $\ell>1$ viene poi dedotto applicando il medesimo risultato alla successione reciproca.

### Caso $\ell<1$

Scegliamo $q$ con $\ell<q<1$. Per la definizione di limite, definitivamente

$$
0<\frac{a_{n+1}}{a_n}<q<1,
$$

quindi $0<a_{n+1}<a_n$. La coda è decrescente e limitata inferiormente da zero: per [[76 Teorema del Limite delle Successioni Monotone]] converge a un numero $A\geq0$.

Se $A>0$, anche $a_{n+1}\to A$ perché togliere il primo termine non modifica il limite. L'algebra dei limiti darebbe

$$
\frac{a_{n+1}}{a_n}\to\frac AA=1,
$$

in contraddizione con $\ell<1$. Perciò $A=0$.

### Caso $\ell>1$

Poniamo $b_n=1/a_n>0$. Il suo rapporto è

$$
\frac{b_{n+1}}{b_n}=\frac{a_n}{a_{n+1}}\to\frac1\ell<1,
$$

con limite $0$ se $\ell=+\infty$. Il caso precedente dà $b_n\to0^+$. Di conseguenza $a_n=1/b_n\to+\infty$, per [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate]].

## Perché $\ell=1$ non basta

Le tre successioni $a_n=1/n$, $a_n=1$ e $a_n=n$ soddisfano rispettivamente

$$
\frac{a_{n+1}}{a_n}=\frac n{n+1}\to1,\qquad
\frac{a_{n+1}}{a_n}=1,\qquad
\frac{a_{n+1}}{a_n}=\frac{n+1}{n}\to1.
$$

I loro limiti sono però $0$, $1$ e $+\infty$. Il valore $1$ del rapporto non decide neppure fra queste tre possibilità. Va cambiato metodo.

## Esempio 1 del PDF: esponenziale su fattoriale

### Testo

Per $a>0$ fissato studiare $u_n=a^n/n!$.

### Idea e svolgimento passo per passo

I termini sono positivi. Usando $(n+1)!=(n+1)n!$,

$$
\frac{u_{n+1}}{u_n}
=\frac{a^{n+1}}{(n+1)!}\frac{n!}{a^n}
=\frac a{n+1}\to0<1.
$$

Il criterio dà

$$
\boxed{\frac{a^n}{n!}\to0.}
$$

Per $a>1$ è il confronto già enunciato in [[85 Gerarchia degli Infiniti]]. La prova funziona in realtà per ogni base positiva fissata. Il caso $a=0$ si tratta direttamente per $n\geq1$.

## Esempio 2 del PDF: $n^n$ su fattoriale

### Testo e svolgimento

Poniamo $v_n=n^n/n!>0$. Allora

$$
\begin{aligned}
\frac{v_{n+1}}{v_n}
&=\frac{(n+1)^{n+1}}{(n+1)!}\frac{n!}{n^n}\\
&=\frac{(n+1)^n}{n^n}
=\left(1+\frac1n\right)^n\to e>1.
\end{aligned}
$$

Per [[90 Numero di Nepero e Limiti di Tipo Esponenziale]] il limite del rapporto è $e$. Quindi

$$
\boxed{\frac{n^n}{n!}\to+\infty,\qquad\frac{n!}{n^n}\to0.}
$$

La seconda conclusione segue passando al reciproco di una successione positiva divergente.

## Procedura pratica ed errori comuni

1. Controllare la positività definitiva.
2. Scrivere $a_{n+1}$ sostituendo **tutte** le occorrenze di $n$ con $n+1$.
3. Calcolare e semplificare $a_{n+1}/a_n$.
4. Calcolarne il limite e confrontarlo con $1$.
5. Se vale $1$, scegliere un altro metodo.

Errori frequenti: invertire il rapporto e dimenticare che le conclusioni si scambiano; perdere il fattore $n+1$ nel fattoriale; confondere il limite del rapporto con il limite di $a_n$.

Potenziale rilevanza d'esame: enunciato con positività e caso inconclusivo, calcoli con fattoriali e dimostrazione dei confronti già enunciati. Questo criterio riguarda il limite di una successione; i criteri di convergenza delle serie saranno un argomento successivo.
