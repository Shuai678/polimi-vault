---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 07, PDF pp. 5-6
  - Libro, §3.2, Teorema 3.13 e Osservazione 3.14, pp. 81-82
---

# Limitatezza delle successioni convergenti

## Teorema

Se una successione reale $(a_n)$ converge a un limite **finito** $\ell\in\mathbb R$, allora è limitata: esistono $P,L\in\mathbb R$ tali che

$$
P\leq a_n\leq L\qquad\text{per ogni indice ammesso}.
$$

Non occorre che la successione sia monotona. L'ipotesi è la [[72 Limite Finito di una Successione|convergenza]]; la tesi è la [[70 Grafico e Limitatezza delle Successioni|limitatezza dell'intera successione]].

## Intuizione e strategia

I termini abbastanza avanzati stanno vicino al limite, quindi dentro un intervallo limitato. Prima della soglia rimane soltanto un numero finito di termini reali: anche questi possono essere racchiusi fra due barriere. Unendo i due controlli otteniamo una stima globale.

![[77 Convergenza e Limitatezza.svg|720]]

## Dimostrazione

Supponiamo che la successione inizi dall'indice $n_0$. Dalla definizione di limite, scegliendo $\varepsilon=1$, esiste $N\geq n_0$ tale che

$$
\ell-1<a_n<\ell+1\qquad\text{per ogni }n\geq N.
$$

Il valore $1$ non ha nulla di speciale: basta una fascia di ampiezza fissa. Consideriamo ora l'insieme iniziale

$$
\{a_{n_0},a_{n_0+1},\ldots,a_N\}.
$$

È finito e non vuoto, perciò possiede un massimo $M$ e un minimo $m$, entrambi reali. Poniamo

$$
L=\max\{M,\ell+1\},\qquad P=\min\{m,\ell-1\}.
$$

Se $n_0\leq n\leq N$, allora $P\leq m\leq a_n\leq M\leq L$. Se $n\geq N$, allora $P\leq\ell-1<a_n<\ell+1\leq L$. Quindi

$$
P\leq a_n\leq L\qquad\forall n\geq n_0.
$$

Questo dimostra la tesi. Volendo una stima in valore assoluto, basta prendere $K=\max\{|P|,|L|\}+1>0$: allora $|a_n|\leq K$ per tutti gli indici.

### Da dire all'orale

> Ogni successione convergente è limitata. La definizione di limite controlla la coda dentro una fascia centrata nel limite; i termini iniziali sono finiti e hanno massimo e minimo. Combinando queste barriere si controlla tutta la successione.

## Perché il viceversa è falso

La successione $a_n=(-1)^n$ soddisfa $-1\leq a_n\leq1$, ma alterna indefinitamente $1$ e $-1$. Non può convergere: se convergesse a $\ell$, anche i termini di indice pari e quelli di indice dispari dovrebbero avvicinarsi allo stesso $\ell$, mentre valgono rispettivamente $1$ e $-1$.

La limitatezza diventa sufficiente per la convergenza quando si aggiunge la monotonia, come nel [[76 Teorema del Limite delle Successioni Monotone|teorema del limite monotono]].

## Esempio: i primi termini non decidono il limite

Sia $a_0=100$, $a_1=-50$ e $a_n=1/n$ per $n\geq2$. La successione tende a zero: da $n=2$ in poi coincide con $1/n$. Tuttavia le barriere $-1$ e $1$ non controllano tutti i termini. Una stima globale è

$$
-50\leq a_n\leq100.
$$

Una modifica di un numero finito di termini non cambia il limite, ma può cambiare massimo, minimo e barriere globali.

## Uso negli esercizi ed errori comuni

- Da $a_n\to\ell\in\mathbb R$ si può usare una costante $K$ con $|a_n|\leq K$, anche senza determinarne il valore preciso. Questo sarà decisivo nella [[80 Algebra dei Limiti di Successioni|prova del limite del prodotto]].
- Per contrapposizione, una successione illimitata non può avere limite finito; può però avere limite infinito oppure essere irregolare.
- Non sostituire “convergente” con “regolare”: $a_n=n$ è regolare e illimitata.
- Non concludere che una successione limitata converge e non dimenticare i termini prima della soglia $N$.

## Prospettiva d'esame

Potenziale rilevanza d'esame: distinguere l'implicazione corretta dal falso viceversa e ricostruire la dimostrazione con controllo separato della coda e del blocco iniziale.
