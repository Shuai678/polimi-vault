---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 11, PDF pp. 2-6, stampate 97-101"
---

# Spazi affini ed equazioni cartesiane e parametriche

Stato: **da studiare**.

## Due descrizioni dello stesso insieme

In $\mathbb R^n$, un sistema lineare compatibile può descrivere un punto, una retta, un piano oppure un insieme affine di altra dimensione.

- Le **equazioni cartesiane** impongono condizioni alle coordinate: $Ax=b$.
- Le **equazioni parametriche** costruiscono i punti: $x=P+t_1v_1+\cdots+t_dv_d$.

La prima descrizione è implicita: indica quali vincoli soddisfare. La seconda è esplicita: indica come ottenere i punti facendo variare i parametri.

## Definizione 11.1 e condizione di compatibilità

Il PDF chiama (sotto)spazio affine l'insieme delle soluzioni di un sistema lineare:

$$
S=\{x\in\mathbb R^n:Ax=b\}.
$$

Per un sistema **compatibile**, il [[33 Nucleo e Struttura delle Soluzioni|teorema di struttura]] dà

$$
\boxed{S=P+\ker(A),\qquad AP=b.}
$$

Qui $P$ è un punto di $S$; $\ker(A)$ è l'insieme dei vettori direzione. L'origine scelta per rappresentare le coordinate non deve appartenere a $S$.

**Precisazione del tutor sulla convenzione:** la formulazione mediante sistemi può includere l'insieme vuoto se il sistema è incompatibile. Molti usi riservano «spazio affine» agli insiemi non vuoti; in queste note si segnala sempre la compatibilità prima di scrivere $P+\ker(A)$. Un insieme vuoto non ammette un punto $P$.

La formulazione astratta generale degli spazi affini non viene qui attribuita alla lezione: si lavora con sottoinsiemi di $\mathbb R^n$.

## Dal sistema alle equazioni parametriche

Si applicano [[31 Risoluzione dei Sistemi con Gauss e Parametri|Gauss e sostituzione all'indietro]].

Esempio del tutor:

$$
\begin{cases}
x+y+z=2,\\
x-y+z=0.
\end{cases}
$$

Sottraendo la seconda dalla prima: $2y=2$, quindi $y=1$. La seconda diventa $x+z=1$. Ponendo $z=t$:

$$
x=\begin{pmatrix}1\\1\\0\end{pmatrix}
+t\begin{pmatrix}-1\\0\\1\end{pmatrix}.
$$

È una retta in $\mathbb R^3$, intersezione dei due piani delle equazioni iniziali.

La matrice dei coefficienti ha rango 2; tre incognite meno due pivot danno un parametro libero.

## Dalle equazioni parametriche a quelle cartesiane

Si eliminano i parametri, conservando le condizioni necessarie **e sufficienti**.

Nell'esempio:

$$
x=1-t,\qquad y=1,\qquad z=t.
$$

Da $t=z$ si ricava $x+z=1$, e resta $y=1$. Viceversa, ogni punto con $y=1$ e $x+z=1$ si ottiene scegliendo $t=z$. Quindi

$$
S=\{(x,y,z):y=1,\ x+z=1\}.
$$

Le nuove equazioni non devono essere letteralmente uguali alle originali: devono avere lo stesso insieme di soluzioni.

## Quanti vincoli e quante direzioni

Se il sistema è compatibile e ha rango $r$, Gauss produce $n-r$ parametri liberi non ridondanti.

$$
\boxed{\text{parametri liberi}=n-r,\qquad
\text{vincoli lineari non ridondanti}=r.}
$$

Il numero di righe di una rappresentazione può essere maggiore di $r$ per la presenza di equazioni ridondanti.

La parola «dimensione» può essere usata qui in senso geometrico come numero delle direzioni indipendenti; la teoria astratta di basi e dimensione non è ancora sviluppata in questo PDF.

## Caso omogeneo e caso traslato

Se $b=0$, si può scegliere $P=0$:

$$
S=\ker(A).
$$

La retta o il piano passa per l'origine. Inoltre le soluzioni sono chiuse rispetto a somma e prodotto per scalare.

Se $b\ne0$ e il sistema è compatibile, $0$ non è soluzione, perché $A0=0\ne b$. Non si ha un sottospazio vettoriale con le operazioni ereditate.

Il disegno in [[33 Nucleo e Struttura delle Soluzioni]] mette a confronto proprio una retta per l'origine e una sua traslazione.

## Cambiare punto iniziale non cambia necessariamente l'insieme

Per la retta precedente, $P=(1,1,0)$ e $Q=(0,1,1)$ sono entrambi punti della retta:

$$
Q=P+(-1,0,1).
$$

Pertanto $P+t(-1,0,1)$ e $Q+s(-1,0,1)$ descrivono lo stesso insieme, con $t=s+1$. Parametri e punto iniziale non sono unici; l'insieme è l'oggetto geometrico da confrontare.

## Da dire all'orale

> Le equazioni cartesiane descrivono un insieme affine mediante vincoli lineari; quelle parametriche mediante un punto particolare e vettori direzione. Se il sistema è compatibile, l'insieme è la traslazione del nucleo della matrice dei coefficienti.

## Collegamenti e fonte

- [[32 Teorema di Rouché-Capelli]], [[37 Rette e Piani tra Parametri e Vincoli]], [[41 Sottospazi Vettoriali e Criterio di Chiusura]].
- [[GAL 2026-2027 - 20261015 - LEZIONE 11.pdf#page=2|Lezione 11, pp. 2-6, stampate 97-101]].
