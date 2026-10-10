---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 07, PDF pp. 15-16
  - Libro, §3.3.1, Teorema 3.30, p. 88
---

# Teorema dei due carabinieri

## Teorema del confronto per successioni convergenti

Siano $(a_n)$, $(b_n)$ e $(c_n)$ tre successioni reali tali che

$$
a_n\leq b_n\leq c_n\qquad\text{definitivamente}.
$$

Se le due successioni esterne convergono allo **stesso limite finito**,

$$
a_n\to\ell,\qquad c_n\to\ell,\qquad\ell\in\mathbb R,
$$

allora la successione intermedia converge e

$$
b_n\to\ell.
$$

La convergenza di $b_n$ è la tesi, quindi non va assunta prima di applicare il teorema. La notazione segue il PDF: $b_n$ è la successione intermedia, mentre nel libro il ruolo intermedio è assegnato a $c_n$.

## Intuizione e utilità

Se due barriere si avvicinano allo stesso numero, una successione che resta fra esse deve avvicinarsi a quel numero. I termini intermedi possono oscillare: ciò che conta è il controllo fra le barriere.

![[82 Due Carabinieri.svg|740]]

## Dimostrazione

Fissiamo $\varepsilon>0$. Dalla convergenza di $a_n$ esiste $N_1$ tale che

$$
\ell-\varepsilon<a_n<\ell+\varepsilon\qquad(n\geq N_1).
$$

Dalla convergenza di $c_n$ esiste $N_2$ tale che

$$
\ell-\varepsilon<c_n<\ell+\varepsilon\qquad(n\geq N_2).
$$

Il confronto definitivo fornisce un terzo indice $N_3$ tale che $a_n\leq b_n\leq c_n$ per $n\geq N_3$. Poniamo

$$
N=\max\{N_1,N_2,N_3\}.
$$

Per ogni $n\geq N$ tutte le condizioni valgono insieme, quindi

$$
\ell-\varepsilon<a_n\leq b_n\leq c_n<\ell+\varepsilon.
$$

Ne segue $|b_n-\ell|<\varepsilon$, esattamente la definizione di $b_n\to\ell$.

### Da dire all'orale

> Se una successione è definitivamente compresa tra due successioni convergenti allo stesso limite finito, converge anch'essa a quel limite. Si prende il massimo delle soglie necessarie per i due limiti e per il confronto, ottenendo la fascia richiesta dalla definizione.

## Metodo negli esercizi

Si usa quando la formula contiene un fattore oscillante o complicato, ma sono disponibili disuguaglianze semplici. La procedura è:

1. individuare la successione di cui si cerca il limite;
2. trovare un minorante e un maggiorante validi definitivamente;
3. calcolare i limiti di entrambe le barriere;
4. verificare che coincidano e applicare il teorema.

## Esercizio svolto

### Testo

Calcolare $\displaystyle\lim_{n\to+\infty}\left(2+\frac{(-1)^n}{n}\right)$.

### Idea

$(-1)^n$ oscilla, ma sta sempre fra $-1$ e $1$. Possiamo racchiudere l'intera successione fra due espressioni più semplici.

### Svolgimento passo per passo

Per $n\geq1$, essendo $n>0$, dividiamo $-1\leq(-1)^n\leq1$ per $n$ senza cambiare il verso:

$$
-\frac1n\leq\frac{(-1)^n}{n}\leq\frac1n.
$$

Aggiungendo $2$,

$$
2-\frac1n\leq2+\frac{(-1)^n}{n}\leq2+\frac1n.
$$

Le due barriere tendono a $2$, dunque

$$
\lim_{n\to+\infty}\left(2+\frac{(-1)^n}{n}\right)=2.
$$

### Cosa imparare

L'oscillazione di un fattore può essere controllata dalla sua ampiezza, anche quando quel fattore non ha limite.

## Errori comuni

- Supporre che le barriere debbano essere monotone: basta che convergano allo stesso limite.
- Usare barriere con limiti diversi: $0\leq(-1)^n+1\leq2$ non prova la convergenza.
- Applicare il confronto senza controllare il verso delle disuguaglianze, soprattutto dividendo per quantità negative.
- Passare al limite nella successione intermedia dando già per nota la sua convergenza.

## Connessioni e prospettiva d'esame

La dimostrazione usa [[72 Limite Finito di una Successione]] e [[71 Proprietà Definitivamente Vere]]. Il [[84 Confronto in Modulo e Prodotto con un Infinitesimo|confronto in modulo]] sarà una forma particolarmente pratica dello stesso principio.

Potenziale rilevanza d'esame: enunciato con le tre ipotesi, costruzione della soglia comune e scelta delle barriere negli esercizi con oscillazioni.
