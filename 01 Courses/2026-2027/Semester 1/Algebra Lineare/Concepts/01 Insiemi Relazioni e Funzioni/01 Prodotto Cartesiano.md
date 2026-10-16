---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 0, PDF pp. 6-8"
---

# Prodotto cartesiano

Stato: **da studiare**.

## Intuizione

Il prodotto cartesiano raccoglie tutte le possibilità di scegliere un primo elemento da un insieme e un secondo elemento da un altro insieme. Si conservano sia le scelte sia il loro ordine.

Per esempio, con $A=\{1,2\}$ e $B=\{3,4\}$:

$$
A\times B=\{(1,3),(1,4),(2,3),(2,4)\}.
$$

Fissando il primo elemento $1$ si ottengono le coppie $(1,3)$ e $(1,4)$; fissando $2$ si ottengono $(2,3)$ e $(2,4)$.

## Definizione 0.1

Dati due insiemi $A$ e $B$, il loro **prodotto cartesiano** è

$$
A\times B=\{(a,b)\mid a\in A,\ b\in B\}.
$$

- $(a,b)$ è una coppia ordinata.
- $a\in A$ significa che il primo elemento appartiene ad $A$.
- $b\in B$ significa che il secondo elemento appartiene a $B$.
- La barra verticale si legge «tale che».

Due coppie sono uguali esattamente quando coincidono le componenti nelle rispettive posizioni:

$$
(a,b)=(c,d)\iff a=c\ \text{e}\ b=d.
$$

## Rappresentazione geometrica

![[01 Prodotto Cartesiano.svg|940]]

Il disegno del tutor è in scala. I punti blu rappresentano $A\times B$; quelli arancioni rappresentano $B\times A$. Ogni prodotto contiene soltanto i quattro punti indicati.

In generale $A\times B$ e $B\times A$ sono diversi. Nell'esempio $(1,3)\in A\times B$, mentre $(1,3)\notin B\times A$. Anche quando entrambe le coppie appartengono allo stesso prodotto, $(a,b)$ e $(b,a)$ sono uguali soltanto se $a=b$.

### Il piano cartesiano

Il professore considera

$$
\mathbb R^2=\mathbb R\times\mathbb R.
$$

Fissato un riferimento cartesiano, a ogni punto corrisponde una coppia di coordinate reali. I punti $P=(2,4)$ e $Q=(4,2)$ sono distinti: cambiano ascissa e ordinata.

## Esempi della lezione

### Coppie di valutazioni

A p. 7 il primo insieme rappresenta i voti della parte di esercizi, il secondo quelli della teoria. La coppia $(28,22)$ conserva questo ordine:

$$
\frac7{10}\cdot28+\frac3{10}\cdot22=19{,}6+6{,}6=26{,}2.
$$

Scambiando i voti si ottiene invece:

$$
\frac7{10}\cdot22+\frac3{10}\cdot28=15{,}4+8{,}4=23{,}8.
$$

Il ruolo delle posizioni cambia il significato della coppia e il risultato della media.

### Moneta e dado

Con $M=\{T,C\}$ e $D=\{1,2,3,4,5,6\}$:

$$
M\times D=
\{(T,1),\ldots,(T,6),(C,1),\ldots,(C,6)\}.
$$

Sono dodici esiti ordinati. Questa enumerazione da sola non assegna probabilità agli esiti.

## Due conseguenze della definizione

Le seguenti osservazioni sono integrazioni del tutor.

Se uno dei due insiemi è vuoto, non si può scegliere una coppia:

$$
A\times\varnothing=\varnothing,\qquad
\varnothing\times B=\varnothing.
$$

Se $A$ e $B$ sono finiti e contengono rispettivamente $m$ e $n$ elementi, per ciascuno dei $m$ primi elementi esistono $n$ seconde scelte:

$$
\#(A\times B)=mn.
$$

Il simbolo $\#$ indica il numero di elementi di un insieme finito.

## Errori da evitare

- Confondere $(a,b)$ con l'insieme $\{a,b\}$: nell'insieme l'ordine non conta.
- Controllare soltanto una delle due condizioni di appartenenza.
- Interpretare il simbolo $\times$ come una moltiplicazione fra gli elementi.
- Colorare un'intera regione quando il prodotto contiene solo punti isolati.

## Da dire all'orale

> Il prodotto cartesiano di due insiemi è l'insieme delle coppie ordinate con primo elemento nel primo insieme e secondo elemento nel secondo insieme.

## Collegamenti e fonte

- Una selezione di coppie forma una [[02 Relazioni Binarie|relazione binaria]].
- Estensione: [[10 Prodotti Cartesiani di Più Insiemi]].
- Applicazione: [[11 Matrici come Funzioni e Indici]].
- Esempi svolti: [[01 Prodotti Cartesiani e Relazioni]].
- Fonte: [[GAL 2026-2027 - 20260916 - LEZIONE 0.pdf#page=6|Lezione 0, pp. 6-8]]; definizione 0.1 ed esempi 1-4.
