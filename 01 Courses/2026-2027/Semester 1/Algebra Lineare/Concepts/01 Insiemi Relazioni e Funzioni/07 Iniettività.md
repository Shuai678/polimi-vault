---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 1, PDF pp. 7-8, pagine stampate 17-18"
---

# Iniettività

Stato: **da studiare**.

## Intuizione e definizione 1.2

Una funzione è iniettiva quando due elementi diversi del dominio non hanno la stessa immagine.

Sia $F:A\to B$ una [[05 Funzioni|funzione]]. Si dice **iniettiva** se

$$
\forall a_1,a_2\in A,\qquad
F(a_1)=F(a_2)\implies a_1=a_2.
$$

In termini di coppie: se $(a_1,b)\in F$ e $(a_2,b)\in F$, allora $a_1=a_2$.

Per [[06 Implicazione e Contrapposizione|contrapposizione]], la condizione equivale a

$$
a_1\ne a_2\implies F(a_1)\ne F(a_2).
$$

## Interpretazione con frecce

![[07 Funzioni Iniettive Suriettive e Biiettive.svg|1000]]

Gli schemi del tutor rappresentano insiemi finiti, senza una scala geometrica. In ogni pannello parte esattamente una freccia da ogni elemento del dominio.

Nei pannelli «iniettiva, non suriettiva» e «biiettiva» non arrivano due frecce allo stesso elemento del codominio. Questa è l'iniettività. Possono rimanere elementi del codominio non raggiunti.

## Esempio del professore

La funzione che assegna a un frutto la sua iniziale non è iniettiva quando il dominio contiene limone e lampone:

$$
F(\text{limone})=l=F(\text{lampone}),
\qquad
\text{limone}\ne\text{lampone}.
$$

Questo è un controesempio alla condizione universale.

## Esempio con dimostrazione del tutor

Consideriamo $f:\mathbb R\to\mathbb R$ definita da $f(x)=2x+1$.

Supponiamo $f(x_1)=f(x_2)$. Allora

$$
\begin{aligned}
2x_1+1&=2x_2+1,\\
2x_1&=2x_2 &&\text{sottraendo }1,\\
x_1&=x_2 &&\text{dividendo per }2\ne0.
\end{aligned}
$$

Quindi $f$ è iniettiva.

## Distinzione essenziale

Nella definizione di funzione, a ogni ingresso corrisponde un solo valore. Nell'iniettività, un valore di arrivo può provenire da al massimo un ingresso.

Una funzione può non essere iniettiva; una relazione con due uscite distinte dallo stesso ingresso non è neppure una funzione.

## Da dire all'orale

> Una funzione è iniettiva se l'uguaglianza delle immagini di due elementi implica l'uguaglianza degli elementi stessi.

## Collegamenti e fonte

- [[08 Suriettività]] e [[09 Biiettività]].
- Esempi svolti: [[02 Esempi Svolti sulle Funzioni]].
- Fonte: [[GAL 2026-2027 - 20260917 - LEZIONE 1.pdf#page=7|Lezione 1, pp. 7-8, stampate 17-18]].
