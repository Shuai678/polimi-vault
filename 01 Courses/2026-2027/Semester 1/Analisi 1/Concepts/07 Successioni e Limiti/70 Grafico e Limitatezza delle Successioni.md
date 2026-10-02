---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF pp. 9-11
  - Libro, §3.1, pp. 75-76
---

# Grafico e limitatezza delle successioni

## Successione come funzione

Una successione reale è una funzione definita su $\mathbb N$, oppure su una sua coda, e a valori reali:

$$
a:\{n\in\mathbb N:n\geq n_0\}\to\mathbb R.
$$

Il valore assunto in $n$ si indica con $a_n$ e la successione con $(a_n)$. Per esempio,

$$
a_n=\frac1n \quad(n\geq1),
\qquad
b_n=\log(n-7) \quad(n\geq8).
$$

Il dominio può quindi iniziare da un indice diverso da zero quando la formula lo richiede.

## Grafico discreto

Il grafico della successione è l'insieme

$$
G(a)=\{(n,a_n):n\geq n_0\}.
$$

Poiché gli indici sono naturali, il grafico è formato da punti isolati e non da una curva continua. Per

$$
a_n=\frac{2}{n+1},
\qquad n\geq0,
$$

i primi punti sono $(0,2)$, $(1,1)$, $(2,2/3)$ e così via.

![[70 Grafico e Limitatezza Successioni.svg|595]]

## Limitatezza superiore e inferiore

La successione $(a_n)$ è:

- **limitata superiormente** se esiste $M\in\mathbb R$ tale che $a_n\leq M$ per ogni indice ammesso;
- **limitata inferiormente** se esiste $m\in\mathbb R$ tale che $m\leq a_n$ per ogni indice ammesso;
- **limitata** se è limitata sia superiormente sia inferiormente.

Essere limitata equivale all'esistenza di una costante $K>0$ tale che

$$
|a_n|\leq K
$$

per ogni indice ammesso. Infatti $|a_n|\leq K$ equivale a $-K\leq a_n\leq K$.

### Da dire all'orale

> Una successione è una funzione con variabile naturale. Il suo grafico è discreto, mentre la limitatezza riguarda l'intero insieme dei valori assunti.

## Errori comuni

- Disegnare il grafico di una successione come una curva continua.
- Dimenticare di dichiarare da quale indice è definita la formula.
- Scambiare la limitatezza della successione con la limitatezza dell'insieme degli indici.
- Verificare $|a_n|\leq K$ soltanto per gli indici grandi quando si vuole la limitatezza globale.

## Connessioni

- Approfondisce [[58 Successioni di Numeri Reali|la prima definizione di successione]].
- Usa [[24 Maggioranti Minoranti e Insiemi Limitati|insiemi limitati]] applicati all'insieme dei valori $\{a_n\}$.
- Prepara [[72 Limite Finito di una Successione|il limite di una successione]].

## Prospettiva d'esame

Per dimostrare che una successione è limitata bisogna trovare una costante valida per tutti gli indici del dominio, non soltanto osservare alcuni termini o il grafico.
