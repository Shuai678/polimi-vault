---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 07, PDF pp. 18-19
  - Libro, §3.3.2, pp. 89-90
---

# Confronto in modulo e prodotto con un infinitesimo

## Intuizione

Una successione è [[74 Limiti Infiniti e Regolarità delle Successioni|infinitesima]] quando tende a zero. Per provarlo è spesso sufficiente controllarne la distanza da zero, senza determinarne il segno.

Il prodotto di un fattore limitato e un fattore infinitesimo tende a zero: il fattore limitato può oscillare, ma non può amplificare senza limite la piccolezza dell'altro.

## Primo corollario: confronto in modulo

Se

$$
|b_n|\leq c_n\qquad\text{definitivamente},\qquad c_n\to0,
$$

allora $b_n\to0$ e $|b_n|\to0$.

La stima implica automaticamente che $c_n\geq0$ sulla coda in cui vale. Non si richiede che $b_n$ abbia un segno fisso.

### Dimostrazione

Poiché $|b_n|\leq c_n$, abbiamo

$$
-c_n\leq b_n\leq c_n\qquad\text{definitivamente}.
$$

Entrambe le barriere tendono a zero, quindi il [[82 Teorema dei Due Carabinieri|teorema dei due carabinieri]] dà $b_n\to0$. Anche $0\leq|b_n|\leq c_n$ implica $|b_n|\to0$.

In generale vale l'equivalenza

$$
b_n\to0\quad\Longleftrightarrow\quad|b_n|\to0:
$$

le condizioni $|b_n-0|<\varepsilon$ e $\bigl||b_n|-0\bigr|<\varepsilon$ sono identiche.

## Secondo corollario: limitata per infinitesima

Se $(c_n)$ è limitata e $b_n\to0$, allora

$$
c_nb_n\to0.
$$

Non è necessario che $c_n$ ammetta limite. È proprio questa l'utilità rispetto alla regola del prodotto di due successioni convergenti.

### Dimostrazione mediante una stima

Esiste $K>0$ tale che $|c_n|\leq K$. Quindi

$$
|c_nb_n|=|c_n|\,|b_n|\leq K|b_n|.
$$

Poiché $|b_n|\to0$, per l'algebra dei limiti $K|b_n|\to0$. Il primo corollario dà $c_nb_n\to0$.

La stessa conclusione si legge direttamente dalla definizione: dato $\varepsilon>0$, scegliamo $N$ con $|b_n|<\varepsilon/K$ per ogni $n\geq N$; allora $|c_nb_n|\leq K|b_n|<\varepsilon$.

> [!info] Approfondimento dal libro
> Il PDF enuncia questi corollari e mostra l'applicazione al seno. La stima $|c_nb_n|\leq K|b_n|$ esplicita la dimostrazione del Teorema 3.34 del libro (§3.3.2, p. 89): permette di vedere perché basta la limitatezza del primo fattore, senza supporne la convergenza.

### Da dire all'orale

> Una successione il cui modulo è definitivamente maggiorato da una successione infinitesima tende a zero. In particolare, il prodotto di una successione limitata e una infinitesima è infinitesimo, anche se la successione limitata non ha limite.

## Esercizio della lezione

### Testo

Calcolare $\displaystyle\lim_{n\to+\infty}\frac{\sin n}{n}$.

### Idea

Scriviamo la successione come prodotto di $c_n=\sin n$, che è limitata, e $b_n=1/n$, che tende a zero. Non occorre calcolare il limite di $\sin n$.

### Svolgimento passo per passo

Per ogni $n\geq1$,

$$
|\sin n|\leq1,\qquad\frac1n\to0.
$$

Per il secondo corollario,

$$
\frac{\sin n}{n}=\sin n\cdot\frac1n\to0.
$$

Equivalentemente, la stima

$$
\left|\frac{\sin n}{n}\right|\leq\frac1n
$$

permette di applicare direttamente il primo corollario.

![[84 Oscillazione e Infinitesimo.svg|740]]

### Risultato e cosa imparare

Il limite è zero. L'ampiezza massima dell'oscillazione scende a zero: una stima è sufficiente anche quando l'algebra dei limiti sui singoli fattori non è applicabile.

## Altro esempio svolto

Per $n\geq1$,

$$
\frac{3+\cos n}{\sqrt n}=(3+\cos n)\frac1{\sqrt n}.
$$

Da $-1\leq\cos n\leq1$ ricaviamo $2\leq3+\cos n\leq4$, dunque il primo fattore è limitato. Il secondo è $n^{-1/2}\to0$. Il prodotto tende a zero.

## Errori comuni

- Cercare di moltiplicare un “limite di $\sin n$” per zero: si usa la limitatezza, non la convergenza.
- Supporre che $b_n\to0$ basti per ogni prodotto: se $c_n=n$ e $b_n=1/n$, il prodotto vale $1$. Se $c_n=n^2$, il prodotto vale $n$.
- Deducere $b_n\to0$ dalla sola disuguaglianza $b_n\leq c_n\to0$: manca il controllo inferiore. Per esempio $-n\leq1/n$.
- Confondere un termine piccolo per qualche indice con una stima definitiva per tutti gli indici avanzati.

## Connessioni e prospettiva d'esame

Combina [[70 Grafico e Limitatezza delle Successioni|limitatezza]], [[82 Teorema dei Due Carabinieri|confronto]] e [[80 Algebra dei Limiti di Successioni|algebra dei limiti]].

Potenziale rilevanza d'esame: riconoscere i fattori oscillanti limitati e costruire una maggiorazione in valore assoluto valida definitivamente.
