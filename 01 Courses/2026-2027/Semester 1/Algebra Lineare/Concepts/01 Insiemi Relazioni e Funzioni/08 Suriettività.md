---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 1, PDF pp. 7-8, pagine stampate 17-18"
---

# Suriettività

Stato: **da studiare**.

## Intuizione e definizione

Una [[05 Funzioni|funzione]] $F:A\to B$ è **suriettiva** quando ogni elemento del codominio è immagine di almeno un elemento del dominio:

$$
\forall b\in B,\quad \exists a\in A:\ F(a)=b.
$$

L'elemento $a$ può dipendere da $b$. Per uno stesso $b$ possono esistere più ingressi: la suriettività non richiede unicità.

Nel disegno [[07 Funzioni Iniettive Suriettive e Biiettive.svg|delle funzioni con frecce]], i pannelli suriettivi sono quelli in cui ogni punto di $B$ viene raggiunto.

## Immagine e controimmagini

Definiamo

$$
\operatorname{Im}F=\{F(a)\mid a\in A\}\subseteq B.
$$

La suriettività equivale a $\operatorname{Im}F=B$.

Nel PDF si usa anche

$$
F^{-1}(b)=\{a\in A\mid F(a)=b\},
$$

cioè l'insieme delle controimmagini di $b$. Più esplicitamente si può scrivere $F^{-1}(\{b\})$. Non si sta assumendo che esista una funzione inversa.

Quindi:

$$
F\text{ suriettiva}
\iff
\forall b\in B,\ F^{-1}(\{b\})\ne\varnothing.
$$

## Esempio del professore

Per la funzione iniziale dei frutti

$$
A=\{\text{ananas},\text{banana},\text{limone},\text{lampone}\},
\qquad B=\{a,b,l\},
$$

ogni elemento di $B$ è raggiunto: $a$ da ananas, $b$ da banana e $l$ da limone e lampone. La funzione è suriettiva, pur non essendo iniettiva.

## Il codominio conta

Esempio del tutor:

$$
f:\mathbb R\to\mathbb R,\qquad f(x)=x^2.
$$

Non è suriettiva: il numero $-1$ appartiene al codominio ma non è il quadrato di un reale.

Con la stessa formula e lo stesso dominio, ma codominio $[0,+\infty)$:

$$
g:\mathbb R\to[0,+\infty),\qquad g(x)=x^2,
$$

la funzione è suriettiva. Per ogni $y\ge0$ si può scegliere $x=\sqrt y$, ottenendo $g(x)=y$.

## Metodo

Per dimostrare la suriettività si prende un elemento arbitrario $b$ del codominio e si trova almeno un ingresso ammissibile $a$ con $F(a)=b$.

Per confutarla basta un elemento del codominio privo di controimmagini.

## Da dire all'orale

> Una funzione è suriettiva se ogni elemento del codominio è immagine di almeno un elemento del dominio.

## Collegamenti e fonte

- [[07 Iniettività]] e [[09 Biiettività]].
- [[02 Esempi Svolti sulle Funzioni]].
- Fonte: [[GAL 2026-2027 - 20260917 - LEZIONE 1.pdf#page=7|Lezione 1, pp. 7-8, stampate 17-18]]. Il confronto tra i due codomini è un'integrazione del tutor.
