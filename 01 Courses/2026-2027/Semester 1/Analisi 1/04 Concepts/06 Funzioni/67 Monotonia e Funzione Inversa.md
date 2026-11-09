---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 16, PDF pp. 13-14
  - Libro, §6.3, p. 200, teorema 6.28
  - Lezione 05, PDF pp. 16-19
  - Libro, §2.3.4, pp. 46-51 e §2.3.6, pp. 52-53
---

# Monotonia e funzione inversa

## Teorema

Sia

$$
f:A\subseteq\mathbb R\to\mathbb R.
$$

Se $f$ è strettamente monotona in $A$, allora:

1. $f$ è iniettiva;
2. l'inversa
   $$
   f^{-1}:\operatorname{Im}f\to A
   $$
   è strettamente monotona nello stesso verso di $f$.

In particolare:

- se $f$ è strettamente crescente, anche $f^{-1}$ è strettamente crescente;
- se $f$ è strettamente decrescente, anche $f^{-1}$ è strettamente decrescente.

## Dimostrazione: caso strettamente crescente

### 1. Iniettività

Prendiamo $x_1,x_2\in A$ con $x_1\neq x_2$. Per l'ordine totale dei reali, vale $x_1<x_2$ oppure $x_2<x_1$.

Se $x_1<x_2$, la stretta crescenza dà

$$
f(x_1)<f(x_2),
$$

quindi $f(x_1)\neq f(x_2)$. Il caso opposto è analogo. Dunque $f$ è iniettiva e l'inversa sulla sua immagine esiste.

### 2. Monotonia dell'inversa

Siano

$$
y_1,y_2\in\operatorname{Im}f,
\qquad y_1<y_2,
$$

e poniamo

$$
x_1=f^{-1}(y_1),
\qquad
x_2=f^{-1}(y_2).
$$

Vogliamo dimostrare $x_1<x_2$. Se per assurdo fosse $x_1\geq x_2$, la crescenza di $f$ implicherebbe

$$
f(x_1)\geq f(x_2),
$$

cioè

$$
y_1\geq y_2,
$$

in contraddizione con $y_1<y_2$. Pertanto

$$
x_1<x_2,
$$

e $f^{-1}$ è strettamente crescente.

Il caso strettamente decrescente si dimostra nello stesso modo, tenendo conto che $f$ inverte l'ordine.

### Da dire all'orale

> La stretta monotonia impedisce a due punti distinti di avere la stessa immagine, quindi garantisce l'iniettività. Nell'inversa l'ordine resta dello stesso tipo: crescente resta crescente e decrescente resta decrescente.

## Il viceversa è falso in generale

Una funzione invertibile non deve necessariamente essere monotona quando il dominio non impone un andamento ordinato unico. L'esempio della lezione è

$$
f:[0,2]\to[0,2],
$$

$$
f(x)=
\begin{cases}
x, & x\in[0,1),\\
3-x, & x\in[1,2].
\end{cases}
$$

Le immagini dei due rami sono rispettivamente $[0,1)$ e $[1,2]$, quindi sono disgiunte e coprono tutto $[0,2]$. Ogni valore ha esattamente una controimmagine: $f$ è biiettiva.

Tuttavia non è crescente, perché $1<2$ ma

$$
f(1)=2>1=f(2),
$$

e non è decrescente, perché $0<\frac12$ ma

$$
f(0)=0<\frac12=f\left(\frac12\right).
$$

![[67 Funzione Invertibile Non Monotona.svg|622]]

L'inversa è

$$
f^{-1}(y)=
\begin{cases}
y, & y\in[0,1),\\
3-y, & y\in[1,2].
\end{cases}
$$

In questo esempio $f^{-1}=f$.

## Struttura logica da ricordare

Il teorema afferma

$$
\text{stretta monotonia}
\quad\Longrightarrow\quad
\text{iniettività}.
$$

Non afferma in generale il viceversa:

$$
\text{iniettività}
\centernot\Longrightarrow
\text{stretta monotonia}.
$$

Il controesempio precedente è sufficiente per confutare l'implicazione inversa.

## Errori comuni

- Usare monotonia non stretta per concludere automaticamente l'iniettività: un tratto costante la contraddice.
- Dire che l'inversa di una funzione decrescente è crescente; resta invece decrescente.
- Confondere il teorema con il suo viceversa.
- Omettere che l'inversa è definita su $\operatorname{Im}f$.
- Nella prova, supporre già l'ordine delle controimmagini che si deve dimostrare.
- Nel controesempio, includere $x=1$ in entrambi i rami e rendere ambigua la definizione.

## Connessioni

- Combina [[62 Funzioni Monotone|stretta monotonia]], [[65 Funzioni Iniettive e Biiettive|iniettività]] e [[66 Funzione Inversa|inversa]].
- Usa il metodo del [[20 Dimostrazione per Assurdo|ragionamento per assurdo]] nella prova della monotonia dell'inversa.
- Il controesempio applica [[19 Controesempio|la logica di confutazione del viceversa]].

## Prospettiva d'esame

Teorema e dimostrazione sono materiale tipico da orale. Bisogna distinguere con precisione ipotesi, conclusioni e falso viceversa, sapendo riprodurre il controesempio della funzione a tratti.

## Lezione 16 - Continuità e invertibilità su un intervallo - Da studiare

> [!note] Nuova parte da studiare
> Il PDF L16, pp. 13-14, riprende prima il teorema e il controesempio già presenti in questa nota, poi aggiunge le ipotesi di continuità e dominio intervallo. Lo stato precedente della nota è conservato; questa integrazione è **Da studiare**.

### Richiamo del docente

Una funzione strettamente monotona è invertibile sulla propria immagine e la sua inversa è strettamente monotona nello stesso verso. Il teorema e la dimostrazione sono già nella parte iniziale della nota.

Il viceversa non vale in generale. Il docente ripropone proprio [[67 Monotonia e Funzione Inversa#Il viceversa è falso in generale|la funzione a tratti già presente]] già sviluppata sopra: $f^{-1}=f$, ma la funzione non è monotona. Si conservano il grafico e la formula esistenti, senza duplicare il controesempio. In questo esempio dominio e immagine sono entrambi $[0,2]$, ma manca la continuità in $x=1$.

### Teorema del docente con la continuità

Sia $f:I\subseteq\mathbb R\to\mathbb R$, con $I$ **intervallo**, continua in $I$. Allora

$$
\boxed{f\text{ strettamente monotona}\iff f\text{ invertibile}.}
$$

In tal caso:

- $f^{-1}$ è strettamente monotona come $f$;
- $\operatorname{Im}f=D(f^{-1})$ è un intervallo;
- $f^{-1}:\operatorname{Im}f\to I$ è **continua sul proprio dominio**.

Nel PDF questo teorema è enunciato, senza una dimostrazione sviluppata. L'ordine è quello del docente: prima il falso viceversa generale, poi l'equivalenza nel caso continuo su un intervallo e la continuità dell'inversa.

### Corollario annunciato dal docente

Le funzioni elementari sono continue sui loro domini. L'applicazione del risultato alle radici, ai logaritmi e alle inverse goniometriche è sviluppata in [[145 Continuità delle Funzioni Elementari]], nello stesso ordine del PDF.

### Commenti: cosa significa invertibile e quali ipotesi servono

Come in [[66 Funzione Inversa]], qui invertibile significa **sulla propria immagine**: la funzione $f:I\to\operatorname{Im}f$ è biiettiva. Non si sta deducendo che $f$ sia suriettiva su tutto $\mathbb R$. Per esempio l'esponenziale ha inversa sul dominio $(0,+\infty)$ del logaritmo, non su tutto $\mathbb R$.

L'immagine è un intervallo per [[143 Teorema dei Valori Intermedi e Immagine di un Intervallo]]. La continuità dell'inversa è una conclusione ulteriore: la sola esistenza algebrica di un'inversa non basta a darla. Il controesempio sopra, essendo uguale alla propria inversa e discontinuo, rende visibile questa distinzione.

> [!info] Approfondimento dal libro
> Il §6.3, p. 200, formula la continuità dell'inversa di una funzione continua e invertibile su un intervallo e mostra che togliere l'ipotesi di intervallo può far fallire la conclusione. Si usa il risultato come supporto al teorema del docente; non si introduce una prova diversa attribuita alla lezione.

### Uso negli esercizi

Per giustificare un'inversa continua, verificare il dominio intervallo, la continuità di $f$ e la sua stretta monotonia; dichiarare poi il dominio dell'inversa come $\operatorname{Im}f$. Non basta scrivere la formula risolta rispetto a $x$.

Nell'esempio già presente in [[66 Funzione Inversa#Esempio della Lezione 06: esponenziale composta|Concept 66]], $f(x)=e^{x^3+2}$ è continua e strettamente crescente su $\mathbb R$, con immagine $(0,+\infty)$. La sua inversa $\sqrt[3]{\log y-2}$ è quindi continua per $y>0$. Questo aggiorna la giustificazione dell'esempio senza risolverlo una seconda volta.

### Da dire all'orale

> Per una funzione continua su un intervallo, l'invertibilità sulla propria immagine equivale alla stretta monotonia. In questo caso l'immagine è un intervallo e l'inversa è continua sul suo dominio, con lo stesso verso di monotonia della funzione di partenza. Continuità e dominio intervallo sono ipotesi del risultato, non conseguenze della sola invertibilità.
