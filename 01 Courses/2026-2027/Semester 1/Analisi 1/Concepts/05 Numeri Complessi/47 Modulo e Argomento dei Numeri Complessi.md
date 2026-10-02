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

Un numero complesso non nullo può essere individuato geometricamente con due informazioni: la distanza dall'origine e la direzione della semiretta che lo congiunge all'origine.

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
