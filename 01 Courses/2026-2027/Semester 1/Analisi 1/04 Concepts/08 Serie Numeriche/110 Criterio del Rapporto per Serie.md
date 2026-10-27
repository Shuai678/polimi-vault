---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 14-15, 18
  - Lezione 12, PDF pp. 2-6, dimostrazione del docente e schema degli intorni a p. 2
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

## Dimostrazione del docente

> [!note] Integrazione della Lezione 12
> La prova di supporto già presente dal libro è ora completata con le scelte esplicite di $\varepsilon$ e i confronti geometrici svolti dal docente alle pp. 2-6 del PDF L12.

![[110 Intorni del Limite nel Criterio del Rapporto.svg|1000]]

Schema ricostruito dal disegno del docente a **p. 2 del PDF L12**. Il punto $1$ è la soglia; i due $\ell$ rappresentano **due casi distinti**:

- **Rosso, $0\leq\ell<1$:** scegliamo $\varepsilon=(1-\ell)/2$, così l'estremo destro dell'intorno è $q=\ell+\varepsilon<1$.
- **Blu, $1<\ell<+\infty$:** scegliamo $\varepsilon=(\ell-1)/2$, così l'estremo sinistro dell'intorno è $r=\ell-\varepsilon>1$.

Per definizione di limite, da un certo indice il rapporto $a_{n+1}/a_n$ resta nell'intorno di $\ell$: quindi resta **sotto $q<1$** nel primo caso, **sopra $r>1$** nel secondo. Se $\ell=0$, l'intorno si estende anche a sinistra di $0$, ma il rapporto resta positivo per ipotesi.

### Caso $\ell<1$: costruire un maggiorante sommabile

Scegliamo

$$
\varepsilon=\frac{1-\ell}{2}>0,
\qquad q=\ell+\varepsilon=\frac{1+\ell}{2}\in(0,1).
$$

Per definizione di limite, esiste $N_0$ tale che, per $n\geq N_0$, i termini siano positivi e

$$
\left|\frac{a_{n+1}}{a_n}-\ell\right|<\varepsilon,
\qquad0<\frac{a_{n+1}}{a_n}\leq q.
$$

Quindi $a_{N_0+1}\leq qa_{N_0}$, $a_{N_0+2}\leq q^2a_{N_0}$ e, per induzione,

$$
0<a_n\leq a_{N_0}q^{n-N_0}=Cq^n,
\qquad C=\frac{a_{N_0}}{q^{N_0}}>0.
$$

La serie del maggiorante è un multiplo positivo di una geometrica di ragione $q\in(0,1)$, dunque converge. Il [[107 Criterio del Confronto per Serie|teorema del confronto per le serie]] dà la convergenza della coda e quindi della serie originale. Inoltre $Cq^n\to0$, perciò $a_n\to0$.

### Caso $1<\ell<+\infty$: un minorante geometrico crescente

Scegliamo

$$
\varepsilon=\frac{\ell-1}{2}>0,
\qquad r=\ell-\varepsilon=\frac{\ell+1}{2}>1.
$$

Per definizione di limite, definitivamente $a_{n+1}/a_n\geq r$. Iterando la disuguaglianza,

$$
a_n\geq a_{N_0}r^{n-N_0}\longrightarrow+\infty.
$$

La [[103 Condizione Necessaria di Convergenza di una Serie]] fallisce e la serie non converge. Essendo definitivamente positiva, diverge a $+\infty$ per [[106 Serie a Termini Positivi]].

### Caso $\ell=+\infty$

La definizione di limite infinito permette di imporre definitivamente $a_{n+1}/a_n\geq2$. Ripetendo il ragionamento con $r=2$ otteniamo $a_n\geq a_{N_0}2^{n-N_0}\to+\infty$ e la divergenza positiva della serie.

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

## Applicazioni della Lezione 12 — Da studiare

Gli esempi $\sum a^n/n^n$, $\sum n^a b^n$ e $\sum a^n(\log n)^b$, con tutti i casi dei parametri, sono raccolti in [[113 Serie con Fattori Esponenziali Potenze e Logaritmi]]. Il rapporto è la dimostrazione **D13** nell'elenco del [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.
