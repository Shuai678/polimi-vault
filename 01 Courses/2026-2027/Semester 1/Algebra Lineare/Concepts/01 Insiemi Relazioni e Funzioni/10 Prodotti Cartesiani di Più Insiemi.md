---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 1, PDF pp. 9-10, pagine stampate 19-20"
---

# Prodotti cartesiani di più insiemi

Stato: **da studiare**.

## Dalle coppie alle terne

Per tre insiemi $A,B,C$ si definisce

$$
A\times B\times C
=\{(a,b,c)\mid a\in A,\ b\in B,\ c\in C\}.
$$

Gli elementi sono terne ordinate: l'ordine e l'appartenenza di ciascuna componente fanno parte della definizione.

Il caso geometrico è

$$
\mathbb R^3
=\mathbb R\times\mathbb R\times\mathbb R
=\{(x,y,z)\mid x,y,z\in\mathbb R\}.
$$

Fissato un riferimento nello spazio, le tre coordinate individuano un punto.

## Costruzione mediante coppie

Si può procedere usando soltanto il prodotto tra due insiemi:

1. si costruisce $S=A\times B$;
2. si costruisce $S\times C$;
3. si ottiene $(A\times B)\times C$.

Un elemento di questo insieme ha la forma

$$
((a,b),c).
$$

È una coppia il cui primo elemento è a sua volta una coppia. La scrittura è diversa dalla terna $(a,b,c)$.

## La biiezione naturale

Il professore introduce

$$
\begin{aligned}
\Phi:(A\times B)\times C&\longrightarrow A\times B\times C,\\
((a,b),c)&\longmapsto(a,b,c).
\end{aligned}
$$

### È ben definita

Se $((a,b),c)$ appartiene al dominio, allora $a\in A$, $b\in B$, $c\in C$. Quindi $(a,b,c)$ appartiene al codominio.

### È iniettiva

Se due immagini coincidono, allora

$$
(a,b,c)=(a',b',c').
$$

Per uguaglianza componente per componente, $a=a'$, $b=b'$ e $c=c'$. Dunque anche $((a,b),c)=((a',b'),c')$.

### È suriettiva

Ogni terna $(a,b,c)$ nel codominio è l'immagine della coppia $((a,b),c)$, che appartiene al dominio.

Quindi $\Phi$ è [[09 Biiettività|biiettiva]]. Le due costruzioni contengono la stessa informazione, pur mantenendo una diversa forma degli elementi.

## Estensione

Per un numero finito $n$ di insiemi si considerano liste ordinate:

$$
A_1\times\cdots\times A_n
=\{(a_1,\ldots,a_n)\mid a_i\in A_i
\text{ per }i=1,\ldots,n\}.
$$

Quando tutti gli insiemi sono $\mathbb K$, si scrive $\mathbb K^n$. Questa notazione ricompare nei vettori riga e colonna della [[11 Matrici come Funzioni e Indici|Lezione 3]].

## Da dire all'orale

> Il prodotto cartesiano di tre insiemi contiene le terne ordinate con una componente in ciascun insieme. La corrispondenza che elimina le parentesi interne è una biiezione tra coppie annidate e terne.

## Collegamenti e fonte

- Prerequisiti: [[01 Prodotto Cartesiano]] e [[09 Biiettività]].
- Fonte: [[GAL 2026-2027 - 20260917 - LEZIONE 1.pdf#page=9|Lezione 1, pp. 9-10, stampate 19-20]]. Le verifiche della biiezione sono esplicitate dal tutor.
