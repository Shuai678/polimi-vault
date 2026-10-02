---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 05, PDF pp. 6-8
  - Libro, §2.3.4, pp. 46-51
---

# Funzioni monotone

## Significato intuitivo

La monotonia descrive come cambia l'uscita quando aumenta l'ingresso. Una funzione crescente conserva l'ordine; una funzione decrescente lo inverte.

Sia $f:A\to\mathbb R$, con $A\subseteq\mathbb R$.

## Le quattro definizioni

La funzione è **crescente** o **non decrescente** in $A$ se

$$
x_1<x_2
\quad\Longrightarrow\quad
f(x_1)\leq f(x_2)
$$

per ogni $x_1,x_2\in A$.

È **strettamente crescente** se

$$
x_1<x_2
\quad\Longrightarrow\quad
f(x_1)<f(x_2).
$$

È **decrescente** o **non crescente** se

$$
x_1<x_2
\quad\Longrightarrow\quad
f(x_1)\geq f(x_2).
$$

È **strettamente decrescente** se

$$
x_1<x_2
\quad\Longrightarrow\quad
f(x_1)>f(x_2).
$$

Una funzione che soddisfa una di queste proprietà si dice **monotona**; nei casi stretti si dice **strettamente monotona**.

![[62 Funzioni Monotone.svg|666]]

## Stretta e non stretta

Una funzione crescente può avere tratti costanti, perché è ammessa l'uguaglianza $f(x_1)=f(x_2)$. Una funzione strettamente crescente non può assumere lo stesso valore in due punti distinti.

Ogni funzione strettamente crescente è crescente, ma non vale il viceversa. Lo stesso vale nel caso decrescente.

### Da dire all'orale

> Una funzione crescente conserva le disuguaglianze tra gli argomenti; se è strettamente crescente conserva anche la loro stretta disuguaglianza. Una funzione decrescente inverte il verso.

## Attenzione ai domini non connessi

La funzione

$$
f(x)=\frac1x
$$

è strettamente decrescente su ciascuno degli intervalli $(-\infty,0)$ e $(0,+\infty)$, ma non sull'intero dominio

$$
(-\infty,0)\cup(0,+\infty).
$$

Infatti $-1<1$, ma

$$
f(-1)=-1<1=f(1),
$$

mentre una funzione decrescente dovrebbe soddisfare $f(-1)\geq f(1)$.

La monotonia si verifica confrontando **tutte** le coppie ordinate del dominio, anche se appartengono a componenti diverse.

## Caratterizzazione con il rapporto incrementale

Per $x_1\neq x_2$ definiamo il rapporto

$$
\frac{f(x_2)-f(x_1)}{x_2-x_1}.
$$

La funzione è crescente in $A$ se e solo se

$$
\frac{f(x_2)-f(x_1)}{x_2-x_1}\geq0
\qquad
\text{per ogni }x_1\neq x_2\text{ in }A.
$$

È decrescente se e solo se il rapporto è $\leq0$. Nei casi strettamente crescente e strettamente decrescente le disuguaglianze diventano rispettivamente $>0$ e $<0$.

### Perché la caratterizzazione funziona

Se $x_2>x_1$, il denominatore è positivo. Il segno del rapporto coincide quindi con quello di $f(x_2)-f(x_1)$ e traduce esattamente il confronto richiesto dalla definizione. Se gli indici sono scambiati, numeratore e denominatore cambiano entrambi segno e il quoziente resta invariato.

## Errori comuni

- Confondere crescente con strettamente crescente.
- Controllare soltanto punti vicini o appartenenti allo stesso intervallo del dominio.
- Credere che un salto renda automaticamente una funzione non monotona.
- Dimenticare che una funzione decrescente inverte il verso della disuguaglianza.
- Usare il segno del rapporto senza imporre $x_1\neq x_2$.
- Chiamare “rapporto incrementale” una derivata: qui si confrontano due punti distinti, senza alcun limite.

## Connessioni

- La monotonia si legge sul [[57 Grafico di una Funzione|grafico]] ma si dimostra con le disuguaglianze.
- La stretta monotonia implicherà [[65 Funzioni Iniettive e Biiettive|iniettività]].
- Il rapporto incrementale prepara il linguaggio delle derivate, senza ancora usarle.

## Prospettiva d'esame

Bisogna saper enunciare tutte e quattro le definizioni, distinguere i casi stretti, verificare la proprietà su tutto il dominio e usare correttamente la caratterizzazione tramite il rapporto incrementale.
