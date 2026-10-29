---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 14-15, 18
  - Lezione 12, PDF pp. 2-6, dimostrazione trascritta dal docente; commenti separati e schema degli intorni a p. 2
  - Libro, §4.2.2, pp. 121-123; teorema 4.19 ed esempio 4.21
---

# Criterio del rapporto per serie

## Quando si usa e intuizione

Il rapporto tra termini consecutivi è utile quando fattoriali, prodotti o potenze si semplificano passando da $a_n$ ad $a_{n+1}$. Se il rapporto resta sopra una costante $q>1$, i termini crescono senza limite. Se resta sotto una costante $q<1$, i termini sono maggiorati da una progressione geometrica **sommabile**.

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
\ell>1&\Longrightarrow\sum a_n=+\infty\text{ e }a_n\to+\infty,\\
0\leq\ell<1&\Longrightarrow\sum a_n\text{ converge e }a_n\to0.
\end{aligned}}
$$

Il caso $\ell>1$ comprende $\ell=+\infty$. Per **$\ell=1$ il criterio è inconclusivo**. La positività stretta nella coda assicura che il rapporto sia definito. Il limite, se esiste, non può essere negativo.

## Dimostrazione del professore — PDF L12, pp. 2-6

> [!note] Trascrizione dal PDF — Da studiare
> Sono mantenuti ordine dei casi, notazione $N$, $n$, $m$, $q$, disuguaglianze strette, iterazioni e conclusioni del professore. I commenti esplicativi sono raccolti **dopo** la dimostrazione, in una sezione separata.

Per semplicità supponiamo $a_n>0$ per ogni $n\in\mathbb N$.

$$
\ell=\lim_{n\to+\infty}\frac{a_{n+1}}{a_n}\in\overline{\mathbb R},
\qquad\ell\neq1.
$$

### 1) Se $\ell>1$, ci sono due casi

$$
\ell\in(1,+\infty)\qquad\text{o}\qquad\ell=+\infty.
$$

#### Se $\ell\in(1,+\infty)$ — PDF pp. 3-4

Scegliamo $\varepsilon=(\ell-1)/2>0$ nella definizione di limite. Allora esiste $N\in\mathbb N$ tale che, per ogni $n\geq N$,

$$
1<\frac{\ell+1}{2}
=\ell-\varepsilon
<\frac{a_{n+1}}{a_n}
<\ell+\varepsilon.
$$

Quindi, per ogni $n\geq N$,

$$
\frac{a_{n+1}}{a_n}>\frac{\ell+1}{2}>1.
$$

Se chiamiamo

$$
q=\frac{\ell+1}{2}>1,
$$

vale

$$
a_{n+1}>q\,a_n\qquad\forall n\geq N.\tag{*}
$$

Per ogni $n\geq N$,

$$
a_{n+1}>q\,a_n>q^2a_{n-1}>q^3a_{n-2}>\cdots
>q^{n+1-N}a_N,
$$

per iterazione della formula $(*)$.

Quindi, per ogni $n\geq N$,

$$
a_{n+1}>\frac{a_N}{q^N}\,q^{n+1}.
$$

Definitivamente in $m\in\mathbb N$, cioè per ogni $m\geq N+1$,

$$
a_m>\frac{a_N}{q^N}\,q^m>0.\tag{**}
$$

Per il teorema del confronto per serie, poiché

$$
\sum_{m=0}^{+\infty}q^m
$$

con $q>1$ diverge — serie geometrica di ragione $q=(\ell+1)/2>1$ — anche la serie

$$
\sum_{m=0}^{+\infty}a_m
$$

diverge.

Per il teorema del confronto per successioni divergenti, poiché

$$
\lim_{m\to+\infty}q^m=+\infty,
$$

per $(**)$ vale

$$
\lim_{m\to+\infty}a_m=+\infty.
$$

#### Se $\ell=+\infty$ — PDF p. 4

Per definizione di limite infinito, per $M=2$ esiste $N\in\mathbb N$ tale che, per ogni $n\geq N$,

$$
\frac{a_{n+1}}{a_n}>M=2.
$$

Quindi

$$
a_{n+1}>q\,a_n
\qquad\text{con }q=2>1,
\qquad\forall n\geq N,
$$

e da qui si ripete l'argomento precedente da $(*)$ in poi.

### 2) Se $0\leq\ell<1$ — PDF pp. 4-6

Per $\varepsilon=(1-\ell)/2>0$ esiste $N\in\mathbb N$ tale che, per ogni $n\geq N$,

$$
\ell-\varepsilon
<\frac{a_{n+1}}{a_n}
<\ell+\varepsilon
=\frac{1+\ell}{2}<1.
$$

Quindi

$$
\frac{a_{n+1}}{a_n}<\frac{1+\ell}{2}<1
\qquad\forall n\geq N.
$$

Definiamo

$$
q=\frac{1+\ell}{2}\in(0,1).
$$

Allora

$$
0<a_{n+1}<q\,a_n
\qquad\forall n\geq N.\tag{***}
$$

Per ogni $n\geq N$,

$$
0<a_{n+1}<q\,a_n<q^2a_{n-1}<q^3a_{n-2}<\cdots
<q^{n+1-N}a_N.
$$

Quindi, per ogni $n\geq N$,

$$
0<a_{n+1}<\frac{a_N}{q^N}\,q^{n+1}.
$$

Segue che, definitivamente in $m\in\mathbb N$, cioè per ogni $m\geq N+1$,

$$
0<a_m<\frac{a_N}{q^N}\,q^m.
$$

Poiché $0<q<1$, per il criterio del confronto per serie, essendo

$$
\sum_{m=0}^{+\infty}q^m=\frac1{1-q}
$$

convergente, deve essere convergente anche

$$
\sum_{m=0}^{+\infty}a_m.
$$

La serie di confronto è una serie geometrica di ragione $q=(\ell+1)/2\in(0,1)$.

Per confronto per successioni, cioè per il teorema dei due carabinieri, essendo

$$
\lim_{m\to+\infty}q^m=0,
$$

deve essere

$$
\lim_{m\to+\infty}a_m=0.
$$

$\square$

## Commenti alla dimostrazione — aggiunti agli appunti

Questi commenti spiegano i passaggi del PDF; sono separati dalla trascrizione e restano **Da studiare**.

### Perché il professore può supporre tutti i termini positivi

L'ipotesi del teorema è la positività **definitiva**. Si può partire da una coda nella quale tutti i termini sono positivi e rinumerarla. Cambiare o escludere un numero finito di termini non cambia il carattere della serie né il limite del termine generale: vedi [[105 Code e Resto di una Serie]]. La semplificazione iniziale del docente non aggiunge un'ipotesi al teorema.

### La scelta di $\varepsilon$ e il significato di $q$

![[110 Intorni del Limite nel Criterio del Rapporto.svg|1000]]

Schema esplicativo ricostruito dal disegno a p. 2 del PDF. Il docente usa la stessa lettera $q=(\ell+1)/2$ in **due casi distinti**:

- se $\ell>1$ è finito, $\varepsilon=(\ell-1)/2$ e $q=\ell-\varepsilon>1$;
- se $0\leq\ell<1$, $\varepsilon=(1-\ell)/2$ e $q=\ell+\varepsilon\in(0,1)$.

La definizione di limite fornisce entrambe le disuguaglianze $\ell-\varepsilon<a_{n+1}/a_n<\ell+\varepsilon$. Nel primo caso serve quella inferiore; nel secondo quella superiore. Per $\ell=0$ l'intorno attraversa lo zero, ma il rapporto resta positivo per ipotesi.

### Come leggere l'iterazione e il cambio di indice

Nella catena si applica ogni volta $(*)$, oppure $(***)$, scendendo di un indice e moltiplicando per $q>0$. La catena si **arresta al termine $a_N$**: i puntini non richiedono di scendere sotto $N$. Per $n=N$ c'è soltanto $a_{N+1}>qa_N$, oppure $0<a_{N+1}<qa_N$; per $n=N+1$ c'è un passaggio ulteriore.

L'esponente finale è $n+1-N$, perché da $a_N$ ad $a_{n+1}$ ci sono $n+1-N$ passi. Si usa poi

$$
q^{n+1-N}a_N=\frac{a_N}{q^N}\,q^{n+1}.
$$

Ponendo $m=n+1$, la condizione $n\geq N$ diventa **$m\geq N+1$**, come scritto in rosso dal docente.

### Il fattore costante nel confronto geometrico

In entrambi i casi $a_N/q^N$ è un numero **positivo, finito e indipendente da $m$**. Il termine da confrontare con $a_m$ è quindi $(a_N/q^N)q^m$. La sua serie ha lo stesso carattere di $\sum q^m$; per $0<q<1$,

$$
\sum_{m=0}^{+\infty}\frac{a_N}{q^N}q^m
=\frac{a_N}{q^N}\frac1{1-q}<+\infty.
$$

Per $q>1$ quel multiplo della geometrica diverge a $+\infty$. Il [[107 Criterio del Confronto per Serie]] si applica nella coda indicata; i termini iniziali non cambiano il carattere. Questo rende esplicito il fattore costante sottinteso dal professore quando richiama la geometrica $\sum q^m$.

Nel caso divergente il limite $a_m\to+\infty$ segue dal [[83 Teorema del confronto per successioni divergenti]]; nel caso convergente $a_m\to0$ segue dal [[82 Teorema dei Due Carabinieri]]. Sono conclusioni ottenute **dopo** il confronto per serie, nello stesso ordine del PDF.

### Perché nel PDF la somma parte anche da $0$

L'enunciato a p. 2 scrive la serie da $n=1$; durante la dimostrazione il docente usa $\sum_{m=0}^{+\infty}a_m$. La differenza è un solo termine e non cambia il carattere. Qui sono mantenuti gli indici del PDF; il confronto effettivo vale dalla coda $m\geq N+1$.

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

> Per una serie con termini definitivamente strettamente positivi, se il rapporto del termine successivo sul corrente tende a un valore maggiore di uno, incluso più infinito, la serie diverge positivamente e i termini tendono a più infinito. Se tende a un valore minore di uno, la serie converge. Il valore uno non dà conclusioni. La prova usa confronti con progressioni geometriche.

Potenziale rilevanza d'esame: ipotesi e soglia, dimostrazione tramite il maggiorante geometrico e calcoli con fattoriali.

## Applicazioni della Lezione 12 — Da studiare

Gli esempi $\sum a^n/n^n$, $\sum n^a b^n$ e $\sum a^n(\log n)^b$, con tutti i casi dei parametri, sono raccolti in [[113 Serie con Fattori Esponenziali Potenze e Logaritmi]]. Il rapporto è la dimostrazione **D13** nell'elenco del [[AM1-regolamento26-27.pdf|regolamento ufficiale]], p. 2.
