---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 05, PDF p. 5
  - Libro, §2.3.3, pp. 45-46
---

# Funzioni pari e dispari

## Prima condizione: dominio simmetrico

Per parlare di parità o disparità, il dominio $A\subseteq\mathbb R$ deve essere simmetrico rispetto a zero:

$$
x\in A\quad\Longrightarrow\quad -x\in A.
$$

Gli intervalli $(-a,a)$, compreso il caso $a=+\infty$, hanno questa proprietà. Senza simmetria del dominio, il confronto tra $f(x)$ e $f(-x)$ non è disponibile per tutti i punti.

## Funzione pari

La funzione $f:A\to\mathbb R$ è **pari** se

$$
f(-x)=f(x)
\qquad\text{per ogni }x\in A.
$$

Il suo grafico è simmetrico rispetto all'asse delle ordinate. Conoscendo il grafico per $x\geq0$, la parte per $x\leq0$ si ottiene per riflessione rispetto all'asse $y$.

Esempi:

$$
x^2,\quad x^4,\quad x^6,\quad \cos x.
$$

## Funzione dispari

La funzione $f:A\to\mathbb R$ è **dispari** se

$$
f(-x)=-f(x)
\qquad\text{per ogni }x\in A.
$$

Il suo grafico è simmetrico rispetto all'origine. La simmetria trasforma il punto $(x,f(x))$ nel punto $(-x,-f(x))$.

Esempi:

$$
x,\quad x^3,\quad x^5,\quad \sin x.
$$

![[61 Funzioni Pari e Dispari.svg|700]]

### Da dire all'orale

> Una funzione pari ha dominio simmetrico e soddisfa $f(-x)=f(x)$; il grafico è simmetrico rispetto all'asse $y$. Una funzione dispari soddisfa $f(-x)=-f(x)$; il grafico è simmetrico rispetto all'origine.

## Come verificare la proprietà

1. Controllare che $D(f)$ sia simmetrico rispetto a zero.
2. Calcolare $f(-x)$ senza semplificare mentalmente i segni.
3. Confrontare il risultato con $f(x)$ e con $-f(x)$.
4. Se non coincide con nessuno dei due per ogni $x$, la funzione non è né pari né dispari.

Per esempio, se $f(x)=x^3+x$, allora

$$
f(-x)=(-x)^3+(-x)=-x^3-x=-f(x),
$$

quindi $f$ è dispari.

## Osservazione

La funzione identicamente nulla è sia pari sia dispari. Per una funzione non nulla, le due proprietà non possono valere contemporaneamente.

## Errori comuni

- Omettere il controllo sulla simmetria del dominio.
- Confondere $f(-x)$ con $-f(x)$.
- Affermare che una funzione è dispari solo perché il suo grafico attraversa l'origine.
- Controllare l'uguaglianza soltanto in alcuni punti anziché per ogni $x$ del dominio.
- Confondere la simmetria rispetto all'origine con quella rispetto all'asse $x$.

## Connessioni

- La proprietà si legge sul [[57 Grafico di una Funzione|grafico]].
- Usa sostituzione e controllo del [[60 Dominio Naturale di una Funzione|dominio naturale]].

## Prospettiva d'esame

La verifica algebrica deve includere dominio, calcolo di $f(-x)$ e conclusione. La sola impressione visiva del grafico non sostituisce la dimostrazione.
