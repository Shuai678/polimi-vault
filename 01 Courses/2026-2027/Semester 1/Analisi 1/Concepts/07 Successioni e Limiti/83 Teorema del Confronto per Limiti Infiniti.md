---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 07, PDF pp. 17-18
  - Libro, §3.3.1, Teorema 3.31, p. 89
---

# Teorema del confronto per limiti infiniti

## Teorema

Siano $(a_n)$ e $(b_n)$ successioni reali con

$$
a_n\leq b_n\qquad\text{definitivamente}.
$$

Allora:

- se $a_n\to+\infty$, anche $b_n\to+\infty$;
- se $b_n\to-\infty$, anche $a_n\to-\infty$.

Per $+\infty$ serve una barriera **inferiore** che tenda a $+\infty$; per $-\infty$ serve una barriera **superiore** che tenda a $-\infty$. Qui è sufficiente una sola barriera.

## Intuizione

Una successione che supera qualcosa di già definitivamente più grande di ogni soglia deve superare essa stessa ogni soglia. Il ragionamento si inverte verso il basso per $-\infty$.

## Dimostrazione del caso $+\infty$

Fissiamo $M>0$. Poiché $a_n\to+\infty$, esiste $N_1$ tale che $a_n>M$ per ogni $n\geq N_1$. Dal confronto definitivo esiste $N_2$ tale che $a_n\leq b_n$ per ogni $n\geq N_2$.

Per $n\geq N=\max\{N_1,N_2\}$,

$$
M<a_n\leq b_n.
$$

Abbiamo dimostrato che $\forall M>0\ \exists N\ \forall n\geq N$, $b_n>M$: quindi $b_n\to+\infty$.

## Caso $-\infty$

Se $b_n\to-\infty$, dato $M>0$ troviamo una soglia $N_1$ tale che $b_n<-M$ per $n\geq N_1$. Unendola alla soglia $N_2$ del confronto, per $n\geq\max\{N_1,N_2\}$ otteniamo

$$
a_n\leq b_n<-M,
$$

che prova $a_n\to-\infty$.

### Da dire all'orale

> Una successione definitivamente maggiore di una successione che tende a più infinito tende anch'essa a più infinito. Una successione definitivamente minore di una che tende a meno infinito tende anch'essa a meno infinito.

## Esercizi svolti

### Testo e idea

Determinare i limiti di $n+\sin n$ e $-n+\cos n$. Le oscillazioni goniometriche sono limitate e possiamo trovare la barriera adatta.

### Svolgimento passo per passo

Da $\sin n\geq-1$ segue

$$
n+\sin n\geq n-1.
$$

La barriera $n-1$ tende a $+\infty$: dato $M>0$, basta $n>M+1$. Per confronto,

$$
n+\sin n\to+\infty.
$$

Da $\cos n\leq1$ segue

$$
-n+\cos n\leq-n+1.
$$

La barriera $-n+1$ tende a $-\infty$: dato $M>0$, per $n>M+1$ vale $-n+1<-M$. Quindi

$$
-n+\cos n\to-\infty.
$$

### Cosa imparare

Non è necessario conoscere il limite del termine oscillante quando una barriera controlla già il comportamento dell'intera successione.

## Errori comuni

- Invertire il ruolo della barriera: da $a_n\leq b_n$ e $b_n\to+\infty$ non segue $a_n\to+\infty$. Il controesempio è $a_n=0$, $b_n=n$.
- Confondere illimitatezza con limite infinito: il superamento delle soglie deve valere definitivamente.
- Usare confronti verificati soltanto per un numero finito di termini.

## Connessioni e prospettiva d'esame

La prova applica direttamente [[74 Limiti Infiniti e Regolarità delle Successioni|la definizione di limite infinito]]. A differenza del [[82 Teorema dei Due Carabinieri|confronto finito]], qui una sola barriera orientata correttamente basta.

Potenziale rilevanza d'esame: enunciati in entrambe le direzioni, prova mediante soglie e scelta del minorante o maggiorante negli esercizi.
