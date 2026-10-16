---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 11, PDF pp. 2-5, stampate 97-100"
---

# Rette e piani tra parametri e vincoli

Stato: **da studiare**.

## Punti, vettori e coordinate

Un punto $P$ indica una posizione. Un vettore $v$ indica uno spostamento. Fissato un riferimento, entrambi sono rappresentati da colonne, ma hanno ruoli diversi:

$$
x=P+tv
$$

significa: partire dal punto $P$ e aggiungere lo spostamento $tv$.

## Retta parametrica

$$
\boxed{\ell=\{P+tv:t\in\mathbb R\},\qquad v\ne0.}
$$

$P\in\mathbb R^n$ è un punto della retta; $v\in\mathbb R^n$ è un vettore direzione non nullo; $t$ è un parametro scalare. Se $v=0$, la formula descrive solo un punto e non una retta.

Una retta ha un parametro libero effettivo. Per Rouché-Capelli, una rappresentazione cartesiana non ridondante in $\mathbb R^n$ ha rango

$$
r=n-1.
$$

- In $\mathbb R^2$: una equazione cartesiana non banale.
- In $\mathbb R^3$: due equazioni non ridondanti.
- In $\mathbb R^n$: $n-1$ vincoli lineari non ridondanti.

## Esempio nel piano, del tutor

$$
P=(1,2),\qquad v=(2,-1).
$$

Le equazioni parametriche sono $x=1+2t$, $y=2-t$. Dalla seconda $t=2-y$:

$$
x=1+2(2-y)=5-2y,
\qquad\boxed{x+2y=5}.
$$

Viceversa, da $x+2y=5$ si sceglie $t=2-y$ e si ritrovano entrambe le equazioni parametriche. Il passaggio è quindi equivalente, non soltanto necessario.

## Retta nello spazio e conversione senza divisioni rischiose

Per

$$
\ell=\{(1,1,0)+t(-1,0,1):t\in\mathbb R\}
$$

la coordinata $y$ è costante e il vettore direzione ha componente $y$ nulla. Non si scrive un rapporto con denominatore zero. Si usa invece

$$
\boxed{\begin{cases}y=1,\\x+z=1.\end{cases}}
$$

Il rango della matrice dei coefficienti è 2 e rimane un parametro. Due equazioni proporzionali non basterebbero a isolare una retta nello spazio.

## Piano parametrico

$$
\boxed{\pi=\{P+sv+tw:s,t\in\mathbb R\}.}
$$

Per descrivere davvero un piano, $v$ e $w$ devono fornire due direzioni indipendenti: l'uguaglianza $\alpha v+\beta w=0$ deve implicare $\alpha=\beta=0$.

Se $w=2v$, i due simboli $s,t$ entrano solo nella combinazione $s+2t$: l'insieme è una retta, non un piano. Scrivere due parametri non basta a garantire due gradi di libertà.

Un piano in $\mathbb R^n$, per $n\ge2$, ha rango cartesiano $n-2$:

- in $\mathbb R^3$: una equazione non banale;
- in $\mathbb R^2$: è tutto il piano ambiente, senza vincoli non banali;
- in $\mathbb R^n$: $n-2$ vincoli lineari non ridondanti.

## Esempio di piano nello spazio, del tutor

$$
P=\begin{pmatrix}0\\0\\1\end{pmatrix},\qquad
v=\begin{pmatrix}1\\0\\1\end{pmatrix},\qquad
w=\begin{pmatrix}0\\1\\-1\end{pmatrix}.
$$

Dalle coordinate $x=s$, $y=t$, $z=1+s-t$ si elimina $s,t$:

$$
\boxed{-x+y+z=1.}
$$

Le prime due coordinate di $\alpha v+\beta w=0$ danno $\alpha=\beta=0$, quindi le direzioni sono indipendenti.

Viceversa, se $-x+y+z=1$, scegliendo $s=x$ e $t=y$ si ricostruisce il punto. La matrice $A=\begin{pmatrix}-1&1&1\end{pmatrix}$ ha rango 1, dunque tre incognite meno un vincolo danno due parametri.

![[37 Retta e Piano nello Spazio.svg|1040]]

**Figura del tutor:** sono rappresentati la retta e il piano degli esempi. La proiezione obliqua è dichiaratamente schematica, non conserva angoli o lunghezze dello spazio. Le coordinate etichettate e le combinazioni sono esatte. La porzione colorata del piano è solo una finestra: i parametri non sono limitati al parallelogramma disegnato.

Nel pannello del piano, $Q=P+v+w=(1,1,1)$ soddisfa $-1+1+1=1$.

## Passaggio per l'origine

Una retta o un piano che passa per l'origine può essere scritto con $P=0$.

Anche se una rappresentazione usa inizialmente $P\ne0$, l'insieme può contenere lo zero. Per esempio $(1,0)+t(1,0)$ è l'asse $x$: scegliendo $t=-1$ si ottiene l'origine. Non si giudica l'insieme guardando soltanto il punto scelto nella formula.

## Da dire all'orale

> Una retta è un punto più tutti i multipli di una direzione non nulla. Un piano è un punto più tutte le combinazioni di due direzioni indipendenti. In $\mathbb R^n$ richiedono rispettivamente $n-1$ e $n-2$ vincoli cartesiani non ridondanti.

## Fonte e collegamenti

- [[36 Spazi Affini ed Equazioni Cartesiane e Parametriche]], [[09 Spazi Vettoriali Sottospazi e Geometria]].
- [[GAL 2026-2027 - 20261015 - LEZIONE 11.pdf#page=2|Lezione 11, pp. 2-5, stampate 97-100]].
