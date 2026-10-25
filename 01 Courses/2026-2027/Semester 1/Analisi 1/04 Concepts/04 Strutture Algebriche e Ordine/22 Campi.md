---
course: Analisi 1
type: concept
status: studied
source:
  - Lezione 02, PDF pp. 2-4
  - Libro, cap. 1.1.2
---

# Campi

## Intuizione

Un campo è un insieme nel quale si possono eseguire somma, sottrazione, prodotto e divisione per elementi non nulli, rimanendo nell'insieme e rispettando regole algebriche precise.

## Definizione formale

Un insieme $X$, dotato delle operazioni di somma e prodotto, è un **campo** se valgono le seguenti proprietà per ogni $a,b,c\in X$:

Somma (S): 
- commutatività della somma: $a+b=b+a$;
- associatività della somma: $(a+b)+c=a+(b+c)$;
- esistenza dell'elemento neutro: $a+0=0+a=a$;
- esistenza dell'opposto: per ogni $a\in X$ esiste $-a\in X$ tale che $a+(-a)=0$;

Prodotto (P): 
- commutatività del prodotto: $ab=ba$;
- associatività del prodotto: $(ab)c=a(bc)$;
- esiste un elemento neutro: $a\cdot1=1\cdot a=a$;
- esistenza dell'inverso: per ogni $a\in X$ con $a\neq0$ esiste $a^{-1}\in X$ tale che $aa^{-1}=1$;

Prodotto e somma (SP):
- distributività: $a(b+c)=ab+ac$.

### Da dire all'orale

> Un campo è un insieme dotato di somma e prodotto commutativi e associativi, con elementi neutri, opposto per ogni elemento, inverso per ogni elemento non nullo e proprietà distributiva del prodotto rispetto alla somma.

## Notazione

- $0$ è l'elemento neutro della somma.
- $-a$ è l'opposto di $a$.
- $1$ è l'elemento neutro del prodotto.
- $a^{-1}$ è l'inverso moltiplicativo di $a$, definito soltanto quando $a\neq0$.
- La sottrazione è definita da $a-b=a+(-b)$.
- Per $b\neq0$, la divisione è definita da $\frac{a}{b}=ab^{-1}$.

## Condizioni

L'inverso moltiplicativo è richiesto soltanto per gli elementi non nulli. Lo zero non può avere inverso perché $0\cdot x=0$ per ogni $x$, quindi non può esistere un elemento $x$ tale che $0\cdot x=1$.

## Esempi

- $\mathbb{Q}$ è un campo: se $\frac{m}{n}\neq0$, il suo inverso è $\frac{n}{m}\in\mathbb{Q}$.
- $\mathbb{R}$ è un campo.
- $\mathbb{C}$ è un campo.
- $\mathbb{Z}$ non è un campo: per esempio, $2^{-1}=\frac12\notin\mathbb{Z}$.
- $\mathbb{N}$ non è un campo: per esempio, l'opposto di $3$ è $-3\notin\mathbb{N}$.

## Errori comuni

- Confondere l'opposto $-a$, che annulla $a$ rispetto alla somma, con l'inverso $a^{-1}$, che produce $1$ rispetto al prodotto.
- Affermare che $\mathbb{Z}$ non possiede gli opposti: ogni intero possiede il proprio opposto in $\mathbb{Z}$; mancano invece gli inversi moltiplicativi di molti elementi non nulli.
- Dimenticare la condizione $a\neq0$ nell'esistenza dell'inverso.

## Connessioni

- [[02 Numeri Interi|Gli interi]] possiedono gli opposti ma non tutti gli inversi moltiplicativi.
- [[03 Numeri Razionali|I razionali]] e [[06 Numeri Reali e Irrazionali|i reali]] sono campi.
- Il concetto di campo verrà completato dalla relazione d'ordine per definire i campi ordinati.

## Prospettiva d'esame

Quando si stabilisce se un insieme è un campo, bisogna verificare tutte le proprietà. Per mostrare che non lo è, basta individuare una proprietà che fallisce e fornire un esempio valido.
