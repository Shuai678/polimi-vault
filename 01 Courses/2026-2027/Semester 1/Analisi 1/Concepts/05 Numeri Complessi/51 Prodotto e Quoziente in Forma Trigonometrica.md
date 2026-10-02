---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 04, PDF pp. 3-7
  - Libro, §1.8.1, pp. 20-21
---

# Prodotto e quoziente in forma trigonometrica

## Perché servono

In forma algebrica il prodotto richiede di sviluppare le parentesi e usare $i^2=-1$. In forma trigonometrica o esponenziale, invece, la moltiplicazione separa nettamente due effetti:

- i moduli si moltiplicano;
- gli argomenti si sommano.

Per il quoziente avviene l'operazione inversa:

- i moduli si dividono;
- gli argomenti si sottraggono.

Queste regole rendono più semplici anche il calcolo delle potenze e delle radici complesse.

## Prodotto in forma trigonometrica

Siano $z,w\in\mathbb{C}\setminus\{0\}$ scritti come

$$
z=r(\cos\theta+i\sin\theta)=re^{i\theta},
$$

$$
w=R(\cos\varphi+i\sin\varphi)=Re^{i\varphi},
$$

con

$$
r=|z|>0,
\qquad
R=|w|>0.
$$

Allora

$$
zw=rR\bigl(\cos(\theta+\varphi)+i\sin(\theta+\varphi)\bigr)
=rRe^{i(\theta+\varphi)}.
$$

### Da dire all'orale

> Moltiplicando due numeri complessi non nulli in forma trigonometrica, i moduli si moltiplicano e gli argomenti si sommano. Se $\theta$ è un argomento di $z$ e $\varphi$ è un argomento di $w$, allora $\theta+\varphi$ è un argomento di $zw$.

## Dimostrazione passo per passo

Partiamo dalle forme trigonometriche:

$$
zw
=r(\cos\theta+i\sin\theta)
 R(\cos\varphi+i\sin\varphi).
$$

### 1. Raccogliere i moduli reali

Poiché $r$ e $R$ sono reali, si può scrivere

$$
zw
=rR(\cos\theta+i\sin\theta)
(\cos\varphi+i\sin\varphi).
$$

### 2. Sviluppare il prodotto

Applicando la proprietà distributiva,

$$
\begin{aligned}
zw
=rR\bigl(&\cos\theta\cos\varphi
+i\cos\theta\sin\varphi\\
&+i\sin\theta\cos\varphi
+i^2\sin\theta\sin\varphi\bigr).
\end{aligned}
$$

### 3. Usare l'unità immaginaria

Dato che $i^2=-1$,

$$
\begin{aligned}
zw
=rR\bigl[&\cos\theta\cos\varphi
-\sin\theta\sin\varphi\\
&+i(\sin\theta\cos\varphi
+\cos\theta\sin\varphi)\bigr].
\end{aligned}
$$

### 4. Riconoscere le formule di addizione

Si usano le identità

$$
\cos(\theta+\varphi)
=\cos\theta\cos\varphi-\sin\theta\sin\varphi,
$$

$$
\sin(\theta+\varphi)
=\sin\theta\cos\varphi+\cos\theta\sin\varphi.
$$

Pertanto

$$
zw=rR\bigl(\cos(\theta+\varphi)+i\sin(\theta+\varphi)\bigr).
$$

La stessa conclusione si legge immediatamente usando la [[50 Forma Esponenziale e Identità di Eulero|forma esponenziale]]:

$$
zw=(re^{i\theta})(Re^{i\varphi})
=rRe^{i(\theta+\varphi)}.
$$

## Conseguenze su modulo e argomento

Per ogni $z,w\in\mathbb{C}$ vale

$$
|zw|=|z|\,|w|.
$$

Se $z$ e $w$ sono entrambi non nulli, allora

$$
\arg(zw)=\arg z+\arg w
\pmod{2\pi}.
$$

La scrittura modulo $2\pi$ ricorda che gli argomenti non sono unici. Se si lavora con argomenti principali, dopo la somma può essere necessario riportare il risultato nell'intervallo scelto.

## Interpretazione geometrica

![[Assets/51 Prodotto Complesso - Rotazione e Dilatazione.svg|780]]

Moltiplicare $z$ per

$$
w=Re^{i\varphi}
$$

significa:

1. moltiplicare la distanza dall'origine per $R=|w|$;
2. ruotare il vettore associato a $z$ di un angolo $\varphi$.

Se $R>1$ si ha un allungamento; se $0<R<1$ si ha una contrazione; se $R=1$ resta soltanto la rotazione.

## Quoziente in forma trigonometrica

Siano ancora

$$
z=re^{i\theta},
\qquad
w=Re^{i\varphi},
$$

con $w\neq0$, quindi $R>0$. Se anche $z\neq0$, allora

$$
\frac zw
=\frac rR
\bigl(\cos(\theta-\varphi)+i\sin(\theta-\varphi)\bigr)
=\frac rR e^{i(\theta-\varphi)}.
$$

### Perché si sottraggono gli argomenti

L'inverso di $w$ è

$$
w^{-1}
=\frac1R\bigl(\cos(-\varphi)+i\sin(-\varphi)\bigr)
=\frac1R e^{-i\varphi}.
$$

Quindi

$$
\begin{aligned}
\frac zw
&=zw^{-1}\\
&=re^{i\theta}\frac1R e^{-i\varphi}\\
&=\frac rR e^{i(\theta-\varphi)}.
\end{aligned}
$$

### Da dire all'orale

> Nel quoziente tra due numeri complessi, con denominatore non nullo, il modulo del risultato è il rapporto dei moduli e l'argomento è la differenza tra l'argomento del numeratore e quello del denominatore.

## Conseguenze per il quoziente

Per $z\in\mathbb{C}$ e $w\in\mathbb{C}\setminus\{0\}$,

$$
\left|\frac zw\right|=\frac{|z|}{|w|}.
$$

Se anche $z\neq0$, allora

$$
\arg\left(\frac zw\right)
=\arg z-\arg w
\pmod{2\pi}.
$$

Se $z=0$, il quoziente vale $0$, ma non gli si può assegnare un argomento.

## Esempio

Siano

$$
z=2e^{i\pi/6},
\qquad
w=3e^{i\pi/4}.
$$

Per il prodotto,

$$
\begin{aligned}
zw
&=2\cdot3\,e^{i(\pi/6+\pi/4)}\\
&=6e^{i(2\pi/12+3\pi/12)}\\
&=6e^{i5\pi/12}.
\end{aligned}
$$

Per il quoziente,

$$
\begin{aligned}
\frac zw
&=\frac23e^{i(\pi/6-\pi/4)}\\
&=\frac23e^{i(2\pi/12-3\pi/12)}\\
&=\frac23e^{-i\pi/12}.
\end{aligned}
$$

## Condizioni

- Per assegnare un argomento a $z$, $w$, $zw$ o $z/w$, il numero considerato deve essere non nullo.
- Il quoziente richiede sempre $w\neq0$.
- Le uguaglianze tra argomenti sono da intendere a meno di multipli interi di $2\pi$.
- La formula $|zw|=|z||w|$ resta valida anche se uno dei fattori è nullo.

## Errori comuni

- Sommare i moduli invece di moltiplicarli.
- Moltiplicare gli argomenti invece di sommarli.
- Nel quoziente, invertire l'ordine della sottrazione degli argomenti.
- Dimenticare la condizione $w\neq0$.
- Trattare l'argomento principale come se la somma o la differenza restasse automaticamente nell'intervallo scelto.
- Scrivere un argomento per un prodotto o un quoziente che vale $0$.
- Confondere la formula trigonometrica del quoziente con la [[45 Divisione tra Numeri Complessi|razionalizzazione mediante il coniugato]] in forma algebrica.

## Connessioni

- Richiede [[47 Modulo e Argomento dei Numeri Complessi|modulo e argomento]].
- Usa la [[48 Forma Trigonometrica dei Numeri Complessi|forma trigonometrica]] e la [[50 Forma Esponenziale e Identità di Eulero|forma esponenziale]].
- Fornisce una lettura geometrica del prodotto già definito in [[38 Operazioni con i Numeri Complessi|forma algebrica]].
- Il quoziente è equivalente al metodo con il coniugato descritto in [[45 Divisione tra Numeri Complessi|divisione tra numeri complessi]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: calcolare prodotti e quozienti in forma trigonometrica o esponenziale, giustificare le formule, interpretare geometricamente l'operazione e gestire correttamente condizioni e argomenti principali.
