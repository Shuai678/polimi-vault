---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 2-5 (code e prosecuzione sulle serie positive)
  - Lezione 10, PDF pp. 7-13
  - Libro, §4.1, p. 113
---

# Serie numeriche e somme parziali

## Perché introdurre una somma infinita

Una rappresentazione decimale contiene potenzialmente infinite cifre; una figura può essere suddivisa in pezzi sempre più piccoli; nel paradosso di Achille e la tartaruga compaiono infinite tappe di inseguimento. Per dare significato alla somma di infiniti contributi non eseguiamo un'infinità di operazioni tutte insieme: studiamo il limite delle **somme finite iniziali**.

Per esempio la scrittura $1+1/2+1/4+\cdots$ acquista significato calcolando prima $1$, poi $1+1/2$, poi $1+1/2+1/4$ e infine il limite di questa successione. Il risultato sarà giustificato in [[100 Serie Geometrica e Rappresentazioni Decimali]].

## Definizione formale e notazione

Data una successione reale $(a_n)_{n\in\mathbb N}$, definiamo la **successione delle somme parziali**

$$
\boxed{S_N:=\sum_{n=0}^{N}a_n=a_0+a_1+\cdots+a_N,\qquad N\in\mathbb N.}
$$

Chiamiamo **serie degli $a_n$** la scrittura formale

$$
\sum_{n=0}^{+\infty}a_n.
$$

$a_n$ è il termine generale, $n$ l'indice di sommazione, $N$ l'ultimo indice incluso nella somma parziale. A partire da $0$, $S_N$ contiene **$N+1$ termini**. Se si parte da $n=1$, la somma fino a $N$ contiene invece $N$ termini. L'indice iniziale va sempre letto nella formula.

Per $N\geq1$ vale l'identità esatta

$$
S_N=S_{N-1}+a_N,\qquad a_N=S_N-S_{N-1},\qquad S_0=a_0.
$$

Studiare una serie coinvolge quindi due successioni diverse: $(a_n)$ e $(S_N)$. Il comportamento di una non va confuso con quello dell'altra.

## Convergenza, divergenza e irregolarità

Il **carattere della serie** è determinato dal limite di $(S_N)$, secondo la terminologia del docente:

| Comportamento delle somme parziali | Carattere della serie | Scrittura |
|---|---|---|
| $S_N\to S\in\mathbb R$ | Convergente; $S$ è la somma | $\sum_{n=0}^{+\infty}a_n=S$ |
| $S_N\to+\infty$ | Divergente positivamente | $\sum_{n=0}^{+\infty}a_n=+\infty$ |
| $S_N\to-\infty$ | Divergente negativamente | $\sum_{n=0}^{+\infty}a_n=-\infty$ |
| Il limite non esiste nemmeno in $\overline{\mathbb R}$ | Irregolare o indeterminata | La serie non ha somma |

Una serie convergente o divergente è detta **regolare**. Qui $\overline{\mathbb R}=\mathbb R\cup\{-\infty,+\infty\}$, come in [[74 Limiti Infiniti e Regolarità delle Successioni]]. L'uguaglianza con $\pm\infty$ indica un limite infinito, non un numero reale ottenuto sommando.

Solo quando il limite esiste si può attribuire un valore alla scrittura formale:

$$
\sum_{n=0}^{+\infty}a_n
:=\lim_{N\to+\infty}S_N
=\lim_{N\to+\infty}\sum_{n=0}^{N}a_n.
$$

### Da dire all'orale

> Data una successione reale, considero la successione delle somme parziali dei suoi termini nell'ordine assegnato. La serie converge se queste somme parziali hanno limite reale finito, che si chiama somma della serie. Diverge positivamente o negativamente se il limite è rispettivamente più o meno infinito; è irregolare se il limite non esiste nemmeno nei reali estesi.

## Esempi del PDF: calcolare prima $S_N$

### Serie nulla

Se $a_n=0$ per ogni $n$, allora $S_N=0$ per ogni $N$. Perciò $\sum_{n=0}^{+\infty}0=0$: la serie converge.

### Serie di termini tutti uguali a $1$

Se $a_n=1$, allora

$$
S_N=\sum_{n=0}^{N}1=N+1\to+\infty.
$$

La serie diverge positivamente. Il termine generale ha limite $1$, mentre le somme parziali hanno limite $+\infty$.

### Serie con termini $(-1)^n$

Per $N$ pari, fino all'indice $N$ ci sono coppie $1-1$ e un ultimo $1$; per $N$ dispari tutte le coppie si chiudono. Quindi

$$
S_N=\sum_{n=0}^{N}(-1)^n=
\begin{cases}
1,&N\text{ pari},\\
0,&N\text{ dispari}.
\end{cases}
$$

I valori non si avvicinano a un unico limite; la serie è **irregolare**, non divergente a $+\infty$ o a $-\infty$. La scrittura $1-1+1-1+\cdots$ non ha somma secondo la definizione del corso.

![[99 Carattere dalle Somme Parziali.svg|1000]]

Nel grafico il primo caso è la serie geometrica di ragione $1/2$, dimostrata nella nota successiva. Tutti i pannelli mostrano $S_N$, non $a_n$.

## Carattere e valore della somma sono problemi diversi

Stabilire che una serie converge non significa aver calcolato esplicitamente la somma. Spesso è più accessibile determinarne il carattere mediante condizioni necessarie o sufficienti. Il calcolo esatto o approssimato della somma è un problema ulteriore: nel PDF questa distinzione motiva i futuri criteri.

I **primi termini in numero finito** non influenzano il carattere. Se modifichiamo soltanto $a_0,\ldots,a_m$, per $N\geq m$ la nuova somma parziale è

$$
\widetilde S_N=S_N+C,\qquad
C=\sum_{n=0}^{m}(\widetilde a_n-a_n)\in\mathbb R.
$$

Aggiungere una costante conserva convergenza, divergenza con segno e irregolarità. Se però la serie converge a $S$, la nuova somma è $S+C$: i termini iniziali contano per il **valore**. È consentito anche studiare una coda e reinserire poi la somma finita esclusa.

## L'ordine dei termini fa parte della definizione

Il PDF richiede di sommare i termini nell'ordine assegnato. La commutatività di una somma finita non autorizza a riordinare liberamente una serie infinita: cambia la successione di somme parziali a cui si sta applicando il limite. Qui non si introducono teoremi sui riordinamenti.

## Prosecuzione nella Lezione 11 — Da studiare

Il teorema iniziale della nuova lezione precisa il legame tra la serie e le sue code: [[105 Code e Resto di una Serie]] introduce il resto $R_N=S-S_N$ e ne dimostra il limite zero per serie convergenti.

Per le [[106 Serie a Termini Positivi]], le somme parziali sono definitivamente crescenti: la loro limitatezza superiore decide la convergenza. Su questa proprietà si fondano i criteri di confronto successivi.

## Errori comuni e prospettiva d'esame

- Calcolare $\lim a_n$ e chiamarlo somma della serie: la somma è il limite di $S_N$.
- Considerare ogni serie non convergente come divergente a infinito, ignorando il caso irregolare.
- Perdere o aggiungere un termine confondendo partenza da $0$ e da $1$.
- Concludere che cambiare pochi termini conserva il valore della somma, anziché soltanto il carattere.

Potenziale rilevanza d'esame: definizione completa, distinzione fra le due successioni e calcolo delle somme parziali negli esempi elementari.
