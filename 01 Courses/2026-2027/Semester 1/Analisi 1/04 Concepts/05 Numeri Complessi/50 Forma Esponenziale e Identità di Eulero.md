---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 04, PDF pp. 2-3
  - Libro, §1.8.1, pp. 20-21
---

# Forma esponenziale e identità di Eulero

## Perché serve

La [[48 Forma Trigonometrica dei Numeri Complessi|forma trigonometrica]] descrive un numero complesso mediante modulo e argomento. La forma esponenziale raccoglie la stessa informazione in una scrittura più compatta, particolarmente utile per prodotti, quozienti, potenze e radici complesse.

## Intuizione

Il fattore reale positivo rappresenta la distanza dall'origine, mentre l'esponente immaginario rappresenta la direzione nel piano complesso. Nella scrittura

$$
z=\rho e^{i\theta},
$$

$\rho$ determina il modulo di $z$ e $\theta$ ne determina un argomento.

## Identità di Eulero

Per ogni $\theta\in\mathbb{R}$ si pone

$$
e^{i\theta}=\cos\theta+i\sin\theta.
$$

Questa relazione è chiamata identità, o formula, di Eulero.

### Da dire all'orale

> L'identità di Eulero esprime l'esponenziale con esponente puramente immaginario mediante seno e coseno: per ogni angolo reale $\theta$, vale $e^{i\theta}=\cos\theta+i\sin\theta$.

## Definizione formale

Sia $z\in\mathbb{C}\setminus\{0\}$, con

$$
z=x+iy,
\qquad
\rho=|z|>0,
\qquad
\theta=\arg z.
$$

Dalla forma trigonometrica,

$$
z=\rho(\cos\theta+i\sin\theta).
$$

Usando l'identità di Eulero si ottiene

$$
z=\rho e^{i\theta}.
$$

Questa è una rappresentazione di $z$ in forma esponenziale.

### Da dire all'orale

> Se $z\neq0$ ha modulo $\rho$ e argomento $\theta$, la sua forma esponenziale è $z=\rho e^{i\theta}$, dove $\rho=|z|>0$ ed $e^{i\theta}=\cos\theta+i\sin\theta$.

## Significato dei simboli

- $\rho=|z|$ è un numero reale strettamente positivo.
- $\theta$ è un argomento di $z$.
- $e^{i\theta}$ ha modulo $1$ e individua la direzione di $z$.
- Il prodotto $\rho e^{i\theta}$ dilata di un fattore $\rho$ il punto della circonferenza unitaria individuato da $e^{i\theta}$.

Infatti,

$$
|e^{i\theta}|
=\sqrt{\cos^2\theta+\sin^2\theta}
=1.
$$

## Non unicità dell'angolo

Poiché seno e coseno hanno periodo $2\pi$, per ogni $k\in\mathbb{Z}$ vale

$$
e^{i(\theta+2k\pi)}
=\cos(\theta+2k\pi)+i\sin(\theta+2k\pi)
=e^{i\theta}.
$$

Di conseguenza, se

$$
z=\rho e^{i\theta},
$$

allora anche

$$
z=\rho e^{i(\theta+2k\pi)}
\qquad
\text{per ogni }k\in\mathbb{Z}.
$$

La forma esponenziale è quindi unica nel modulo, ma non nell'argomento, a meno di fissare un intervallo per l'argomento principale.

## Metodo di conversione

### Dalla forma algebrica alla forma esponenziale

Per $z=x+iy\neq0$:

1. calcolare il modulo

$$
\rho=\sqrt{x^2+y^2};
$$

2. determinare un argomento $\theta$ controllando il quadrante, come in [[49 Determinazione dell'Argomento per Quadranti|determinazione dell'argomento per quadranti]];
3. scrivere

$$
z=\rho e^{i\theta}.
$$

### Dalla forma esponenziale alla forma algebrica

Se

$$
z=\rho e^{i\theta},
$$

allora

$$
z=\rho(\cos\theta+i\sin\theta)
=\rho\cos\theta+i\rho\sin\theta.
$$

Pertanto

$$
\operatorname{Re}z=\rho\cos\theta,
\qquad
\operatorname{Im}z=\rho\sin\theta.
$$

## Esempio della lezione: il numero meno uno

Per $z=-1$ si ha

$$
|z|=1
$$

e un argomento è $\pi$. Quindi

$$
-1=\cos\pi+i\sin\pi=e^{i\pi}.
$$

Da questa uguaglianza segue la celebre relazione

$$
e^{i\pi}+1=0.
$$

La scrittura

$$
-1=-1(\cos0+i\sin0)
$$

è algebricamente corretta, ma non è una forma trigonometrica o esponenziale valida secondo la convenzione adottata: il coefficiente davanti alla parentesi dovrebbe essere il modulo, quindi deve essere non negativo e, per un numero non nullo, strettamente positivo.

## Condizioni

- La rappresentazione $z=\rho e^{i\theta}$ con $\rho=|z|>0$ riguarda $z\neq0$.
- Il numero $0$ ha modulo nullo, ma non possiede un argomento; non gli si assegna quindi una forma esponenziale con un angolo determinato.
- L'angolo $\theta$ è reale ed è definito a meno di multipli interi di $2\pi$.
- Il coefficiente $\rho$ non può essere scelto negativo se deve rappresentare il modulo.

## Approfondimento dal libro

Al variare di $\theta\in\mathbb{R}$, il punto $e^{i\theta}$ percorre la circonferenza di centro l'origine e raggio $1$. La forma esponenziale separa quindi il numero complesso in una parte radiale, $\rho$, e una parte angolare, $e^{i\theta}$.

## Errori comuni

- Usare un coefficiente negativo al posto del modulo.
- Dimenticare che l'argomento non è unico.
- Assegnare un argomento a $0$.
- Scrivere $e^{i\theta}=\cos\theta+\sin\theta$ omettendo l'unità immaginaria.
- Confondere $e^{i\theta}$, che è in generale complesso, con un esponenziale reale positivo.
- Scambiare il ruolo del modulo e quello dell'argomento.

## Connessioni

- È una riscrittura della [[48 Forma Trigonometrica dei Numeri Complessi|forma trigonometrica]].
- Richiede [[47 Modulo e Argomento dei Numeri Complessi|modulo e argomento]].
- Prepara il calcolo di prodotti, quozienti, potenze e radici dei numeri complessi.

## Prospettiva d'esame

Potenziale rilevanza d'esame: convertire un numero complesso tra forma algebrica, trigonometrica ed esponenziale; dichiarare le condizioni sul modulo; gestire correttamente la non unicità dell'argomento.
