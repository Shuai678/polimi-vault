---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 07, PDF p. 20
  - Libro, §3.7, pp. 99-101 (enunciati e interpretazione)
---

# Gerarchia degli infiniti

## Perché viene introdotta

Sapere che numeratore e denominatore crescono entrambi senza limite non determina il limite del loro rapporto. Dobbiamo confrontare le velocità di crescita. La gerarchia fornisce quattro confronti fondamentali già enunciati nella Lezione 07.

## Teorema

Per $\alpha>0$ e $a>1$,

$$
\lim_{n\to+\infty}\frac{\log_a n}{n^\alpha}=0,
\qquad
\lim_{n\to+\infty}\frac{n^\alpha}{a^n}=0.
$$

Per ogni $a>1$,

$$
\lim_{n\to+\infty}\frac{a^n}{n!}=0.
$$

Infine,

$$
\lim_{n\to+\infty}\frac{n!}{n^n}=0.
$$

Gli indici si considerano almeno da $n=1$; per rapporti con logaritmo al denominatore si parte da $n=2$. Le costanti $a$ e $\alpha$ sono **fissate**, indipendenti da $n$.

## Notazione e significato

Il fattoriale è

$$
n!=1\cdot2\cdot\ldots\cdot n\quad(n\geq1),\qquad0!=1.
$$

Per esempio $4!=24$, mentre $4^4=256$. In $n!$ i fattori variano da $1$ a $n$; in $n^n$ ci sono $n$ fattori tutti uguali a $n$.

Il primo limite dice che qualunque potenza positiva dell'indice cresce più rapidamente del logaritmo. Il secondo dice che un'esponenziale con base maggiore di uno cresce più rapidamente di qualunque potenza positiva fissata. Il terzo pone il fattoriale sopra le esponenziali a base fissata, il quarto pone $n^n$ sopra il fattoriale.

L'ordine da ricordare è quindi:

$$
\log_a n < \qquad n^\alpha < \qquad a^n < \qquad n! < \qquad n^n.
$$

In questa lista ogni termine cresce più lentamente del successivo **nel senso dei rapporti sopra**, non nel senso di una disuguaglianza valida per ogni indice. La gerarchia descrive il comportamento per $n$ grande: una potenza di esponente molto alto può superare un'esponenziale per molti indici iniziali.

### Da dire all'orale

> A base esponenziale maggiore di uno ed esponente della potenza positivo, entrambi fissati, il logaritmo cresce più lentamente della potenza, la potenza dell'esponenziale, l'esponenziale del fattoriale e il fattoriale di $n^n$. Il significato rigoroso è che ciascuno dei quattro rapporti enunciati tende a zero.

## Dimostrazioni e confine della lezione

A p. 20 il docente enuncia i quattro limiti senza dimostrarli. Il libro li dimostra nel §3.7 usando anche strumenti di sezioni precedenti che il PDF della Lezione 07 non ha svolto. Qui si registrano gli enunciati, le condizioni e le applicazioni; non si introducono il criterio del rapporto, il numero di Nepero o le stime asintotiche formali come nuovi argomenti della lezione.

## Metodo di riconoscimento

1. Identificare logaritmi, potenze dell'indice, esponenziali a base fissata, fattoriali e $n^n$.
2. Controllare che la base sia maggiore di uno e che gli esponenti richiesti siano positivi e fissati.
3. Riscrivere il rapporto in una delle forme del teorema, eventualmente moltiplicata per una costante.
4. Se compaiono somme, dividerle per il termine adatto e verificare il limite di ogni addendo. Il quoziente finale con limiti finiti si giustifica con [[80 Algebra dei Limiti di Successioni]].

## Esercizio svolto: rapporto con una somma

### Testo

Calcolare

$$
\lim_{n\to+\infty}\frac{n^3+\log_2 n}{2^n}.
$$

### Idea

L'esponenziale deve essere confrontata prima con la potenza. Per il logaritmo usiamo una catena di rapporti già noti.

### Svolgimento passo per passo

Separiamo esattamente i due addendi:

$$
\frac{n^3+\log_2 n}{2^n}
=\frac{n^3}{2^n}+\frac{\log_2 n}{2^n}.
$$

Il primo rapporto tende a zero per il secondo limite della gerarchia, con $\alpha=3$ e $a=2$. Per il secondo, scriviamo

$$
\frac{\log_2 n}{2^n}
=\frac{\log_2 n}{n}\cdot\frac{n}{2^n}.
$$

Entrambi i fattori tendono a zero per i primi due confronti del teorema. Per la regola del prodotto il secondo addendo tende a zero, e per la somma il risultato è

$$
\lim_{n\to+\infty}\frac{n^3+\log_2 n}{2^n}=0.
$$

### Cosa imparare

Il confronto di quantità non adiacenti nella lista si può costruire attraverso un prodotto di rapporti adiacenti, ciascuno con limite noto.

## Esercizio svolto: fattoriale

### Testo e svolgimento

Calcolare il limite di $\displaystyle\frac{5^n+n!}{n!}$. Per $n\geq1$,

$$
\frac{5^n+n!}{n!}=\frac{5^n}{n!}+1\to0+1=1,
$$

usando il terzo confronto con base fissata $a=5>1$. Il risultato nasce da una riscrittura esatta, non dalla cancellazione approssimativa del termine $5^n$.

## Errori comuni e prospettiva d'esame

- Interpretare la gerarchia come ordine puntuale valido già per i primi indici.
- Confondere $a^n$ con $n^a$ o $n^n$: il ruolo dell'indice è diverso.
- Applicare $a^n/n!\to0$ con una base che dipende da $n$: il caso $a=n$ non rientra nelle ipotesi.
- Applicare $n^\alpha/a^n\to0$ con $a=1$ o con $0<a<1$.
- Sostituire simbolicamente un rapporto di due infiniti con $1$, $0$ o un valore non giustificato.

Potenziale rilevanza d'esame: enunciare i quattro limiti con le condizioni e riconoscerli dentro espressioni più articolate. Questi risultati completano il materiale presente nel PDF L7; la prosecuzione della preparazione seguirà il prossimo PDF disponibile.
