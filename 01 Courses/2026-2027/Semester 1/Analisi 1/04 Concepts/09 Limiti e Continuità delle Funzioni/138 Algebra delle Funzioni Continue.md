---
course: Analisi 1
type: concept
status: Da studiare
updated: 2026-11-06
source:
  - Lezione 15, PDF pp. 2-3
  - Libro, §5.6, pp. 148-149, condizioni sulle operazioni
---

# Algebra delle funzioni continue

## Teorema del docente

Siano $f$ e $g$ continue in $x_0\in\mathbb R$, punto del loro dominio comune e di accumulazione per esso. Quindi

$$
\lim_{x\to x_0}f(x)=f(x_0),\qquad
\lim_{x\to x_0}g(x)=g(x_0).
$$

Il professore elenca le conseguenze nel seguente ordine.

### 1. Somma e differenza

$$
\lim_{x\to x_0}(f(x)\pm g(x))=f(x_0)\pm g(x_0).
$$

Perciò $f\pm g$ è continua in $x_0$.

### 2. Prodotto

$$
\lim_{x\to x_0}f(x)g(x)=f(x_0)g(x_0).
$$

Perciò $fg$ è continua in $x_0$.

### 3. Quoziente

Se $g(x_0)\neq0$,

$$
\lim_{x\to x_0}\frac{f(x)}{g(x)}=\frac{f(x_0)}{g(x_0)}.
$$

Perciò $f/g$ è continua in $x_0$.

### 4. Potenza con esponente reale fissato

Per $\alpha\in\mathbb R$, se $(f(x))^\alpha$ è ben definita in un intorno di $x_0$, compreso il punto nel quale ne studiamo la continuità,

$$
\lim_{x\to x_0}(f(x))^\alpha=(f(x_0))^\alpha.
$$

Perciò $f^\alpha$ è continua in $x_0$.

## Dimostrazione del professore

Segue dal teorema sull'algebra dei limiti, perché esistono finiti

$$
\ell_1=\lim_{x\to x_0}f(x)=f(x_0)\in\mathbb R,
$$

$$
\ell_2=\lim_{x\to x_0}g(x)=g(x_0)\in\mathbb R.
$$

$\square$

## Commenti alla dimostrazione e alle ipotesi

La prova breve è quella del PDF: si applica [[137 Algebra dei Limiti di Funzioni]] ai limiti finiti forniti dalla [[130 Continuità di una Funzione|continuità]]. La conclusione si riconosce confrontando il limite dell'operazione con il suo valore in $x_0$.

Nel quoziente, dalla continuità di $g$ e da $g(x_0)\neq0$ segue, per [[136 Permanenza del Segno per Funzioni]], che $g(x)$ rimane non nulla vicino a $x_0$. Il quoziente è quindi effettivamente definito nella zona necessaria.

Nella potenza, la condizione sul dominio non si può omettere. Per esponenti interi positivi non occorrono restrizioni di segno; per esponenti negativi la base deve essere non nulla; per una radice di indice pari la base deve essere non negativa. Una condizione sufficiente per un qualsiasi esponente reale fissato è la positività della base. Il caso $\alpha=0$ richiede di tenere conto del dominio della potenza, senza assegnare arbitrariamente un significato a $0^0$.

## Esempio di supporto svolto

Consideriamo

$$
h(x)=\frac{x^2+1}{x^2+2}.
$$

Le funzioni $x\mapsto x$ e le costanti sono continue: il loro limite nel punto coincide con il valore. Prodotti e somme mostrano quindi la continuità di numeratore e denominatore. Inoltre $x^2+2\geq2>0$ per ogni reale. Il quoziente è continuo su $\mathbb R$ e, per esempio,

$$
\lim_{x\to2}\frac{x^2+1}{x^2+2}
=\frac{2^2+1}{2^2+2}=\frac56.
$$

La sostituzione diretta è la conclusione del teorema, dopo il controllo delle ipotesi.

## Uso negli esercizi ed errori comuni

Per una formula ottenuta con operazioni algebriche, individuare le funzioni di partenza, le operazioni usate e i punti nei quali il dominio impone restrizioni. Non dedurre la continuità di un quoziente in un punto dove il denominatore vale zero. Non confondere questa algebra con la [[139 Cambio di Variabile nei Limiti e Continuità della Composta|composizione]], che è il risultato successivo del docente.

### Da dire all'orale

> Somma, differenza e prodotto di due funzioni continue in un punto sono continui nel punto. Lo è anche il quoziente se il denominatore nel punto è diverso da zero. Una potenza con esponente reale fissato conserva la continuità quando è ben definita vicino al punto e nel punto. La prova applica l'algebra dei limiti ai limiti finiti delle due funzioni.
