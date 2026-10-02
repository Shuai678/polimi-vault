---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF p. 16
  - Libro, §1.8.1, p. 20
---

# Forma trigonometrica dei numeri complessi

## Intuizione

La forma algebrica descrive un numero complesso mediante le coordinate cartesiane $(x,y)$. La forma trigonometrica descrive lo stesso punto mediante distanza dall'origine e angolo.

## Definizione formale

Sia $z=x+iy\neq0$, con

$$
\rho=|z|,
\qquad
\theta=\arg z.
$$

Dal triangolo rettangolo associato al punto $z$,

$$
\cos\theta=\frac{x}{\rho},
\qquad
\sin\theta=\frac{y}{\rho}.
$$

Quindi

$$
x=\rho\cos\theta,
\qquad
y=\rho\sin\theta.
$$

Sostituendo in $z=x+iy$ si ottiene

$$
z=\rho(\cos\theta+i\sin\theta).
$$

### Da dire all'orale

> Se $z\neq0$ ha modulo $\rho$ e argomento $\theta$, allora la sua forma trigonometrica è $z=\rho(\cos\theta+i\sin\theta)$.

## Notazione

- $\rho=|z|$ è il modulo e soddisfa $\rho>0$.
- $\theta$ è un argomento di $z$ ed è definito a meno di multipli interi di $2\pi$.
- $x=\rho\cos\theta$ e $y=\rho\sin\theta$ riconducono alla forma algebrica.

## Metodo

Per passare dalla forma algebrica alla forma trigonometrica:

1. Calcolare $\rho=\sqrt{x^2+y^2}$.
2. Individuare il quadrante di $(x,y)$.
3. Determinare un argomento $\theta$ compatibile con entrambi i segni di $x$ e $y$.
4. Scrivere $z=\rho(\cos\theta+i\sin\theta)$.

Per tornare alla forma algebrica:

$$
x=\rho\cos\theta,
\qquad
y=\rho\sin\theta.
$$

## Condizioni

Per $z=0$, il modulo è $0$ ma l'argomento non è definito; perciò la rappresentazione polare non determina un angolo unico per lo zero.

## Esempio

Per $z=-1-i$,

$$
\rho=\sqrt{(-1)^2+(-1)^2}=\sqrt2.
$$

Il punto è nel terzo quadrante e un argomento principale è $-3\pi/4$. Pertanto

$$
z=\sqrt2\left(\cos\left(-\frac{3\pi}{4}\right)+i\sin\left(-\frac{3\pi}{4}\right)\right).
$$

## Errori comuni

- Calcolare l'angolo senza controllare il quadrante.
- Dimenticare il fattore $\rho$ davanti alle funzioni trigonometriche.
- Scambiare seno e coseno: il coseno produce la parte reale, il seno quella immaginaria.
- Assegnare un argomento allo zero.

## Connessioni

- Converte le coordinate cartesiane del [[40 Piano Complesso e Interpretazione Vettoriale|piano complesso]] in coordinate polari.
- Richiede [[47 Modulo e Argomento dei Numeri Complessi|modulo e argomento]].
- Il titolo del PDF anticipa anche la forma esponenziale, ma nelle pagine della Lezione 03 essa non viene ancora sviluppata.

## Prospettiva d'esame

Potenziale rilevanza d'esame: passare correttamente dalla forma algebrica a quella trigonometrica e viceversa, controllando quadrante e condizioni.
