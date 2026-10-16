---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 11, PDF pp. 11-12, stampate 106-107"
---

# Sottospazi vettoriali e criterio di chiusura

Stato: **da studiare**.

## Definizione 11.3

Sia $V$ uno spazio vettoriale su $\mathbb K$. Un sottoinsieme non vuoto $H\subseteq V$ è un **sottospazio vettoriale** se è uno spazio vettoriale con le operazioni ereditate da $V$.

«Ereditate» significa che non si inventano operazioni nuove: per elementi di $H$ si usa la stessa somma e lo stesso prodotto per scalare dell'ambiente.

Il problema essenziale è che i risultati non escano da $H$.

## Criterio operativo

$H\subseteq V$ è un sottospazio se e solo se:

1. $0_V\in H$;
2. per ogni $u,v\in H$, $u+v\in H$;
3. per ogni $\lambda\in\mathbb K$ e $v\in H$, $\lambda v\in H$.

Sono condizioni universali: non basta provare uno o due esempi favorevoli.

Il PDF sottolinea zero e chiusura; la dimostrazione completa del criterio è esplicitata qui dal tutor.

### Necessità

Se $H$ è uno spazio vettoriale con le operazioni ereditate, esse sono operazioni su $H$, quindi sono chiuse. Scegliendo $h\in H$, si ha $0_{\mathbb K}h=0_V\in H$.

### Sufficienza

Le due chiusure rendono le operazioni ben definite su $H$. Associatività, commutatività e distributività sono già vere in $V$, quindi restano vere per elementi di $H$.

Lo zero appartiene a $H$. Per ogni $h\in H$, la chiusura per scalari dà $(-1)h=-h\in H$, quindi esiste anche l'opposto. Tutti gli assiomi sono soddisfatti.

## Versione con un'unica combinazione

Equivalentemente, basta richiedere $H\ne\varnothing$ e

$$
\boxed{\alpha u+\beta v\in H
\quad\text{per ogni }u,v\in H,\ \alpha,\beta\in\mathbb K.}
$$

Dalla non-vuotezza si sceglie un elemento; prendendo coefficienti zero si ottiene lo zero. Con $(\alpha,\beta)=(1,1)$ si ha la somma; con $(\lambda,0)$ il prodotto per scalare.

La non-vuotezza non va dimenticata: sull'insieme vuoto la frase universale sulle coppie sarebbe vera senza fornire uno spazio vettoriale.

## Nucleo: esempio fondamentale della lezione

$$
H=\ker(A)=\{x\in\mathbb K^n:Ax=0\}.
$$

- $A0=0$, quindi $0\in H$.
- Se $Au=Av=0$, allora $A(u+v)=0$.
- Se $Au=0$, allora $A(\lambda u)=0$.

Quindi $\ker(A)$ è un sottospazio di $\mathbb K^n$.

Le soluzioni di $Ax=b$ con $b\ne0$, invece, non contengono lo zero. Se il sistema è compatibile, formano uno spazio affine traslato, non un sottospazio vettoriale.

## Zero necessario, ma non sufficiente

Esempio del tutor:

$$
H=\{(x,y)\in\mathbb R^2:xy=0\}
$$

è l'unione dei due assi. Contiene $(0,0)$ ed è chiuso per prodotti scalari.

Ma $(1,0),(0,1)\in H$, mentre $(1,0)+(0,1)=(1,1)\notin H$. Quindi **non** è un sottospazio. La condizione $xy=0$ non è un sistema lineare nelle due incognite.

## Rette e piani

Una retta per l'origine $\{tv:t\in\mathbb R\}$ è chiusa:

$$
sv+tv=(s+t)v,\qquad \lambda(tv)=(\lambda t)v.
$$

Un piano per l'origine $\{sv+tw:s,t\in\mathbb R\}$ è anch'esso chiuso, sommando o riscalando i coefficienti.

Una retta o un piano che non contiene l'origine non è un sottospazio. La figura di [[33 Nucleo e Struttura delle Soluzioni]] confronta una retta vettoriale e una affine.

Il passaggio per l'origine non basta per un sottoinsieme arbitrario, come mostra l'unione degli assi.

## Esempi non geometrici del PDF

- $C^0(I)\subseteq V(I)$: zero, somme e multipli di funzioni continue sono continui.
- $\mathbb K[t]_{\le d}\subseteq\mathbb K[t]$: somma e riscalamento non introducono potenze maggiori di $d$; il polinomio nullo è incluso.

Attenzione a «grado esattamente $d$»: non è la condizione del sottospazio. Per esempio $t$ e $-t$ hanno grado 1, ma la loro somma è nulla.

Gli spazi banali $\{0_V\}$ e $V$ stesso sono sempre sottospazi di $V$.

## Chiusura algebrica, non topologica

Qui «chiuso» significa chiuso **rispetto a una specifica operazione**: il risultato resta nell'insieme. Non significa «insieme chiuso» nel senso della topologia o dell'analisi.

## Da dire all'orale

> Un sottospazio è un sottoinsieme non vuoto che rimane uno spazio vettoriale con le operazioni dell'ambiente. Basta verificare che contenga lo zero e sia chiuso rispetto alla somma e al prodotto per qualsiasi scalare; gli altri assiomi sono ereditati.

## Collegamenti e fonte

- [[38 Spazi Vettoriali e Assiomi]], [[39 Esempi di Spazi Vettoriali]], [[40 Proprietà Elementari degli Spazi Vettoriali]].
- [[09 Spazi Vettoriali Sottospazi e Geometria]].
- [[GAL 2026-2027 - 20261015 - LEZIONE 11.pdf#page=11|Lezione 11, pp. 11-12, stampate 106-107]].
