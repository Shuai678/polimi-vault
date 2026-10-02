---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 04, PDF pp. 8-14
  - Libro, §1.8.1, pp. 21-22
---

# Radici ennesime complesse

## Perché servono

Nei numeri reali alcune equazioni della forma $x^n=w$ non hanno soluzioni oppure hanno un numero di soluzioni che dipende dal segno di $w$ e dalla parità di $n$. Nel campo complesso, invece, ogni numero non nullo possiede esattamente $n$ radici ennesime distinte.

La forma trigonometrica permette di trovarle tutte senza perdere soluzioni.

## Definizione formale

Siano $w\in\mathbb{C}$ e $n\in\mathbb{N}$ con $n\geq1$. Un numero $z\in\mathbb{C}$ si chiama radice ennesima complessa di $w$ se

$$
z^n=w.
$$

### Da dire all'orale

> Una radice ennesima complessa di $w$ è un numero complesso $z$ che, elevato alla potenza $n$, restituisce $w$.

## Il caso w uguale a zero

Se

$$
z^n=0,
$$

allora necessariamente

$$
z=0.
$$

Quindi $0$ possiede una sola radice ennesima distinta, cioè $0$. Il teorema delle $n$ radici distinte riguarda invece $w\neq0$.

## Teorema delle radici ennesime complesse

### In parole semplici

Ogni numero complesso non nullo ha esattamente $n$ radici ennesime distinte. Esse hanno tutte lo stesso modulo e argomenti equidistanti.

### Condizioni

Siano

$$
w=Re^{i\varphi}
=R(\cos\varphi+i\sin\varphi)
\in\mathbb{C}\setminus\{0\},
$$

con $R=|w|>0$, e $n\in\mathbb{N}$ con $n\geq1$.

### Conclusione

Le radici ennesime complesse di $w$ sono esattamente

$$
z_k
=R^{1/n}e^{i\theta_k}
=R^{1/n}\bigl(\cos\theta_k+i\sin\theta_k\bigr),
$$

dove

$$
\theta_k=\frac{\varphi+2k\pi}{n},
\qquad
k=0,1,\ldots,n-1.
$$

### Da dire all'orale

> Se $w=Re^{i\varphi}\neq0$, le sue radici ennesime sono i numeri $z_k=R^{1/n}e^{i(\varphi+2k\pi)/n}$, con $k$ da $0$ a $n-1$. Sono esattamente $n$, hanno modulo $R^{1/n}$ e argomenti consecutivi separati da $2\pi/n$.

## Perché è utile

Il teorema permette di:

- risolvere completamente equazioni della forma $z^n=w$;
- elencare tutte le soluzioni senza duplicazioni;
- interpretare geometricamente le soluzioni;
- passare dalla potenza alla radice usando la [[52 Formula di De Moivre e Potenze Complesse|formula di De Moivre]].

## Intuizione

Per ottenere $w$ dopo aver elevato $z$ alla potenza $n$:

- il modulo di $z$, elevato a $n$, deve diventare il modulo $R$ di $w$;
- l'argomento di $z$, moltiplicato per $n$, deve coincidere con un argomento di $w$.

Poiché tutti gli argomenti di $w$ sono

$$
\varphi+2h\pi,
\qquad h\in\mathbb{Z},
$$

si devono dividere per $n$ non soltanto $\varphi$, ma tutti gli angoli $\varphi+2h\pi$.

## Strategia della dimostrazione

1. Scrivere l'incognita come $z=\rho e^{i\theta}$.
2. Applicare De Moivre a $z^n$.
3. Uguagliare separatamente moduli e argomenti.
4. Ottenere tutte le soluzioni indicizzate da un intero $h$.
5. Usare la divisione con resto di $h$ per $n$ per ridurre l'elenco a $k=0,\ldots,n-1$.
6. Verificare che queste $n$ soluzioni siano distinte.

## Dimostrazione passo per passo

Cerchiamo un numero

$$
z=\rho e^{i\theta},
\qquad \rho>0,
$$

tale che

$$
z^n=w.
$$

### 1. Applicare De Moivre

Si ha

$$
z^n=\rho^n e^{in\theta}.
$$

L'equazione diventa quindi

$$
\rho^n e^{in\theta}=Re^{i\varphi}.
$$

### 2. Uguagliare i moduli

I moduli devono soddisfare

$$
\rho^n=R.
$$

Poiché $R>0$ e $\rho$ è un modulo, cioè $\rho>0$, esiste un'unica soluzione reale positiva:

$$
\rho=R^{1/n}.
$$

### 3. Uguagliare gli argomenti

Due numeri complessi non nulli con lo stesso modulo coincidono quando i loro argomenti differiscono per un multiplo intero di $2\pi$. Pertanto

$$
n\theta=\varphi+2h\pi,
\qquad h\in\mathbb{Z}.
$$

Dividendo per $n$,

$$
\theta=\frac{\varphi+2h\pi}{n},
\qquad h\in\mathbb{Z}.
$$

Si ottengono quindi i candidati

$$
z_h
=R^{1/n}e^{i(\varphi+2h\pi)/n},
\qquad h\in\mathbb{Z}.
$$

### 4. Verificare che ogni candidato sia una radice

Elevando $z_h$ alla potenza $n$,

$$
\begin{aligned}
z_h^n
&=\left(R^{1/n}e^{i(\varphi+2h\pi)/n}\right)^n\\
&=Re^{i(\varphi+2h\pi)}\\
&=Re^{i\varphi}e^{i2h\pi}\\
&=Re^{i\varphi}\\
&=w,
\end{aligned}
$$

perché $e^{i2h\pi}=1$ per ogni $h\in\mathbb{Z}$.

### 5. Eliminare le ripetizioni

Ogni intero $h$ può essere scritto mediante la divisione con resto come

$$
h=qn+k,
$$

con

$$
q\in\mathbb{Z},
\qquad
k\in\{0,1,\ldots,n-1\}.
$$

Allora

$$
\begin{aligned}
\frac{\varphi+2h\pi}{n}
&=\frac{\varphi+2(qn+k)\pi}{n}\\
&=\frac{\varphi+2k\pi}{n}+2q\pi.
\end{aligned}
$$

L'aggiunta di $2q\pi$ non cambia il numero complesso. Quindi ogni valore intero di $h$ produce una delle soluzioni corrispondenti ai soli resti

$$
k=0,1,\ldots,n-1.
$$

### 6. Dimostrare che le n radici sono distinte

Supponiamo che due indici $k_1,k_2\in\{0,1,\ldots,n-1\}$ producano la stessa radice. I loro argomenti dovrebbero differire per un multiplo intero di $2\pi$:

$$
\frac{\varphi+2k_2\pi}{n}
-\frac{\varphi+2k_1\pi}{n}
=2m\pi
$$

per qualche $m\in\mathbb{Z}$. Semplificando,

$$
\frac{2(k_2-k_1)\pi}{n}=2m\pi.
$$

Quindi

$$
k_2-k_1=mn.
$$

Ma $k_1$ e $k_2$ appartengono entrambi a $\{0,\ldots,n-1\}$, perciò

$$
-(n-1)\leq k_2-k_1\leq n-1.
$$

L'unico multiplo di $n$ in questo intervallo è $0$. Ne segue

$$
k_2-k_1=0,
$$

e quindi $k_1=k_2$. Le $n$ radici elencate sono dunque tutte distinte.

## Interpretazione geometrica

Tutte le radici hanno modulo

$$
|z_k|=R^{1/n}.
$$

Si trovano quindi sulla stessa circonferenza, con centro nell'origine e raggio $R^{1/n}$.

Inoltre, due argomenti consecutivi differiscono di

$$
\theta_{k+1}-\theta_k
=\frac{2\pi}{n}.
$$

Le radici sono perciò equidistanti angolarmente e formano i vertici di un poligono regolare di $n$ lati.

![[Assets/53 Radici Ennesime Complesse - Poligono Regolare.svg|800]]

## Metodo operativo

Per risolvere $z^n=w$ con $w\neq0$:

1. scrivere $w$ nella forma $w=Re^{i\varphi}$;
2. calcolare il modulo comune $R^{1/n}$;
3. calcolare gli angoli

$$
\theta_k=\frac{\varphi+2k\pi}{n},
\qquad k=0,\ldots,n-1;
$$

4. scrivere ogni radice in forma esponenziale o trigonometrica;
5. se richiesto, convertire le radici in forma algebrica;
6. controllare che siano $n$ valori distinti e che siano equidistanti sulla circonferenza.

## Esempio della lezione: radici seste di meno uno

Vogliamo risolvere

$$
z^6=-1.
$$

### Dati

Si ha

$$
|-1|=1
$$

e si può scegliere

$$
\arg(-1)=\pi.
$$

Quindi

$$
-1=e^{i\pi}.
$$

### Applicazione della formula

Il modulo delle radici è

$$
1^{1/6}=1.
$$

Gli argomenti sono

$$
\theta_k
=\frac{\pi+2k\pi}{6}
=\frac{\pi}{6}+\frac{k\pi}{3},
\qquad k=0,1,2,3,4,5.
$$

Le sei radici sono quindi

$$
z_k=e^{i(\pi/6+k\pi/3)}.
$$

### Conversione in forma algebrica

Per $k=0$,

$$
z_0=e^{i\pi/6}
=\frac{\sqrt3}{2}+\frac12i.
$$

Per $k=1$,

$$
z_1=e^{i\pi/2}=i.
$$

Per $k=2$,

$$
z_2=e^{i5\pi/6}
=-\frac{\sqrt3}{2}+\frac12i.
$$

Per $k=3$,

$$
z_3=e^{i7\pi/6}
=-\frac{\sqrt3}{2}-\frac12i.
$$

Per $k=4$,

$$
z_4=e^{i3\pi/2}=-i.
$$

Per $k=5$,

$$
z_5=e^{i11\pi/6}
=\frac{\sqrt3}{2}-\frac12i.
$$

### Controllo del risultato

Per ogni $k=0,\ldots,5$,

$$
\begin{aligned}
z_k^6
&=e^{i6(\pi/6+k\pi/3)}\\
&=e^{i(\pi+2k\pi)}\\
&=e^{i\pi}\\
&=-1.
\end{aligned}
$$

Le sei radici hanno tutte modulo $1$ e argomenti separati da $\pi/3$; sono quindi i vertici di un esagono regolare.

## Confronto con la radice reale

Nei numeri reali il simbolo

$$
\sqrt{4}
$$

indica per convenzione l'unica radice quadrata non negativa, cioè $2$. L'equazione

$$
z^2=4
$$

ha invece in $\mathbb{C}$ due soluzioni:

$$
z=2
\qquad\text{oppure}\qquad
z=-2.
$$

Bisogna quindi distinguere il valore convenzionale della radice reale dalle soluzioni dell'equazione complessa.

## La radice complessa non è automaticamente una funzione

Per $n\geq2$, a ogni $w\neq0$ corrispondono $n$ radici distinte. Senza scegliere una particolare radice, il simbolo di radice ennesima complessa non associa dunque a $w$ un unico valore.

Di conseguenza, la “radice ennesima complessa” considerata come insieme di tutte le radici non è una funzione da $\mathbb{C}$ in $\mathbb{C}$. Per ottenere una funzione occorre introdurre una scelta coerente di un solo valore, argomento che richiede convenzioni ulteriori non sviluppate in questa lezione.

## Errori comuni

- Dividere soltanto l'argomento principale $\varphi$ per $n$ e trovare una sola radice.
- Usare valori di $k$ diversi da $0,\ldots,n-1$ senza riconoscere che producono ripetizioni.
- Dimenticare il fattore $2k\pi$ prima di dividere l'argomento per $n$.
- Usare $R/n$ al posto di $R^{1/n}$ per il modulo.
- Credere che le radici abbiano argomenti separati da $2\pi$ invece che da $2\pi/n$.
- Confondere il valore della radice reale principale con tutte le soluzioni complesse.
- Affermare che anche $0$ possiede $n$ radici distinte.
- Trattare la radice complessa come una funzione a valore unico senza dichiarare una scelta.

## Connessioni

- Usa [[47 Modulo e Argomento dei Numeri Complessi|modulo e argomento]].
- Richiede la [[48 Forma Trigonometrica dei Numeri Complessi|forma trigonometrica]] o la [[50 Forma Esponenziale e Identità di Eulero|forma esponenziale]].
- Deriva dalla [[52 Formula di De Moivre e Potenze Complesse|formula di De Moivre]].
- Riprende la distinzione tra radice reale ed equazione associata studiata in [[33 Radice Ennesima Reale|radice ennesima reale]].

## Uso all'esame

Potenziale rilevanza d'esame: determinare tutte le radici di un numero complesso, rappresentarle nel piano, motivare perché sono esattamente $n$ e distinguere correttamente radice reale principale ed equazione complessa.

## Errore comune all'orale

Non basta enunciare la formula: bisogna dichiarare $w\neq0$, indicare $k=0,\ldots,n-1$, spiegare che tutte le radici hanno modulo $R^{1/n}$ e che gli argomenti consecutivi differiscono di $2\pi/n$.
