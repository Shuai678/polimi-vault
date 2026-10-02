---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 04, PDF pp. 5-7
  - Libro, §1.8.1, p. 21
---

# Formula di De Moivre e potenze complesse

## Perché serve

Calcolare una potenza elevata sviluppando ripetutamente la forma algebrica produce molti termini ed espone a errori di segno. La formula di De Moivre permette invece di calcolare la potenza agendo separatamente sul modulo e sull'argomento.

## Teorema: formula di De Moivre

### In parole semplici

Per elevare un numero complesso non nullo a una potenza intera positiva:

- si eleva il modulo alla stessa potenza;
- si moltiplica l'argomento per l'esponente.

### Condizioni

Sia

$$
z=r(\cos\theta+i\sin\theta)=re^{i\theta}
$$

un numero complesso non nullo, con

$$
r=|z|>0,
$$

e sia $n\in\mathbb{N}$ con $n\geq1$.

### Conclusione

Allora

$$
z^n
=r^n\bigl(\cos(n\theta)+i\sin(n\theta)\bigr)
=r^n e^{in\theta}.
$$

In particolare,

$$
|z^n|=|z|^n
$$

e

$$
\arg(z^n)=n\arg z
\pmod{2\pi}.
$$

### Da dire all'orale

> Se $z=r(\cos\theta+i\sin\theta)$ è un numero complesso non nullo e $n$ è un intero positivo, allora $z^n=r^n(\cos(n\theta)+i\sin(n\theta))$. Quindi il modulo viene elevato alla potenza $n$ e l'argomento viene moltiplicato per $n$.

## Perché è utile

La formula consente di:

- calcolare potenze elevate senza sviluppi algebrici ripetuti;
- riconoscere rapidamente modulo e argomento del risultato;
- ridurre l'angolo modulo $2\pi$ prima di calcolare seno e coseno;
- preparare la determinazione delle radici complesse.

## Intuizione

La potenza $z^n$ è il prodotto di $n$ fattori tutti uguali a $z$. Per la regola del [[51 Prodotto e Quoziente in Forma Trigonometrica|prodotto in forma trigonometrica]]:

- i $n$ moduli uguali a $r$ si moltiplicano e producono $r^n$;
- i $n$ argomenti uguali a $\theta$ si sommano e producono $n\theta$.

Geometricamente, ogni moltiplicazione per $z$ applica la stessa dilatazione di fattore $r$ e la stessa rotazione di angolo $\theta$.

## Strategia della dimostrazione

Si usa l'induzione sull'esponente $n$:

1. si verifica la formula per $n=1$;
2. si assume che valga per un esponente arbitrario $n$;
3. si moltiplica $z^n$ per $z$ e si applica la formula del prodotto;
4. si ottiene la formula per $n+1$.

## Dimostrazione passo per passo

### Caso base

Per $n=1$,

$$
z^1
=r\bigl(\cos\theta+i\sin\theta\bigr),
$$

che coincide con la forma trigonometrica di $z$. Il caso base è quindi verificato.

### Ipotesi induttiva

Supponiamo che, per un certo $n\geq1$, valga

$$
z^n
=r^n\bigl(\cos(n\theta)+i\sin(n\theta)\bigr).
$$

Questa è l'ipotesi induttiva.

### Passo da n a n più uno

Per definizione di potenza,

$$
z^{n+1}=z^n z.
$$

Sostituendo l'ipotesi induttiva e la forma trigonometrica di $z$,

$$
\begin{aligned}
z^{n+1}
&=r^n\bigl(\cos(n\theta)+i\sin(n\theta)\bigr)
  r(\cos\theta+i\sin\theta).
\end{aligned}
$$

La formula del prodotto moltiplica i moduli e somma gli argomenti:

$$
\begin{aligned}
z^{n+1}
&=r^{n+1}
\bigl(\cos(n\theta+\theta)+i\sin(n\theta+\theta)\bigr)\\
&=r^{n+1}
\bigl(\cos((n+1)\theta)+i\sin((n+1)\theta)\bigr).
\end{aligned}
$$

Abbiamo così dimostrato la formula per $n+1$. Per il principio di induzione, la tesi vale per ogni $n\in\mathbb{N}$ con $n\geq1$.

## Scrittura esponenziale

Usando la [[50 Forma Esponenziale e Identità di Eulero|forma esponenziale]], la stessa formula assume la forma compatta

$$
(re^{i\theta})^n=r^n e^{in\theta}.
$$

La scrittura è coerente con le proprietà usuali delle potenze: il modulo viene elevato a $n$ e l'esponente $i\theta$ viene moltiplicato per $n$.

## Potenze con esponente zero

Se $z\neq0$, allora

$$
z^0=1.
$$

La formula resta coerente perché

$$
r^0e^{i0\theta}=1\cdot e^0=1.
$$

Il caso $0^0$ non viene definito mediante questa regola.

## Potenze con esponente intero negativo

Sia $m\in\mathbb{N}$ con $m\geq1$. Se $z\neq0$, si definisce

$$
z^{-m}=\frac1{z^m}.
$$

Poiché

$$
z^m=r^m e^{im\theta},
$$

si ottiene

$$
\begin{aligned}
z^{-m}
&=\frac1{r^m e^{im\theta}}\\
&=r^{-m}e^{-im\theta}\\
&=\frac1{r^m}
\bigl(\cos(m\theta)-i\sin(m\theta)\bigr).
\end{aligned}
$$

L'ultima uguaglianza usa

$$
\cos(-m\theta)=\cos(m\theta),
\qquad
\sin(-m\theta)=-\sin(m\theta).
$$

### Condizione essenziale

Le potenze negative richiedono $z\neq0$, perché contengono l'inverso di $z$.

## Metodo di calcolo

Per calcolare $z^n$:

1. scrivere $z$ in forma trigonometrica o esponenziale;
2. calcolare $r^n$;
3. moltiplicare un argomento di $z$ per $n$;
4. ridurre l'angolo modulo $2\pi$;
5. se richiesto, tornare alla forma algebrica calcolando seno e coseno.

## Esempio della lezione

Calcoliamo

$$
z^7
\qquad\text{per}\qquad
z=-1-i\sqrt3.
$$

### 1. Calcolare il modulo

$$
|z|
=\sqrt{(-1)^2+(-\sqrt3)^2}
=\sqrt{1+3}
=2.
$$

### 2. Determinare un argomento

Il punto $(-1,-\sqrt3)$ si trova nel terzo quadrante. Si ha

$$
\cos\theta=-\frac12,
\qquad
\sin\theta=-\frac{\sqrt3}{2}.
$$

Nell'intervallo $[0,2\pi)$ si può scegliere

$$
\theta=\frac{4\pi}{3}.
$$

Quindi

$$
z=2e^{i4\pi/3}.
$$

### 3. Applicare De Moivre

$$
z^7
=2^7e^{i28\pi/3}.
$$

### 4. Ridurre l'angolo modulo due pi greco

Poiché

$$
\frac{28\pi}{3}
=\frac{24\pi}{3}+\frac{4\pi}{3}
=8\pi+\frac{4\pi}{3},
$$

e $8\pi$ è un multiplo di $2\pi$, si ha

$$
e^{i28\pi/3}=e^{i4\pi/3}.
$$

Pertanto

$$
z^7
=2^7\left(\cos\frac{4\pi}{3}
+i\sin\frac{4\pi}{3}\right).
$$

### 5. Tornare alla forma algebrica

Usando

$$
\cos\frac{4\pi}{3}=-\frac12,
\qquad
\sin\frac{4\pi}{3}=-\frac{\sqrt3}{2},
$$

si ottiene

$$
\begin{aligned}
z^7
&=128\left(-\frac12-i\frac{\sqrt3}{2}\right)\\
&=-64-64\sqrt3\,i.
\end{aligned}
$$

### Controllo del risultato

Il modulo del risultato deve essere

$$
|z^7|=|z|^7=2^7=128.
$$

Infatti,

$$
\sqrt{(-64)^2+(-64\sqrt3)^2}
=\sqrt{4096+12288}
=\sqrt{16384}
=128.
$$

## Errori comuni

- Elevare il modulo a $n$ ma lasciare invariato l'argomento.
- Elevare separatamente seno e coseno, scrivendo una formula errata come $\cos^n\theta+i\sin^n\theta$.
- Moltiplicare il modulo per $n$ invece di elevarlo a $n$.
- Dimenticare di ridurre $n\theta$ modulo $2\pi$ prima di valutare seno e coseno.
- Sbagliare il quadrante quando si determina l'argomento iniziale.
- Usare una potenza negativa quando $z=0$.
- Trattare $0^0$ come conseguenza automatica della formula.

## Connessioni

- Usa [[48 Forma Trigonometrica dei Numeri Complessi|forma trigonometrica]] e [[50 Forma Esponenziale e Identità di Eulero|forma esponenziale]].
- Deriva dalla regola del [[51 Prodotto e Quoziente in Forma Trigonometrica|prodotto in forma trigonometrica]].
- La scelta dell'angolo richiede [[49 Determinazione dell'Argomento per Quadranti|determinazione dell'argomento per quadranti]].
- La formula sarà il punto di partenza per calcolare le radici complesse.

## Uso all'esame

Potenziale rilevanza d'esame: convertire il numero in forma trigonometrica, applicare De Moivre, ridurre correttamente l'angolo e controllare il modulo del risultato.

## Errore comune all'orale

Non basta dire che “si moltiplica l'angolo”: bisogna specificare che il modulo viene elevato alla potenza $n$, che l'argomento viene moltiplicato per $n$ e che gli argomenti sono considerati modulo $2\pi$.
