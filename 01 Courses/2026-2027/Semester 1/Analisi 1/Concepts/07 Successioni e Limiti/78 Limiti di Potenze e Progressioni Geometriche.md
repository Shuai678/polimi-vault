---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 07, PDF pp. 6-7
  - Libro, §3.5.1, pp. 92-93
---

# Limiti di potenze e progressioni geometriche

## Due ruoli diversi dell'indice

In $n^\beta$ varia la base e l'esponente $\beta$ è fissato. In $q^n$ la base $q$ è fissata e varia l'esponente. I due comportamenti vanno distinti.

Le formule con $1/n$ sono definite per $n\geq1$. Anche per $q=0$ consideriamo $n\geq1$, evitando $0^0$.

## Potenze dell'indice

Per ogni $\alpha\in\mathbb R$,

$$
\lim_{n\to+\infty}\frac1{n^\alpha}=
\begin{cases}
0,&\alpha>0,\\
1,&\alpha=0,\\
+\infty,&\alpha<0.
\end{cases}
$$

Se $\alpha>0$, la successione è decrescente e positiva. Per verificare il limite zero, dato $\varepsilon>0$,

$$
\frac1{n^\alpha}<\varepsilon
\Longleftrightarrow n^\alpha>\frac1\varepsilon
\Longleftrightarrow n>\varepsilon^{-1/\alpha}.
$$

Basta un naturale $N>\varepsilon^{-1/\alpha}$. Se $\alpha=0$, ogni termine vale $1$. Se $\alpha<0$, ponendo $\beta=-\alpha>0$, si ha $1/n^\alpha=n^\beta$. Dato $M>0$,

$$
n^\beta>M\Longleftrightarrow n>M^{1/\beta},
$$

quindi il limite è $+\infty$.

Equivalentemente,

$$
\lim_{n\to+\infty}n^\beta=
\begin{cases}
+\infty,&\beta>0,\\
1,&\beta=0,\\
0,&\beta<0.
\end{cases}
$$

## Progressione geometrica di ragione $q$

Per $q\in\mathbb R$, la successione $(q^n)$ ha i seguenti comportamenti:

| Ragione | Comportamento dei termini, per $n\geq1$ | Limite |
|---|---|---|
| $q>1$ | positivi, strettamente crescenti, illimitati | $+\infty$ |
| $q=1$ | costanti uguali a $1$ | $1$ |
| $0<q<1$ | positivi, strettamente decrescenti | $0$ |
| $q=0$ | costanti uguali a $0$ | $0$ |
| $-1<q<0$ | alternano segno, con ampiezza che si riduce | $0$ |
| $q=-1$ | alternano $-1$ e $1$, restano limitati | non esiste |
| $q<-1$ | alternano segno, con ampiezza crescente e illimitata | non esiste, neppure infinito |

![[78 Progressioni Geometriche.svg|760]]

Per $q>1$, la divergenza si può verificare direttamente. Dato $M>0$, scegliamo $N>\max\{0,\log_q M\}$. Poiché l'esponenziale di base $q>1$ è crescente, per $n\geq N$ vale $q^n>M$.

Per $0<q<1$, poniamo $r=1/q>1$. Dato $\varepsilon>0$, scegliamo $N>\max\{0,\log_r(1/\varepsilon)\}$. Allora $r^n>1/\varepsilon$ e $q^n=1/r^n<\varepsilon$.

Per $-1<q<0$, il segno alterna, ma

$$
|q^n|=|q|^n\to0.
$$

La distanza da zero tende a zero, dunque anche $q^n\to0$. Il cambiamento di segno non impedisce la convergenza se l'ampiezza si annulla.

Per $q<-1$, scriviamo $q=-r$, con $r>1$. I termini pari sono $q^{2k}=r^{2k}$ e superano ogni soglia positiva; quelli dispari sono $q^{2k+1}=-r^{2k+1}$ e scendono sotto ogni soglia negativa. Un limite finito è escluso dalla [[77 Limitatezza delle Successioni Convergenti|non limitatezza]]; $+\infty$ è escluso dai termini dispari negativi e $-\infty$ dai termini pari positivi.

### Da dire all'orale

> La successione geometrica $q^n$ tende a zero se $|q|<1$, vale sempre uno se $q=1$ e diverge a più infinito se $q>1$. Per $q\leq-1$ non ammette limite, perché l'alternanza di segno non si attenua.

## Esercizio svolto

### Testo

Determinare il comportamento di $(-2/3)^n$, $n^{-3/2}$ e $(-3)^n$.

### Idea e svolgimento

1. Per $(-2/3)^n$, la ragione soddisfa $|-2/3|<1$: il modulo $(2/3)^n$ tende a zero, quindi il limite è zero.
2. $n^{-3/2}=1/n^{3/2}$: l'esponente del denominatore è positivo, quindi il limite è zero.
3. $(-3)^n$ ha ragione minore di $-1$: i termini pari crescono senza limite e quelli dispari scendono senza limite. È irregolare.

### Cosa imparare

Il segno alterno non basta per decidere se un limite esiste: bisogna guardare anche l'ampiezza dei termini.

## Errori comuni e connessioni

- Confondere $n^q$ e $q^n$, oppure supporre che ogni base negativa renda la successione irregolare.
- Scrivere $(-3)^n\to-\infty$: gli indici pari lo impediscono.
- Usare il [[76 Teorema del Limite delle Successioni Monotone|teorema monotono]] nei casi alterni senza verificarne le ipotesi.
- Le stime dalla definizione usano [[35 Potenze con Esponente Reale|potenze reali]], [[36 Logaritmi|logaritmi]] e [[74 Limiti Infiniti e Regolarità delle Successioni|limiti infiniti e regolarità]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: classificare la geometrica per tutti i valori reali della ragione e motivare i casi $q=-1$ e $q<-1$, distinguendo limitatezza e regolarità.
