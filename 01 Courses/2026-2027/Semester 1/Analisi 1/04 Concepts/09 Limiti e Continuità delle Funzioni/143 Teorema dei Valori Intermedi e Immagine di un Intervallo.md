---
course: Analisi 1
type: concept
status: Da studiare
updated: 2026-11-09
source:
  - Lezione 16, PDF pp. 7-10
  - Libro, §6.3, pp. 194-195, teorema 6.20
---

# Teorema dei valori intermedi e immagine di un intervallo

## Teorema del docente

Sia $f:I\subseteq\mathbb R\to\mathbb R$, con $I$ intervallo, continua in $I$. Se $y_1,y_2\in\operatorname{Im}f$, per ogni $\lambda$ compreso fra $y_1$ e $y_2$ esiste $x_0\in I$ tale che

$$
\boxed{f(x_0)=\lambda.}
$$

In particolare, **$\operatorname{Im}f$ è un intervallo**. La continuità impedisce che fra due valori effettivamente assunti rimangano valori non assunti.

## Dimostrazione del professore

Siano $y_1,y_2\in\operatorname{Im}f\subseteq\mathbb R$. Supponiamo $y_1\leq y_2$. Esistono quindi $x_1,x_2\in I$ tali che

$$
f(x_1)=y_1,\qquad f(x_2)=y_2.
$$

Se $\lambda=y_1$ oppure $\lambda=y_2$, allora si prende $x_0=x_1$ oppure $x_0=x_2$ e la dimostrazione è conclusa.

Sia ora $\lambda\in(y_1,y_2)$. Per semplicità supponiamo $x_1<x_2$; il caso $x_2<x_1$ è simile. Poiché $x_1,x_2\in I$, si ha $[x_1,x_2]\subseteq I$ e la restrizione di $f$ a $[x_1,x_2]$ è continua.

Consideriamo la funzione ausiliaria

$$
g:[x_1,x_2]\to\mathbb R,\qquad
g(x)=f(x)-\lambda.
$$

$g$ è continua in $[x_1,x_2]$. Inoltre

$$
g(x_1)=f(x_1)-\lambda=y_1-\lambda<0,
$$

$$
g(x_2)=f(x_2)-\lambda=y_2-\lambda>0.
$$

Per il teorema degli zeri applicato alla funzione continua $g$, esiste $x_0\in[x_1,x_2]\subseteq I$ tale che

$$
0=g(x_0)=f(x_0)-\lambda,
$$

quindi $f(x_0)=\lambda$, con $x_0\in I$.

Abbiamo così $[y_1,y_2]\subseteq\operatorname{Im}f$ per ogni $y_1,y_2\in\operatorname{Im}f$: l'immagine è un intervallo. $\square$

## Osservazione successiva del docente: superiore e inferiore

Per una funzione continua su un intervallo $I$,

$$
\operatorname{Im}f\supseteq\left(\inf_I f,\sup_I f\right).
$$

L'inferiore può appartenere all'immagine oppure no; lo stesso vale, indipendentemente, per il superiore. Dipende dalla funzione e dal suo dominio. Gli estremi infiniti non sono valori reali della funzione e non appartengono all'immagine.

## Corollario del docente: immagine di un intervallo chiuso e limitato

Se $f:[a,b]\to\mathbb R$ è continua, con $a,b\in\mathbb R$ e $a<b$, allora

$$
\boxed{\operatorname{Im}f=[m,M],}
$$

con

$$
m=\min_{[a,b]}f,\qquad M=\max_{[a,b]}f,\qquad m,M\in\mathbb R.
$$

## Dimostrazione del professore del corollario

Per il teorema di Weierstrass esistono

$$
m=\min_{[a,b]}f=f(x_m)\in\mathbb R,
\qquad M=\max_{[a,b]}f=f(x_M)\in\mathbb R,
$$

con $x_m,x_M\in[a,b]$. In particolare $m,M\in\operatorname{Im}f$ e coincidono con

$$
m=\inf_{[a,b]}f,\qquad M=\sup_{[a,b]}f.
$$

Per il teorema dei valori intermedi ogni valore intermedio viene assunto. Quindi $[m,M]=\operatorname{Im}f$. $\square$

## Commenti alle due dimostrazioni

La prova principale è quella del PDF, pp. 7-9: parte dai valori nell'immagine, ne sceglie le controimmagini, tratta prima gli estremi del segmento dei valori e poi trasforma l'equazione $f(x)=\lambda$ in $g(x)=0$. Si applica [[141 Teorema degli Zeri e Metodo di Bisezione]] alla funzione $g=f-\lambda$, continua per [[138 Algebra delle Funzioni Continue]].

L'ipotesi che **il dominio sia un intervallo** permette di includere tutto $[x_1,x_2]$ nel dominio. Se $x_2<x_1$, si usa $[x_2,x_1]$: i segni di $g$ ai due estremi sono scambiati, ma il prodotto rimane negativo. Il punto ottenuto dal teorema degli zeri è anche interno a quel segmento; l'appartenenza al segmento chiuso scritta dal docente è sufficiente per concludere che appartiene a $I$.

Nel corollario, [[142 Teorema di Weierstrass]] dà valori estremi **effettivamente assunti**. Le due inclusioni sono: ogni valore di $f$ sta fra minimo e massimo, quindi $\operatorname{Im}f\subseteq[m,M]$; i valori intermedi fra i due estremi sono tutti assunti, quindi $[m,M]\subseteq\operatorname{Im}f$. Sono necessari entrambi i passaggi per l'uguaglianza.

![[143 Valori Intermedi e Intervalli Immagine.svg|1100]]

## Esempi svolti: quali estremi appartengono all'immagine

Le funzioni seguenti sono continue sui rispettivi intervalli, per l'algebra delle funzioni continue.

| Funzione e dominio | Immagine | Estremi assunti |
|---|---|---|
| $f(x)=x$, $I=(0,1)$ | $(0,1)$ | Né inferiore né superiore |
| $f(x)=x^2$, $I=(-1,1)$ | $[0,1)$ | Minimo $0$ in $x=0$; superiore $1$ non assunto |
| $f(x)=-x^2$, $I=(-1,1)$ | $(-1,0]$ | Massimo $0$ in $x=0$; inferiore $-1$ non assunto |
| $f(x)=x$, $I=[0,1]$ | $[0,1]$ | Entrambi |

Per giustificare la seconda riga, $0\leq x^2<1$ per $|x|<1$. Viceversa, dato $y\in[0,1)$, $x=\sqrt y\in(-1,1)$ e $x^2=y$. La terza riga segue cambiando il segno dei valori. In una funzione costante il corollario restituisce $[m,m]=\{m\}$, anch'esso un intervallo.

Il teorema garantisce esistenza, non unicità della controimmagine: per $f(x)=x^2$ su $[-2,2]$, $\operatorname{Im}f=[0,4]$, e il valore intermedio $1$ è assunto sia in $x=-1$ sia in $x=1$.

## Ruolo delle ipotesi ed errori comuni

> [!info] Approfondimento dal libro
> Il §6.3, pp. 194-195, formula il risultato anche tramite inferiore e superiore e ne ricava la soluzione di $f(x)=\lambda$ applicando il teorema degli zeri a $f-\lambda$. Si segue qui l'enunciato del professore con due valori già appartenenti all'immagine.

Se il dominio ha un vuoto, anche una funzione continua può avere un vuoto nell'immagine: $f(x)=x$ su $[-2,-1]\cup[1,2]$ ha immagine uguale al dominio e non assume $0$, pur assumendo valori di segno opposto. Non è un controesempio al teorema, perché il dominio non è un intervallo.

Non scrivere automaticamente $\operatorname{Im}f=[\inf f,\sup f]$ su un intervallo qualsiasi: occorre controllare il raggiungimento degli estremi. Il teorema non dice che una funzione continua sia suriettiva su $\mathbb R$; descrive l'assenza di lacune fra i valori che assume.

## Prospettiva d'esame

Il regolamento ufficiale include il teorema alla voce **D16**. La [[D16 Teorema dei Valori Intermedi|scheda D16]] incorpora la stessa dimostrazione, senza invertirne l'ordine dei casi. Il corollario combina D16 e D17; non richiede monotonia.

### Da dire all'orale

> Una funzione continua su un intervallo assume ogni valore compreso fra due valori della sua immagine. Di conseguenza la sua immagine è un intervallo. Per dimostrarlo considero la funzione meno il valore da raggiungere e applico il teorema degli zeri fra due controimmagini. Se il dominio è chiuso e limitato, Weierstrass assicura minimo e massimo assunti e l'immagine è il segmento chiuso fra questi valori.
