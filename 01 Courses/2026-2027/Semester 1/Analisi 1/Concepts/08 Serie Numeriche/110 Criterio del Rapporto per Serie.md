---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 14-15, 18
  - Libro, §4.2.2, pp. 121-123; teorema 4.19 ed esempio 4.21
---

# Criterio del rapporto per serie

## Quando si usa e intuizione

Il rapporto tra termini consecutivi è utile quando fattoriali, prodotti o potenze si semplificano passando da $a_n$ ad $a_{n+1}$. Se il rapporto resta sotto una costante $q<1$, i termini sono maggiorati da una progressione geometrica **sommabile**. Se resta sopra una costante $r>1$, i termini crescono senza limite.

Il [[91 Criterio del Rapporto per Successioni]] riguardava il limite dei termini; qui si conclude sul carattere della **serie**. Il semplice fatto che $a_n\to0$ non sarebbe sufficiente: serve il maggiorante geometrico.

## Teorema

Sia $a_n>0$ definitivamente e supponiamo che esista

$$
\ell=\lim_{n\to+\infty}\frac{a_{n+1}}{a_n}\in[0,+\infty].
$$

Allora

$$
\boxed{
\begin{aligned}
0\leq\ell<1&\Longrightarrow\sum a_n\text{ converge e }a_n\to0,\\
\ell>1&\Longrightarrow\sum a_n=+\infty\text{ e }a_n\to+\infty.
\end{aligned}}
$$

Il caso $\ell>1$ comprende $\ell=+\infty$. Per **$\ell=1$ il criterio è inconclusivo**. La positività stretta nella coda assicura che il rapporto sia definito. Il limite, se esiste, non può essere negativo.

## Dimostrazione di supporto

> [!info] Approfondimento dal libro
> Il PDF enuncia il criterio; il teorema 4.19, pp. 121-122, permette di studiarne la prova tramite confronto geometrico. Si mantiene anche la conclusione del PDF sul limite dei termini.

### Caso $\ell<1$: costruire un maggiorante sommabile

Scegliamo $q$ con $\ell<q<1$. Per definizione di limite, esiste $N_0$ tale che

$$
0<\frac{a_{n+1}}{a_n}\leq q\qquad(n\geq N_0).
$$

Quindi $a_{N_0+1}\leq qa_{N_0}$, $a_{N_0+2}\leq q^2a_{N_0}$ e, per induzione,

$$
0<a_n\leq a_{N_0}q^{n-N_0}\qquad(n\geq N_0).
$$

La serie del maggiorante vale $a_{N_0}\sum_{k=0}^{+\infty}q^k$ ed è convergente. Il [[107 Criterio del Confronto per Serie]] dà la convergenza della coda e quindi della serie originale. Inoltre il maggiorante tende a zero, dunque $a_n\to0$.

### Caso $\ell>1$: un minorante geometrico crescente

Scegliamo $r$ con $1<r<\ell$ se $\ell$ è finito; se $\ell=+\infty$, scegliamo un qualunque $r>1$. Definitivamente $a_{n+1}/a_n\geq r$ e quindi, ancora per induzione,

$$
a_n\geq a_{N_0}r^{n-N_0}\to+\infty.
$$

La [[103 Condizione Necessaria di Convergenza di una Serie]] fallisce e la serie non converge. Essendo definitivamente positiva, diverge a $+\infty$ per [[106 Serie a Termini Positivi]].

## Il caso $\ell=1$ non decide

Le serie $\sum1/n^2$ e $\sum1/n$ hanno entrambe rapporto consecutivo tendente a $1$, ma la prima converge e la seconda diverge. Il calcolo per ogni esponente $\alpha$ è svolto in [[108 Serie Armoniche Generalizzate e di Bertrand]]. Non si deve interpretare $\ell=1$ né come convergenza né come divergenza.

## Esempio di supporto — Esponenziale su fattoriale

> [!info] Approfondimento dal libro
> L'esempio 4.21, p. 123, considera $\sum1/n!$. La stessa semplificazione vale per $\sum A^n/n!$ con $A>0$ fissato, riprendendo il termine già studiato nel Concept 91.

Per $a_n=A^n/n!>0$,

$$
\frac{a_{n+1}}{a_n}
=\frac{A^{n+1}}{(n+1)!}\frac{n!}{A^n}
=\frac A{n+1}\to0<1.
$$

Quindi $\sum_{n=1}^{+\infty}A^n/n!$ converge. Il criterio decide la convergenza, senza calcolare il valore della somma. L'esempio del docente $\sum n!/n^n$, svolto con il rapporto e con Stirling, è raccolto in [[112 Formula di Stirling e Serie con Fattoriali]].

## Procedura ed errori comuni

1. Controllare la positività e la non nullità dei termini nella coda.
2. Sostituire ogni occorrenza di $n$ con $n+1$ per costruire $a_{n+1}$.
3. Formare $a_{n+1}/a_n$, semplificare e calcolarne il limite.
4. Confrontare con $1$; se il limite è $1$, cambiare metodo.

Non invertire il rapporto, non perdere il fattore $n+1$ in $(n+1)!$ e non confondere $\ell$ con il limite di $a_n$ o con la somma della serie. Se il rapporto non ha limite, il teorema in questa forma non si applica.

### Da dire all'orale

> Per una serie con termini definitivamente strettamente positivi, se il rapporto del termine successivo sul corrente tende a un valore minore di uno, la serie converge. Se tende a un valore maggiore di uno, incluso più infinito, la serie diverge positivamente e i termini tendono a più infinito. Il valore uno non dà conclusioni. La prova usa confronti con progressioni geometriche.

Potenziale rilevanza d'esame: ipotesi e soglia, dimostrazione tramite il maggiorante geometrico e calcoli con fattoriali.
