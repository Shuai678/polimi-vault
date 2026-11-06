---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 13, PDF pp. 3-6, stampate 110-113"
---

# Generatori e sistemi lineari

Stato: **da studiare**.

## Definizione 13.2

Una famiglia $v_1,\ldots,v_s\in V$ è un insieme di **generatori di $V$** se

$$
\boxed{V=\operatorname{Span}(v_1,\ldots,v_s).}
$$

Poiché le combinazioni appartengono sempre a $V$, per verificare l'uguaglianza bisogna dimostrare che **ogni** elemento di $V$ è ottenibile come combinazione dei vettori dati.

«Generatori» è una proprietà relativa all'ambiente. Un vettore non nullo genera la propria retta, ma non genera tutto $\mathbb R^3$.

## Appartenenza allo span come sistema

Per colonne $v_i\in\mathbb K^m$, formiamo

$$
A=[v_1\mid\cdots\mid v_s]\in M_{\mathbb K}(m,s).
$$

Per un vettore fissato $b$:

$$
b\in\operatorname{Span}(v_1,\ldots,v_s)
\iff
\exists\lambda\in\mathbb K^s:A\lambda=b.
$$

È la [[30 Sistemi Lineari e Rappresentazioni Matriciali|rappresentazione del I tipo]] di un sistema. I coefficienti della combinazione sono le incognite.

Per [[32 Teorema di Rouché-Capelli|Rouché-Capelli]]:

$$
b\in\operatorname{Span}(v_1,\ldots,v_s)
\iff r(A)=r([A\mid b]).
$$

Per generare **tutto** $\mathbb K^m$, serve che il sistema sia risolubile per ogni $b$. Il criterio è

$$
\boxed{\operatorname{Span}(v_1,\ldots,v_s)=\mathbb K^m\iff r(A)=m.}
$$

Se il rango è $m$, la completa non può avere rango maggiore del numero di righe, quindi è sempre compatibile. Viceversa, se $r(A)<m$, dopo Gauss c'è una riga nulla dei coefficienti; scegliendo un termine noto trasformato non nullo in quella posizione, e tornando indietro con la trasformazione invertibile, si costruisce un $b$ incompatibile.

## Esempio del professore

Nella Lezione 13:

$$
v_1=\begin{pmatrix}1\\0\\0\end{pmatrix},\quad
v_2=\begin{pmatrix}-2\\1\\0\end{pmatrix},\quad
v_3=\begin{pmatrix}0\\1\\1\end{pmatrix},\quad
v_4=\begin{pmatrix}1\\-1\\2\end{pmatrix}.
$$

Per un vettore arbitrario $b=(a,b_2,c)^{\mathsf T}$ il sistema è

$$
\begin{bmatrix}
1&-2&0&1&a\\
0&1&1&-1&b_2\\
0&0&1&2&c
\end{bmatrix}.
$$

I tre pivot dei coefficienti garantiscono il rango massimo 3, qualunque sia il termine noto. I quattro vettori generano $\mathbb R^3$.

Esplicitazione del tutor: ponendo $\lambda_4=t$, si ricava dal basso

$$
\lambda_3=c-2t,\qquad
\lambda_2=b_2-c+3t,\qquad
\lambda_1=a+2b_2-2c+5t.
$$

Pertanto ogni $b$ ha le rappresentazioni

$$
b=(a+2b_2-2c)v_1+(b_2-c)v_2+cv_3
+t(5v_1+3v_2-2v_3+v_4).
$$

L'ultimo vettore fra parentesi è nullo. Le rappresentazioni sono molteplici perché i generatori sono ridondanti, non perché descrivano vettori diversi.

Per $b=(0,1,3)^{\mathsf T}$ il PDF mostra

$$
b=v_1+v_2+v_3+v_4
=6v_1+4v_2-v_3+2v_4.
$$

I due insiemi di coefficienti differiscono per $(5,3,-2,1)$, una relazione fra i generatori.

## Polinomi e matrici

I monomi $1,t,\ldots,t^d$ generano $\mathbb K[t]_{\le d}$. Le matrici elementari $E_{ij}$ generano $M_{\mathbb K}(m,n)$ perché

$$
A=\sum_{i=1}^{m}\sum_{j=1}^{n}a_{ij}E_{ij}.
$$

Prima di usare un sistema numerico per polinomi o matrici, si confrontano rispettivamente i coefficienti dei monomi o le entrate delle matrici: le uguaglianze vettoriali diventano uguaglianze scalari.

## Errori da evitare

- Verificare che un solo vettore appartenga allo span non prova che i dati generino l'intero spazio.
- Un insieme di generatori non deve necessariamente essere indipendente.
- Avere quattro vettori in $\mathbb R^3$ non impedisce di generare $\mathbb R^3$: impedisce invece l'indipendenza.
- I vettori che generano un nucleo non generano automaticamente tutto lo spazio ambiente.

## Da dire all'orale

> Una famiglia genera uno spazio se ogni vettore dello spazio si scrive come sua combinazione lineare. Per colonne di altezza $m$, i generatori coprono tutto $\mathbb K^m$ esattamente quando la matrice che le affianca ha rango $m$.

## Collegamenti e fonte

- [[42 Combinazioni Lineari e Span]], [[44 Dipendenza e Indipendenza Lineare]], [[48 Estrazione di una Base con Gauss]].
- [[GAL 2026-2027 - 20261019 - LEZIONE 13.pdf#page=3|Lezione 13, pp. 3-6, stampate 110-113]].
