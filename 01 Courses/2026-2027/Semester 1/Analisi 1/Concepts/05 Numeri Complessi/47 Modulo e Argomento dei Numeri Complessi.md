---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 03, PDF pp. 14-15
  - Libro, §1.8.1, p. 20
---

# Modulo e argomento dei numeri complessi

## Intuizione

Un numero complesso non nullo può essere individuato geometricamente con due informazioni: la **distanza dall'origine** e la **direzione della semiretta che lo congiunge all'origine**.

## Definizione formale

Sia $z=x+iy\neq0$.

- Il modulo è

$$
\rho=|z|=\sqrt{x^2+y^2}>0.
$$

- Un argomento di $z$ è un angolo orientato $\theta$ che il semiasse reale positivo deve compiere per sovrapporsi alla semiretta dall'origine passante per $z$.

Si indica con

$$
\theta=\arg z.
$$

### Da dire all'orale

> Per $z\neq0$, il modulo è la distanza di $z$ dall'origine, mentre un argomento è l'angolo orientato tra il semiasse reale positivo e la semiretta uscente dall'origine e passante per $z$.

## Non unicità dell'argomento

L'argomento non è unico: se $\theta$ è un argomento di $z$, allora lo è anche

$$
\theta+2k\pi,
\qquad k\in\mathbb Z.
$$

Per ottenere un valore unico si sceglie un intervallo di ampiezza $2\pi$ e si parla di argomento principale.

## Calcolo dell'argomento dalle coordinate

Sia $z=x+iy\neq0$ e sia

$$
\rho=|z|=\sqrt{x^2+y^2}.
$$

Dalla rappresentazione geometrica si ottiene

$$
\cos\theta=\frac{x}{\rho},
\qquad
\sin\theta=\frac{y}{\rho}.
$$

ATTENZIONE: Non si può però ricavare sempre $\theta$ usando una sola tra le formule

$$
\theta=\arccos\left(\frac{x}{\sqrt{x^2+y^2}}\right),
\qquad
\theta=\arcsin\left(\frac{y}{\sqrt{x^2+y^2}}\right),
\qquad
\theta=\arctan\left(\frac{y}{x}\right),
$$

perché le funzioni inverse restituiscono valori soltanto in intervalli limitati e possono quindi indicare il quadrante sbagliato. In particolare, $\arctan(y/x)$ non distingue punti appartenenti a quadranti opposti e non è definita quando $x=0$.

Scegliendo l'argomento principale nell'intervallo $[-\pi,\pi)$, si può usare

$$
\operatorname{Arg}z=
\begin{cases}
\arctan\left(\dfrac{y}{x}\right), & x>0,\\[6pt]
\arctan\left(\dfrac{y}{x}\right)+\pi, & x<0,\ y>0,\\[6pt]
\arctan\left(\dfrac{y}{x}\right)-\pi, & x<0,\ y\leq0,\\[6pt]
\dfrac{\pi}{2}, & x=0,\ y>0,\\[6pt]
-\dfrac{\pi}{2}, & x=0,\ y<0.
\end{cases}
$$

La scelta tra aggiungere o sottrarre $\pi$ dipende dal quadrante. Per esempio, se $z=-1-i$, allora

$$
\arctan\left(\frac{y}{x}\right)=\arctan(1)=\frac{\pi}{4},
$$

ma $z$ si trova nel terzo quadrante. Nell'intervallo $[-\pi,\pi)$ bisogna quindi correggere il risultato:

$$
\operatorname{Arg}(-1-i)=\frac{\pi}{4}-\pi=-\frac{3\pi}{4}.
$$

Una volta trovato l'argomento principale, tutti gli argomenti di $z$ sono

$$
\arg z=\operatorname{Arg}z+2k\pi,
\qquad k\in\mathbb Z.
$$

## Condizioni

- L'argomento di $0$ non è definito, perché non esiste una direzione dall'origine verso l'origine stessa.
- Per $z\neq0$, il modulo è strettamente positivo.
- Il verso antiorario corrisponde agli angoli positivi; quello orario agli angoli negativi.

## Rappresentazione geometrica

![[Assets/47 Modulo e Argomento dei Numeri Complessi.svg|650]]

## Luoghi geometrici collegati

- $|z|=\rho$, con $\rho>0$, descrive una circonferenza con centro nell'origine.
- $\arg z=\theta$ descrive una semiretta uscente dall'origine, con l'origine esclusa.

## Approfondimento dal libro

Il libro chiama il piano complesso anche **piano di Argand-Gauss** e propone come intervalli tipici per l'argomento principale $[0,2\pi)$ oppure $[-\pi,\pi)$.

## Errori comuni

- Definire l'argomento di $z=0$.
- Considerare l'argomento unico senza fissare un intervallo principale.
- Confondere il modulo, che è una lunghezza, con l'argomento, che è un angolo.
- Dimenticare che la semiretta $\arg z=\theta$ non contiene l'origine.

## Connessioni

- Estende la rappresentazione del [[40 Piano Complesso e Interpretazione Vettoriale|piano complesso]].
- Il modulo era già stato studiato in [[41 Coniugato e Modulo dei Numeri Complessi|coniugato e modulo]].
- Modulo e argomento permettono di ottenere la [[48 Forma Trigonometrica dei Numeri Complessi|forma trigonometrica]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: distinguere modulo e argomento, dichiarare la non unicità dell'argomento e interpretare geometricamente condizioni su di essi.
