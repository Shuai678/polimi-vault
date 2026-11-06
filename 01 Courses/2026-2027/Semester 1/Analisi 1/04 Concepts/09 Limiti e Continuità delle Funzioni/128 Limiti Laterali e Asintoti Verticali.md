---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 3-6
  - Libro, §5.3, p. 143; §5.12, pp. 170-171
---

# Limiti laterali e asintoti verticali

## Perché distinguere il lato di avvicinamento

Dopo i limiti infiniti al finito, il professore distingue il comportamento quando $x$ si avvicina a $x_0$ **da destra** oppure **da sinistra**. Per la definizione destra occorre che $x_0$ sia di accumulazione per $I\cap(x_0,+\infty)$; per quella sinistra, per $I\cap(-\infty,x_0)$.

## Definizioni del docente: prima il lato destro, poi il sinistro

$$
\lim_{x\to x_0^+}f(x)=+\infty\quad(-\infty)
$$

significa che, per ogni $M>0$, esiste $\delta>0$ tale che, per $x\in I$,

$$
x_0<x<x_0+\delta\Longrightarrow f(x)>M
\quad\bigl(f(x)<-M\bigr).
$$

Analogamente,

$$
\lim_{x\to x_0^-}f(x)=+\infty\quad(-\infty)
$$

significa che, per ogni $M>0$, esiste $\delta>0$ tale che

$$
x_0-\delta<x<x_0\Longrightarrow f(x)>M
\quad\bigl(f(x)<-M\bigr).
$$

Per un limite finito $\ell\in\mathbb R$, si sostituisce la richiesta sui valori con $|f(x)-\ell|<\varepsilon$, quantificando $\forall\varepsilon>0\ \exists\delta>0$.

## Esempio del docente: $1/x$ in zero

Il limite bilatero non esiste, mentre

$$
\lim_{x\to0^+}\frac1x=+\infty,
\qquad
\lim_{x\to0^-}\frac1x=-\infty.
$$

Il segno del denominatore distingue i due risultati.

## Proposizione: limite bilatero e limiti laterali

Supponiamo che $x_0\in\mathbb R$ sia punto di accumulazione del dominio **da entrambi i lati**. Per $\ell\in\overline{\mathbb R}$,

$$
\lim_{x\to x_0}f(x)=\ell
\iff
\lim_{x\to x_0^+}f(x)=\lim_{x\to x_0^-}f(x)=\ell.
$$

Se almeno uno dei due limiti laterali non esiste nella retta estesa, oppure se esistono ma sono diversi, il limite bilatero non esiste. Nel PDF questa proposizione è enunciata, senza una dimostrazione sviluppata.

## Asintoto verticale

Il docente chiama la retta **$x=x_0$ asintoto verticale** se almeno uno dei limiti laterali di $f$ in $x_0$ vale $+\infty$ oppure $-\infty$. Sono inclusi i casi in cui esiste un limite bilatero infinito.

Gli esempi del PDF sono:

- $f(x)=1/x^2$: entrambi i limiti in zero valgono $+\infty$;
- $f(x)=\log x$, dominio $(0,+\infty)$: $\lim_{x\to0^+}\log x=-\infty$;
- $f(x)=1/x$: i due limiti sono infiniti di segno opposto.

Tutte e tre hanno asintoto verticale $x=0$. Per $\log x$ la definizione da sinistra non si applica, perché il dominio non accumula in zero da quel lato.

![[128 Limiti Laterali e Asintoti Verticali.svg|900]]

## Commenti ed errori comuni

Il segno in $x_0^+$ o $x_0^-$ riguarda il lato delle **ascisse**. Il segno in $\ell^+$ o $\ell^-$ dei [[124 Limiti Finiti all'Infinito e Asintoti Orizzontali|limiti per eccesso e difetto]] riguarda invece la posizione dei **valori** rispetto a $\ell$. Si possono usare entrambe le indicazioni contemporaneamente.

Un asintoto verticale può esistere anche se il limite bilatero non esiste, come per $1/x$. Inoltre non impone che la funzione sia priva di valore in $x_0$: un eventuale valore assegnato al solo centro non modifica i limiti laterali.

### Da dire all'orale

> Il limite da destra controlla soltanto i punti del dominio maggiori del punto di avvicinamento; quello da sinistra soltanto i minori. Se il dominio accumula da entrambi i lati, il limite bilatero esiste se e solo se i laterali esistono e coincidono. Una retta verticale è asintoto se almeno un limite laterale è infinito.
