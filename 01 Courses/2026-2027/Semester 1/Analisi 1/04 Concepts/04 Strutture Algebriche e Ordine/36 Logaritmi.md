---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF pp. 2-3
  - Libro, cap. 1.5, pp. 12-13
---

# Logaritmi

## Intuizione

Il logaritmo permette di recuperare l'esponente di una potenza. Se sono noti la base $a$ e il risultato $y$, il numero $\log_a y$ è l'esponente al quale bisogna elevare $a$ per ottenere $y$.

## Definizione formale

Siano $a>0$, $a\neq1$ e $y>0$. Esiste un unico $x\in\mathbb{R}$ tale che

$$
a^x=y.
$$

Tale numero si chiama **logaritmo di $y$ in base $a$** e si indica con

$$
x=\log_a y.
$$

Equivalentemente,

$$
\log_a y=x \Longleftrightarrow a^x=y.
$$

### Da dire all'orale

> Dati una base $a$ positiva e diversa da uno e un argomento $y$ positivo, esiste un unico numero reale $x$ tale che $a^x=y$. Tale numero si chiama logaritmo di $y$ in base $a$ e si indica con $\log_a y$.

## Notazione

- $a$ è la base del logaritmo.
- $y$ è l'argomento del logaritmo.
- $x$ è il valore del logaritmo, cioè l'esponente cercato.

## Condizioni

- $a>0$;
- $a\neq1$;
- $y>0$.

La base $1$ è esclusa perché $1^x=1$ per ogni $x\in\mathbb{R}$: se $y=1$ vi sarebbero infinite soluzioni, mentre se $y\neq1$ non vi sarebbe alcuna soluzione.

## Metodo / Dimostrazione

La funzione esponenziale $f(x)=a^x$ è continua e strettamente monotona: crescente se $a>1$ e decrescente se $0<a<1$. Il suo insieme dei valori è $(0,+\infty)$. La continuità e il comportamento agli estremi garantiscono l'esistenza della soluzione di $a^x=y$ per ogni $y>0$; la stretta monotonia ne garantisce l'unicità.

Per determinare un logaritmo elementare:

1. si pone $x=\log_a y$;
2. si traduce nella forma equivalente $a^x=y$;
3. si cerca l'esponente $x$ che produce $y$.

### Segno del logaritmo

Il riferimento è $a^0=1$.

- Se $a>1$, allora $\log_a y>0$ per $y>1$, vale $0$ per $y=1$ ed è negativo per $0<y<1$.
- Se $0<a<1$, allora $\log_a y<0$ per $y>1$, vale $0$ per $y=1$ ed è positivo per $0<y<1$.

## Proprietà del prodotto

Per $a>0$, $a\neq1$, $y_1>0$ e $y_2>0$ vale

$$
\log_a(y_1y_2)=\log_a y_1+\log_a y_2.
$$

Ponendo $u=\log_a y_1$ e $v=\log_a y_2$, si ha $y_1=a^u$ e $y_2=a^v$. Pertanto

$$
y_1y_2=a^ua^v=a^{u+v},
$$

e, per la definizione e l'unicità del logaritmo,

$$
\log_a(y_1y_2)=u+v=\log_a y_1+\log_a y_2.
$$

I due fattori devono essere positivi separatamente. Non basta che il loro prodotto sia positivo, perché devono esistere entrambi i logaritmi al secondo membro.

## Proprietà del quoziente

Per $a>0$, $a\neq1$, $y_1>0$ e $y_2>0$ vale

$$
\log_a\left(\frac{y_1}{y_2}\right)=\log_a y_1-\log_a y_2.
$$

Ponendo $u=\log_a y_1$ e $v=\log_a y_2$, si ha $y_1=a^u$ e $y_2=a^v$. Pertanto

$$
\frac{y_1}{y_2}=\frac{a^u}{a^v}=a^{u-v},
$$

e, per la definizione e l'unicità del logaritmo,

$$
\log_a\left(\frac{y_1}{y_2}\right)=u-v=\log_a y_1-\log_a y_2.
$$

In particolare, poiché $\log_a1=0$,

$$
\log_a\left(\frac1y\right)=-\log_a y.
$$

L'ordine della sottrazione segue l'ordine del quoziente: prima il numeratore, poi il denominatore.

## Proprietà della potenza

Per $a>0$, $a\neq1$, $y>0$ e $b\in\mathbb{R}$ vale

$$
\log_a(y^b)=b\log_a y.
$$

Ponendo $u=\log_a y$, si ha $y=a^u$. Elevando alla potenza $b$,

$$
y^b=(a^u)^b=a^{ub}.
$$

Per la definizione e l'unicità del logaritmo,

$$
\log_a(y^b)=ub=b\log_a y.
$$

In particolare, per $n\in\mathbb{N}$ positivo,

$$
\log_a\sqrt[n]{y}=\frac1n\log_a y.
$$

## Cambiamento di base

Siano $a>0$, $a\neq1$, $b>0$, $b\neq1$ e $y>0$. Allora

$$
\log_b y=\frac{\log_a y}{\log_a b}.
$$

Ponendo $x=\log_b y$, si ha $b^x=y$. Applicando il logaritmo in base $a$ e usando la proprietà della potenza,

$$
x\log_a b=\log_a y.
$$

Poiché $b\neq1$, si ha $\log_a b\neq0$ e si può dividere:

$$
x=\frac{\log_a y}{\log_a b}.
$$

Il numeratore contiene l'argomento $y$; il denominatore contiene la base originaria $b$.

## Esempi

$$
\log_2 32=5
$$

perché $2^5=32$.

Inoltre,

$$
\log_{1/2}4=-2
$$

perché

$$
\left(\frac12\right)^{-2}=4.
$$

Inoltre,

$$
\log_3(9\cdot27)=\log_3 9+\log_3 27=2+3=5.
$$

Per il quoziente,

$$
\log_3\left(\frac{81}{3}\right)=\log_3 81-\log_3 3=4-1=3.
$$

Per la proprietà della potenza,

$$
\log_3(9^4)=4\log_3 9=4\cdot2=8.
$$

Per il cambiamento di base,

$$
\log_8 4=\frac{\log_2 4}{\log_2 8}=\frac23.
$$

## Errori comuni

- Dimenticare una delle condizioni $a>0$, $a\neq1$ e $y>0$.
- Credere che il segno del logaritmo dipenda soltanto dalla base: dipende anche dal confronto tra l'argomento e $1$.
- Confondere il logaritmo con il risultato della potenza invece di interpretarlo come esponente.
- Applicare la proprietà del prodotto a una somma: in generale $\log_a(y_1+y_2)\neq\log_a y_1+\log_a y_2$.
- Applicare la proprietà a fattori negativi soltanto perché il loro prodotto è positivo.
- Applicare la proprietà del quoziente a una differenza.
- Invertire l'ordine della sottrazione: il logaritmo del denominatore deve essere sottratto da quello del numeratore.
- Scrivere $\log_a(y^b)=(\log_a y)^b$: l'esponente diventa invece un fattore moltiplicativo.
- Applicare la proprietà della potenza con $y\leq0$, per cui il logaritmo reale di $y$ non esiste.
- Invertire il rapporto nella formula del cambiamento di base: al numeratore va l'argomento e al denominatore la base originaria.

## Connessioni

- [[35 Potenze con Esponente Reale|Le potenze con esponente reale]] permettono di definire il logaritmo.
- Il logaritmo è l'operazione inversa dell'esponenziale rispetto all'esponente.
- La stretta monotonia dell'esponenziale garantisce l'unicità del logaritmo.

## Prospettiva d'esame

Prima di calcolare un logaritmo bisogna controllare base e argomento. La traduzione $\log_a y=x\Longleftrightarrow a^x=y$ è il passaggio fondamentale sia nei calcoli sia nelle spiegazioni teoriche.
