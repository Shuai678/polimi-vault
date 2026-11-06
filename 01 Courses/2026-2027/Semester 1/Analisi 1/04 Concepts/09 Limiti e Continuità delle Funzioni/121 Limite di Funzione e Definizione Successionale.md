---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 13, PDF pp. 4-6
---

# Limite di funzione e definizione successionale

## Definizione successionale del docente

Siano $f:I\subseteq\mathbb R\to\mathbb R$, $x_0\in\overline{\mathbb R}$ punto di accumulazione per $I$, e $\ell\in\overline{\mathbb R}$. Diciamo che

$$
\lim_{x\to x_0}f(x)=\ell
$$

se **per ogni successione** $(x_n)$ tale che

1. $x_n\in I$;
2. $x_n\neq x_0$ per ogni $n\geq1$;
3. $\lim_{n\to+\infty}x_n=x_0$;

vale

$$
\lim_{n\to+\infty}f(x_n)=\ell.
$$

L'ipotesi sui [[120 Punti di Accumulazione]] garantisce che esistano successioni ammissibili. Se $x_0$ è infinito, $x_n\neq x_0$ è automatico perché $x_n$ è reale.

## Osservazione del docente: due successioni per negare un limite

Se esistono due successioni ammissibili $(x_n)$ e $(z_n)$, entrambe tendenti a $x_0$, ma

$$
\lim_{n\to+\infty}f(x_n)=\ell_1,\qquad
\lim_{n\to+\infty}f(z_n)=\ell_2,\qquad\ell_1\neq\ell_2,
$$

allora **non esiste** $\lim_{x\to x_0}f(x)$ nella retta reale estesa. Un eventuale limite dovrebbe essere lo stesso lungo entrambe le successioni.

## Esempio del docente: $\sin x$ per $x\to+\infty$

Scegliamo, come nel PDF,

$$
x_n=\frac\pi2+2n\pi,\qquad
z_n=\frac{3\pi}2+2n\pi,\qquad n\geq1.
$$

Entrambe tendono a $+\infty$. Tuttavia

$$
\lim_{n\to+\infty}\sin z_n=-1
\neq1=\lim_{n\to+\infty}\sin x_n.
$$

Quindi $\lim_{x\to+\infty}\sin x$ non esiste, nemmeno come limite infinito.

![[121 Seno e Due Successioni.svg|900]]

## Commenti: cosa significa “per ogni”

Per **provare** un limite non basta scegliere una successione comoda. Il limite $f(n)\to\ell$ controlla soltanto gli interi; una funzione può comportarsi diversamente fra un intero e il successivo. Per **confutare** il limite bastano invece due percorsi con esiti diversi, come nell'esempio.

Il valore $f(x_0)$ non entra nella definizione: $x_0$ può essere fuori dal dominio oppure avere un valore diverso da quello suggerito dai punti vicini. Questa distinzione sarà decisiva per la [[130 Continuità di una Funzione]].

### Uso negli esercizi

Si individua il dominio, si verifica che $x_0$ sia di accumulazione e si scelgono successioni che rendano semplici i valori della funzione. Per funzioni oscillanti, spesso si fissano fasi del seno o del coseno che producono valori costanti diversi. Entrambe le successioni devono tendere allo **stesso** punto nella stessa direzione richiesta.

### Da dire all'orale

> Una funzione tende a un limite in un punto di accumulazione del dominio se, per ogni successione di punti del dominio diversi dal punto e tendente a esso, la successione dei valori della funzione tende a quel limite. Due successioni ammissibili con immagini aventi limiti diversi ne escludono l'esistenza.
