---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 8-9, 16-17
  - Libro, §4.1, p. 116 (serie armonica generalizzata)
---

# Serie armoniche generalizzate e di Bertrand

## Perché sono serie campione

I criteri di confronto richiedono serie di cui conosciamo già il carattere. Le potenze di $n$ e i fattori logaritmici forniscono famiglie abbastanza semplici da riconoscere negli equivalenti di molti termini generali.

Le classificazioni seguenti sono gli **enunciati adottati dal docente**. Per l'armonica generalizzata il PDF rinvia la dimostrazione completa al futuro criterio del confronto integrale; la tabella di Bertrand è riportata senza dimostrazione. Le spiegazioni sotto chiariscono i casi già deducibili dagli strumenti attuali.

## Serie armonica generalizzata

Per $\alpha\in\mathbb R$ fissato,

$$
\boxed{
\sum_{n=1}^{+\infty}\frac1{n^\alpha}
\begin{cases}
\text{converge},&\alpha>1,\\
\text{diverge a }+\infty,&\alpha\leq1.
\end{cases}}
$$

La soglia è **strettamente** $\alpha>1$. Per $\alpha=1$ ritroviamo la [[104 Serie Armonica]], che diverge.

### Casi giustificabili subito

Se $\alpha\leq0$, il termine $n^{-\alpha}$ non tende a zero, quindi la serie non converge; essendo positiva, diverge a $+\infty$. Se $0<\alpha\leq1$, per $n\geq1$ vale $1/n^\alpha\geq1/n$: il [[107 Criterio del Confronto per Serie]] con l'armonica dà la divergenza.

La convergenza per ogni esponente reale $\alpha>1$ viene qui utilizzata come risultato enunciato nel PDF; la dimostrazione generale segue il rinvio del professore. Per un caso già dimostrabile, $n\geq2$ implica

$$
\frac1{n^2}\leq\frac1{n(n-1)}
=\frac1{n-1}-\frac1n.
$$

La serie a destra è una coda telescopica convergente, perciò anche $\sum1/n^2$ converge. È una verifica specifica coerente con la tabella.

## Serie di Bertrand generalizzata

Per $\alpha,\beta\in\mathbb R$ fissati consideriamo

$$
\sum_{n=2}^{+\infty}\frac1{n^\alpha(\log n)^\beta}.
$$

Si parte da **$n=2$**, così $\log n>0$ e la potenza reale $(\log n)^\beta$ è definita per ogni $\beta$. L'indice $1$ non è utilizzabile uniformemente: $\log1=0$. Correggere l'indice iniziale per avere termini definiti è compatibile con l'invarianza del carattere rispetto a un numero finito di termini.

$$
\boxed{
\begin{array}{ll}
\text{converge}&\alpha>1,\quad\beta\in\mathbb R,\\
\text{converge}&\alpha=1,\quad\beta>1,\\
\text{diverge a }+\infty&\alpha<1,\quad\beta\in\mathbb R,\\
\text{diverge a }+\infty&\alpha=1,\quad\beta\leq1.
\end{array}}
$$

La denominazione **serie di Bertrand**, senza “generalizzata”, indica il caso $\alpha=1$. Fuori dalla soglia $\alpha=1$ decide la potenza di $n$; sulla soglia decide il fattore logaritmico.

![[108 Mappa di Convergenza delle Serie di Bertrand.svg|950]]

### Perché il logaritmo non cambia la decisione quando $\alpha\neq1$

Da [[85 Gerarchia degli Infiniti]], per ogni $\delta>0$ e $\beta$ reale fissato, definitivamente

$$
n^{-\delta}\leq(\log n)^\beta\leq n^\delta.
$$

Per $\beta>0$ questo segue dalla crescita del logaritmo più lenta di ogni potenza; per $\beta<0$ si passa ai reciproci della medesima stima con $|\beta|$; per $\beta=0$ il fattore vale $1$. Quindi

$$
\frac1{n^{\alpha+\delta}}
\leq\frac1{n^\alpha(\log n)^\beta}
\leq\frac1{n^{\alpha-\delta}}.
$$

Se $\alpha>1$, scegliamo $0<\delta<\alpha-1$: la serie maggiorante converge. Se $\alpha<1$, scegliamo $0<\delta<1-\alpha$: la serie minorante diverge. Il caso critico $\alpha=1$ richiede invece la classificazione logaritmica enunciata sopra.

## Esempi risolti dalla tabella

- $\sum_{n=2}^{+\infty}1/[n(\log n)^2]$ converge: $\alpha=1$, $\beta=2>1$.
- $\sum_{n=2}^{+\infty}1/(n\log n)$ diverge: $\alpha=1$, $\beta=1$ è sulla soglia esclusa.
- $\sum_{n=2}^{+\infty}(\log n)^5/n^{3/2}$ converge: $\alpha=3/2>1$, $\beta=-5$.
- $\sum_{n=2}^{+\infty}1/[\sqrt n(\log n)^{100}]$ diverge: $\alpha=1/2<1$, nonostante il fattore logaritmico molto grande.

Il parametro $\beta$ va letto al **denominatore**: un logaritmo al numeratore corrisponde a esponente $\beta$ negativo.

## Perché rapporto e radice non decidono le armoniche generalizzate

Il PDF calcola entrambi i limiti per $a_n=n^{-\alpha}$:

$$
\frac{a_{n+1}}{a_n}=\left(\frac n{n+1}\right)^\alpha\to1,
$$

$$
\sqrt[n]{a_n}=n^{-\alpha/n}
=e^{-\alpha\log n/n}\to e^0=1,
$$

poiché $\log n/n\to0$ per la gerarchia. I [[110 Criterio del Rapporto per Serie|criteri del rapporto]] e della [[111 Criterio della Radice per Serie|radice]] sono entrambi inconclusivi quando il limite è $1$. Questa famiglia fornisce sia casi convergenti ($\alpha=2$) sia divergenti ($\alpha=1$) con quel medesimo limite.

### Da dire all'orale

> La serie armonica generalizzata di esponente alfa converge esattamente per alfa maggiore di uno. Per la famiglia con anche il logaritmo al denominatore, se alfa è maggiore di uno converge per ogni beta e se alfa è minore di uno diverge per ogni beta. Nel caso alfa uguale a uno converge esattamente per beta maggiore di uno. Gli indici dei termini con logaritmo partono da due.

Potenziale rilevanza d'esame: soglie esatte, interpretazione degli esponenti e riconoscimento dei casi in cui rapporto e radice non danno informazioni.
