---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 11, PDF pp. 9-10, stampate 104-105"
---

# Proprietà elementari degli spazi vettoriali

Stato: **da studiare**.

## Dalle regole alle conseguenze

Il PDF elenca proprietà note dei vettori e chiede di esplicitare i passaggi dell'equazione $\lambda x+\mu v=0$. Qui le dimostrazioni sono sviluppate dal tutor a partire dagli [[38 Spazi Vettoriali e Assiomi|assiomi V1-V8]].

Distinguiamo $0_{\mathbb K}$, zero del campo, da $0_V$, vettore nullo.

## Unicità dello zero e dell'opposto

Se $z$ e $z'$ sono entrambi neutri della somma, allora

$$
z=z+z'=z'.
$$

Il primo uguale usa che $z'$ è neutro; il secondo che $z$ è neutro.

Se $w$ e $w'$ sono entrambi opposti di $v$:

$$
w=w+0_V=w+(v+w')=(w+v)+w'=0_V+w'=w'.
$$

Si usano V3, V4, V1 e V2. Perciò l'opposto è unico e si può scrivere $-v$.

Da qui segue la cancellazione additiva: se $a+c=b+c$, sommando $-c$ a entrambi i membri e usando V1-V4 si ottiene $a=b$.

## Zero scalare per un vettore

Da V6:

$$
0_{\mathbb K}v=(0_{\mathbb K}+0_{\mathbb K})v
=0_{\mathbb K}v+0_{\mathbb K}v.
$$

Il membro sinistro è anche $0_{\mathbb K}v+0_V$. Cancellando il vettore $0_{\mathbb K}v$:

$$
\boxed{0_{\mathbb K}v=0_V.}
$$

Non è un assioma separato e non si usa prima di averlo giustificato.

## Uno scalare per il vettore nullo

Da V5:

$$
\lambda0_V=\lambda(0_V+0_V)=\lambda0_V+\lambda0_V.
$$

Con la cancellazione additiva:

$$
\boxed{\lambda0_V=0_V.}
$$

Le due proprietà precedenti hanno ruoli diversi: nella prima è nullo lo scalare, nella seconda il vettore.

## Opposto e prodotto per meno uno

Con V8, V6 e la proprietà appena dimostrata:

$$
v+(-1_{\mathbb K})v
=1_{\mathbb K}v+(-1_{\mathbb K})v
=(1_{\mathbb K}-1_{\mathbb K})v
=0_{\mathbb K}v=0_V.
$$

Per unicità dell'opposto:

$$
\boxed{(-1_{\mathbb K})v=-v.}
$$

Inoltre, per V7:

$$
\lambda(-v)=\lambda((-1)v)
=(-1)(\lambda v)=-(\lambda v).
$$

## Annullamento del prodotto scalare-vettore

$$
\boxed{\lambda v=0_V\iff \lambda=0_{\mathbb K}\ \text{oppure}\ v=0_V.}
$$

Il verso da destra a sinistra segue dalle proprietà dello zero. Per l'altro verso, se $\lambda\ne0$, il campo contiene $\lambda^{-1}$:

$$
v=1v=(\lambda^{-1}\lambda)v
=\lambda^{-1}(\lambda v)
=\lambda^{-1}0_V=0_V.
$$

Si usano V8, V7 e il prodotto di uno scalare per il vettore nullo.

Questa proprietà riguarda **uno scalare e un vettore**. Non afferma che il prodotto di due matrici non nulle sia sempre non nullo.

## Equazione proposta nella lezione

Dati $v\in V$, $\lambda\ne0$, $\mu\in\mathbb K$, cerchiamo $x\in V$ con

$$
\lambda x+\mu v=0_V.
$$

### 1 Aggiungere l'opposto

Sommiamo $-(\mu v)$ a entrambi i membri:

$$
(\lambda x+\mu v)+(-\mu v)=0_V+(-\mu v).
$$

Per associatività, opposto e neutro:

$$
\lambda x=-\mu v.
$$

### 2 Moltiplicare per l'inverso dello scalare

$$
\lambda^{-1}(\lambda x)=\lambda^{-1}(-\mu v).
$$

V7 e V8 danno

$$
\boxed{x=-\frac{\mu}{\lambda}v.}
$$

Non si divide per un vettore: si moltiplica per lo scalare $\lambda^{-1}$.

### 3 Verifica e unicità

Sostituendo:

$$
\lambda\left(-\frac{\mu}{\lambda}v\right)+\mu v
=(-\mu)v+\mu v=0_V.
$$

Se $x'$ fosse un'altra soluzione, gli stessi passaggi reversibili imporrebbero $x'=-(\mu/\lambda)v$. La soluzione è unica.

### Se $\lambda=0$

Questo caso non è coperto dalla divisione:

- se $\mu v=0_V$, ogni $x\in V$ è soluzione;
- se $\mu v\ne0_V$, nessun $x$ è soluzione.

## Esempio del tutor con un polinomio

Nello spazio $\mathbb R[t]$, siano $v(t)=1+t^2$, $\lambda=2$ e $\mu=-3$. L'equazione

$$
2x(t)-3(1+t^2)=0
$$

ha soluzione $x(t)=\frac32(1+t^2)$. Il ragionamento è identico a quello per colonne o vettori geometrici: cambia l'oggetto, non gli assiomi.

## Da dire all'orale

> Le proprietà dello zero e dell'opposto si deducono dagli assiomi. Se uno scalare non nullo moltiplica un vettore dando zero, il vettore è nullo, perché si può moltiplicare per l'inverso dello scalare. La stessa idea permette di risolvere equazioni vettoriali lineari.

## Fonte e collegamenti

- [[38 Spazi Vettoriali e Assiomi]], [[39 Esempi di Spazi Vettoriali]].
- [[GAL 2026-2027 - 20261015 - LEZIONE 11.pdf#page=9|Lezione 11, pp. 9-10, stampate 104-105]].
