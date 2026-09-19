---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 02, PDF pp. 4-7
  - Libro, cap. 1.1.3
---

# Campi ordinati

## Intuizione

Un campo ordinato è un campo nel quale gli elementi possono essere confrontati mediante un ordine totale compatibile con la somma e con il prodotto. La compatibilità garantisce che le operazioni algebriche modifichino le disuguaglianze secondo regole precise.

## Definizione formale

Una relazione $\leq$ su un insieme $X$ è un ordine totale se, per ogni $a,b,c\in X$, valgono:

- riflessività: $a\leq a$; 
	- (ogni numero è minore o uguale a se stesso)
- antisimmetria: se $a\leq b$ e $b\leq a$, allora $a=b$; 
	- ( se due numeri sono contemporaneamente minori o uguali l'uno all'altro, allora devono essere uguali )
- transitività: se $a\leq b$ e $b\leq c$, allora $a\leq c$; 
	- ( se un numero è minore o uguale a un secondo numero, e il secondo numero è minore o uguale a un terzo allora il primo è minore o uguale al terzo )
- totalità: $a\leq b$ oppure $b\leq a$.
	- ( presi due numeri qualsiasi, è sempre possibile confrontarli : uno è minore o uguale all'altro)

Un [[22 Campi|campo]] $X$ è un **campo ordinato** se è dotato di un ordine totale che soddisfa inoltre:

$$
a\leq b \Longrightarrow a+c\leq b+c
$$

per ogni $c\in X$, e

$$
a\leq b,\quad c>0 \Longrightarrow ac\leq bc.
$$

### Da dire all'orale

> Un campo ordinato è un campo dotato di un ordine totale tale che l'aggiunta della stessa quantità conserva l'ordine e la moltiplicazione per una quantità positiva conserva l'ordine.

## Notazione

- $a\leq b$ significa che $a$ è minore o uguale a $b$.
- $a<b$ significa che $a\leq b$ e $a\neq b$.
- $c>0$ indica un elemento positivo.
- $c<0$ indica un elemento negativo.

## Condizioni

Se si moltiplica una disuguaglianza per $c$:

- per $c>0$, il verso rimane invariato;
- per $c=0$, entrambi i membri diventano zero e l'informazione sul confronto iniziale viene persa;
- per $c<0$, il verso si inverte.

In particolare, se $a<b$, moltiplicando per zero si ottiene l'uguaglianza $0=0$, non una disuguaglianza stretta.

## Metodo / Dimostrazione

### Positività dei quadrati

In ogni campo ordinato vale

$$
a^2\geq0
$$

per ogni $a$. Se $a\neq0$, allora $a^2>0$.

- Se $a>0$, il prodotto $a\cdot a$ è positivo.
- Se $a<0$, allora $-a>0$ e $a^2=(-a)^2>0$.
- Se $a=0$, allora $a^2=0$.

### Perché $\mathbb{C}$ non è un campo ordinato

Supponiamo per assurdo che $\mathbb{C}$ possieda un ordine compatibile con le operazioni di campo. Poiché $i\neq0$, dalla positività dei quadrati dovrebbe seguire

$$
i^2>0.
$$

Ma $i^2=-1$, mentre in un campo ordinato $-1<0$. Si ottiene una contraddizione. Pertanto $\mathbb{C}$ è un campo, ma non può essere un campo ordinato.

## Esempi

- $\mathbb{Q}$ e $\mathbb{R}$ sono campi ordinati con l'ordine usuale.
- Da $2<3$, moltiplicando per $4>0$, segue $8<12$.
- Da $2<3$, moltiplicando per $-1<0$, segue $-2>-3$.
- Da $2<3$, moltiplicando per zero, segue $0=0$.

## Errori comuni

- Moltiplicare per un numero negativo senza invertire il verso della disuguaglianza.
- Dimenticare che moltiplicando per zero si perde la stretta disuguaglianza iniziale.
- Credere che ogni campo sia automaticamente ordinato.
- Affermare direttamente che $i^2$ è positivo in $\mathbb{C}$: nella dimostrazione bisogna prima supporre per assurdo che $\mathbb{C}$ sia ordinato.

## Connessioni

- La struttura di campo giustifica le operazioni algebriche; l'ordine totale permette di confrontare gli elementi.
- I campi ordinati consentono di definire insiemi limitati, maggioranti, minoranti, massimo, minimo, estremo superiore ed estremo inferiore.

## Prospettiva d'esame

Quando si manipola una disuguaglianza bisogna dichiarare il segno del fattore. Nella dimostrazione che $\mathbb{C}$ non è ordinabile, occorre esplicitare la supposizione per assurdo prima di usare la positività dei quadrati.
