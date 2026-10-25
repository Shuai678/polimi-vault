---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF p. 8 (richiamo e precisazione dell’indice)
  - Lezione 10, PDF pp. 7, 13-15
  - Libro, §4.1, pp. 114-115; esempio 4.3
---

# Serie geometrica e rappresentazioni decimali

## Intuizione e definizione

In una **serie geometrica** ogni contributo è ottenuto dal precedente moltiplicando per una ragione reale fissa $q$:

$$
\sum_{n=0}^{+\infty}q^n=1+q+q^2+\cdots.
$$

Per $q=0$ si intende la successione con primo termine $1$ e tutti i successivi nulli; il termine iniziale del polinomio geometrico è quindi $1$ anche in questo caso. Il carattere si studia attraverso le [[99 Serie Numeriche e Somme Parziali|somme parziali]], usando i [[78 Limiti di Potenze e Progressioni Geometriche|limiti delle successioni geometriche]].

## Formula della somma parziale: dimostrazione

Per ogni $N\geq0$,

$$
S_N=1+q+q^2+\cdots+q^N,
\qquad qS_N=q+q^2+\cdots+q^{N+1}.
$$

Sottraendo queste due **somme finite**, tutti i termini intermedi si cancellano:

$$
(1-q)S_N=1-q^{N+1}.
$$

Se $q\neq1$, dividiamo per $1-q$; per $q=1$ contiamo i termini. Dunque

$$
\boxed{S_N=
\begin{cases}
\dfrac{1-q^{N+1}}{1-q},&q\neq1,\\[4pt]
N+1,&q=1.
\end{cases}}
$$

## Teorema: carattere per ogni ragione reale

$$
\boxed{
\begin{array}{ll}
|q|<1:&\displaystyle\sum_{n=0}^{+\infty}q^n=\frac1{1-q}\quad\text{(converge)},\\[6pt]
q\geq1:&\displaystyle\sum_{n=0}^{+\infty}q^n=+\infty,\\[4pt]
q\leq-1:&\text{serie irregolare}.
\end{array}}
$$

### Ipotesi, tesi e prova dei casi

La ragione $q$ è reale e fissata; non dipende dall'indice.

- Se $|q|<1$, allora $q^{N+1}\to0$ e la formula di $S_N$ dà il limite $1/(1-q)$. Questo comprende le ragioni negative fra $-1$ e $0$.
- Se $q=1$, $S_N=N+1\to+\infty$.
- Se $q>1$, riscriviamo $S_N=(q^{N+1}-1)/(q-1)\to+\infty$.
- Se $q=-1$, le somme parziali sono $1,0,1,0,\ldots$, quindi non hanno limite.
- Se $q<-1$, per $N$ pari $q^{N+1}$ è negativo e $S_N\to+\infty$ lungo quegli indici; per $N$ dispari è positivo e $S_N\to-\infty$ lungo gli altri. Nessun limite unico esiste.

Non esiste quindi una ragione reale per cui questa serie, con primo termine $1$, diverga a $-\infty$.

### Da dire all'orale

> La serie geometrica di ragione reale q converge se e solo se il valore assoluto di q è minore di uno e in tal caso la somma, partendo dall'indice zero, è uno diviso uno meno q. Per q maggiore o uguale a uno diverge positivamente; per q minore o uguale a meno uno è irregolare. Il risultato segue dalla formula della somma parziale e dal limite della potenza geometrica.

## Esempio geometrico: infiniti pezzi, area finita

Per $q=1/2$,

$$
\sum_{n=0}^{+\infty}\frac1{2^n}
=1+\frac12+\frac14+\frac18+\cdots=2.
$$

![[100 Somma Geometrica per Aree.svg|950]]

La figura riprende l'idea del PDF con un disegno originale: il rettangolo totale ha area $2$. Dopo aver aggiunto i pezzi da $n=0$ a $n=N$ resta un'area $2^{-N}$, perché

$$
S_N=2-2^{-N},\qquad 2-S_N=2^{-N}\to0.
$$

Lo stesso principio chiarisce la motivazione di Achille e la tartaruga: infinite tappe con durate che formano una progressione geometrica di ragione fra $0$ e $1$ possono avere durata totale finita. Il numero infinito di tappe, da solo, non implica un tempo infinito.

## Attenzione all'indice iniziale

Per $|q|<1$ e $m\geq0$,

$$
\sum_{n=m}^{+\infty}q^n
=q^m\sum_{k=0}^{+\infty}q^k=\frac{q^m}{1-q}.
$$

Si verifica prima a livello di somme finite con $n=m+k$, poi si passa al limite. Se il primo termine è un coefficiente reale $A$, la somma è $A/(1-q)$. La formula senza $q^m$ vale quando si parte da $0$.

## Richiamo nella Lezione 11: precisazione dell'indice

A p. 8 del PDF L11 la tabella della geometrica riporta $1/(1-q)$ accanto a una somma con indice iniziale $1$. Quel valore corrisponde alla partenza da **$0$**, come dimostrato sopra. La formula coerente con l'indice $1$ è invece

$$
\sum_{n=1}^{+\infty}q^n=\frac q{1-q}\qquad(|q|<1).
$$

Per $q\geq0$ il carattere richiamato dal docente resta corretto: convergenza per $0\leq q<1$ e divergenza positiva per $q\geq1$. La correzione riguarda il valore della somma, non il carattere.

## Rappresentazioni decimali come serie

Il collegamento con [[05 Rappresentazioni Decimali]] è

$$
r=\pm a_0,a_1a_2a_3\ldots
=\pm\left(a_0+\sum_{n=1}^{+\infty}\frac{a_n}{10^n}\right),
$$

con $a_0\in\mathbb N$ e cifre $a_n\in\{0,\ldots,9\}$ per $n\geq1$. Il segno riguarda l'intero valore fra parentesi. Se $r\in[0,1]$ si può adottare una rappresentazione con $a_0=0$, comprendendo $1$ tramite $0,\overline9$.

### Esercizio — Perché $0,\overline9=1$

Per definizione della rappresentazione infinita,

$$
\begin{aligned}
0,\overline9
&=\sum_{n=1}^{+\infty}\frac9{10^n}
=9\left(\sum_{n=0}^{+\infty}\left(\frac1{10}\right)^n-1\right)\\
&=9\left(\frac1{1-1/10}-1\right)
=9\left(\frac{10}{9}-1\right)=1.
\end{aligned}
$$

Il $-1$ toglie il termine con indice $0$. Equivalentemente, dopo $N$ cifre nove si ha $1-10^{-N}$ e la differenza da $1$ tende a zero. Ogni troncamento è minore di $1$, ma il suo limite è esattamente $1$.

### L'analogo in base otto citato dal docente

In base $8$,

$$
(0,\overline7)_8
=\sum_{n=1}^{+\infty}\frac7{8^n}
=7\frac{1/8}{1-1/8}=1.
$$

La base determina i pesi delle cifre; sette periodico **in base dieci** rappresenterebbe invece $7/9$.

## Errore dopo un numero finito di termini

> [!info] Approfondimento dal libro
> Dalla somma parziale dell'esempio 4.3, pp. 114-115, si ricava direttamente una stima utile per approssimare una serie geometrica convergente. È un'applicazione aggiuntiva della stessa identità, senza nuovi criteri sulle serie.

Per $|q|<1$ il resto dopo $N+1$ termini è

$$
R_N=S-S_N=\frac{q^{N+1}}{1-q},\qquad
|R_N|=\frac{|q|^{N+1}}{|1-q|}.
$$

Per esempio, per la somma di $2^{-n}$, con $N=10$ l'errore è $2^{-10}=1/1024<10^{-3}$.

## Errori comuni e prospettiva d'esame

- Usare $1/(1-q)$ senza la condizione $|q|<1$.
- Dimenticare che $q=-1$ dà irregolarità, non una somma $1/2$.
- Perdere il primo termine quando l'indice parte da $1$.
- Confondere una serie geometrica con una serie qualsiasi il cui termine tende a zero.
- Scrivere $1/(1-q)$ per $q=1$, quando la formula non è definita.

Potenziale rilevanza d'esame: classificazione completa, dimostrazione della somma finita, code e applicazioni alle rappresentazioni numeriche.
