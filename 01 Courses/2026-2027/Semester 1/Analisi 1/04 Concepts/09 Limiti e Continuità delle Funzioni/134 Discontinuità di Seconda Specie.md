---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 16-18
  - Libro, §6.2, pp. 187-189; confronto terminologico con il PDF
---

# Discontinuità di seconda specie

## Terzo caso della classificazione del docente

Sia $x_0\in I$ punto del dominio di accumulazione dai lati considerati. Il professore chiama $x_0$ punto di **discontinuità di seconda specie** se

- esistono i due limiti laterali nella retta estesa e almeno uno è infinito;
- oppure almeno uno dei limiti laterali **non esiste nella retta reale estesa**.

Si comprendono quindi sia divergenze infinite sia oscillazioni senza limite.

## Esempi del docente, nello stesso ordine

In tutti gli esempi viene assegnato $f(0)=a$, con $a\in\mathbb R$. Questo rende zero un punto del dominio: la classificazione come discontinuità ha allora senso.

### 1. $f(x)=1/x$ per $x\neq0$

$$
\lim_{x\to0^-}f(x)=-\infty,\qquad
\lim_{x\to0^+}f(x)=+\infty.
$$

Il limite bilatero non esiste; entrambi i laterali sono infiniti. La discontinuità è di seconda specie per ogni $a$.

### 2. $f(x)=1/x^2$ per $x\neq0$

I due limiti laterali e il limite bilatero valgono $+\infty$. La funzione non è continua in zero, qualunque sia il valore reale $a$; la discontinuità è di seconda specie.

### 3. $f(x)=e^{1/x}$ per $x\neq0$

Da sinistra $1/x\to-\infty$, quindi $e^{1/x}\to0$. Da destra $1/x\to+\infty$, quindi $e^{1/x}\to+\infty$:

$$
\lim_{x\to0^-}f(x)=0,\qquad
\lim_{x\to0^+}f(x)=+\infty.
$$

Basta un solo limite laterale infinito. Anche scegliendo $a=0$ si ottiene continuità soltanto da sinistra, non continuità nel punto.

### 4. $f(x)=\sin(1/x)$ per $x\neq0$

L'oscillazione non si riduce avvicinandosi a zero: i limiti laterali non esistono, nemmeno infiniti. È ancora seconda specie secondo il docente.

![[134 Discontinuita di Seconda Specie.svg|900]]

## Commenti e verifica dell'ultimo esempio

Per il limite destro, scegliamo

$$
x_n=\frac1{\pi/2+2n\pi},\qquad
z_n=\frac1{3\pi/2+2n\pi}.
$$

Entrambe le successioni sono positive e tendono a zero; tuttavia $\sin(1/x_n)=1$ e $\sin(1/z_n)=-1$. Il criterio delle [[121 Limite di Funzione e Definizione Successionale|due successioni]] esclude il limite destro. Usando le successioni negative opposte si esclude anche quello sinistro. La scelta esplicita delle successioni è una spiegazione aggiunta all'esempio grafico del PDF.

> [!info] Approfondimento dal libro: differenza di terminologia
> Il libro, §6.2, pp. 187-189, distingue la seconda specie con limiti infiniti dalla **terza specie** quando manca un limite laterale nella retta estesa. Il professore include entrambe le situazioni nella **seconda specie**. Nel vault si segue la classificazione del professore; perciò anche $\sin(1/x)$ in zero rientra qui.

## Uso negli esercizi ed errori comuni

Per classificare una discontinuità controllare prima che il punto appartenga al dominio, poi calcolare i due limiti laterali e infine confrontarli con il valore nel punto. La seconda specie non richiede che entrambi i limiti siano infiniti, e non coincide con la sola presenza di un asintoto verticale: l'esempio oscillante non ha un limite laterale infinito.

Nessuna scelta di un singolo valore reale $f(0)$ può rendere finito e coincidente un limite inesistente o infinito. Non si tratta quindi di una discontinuità eliminabile.

### Da dire all'orale

> Secondo la classificazione del corso, la discontinuità è di seconda specie se almeno un limite laterale è infinito oppure non esiste nemmeno nella retta reale estesa. Sono inclusi sia comportamenti divergenti sia oscillanti. La scelta del valore nel punto non può eliminare questa discontinuità.
