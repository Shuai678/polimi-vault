---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 2-3
---

# Code e resto di una serie

## Intuizione

Una somma parziale approssima la somma di una serie convergente. Ciò che manca è la somma di tutti i termini successivi: il **resto**. Prima di usarlo come errore di approssimazione occorre distinguere la serie di coda, che è sempre una scrittura formale, dal suo eventuale valore reale.

## Serie di coda e carattere

Consideriamo $\sum_{n=1}^{+\infty}a_n$ e poniamo $S_N=\sum_{n=1}^{N}a_n$. Per un indice $N$ **fissato**, la coda è

$$
\sum_{n=N+1}^{+\infty}a_n.
$$

La serie originale e ciascuna sua coda hanno lo stesso carattere: convergono entrambe, divergono entrambe allo stesso infinito oppure sono entrambe irregolari. È il teorema iniziale del PDF e precisa l'invarianza rispetto ai primi termini già discussa in [[99 Serie Numeriche e Somme Parziali]].

### Dimostrazione

Per $M>N$, la somma parziale della coda è

$$
T_M^{(N)}=\sum_{n=N+1}^{M}a_n=S_M-S_N.
$$

Qui $S_N$ è una costante reale perché $N$ è fissato. Quando $M\to+\infty$, sottrarre tale costante conserva il carattere di $(S_M)$. Il viceversa segue da $S_M=T_M^{(N)}+S_N$. In particolare, per decidere il carattere si può iniziare da qualunque indice successivo a un numero finito di termini.

## Definizione del resto e identità fondamentale

Se la serie converge a $S\in\mathbb R$, la sua coda converge a un numero reale, detto **resto $N$-esimo**:

$$
\boxed{R_N:=\sum_{n=N+1}^{+\infty}a_n=S-S_N.}
$$

L'uguaglianza segue passando al limite per $M\to+\infty$ nell'identità finita precedente. Di conseguenza

$$
S=S_N+R_N,\qquad |S-S_N|=|R_N|.
$$

$|R_N|$ è l'errore assoluto commesso usando $S_N$ al posto di $S$. Per una serie a termini non negativi, $R_N\geq0$ e le somme parziali approssimano $S$ dal basso.

## Teorema: il resto tende a zero

Per una serie convergente,

$$
\boxed{\lim_{N\to+\infty}R_N=0.}
$$

**Dimostrazione.** Ora facciamo variare $N$: poiché $S_N\to S$ e $S$ è finito, $R_N=S-S_N\to S-S=0$.

I due passaggi hanno ruoli diversi: per definire il singolo $R_N$ si somma la coda tenendo $N$ fissato; successivamente si studia la successione $(R_N)$ quando $N$ cresce.

### Da dire all'orale

> Il resto N-esimo di una serie convergente è la somma della coda che comincia dall'indice N più uno. È uguale alla somma totale meno la somma parziale fino a N e tende a zero quando N tende a infinito. Il suo valore assoluto misura l'errore dell'approssimazione mediante la somma parziale.

## Esempi già calcolati nel vault

Per la geometrica di ragione $1/2$, **partendo da $n=0$**, [[100 Serie Geometrica e Rappresentazioni Decimali]] dà

$$
S=2,\quad S_N=2-2^{-N},\quad R_N=2^{-N}.
$$

Per la [[102 Serie Telescopiche e Serie di Mengoli|serie di Mengoli]], **partendo da $n=1$**,

$$
S=1,\quad S_N=1-\frac1{N+1},\quad R_N=\frac1{N+1}.
$$

Per un errore minore di $10^{-3}$ bastano $N=10$ nella prima ($1/1024<10^{-3}$) e $N=1000$ nella seconda ($1/1001<10^{-3}$). Sono rispettivamente $11$ e $1000$ termini, perché gli indici iniziali sono diversi.

## Errori comuni e prospettiva d'esame

- Confondere il resto $R_N$, una somma di infiniti termini, con il primo termine escluso $a_{N+1}$.
- Usare $R_N=S-S_N$ come errore reale quando la serie non converge a un numero reale.
- Confondere $R_N\to0$ con $a_n\to0$: la seconda è solo la [[103 Condizione Necessaria di Convergenza di una Serie|condizione necessaria]] e non prova la convergenza.
- Dimenticare che la coda inizia da $N+1$.

Potenziale rilevanza d'esame: rapporto tra serie e code, definizione del resto e controllo dell'errore di approssimazione.
