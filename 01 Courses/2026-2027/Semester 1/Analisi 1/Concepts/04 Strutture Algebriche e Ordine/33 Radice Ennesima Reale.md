---
course: Analisi 1
type: theorem
status: da-verificare
source:
  - Lezione 02, PDF pp. 25-26
  - Libro, cap. 1.4
---

# Radice ennesima reale

## Teorema

Siano $y\in\mathbb{R}$ con $y\geq0$ e $n\in\mathbb{N}$ con $n\geq1$. Esiste un unico $x\in\mathbb{R}$ tale che

$$
x\geq0
$$

e

$$
x^n=y.
$$

Questo numero è la radice $n$-esima di $y$ e si indica con

$$
x=\sqrt[n]{y}=y^{1/n}.
$$

## In parole semplici

Ogni numero reale non negativo possiede una e una sola radice $n$-esima non negativa.

## Condizioni

- $y\in\mathbb{R}$;
- $y\geq0$;
- $n\in\mathbb{N}$ e $n\geq1$;
- la soluzione individuata dal simbolo di radice soddisfa $x\geq0$.

## Conclusione

$$
\exists!x\geq0:\ x^n=y.
$$

## Perché è utile

Il teorema definisce rigorosamente le radici e permette di introdurre le potenze con esponente razionale.

## Intuizione

La funzione $f(t)=t^n$ è continua e strettamente crescente su $[0,+\infty)$, parte da zero e cresce senza limite. Perciò raggiunge ogni valore $y\geq0$ una sola volta.

## Strategia della dimostrazione

La continuità garantisce l'esistenza tramite il teorema dei valori intermedi; la stretta monotonia garantisce l'unicità.

## Dimostrazione passo per passo

Se $y=0$, l'unica soluzione non negativa è $x=0$.

Sia ora $y>0$ e consideriamo $f(t)=t^n$ per $t\geq0$. Si ha

$$
f(0)=0<y.
$$

Scegliendo $M=y+1$, si ha $M>1$ e

$$
f(M)=M^n\geq M>y.
$$

Poiché $f$ è continua su $[0,M]$, il teorema dei valori intermedi garantisce l'esistenza di $x\in(0,M)$ con $f(x)=y$.

Se esistessero due soluzioni non negative $x_1<x_2$, la stretta crescita di $f$ implicherebbe

$$
x_1^n<x_2^n,
$$

in contraddizione con $x_1^n=x_2^n=y$. La soluzione non negativa è quindi unica.

## Esempi

$$
\sqrt[4]{16}=2.
$$

L'equazione $x^4=16$ ha invece due soluzioni reali, $x=2$ e $x=-2$.

Per ogni $a\in\mathbb{R}$,

$$
\sqrt{a^2}=|a|.
$$

## Uso all'esame

Bisogna distinguere il valore della radice, che per definizione è non negativo, dall'insieme di tutte le soluzioni dell'equazione associata.

## Errore comune

- Scrivere $\sqrt[4]{16}=\pm2$.
- Scrivere $\sqrt{a^2}=a$ senza considerare il caso $a<0$.
- Dimenticare le condizioni sul radicando e sull'indice.

## Da dire all'orale

> Dato $y\in\mathbb{R}$ non negativo e $n\in\mathbb{N}$ positivo, esiste un unico $x\in\mathbb{R}$ non negativo tale che $x^n=y$; tale numero si chiama radice $n$-esima di $y$.

## Connessioni

- [[27 Completezza dei Numeri Reali|La completezza di $\mathbb{R}$]] sostiene l'esistenza delle radici reali.
- Le radici permettono di definire le potenze con esponente razionale.
- [[29 Valore Assoluto|Il valore assoluto]] compare nella formula $\sqrt{a^2}=|a|$.

## Sintassi LaTeX Suite

Le formule sono scritte con sintassi già espansa e renderizzabile, tra cui $\sqrt[n]{y}$, $\exists!$, $\mathbb{R}$ e $\mathbb{N}$.
