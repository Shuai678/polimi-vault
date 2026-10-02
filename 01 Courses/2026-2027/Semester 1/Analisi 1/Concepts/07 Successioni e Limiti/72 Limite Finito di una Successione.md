---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 06, PDF pp. 11-15
  - Libro, §3.2, pp. 78-80
---

# Limite finito di una successione

## Definizione $\varepsilon$-$N$

La successione $(a_n)$ ha limite finito $\ell\in\mathbb R$ se

$$
\forall\varepsilon>0\;\exists N\in\mathbb N\;\forall n\geq N:
|a_n-\ell|<\varepsilon.
$$

Si scrive

$$
\lim_{n\to+\infty}a_n=\ell
\qquad\text{oppure}\qquad
a_n\to\ell.
$$

Una successione che ammette limite finito si dice **convergente**.

## Interpretazione geometrica

La disuguaglianza

$$
|a_n-\ell|<\varepsilon
$$

equivale a

$$
\ell-\varepsilon<a_n<\ell+\varepsilon.
$$

Per ogni fascia orizzontale, per quanto stretta, centrata alla quota $\ell$, tutti i punti del grafico con indice abbastanza grande devono cadere nella fascia.

![[72 Limite Finito Successione.svg|653]]

La soglia $N$ può dipendere da $\varepsilon$: chiedendo una precisione maggiore, in genere occorre andare più avanti nella successione.

## Forme equivalenti

Dire $a_n\to\ell$ equivale a dire

$$
|a_n-\ell|\to0
$$

e anche

$$
a_n-\ell\to0.
$$

La successione $a_n-\ell$ misura infatti l'errore, con segno, rispetto al valore limite.

## Esempio fondamentale: $1/n\to0$

Vogliamo mostrare che, per ogni $\varepsilon>0$, definitivamente

$$
\left|\frac1n-0\right|<\varepsilon.
$$

Per $n\geq1$ la condizione equivale a

$$
\frac1n<\varepsilon
\quad\Longleftrightarrow\quad
n>\frac1\varepsilon.
$$

È quindi sufficiente scegliere un intero $N>1/\varepsilon$, per esempio

$$
N=\left\lfloor\frac1\varepsilon\right\rfloor+1.
$$

Allora ogni $n\geq N$ soddisfa la disuguaglianza richiesta.

## Non tutte le successioni convergono

La successione $a_n=n$ non si avvicina ad alcun numero reale. Anche $a_n=(-1)^n$ non ha limite finito, perché continua ad assumere alternativamente i valori $1$ e $-1$.

### Da dire all'orale

> Per ogni precisione $\varepsilon>0$ devo trovare una soglia $N$, eventualmente dipendente da $\varepsilon$, dopo la quale tutti i termini distano da $\ell$ meno di $\varepsilon$.

## Errori comuni

- Scegliere prima $N$ e poi adattare $\varepsilon$: l'ordine corretto è $\forall\varepsilon\,\exists N$.
- Verificare la disuguaglianza per un solo termine invece che per ogni $n\geq N$.
- Pretendere che la successione raggiunga il valore limite.
- Usare un $N$ reale senza sostituirlo con un indice naturale adeguato.
- Confondere $n\to+\infty$ con il valore di un termine della successione.

## Connessioni

- Usa [[71 Proprietà Definitivamente Vere|proprietà definitivamente vere]].
- La geometria si legge sul [[70 Grafico e Limitatezza delle Successioni|grafico discreto della successione]].
- Il limite, se esiste, è unico per [[73 Unicità del Limite di Successione|unicità del limite]].

## Prospettiva d'esame

In una dimostrazione dalla definizione bisogna partire da un $\varepsilon>0$ arbitrario, ricavare una condizione sufficiente sull'indice e scegliere esplicitamente un $N\in\mathbb N$.
