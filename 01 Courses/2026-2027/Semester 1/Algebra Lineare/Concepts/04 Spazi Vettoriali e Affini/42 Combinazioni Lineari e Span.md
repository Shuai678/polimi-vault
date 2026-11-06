---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 13, PDF pp. 2-4, stampate 109-111"
---

# Combinazioni lineari e span

Stato: **da studiare**.

## Intuizione

Da alcuni vettori di partenza possiamo costruirne altri, sommandoli dopo averli moltiplicati per scalari. Lo **span** raccoglie tutti i vettori ottenibili, non soltanto quelli iniziali.

Gli oggetti possono essere frecce, colonne, matrici, funzioni o polinomi. Si usano sempre le operazioni dello [[38 Spazi Vettoriali e Assiomi|spazio vettoriale]] considerato.

## Definizione 13.1

Siano $V$ uno spazio vettoriale su $\mathbb K$ e $v_1,\ldots,v_s\in V$. Una combinazione lineare è un vettore della forma

$$
\lambda_1v_1+\cdots+\lambda_sv_s,
\qquad \lambda_1,\ldots,\lambda_s\in\mathbb K.
$$

I $\lambda_i$ sono scalari; ogni $\lambda_iv_i$ e la somma finale sono vettori di $V$.

Il sottospazio generato è

$$
\boxed{
\operatorname{Span}(v_1,\ldots,v_s)
=\left\{\sum_{i=1}^{s}\lambda_iv_i:\lambda_i\in\mathbb K\right\}.
}
$$

Il professore usa la notazione $\operatorname{Span}$. Non si confonde l'insieme finito $\{v_1,\ldots,v_s\}$ con l'insieme di tutte le sue combinazioni.

## Perché è un sottospazio

Dimostrazione esplicitata dal tutor del passaggio della p. 2.

Ponendo tutti i coefficienti uguali a zero, otteniamo $0_V$. Se

$$
u=\sum_i\alpha_iv_i,\qquad w=\sum_i\beta_iv_i,
$$

allora per distributività

$$
u+w=\sum_i(\alpha_i+\beta_i)v_i,\qquad
\mu u=\sum_i(\mu\alpha_i)v_i.
$$

Le nuove espressioni sono ancora combinazioni degli stessi vettori. Lo span contiene lo zero ed è chiuso per somma e prodotto per scalare: vale il [[41 Sottospazi Vettoriali e Criterio di Chiusura|criterio di sottospazio]].

## Significato geometrico

- Un vettore non nullo $v\in\mathbb R^2$ genera la retta per l'origine $\{tv:t\in\mathbb R\}$.
- Due vettori non collineari del piano generano tutto $\mathbb R^2$.
- Due vettori non collineari nello spazio generano un piano per l'origine.
- Se tutti i vettori sono nulli, lo span è $\{0\}$.

![[42 Span di una Retta e del Piano.svg|1040]]

**Figura del tutor, in scala:** a sinistra $v=(1,1)$ e $2v=(2,2)$ generano la stessa retta. A destra $v_1=(1,0)$ e $v_2=(0,1)$ generano tutto il piano; il punto $(2,1)$ è $2v_1+v_2$. Il riquadro mostra una finestra finita, non limita lo span ai punti disegnati.

Uno span è sempre vettoriale e contiene l'origine. Una retta affine che non passa per l'origine non è lo span dei propri vettori direzione: è una **traslazione** di quello span.

## Esempi della lezione

### Polinomi di grado al massimo $d$

Ogni $p(t)=a_0+a_1t+\cdots+a_dt^d$ è una combinazione di $1,t,\ldots,t^d$, quindi

$$
\mathbb K[t]_{\le d}=\operatorname{Span}(1,t,\ldots,t^d).
$$

L'inclusione opposta vale perché una combinazione di quei monomi non contiene potenze maggiori di $d$. L'uguaglianza richiede entrambe le inclusioni.

### Nucleo

La parametrizzazione di Gauss dell'omogeneo $Ax=0$ dà

$$
\ker(A)=\operatorname{Span}(h_1,\ldots,h_{n-r(A)}).
$$

Questi vettori generano il **nucleo**, non necessariamente tutto $\mathbb K^n$.

Per esempio $\ker\begin{pmatrix}1&-1\end{pmatrix}=\operatorname{Span}((1,1))$ è una retta propria di $\mathbb R^2$.

## Proprietà utili negli esercizi

Se un sottospazio $H$ contiene tutti i $v_i$, per chiusura contiene ogni loro combinazione. Quindi

$$
\operatorname{Span}(v_1,\ldots,v_s)\subseteq H.
$$

Lo span è il più piccolo sottospazio che contiene i vettori dati, nel senso dell'inclusione.

Se $w\in\operatorname{Span}(v_1,\ldots,v_s)$, aggiungerlo non amplia lo span:

$$
\operatorname{Span}(v_1,\ldots,v_s,w)=\operatorname{Span}(v_1,\ldots,v_s).
$$

Infatti una combinazione che coinvolge $w$ può essere riscritta sostituendo la sua espressione tramite i $v_i$.

Per convenzione, integrazione del tutor, $\operatorname{Span}(\varnothing)=\{0\}$: la somma vuota vale zero. Sarà utile per lo spazio nullo.

## Da dire all'orale

> Lo span di una famiglia di vettori è l'insieme di tutte le loro combinazioni lineari. È un sottospazio perché contiene lo zero ed è chiuso rispetto a somma e prodotto per scalare.

## Collegamenti e fonte

- [[43 Generatori e Sistemi Lineari]], [[44 Dipendenza e Indipendenza Lineare]], [[45 Basi e Unicità delle Coordinate]].
- [[10 Combinazioni Generatori Indipendenza e Basi]].
- [[GAL 2026-2027 - 20261019 - LEZIONE 13.pdf#page=2|Lezione 13, pp. 2-4, stampate 109-111]].
