---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF pp. 16-17
---

# Determinazione dell'argomento per quadranti

## Intuizione

La tangente non identifica da sola il quadrante, perché ha periodo $\pi$. Prima di usare l'arcotangente bisogna quindi osservare i segni della parte reale e della parte immaginaria.

## Metodo

Sia $z=x+iy\neq0$. Scegliendo l'argomento principale in $(-\pi,\pi]$:

$$
\theta=
\begin{cases}
\arctan\!\left(\dfrac yx\right), & x>0,\\[6pt]
\arctan\!\left(\dfrac yx\right)+\pi, & x<0,\ y\geq0,\\[6pt]
\arctan\!\left(\dfrac yx\right)-\pi, & x<0,\ y<0,\\[6pt]
\dfrac\pi2, & x=0,\ y>0,\\[6pt]
-\dfrac\pi2, & x=0,\ y<0.
\end{cases}
$$

### Da dire all'orale

> Per determinare l'argomento controllo prima il quadrante del punto $(x,y)$ e poi correggo il valore dell'arcotangente, perché la tangente ha periodo $\pi$ e non distingue quadranti opposti.

## Rappresentazione geometrica

![[Assets/49 Determinazione dell Argomento per Quadranti.svg|680]]

## Perché non basta l'arcotangente?

I numeri $1+i$ e $-1-i$ hanno lo stesso rapporto

$$
\frac yx=1,
$$

ma appartengono a quadranti opposti. Il valore $\arctan(1)=\pi/4$ è corretto per $1+i$, non per $-1-i$.

## Esempio della lezione

Per

$$
z=-1-i,
$$

si ha $x<0$ e $y<0$, quindi il punto appartiene al terzo quadrante. Inoltre,

$$
\arctan\!\left(\frac yx\right)=\arctan(1)=\frac\pi4.
$$

Per ottenere l'angolo nel terzo quadrante si sottrae $\pi$:

$$
\arg z=\frac\pi4-\pi=-\frac{3\pi}{4}.
$$

## Condizioni

- Se $x=0$, il rapporto $y/x$ non è definito e si usano direttamente gli angoli degli assi.
- Se $z=0$, l'argomento non è definito.
- Le correzioni dipendono dall'intervallo scelto per l'argomento principale.

## Errori comuni

- Usare sempre $\arctan(y/x)$ senza controllare il quadrante.
- Dividere per $x$ quando $x=0$.
- Confondere il terzo quadrante con un angolo principale positivo maggiore di $\pi$ quando si è scelto $(-\pi,\pi]$.
- Usare separatamente $\arcsin(y/\rho)$ o $\arccos(x/\rho)$ senza risolvere l'ambiguità del quadrante.

## Connessioni

- Completa il metodo della [[48 Forma Trigonometrica dei Numeri Complessi|forma trigonometrica]].
- Usa la posizione del punto nel [[40 Piano Complesso e Interpretazione Vettoriale|piano complesso]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: determinare l'argomento senza errori di quadrante, soprattutto quando la parte reale è negativa o nulla.
