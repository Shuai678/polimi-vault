---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-10-16
source: esempi originali del tutor
---

# Esempi svolti sulle funzioni

Stato: **da studiare**. Esempi e soluzioni sono del tutor e non certificano un'esecuzione autonoma dello studente.

## 1 Stesso numero di coppie ma nessuna funzione

### Problema

Siano $A=\{1,2,3\}$, $B=\{a,b\}$ e

$$
R=\{(1,a),(1,b),(2,a)\}.
$$

Stabilire se $R$ è una funzione da $A$ a $B$.

### Svolgimento

Si ha $\#R=\#A=3$, ma:

- $1$ ha due immagini distinte, $a$ e $b$;
- $2$ ha una sola immagine, $a$;
- $3$ non ha immagine.

Falliscono unicità ed esistenza, quindi $R$ non è una funzione.

Questo esempio confuta l'implicazione inversa «stesso numero di coppie, dunque funzione».

Prerequisiti: [[05 Funzioni]], [[06 Implicazione e Contrapposizione]].

## 2 Stessa formula e proprietà diverse

### Problema

Confrontare:

$$
\begin{aligned}
f:\mathbb R&\to\mathbb R,& f(x)&=x^2,\\
g:\mathbb R&\to[0,+\infty),& g(x)&=x^2,\\
h:[0,+\infty)&\to[0,+\infty),& h(x)&=x^2.
\end{aligned}
$$

### Svolgimento per f

Non è iniettiva, perché $f(1)=f(-1)=1$ con $1\ne-1$.

Non è suriettiva, perché $-1$ appartiene al codominio ma $x^2=-1$ non ha soluzioni reali.

### Svolgimento per g

Non è iniettiva, con lo stesso controesempio $1,-1$.

È suriettiva: preso un qualunque $y\ge0$, il numero $x=\sqrt y$ è reale e soddisfa $g(x)=y$.

### Svolgimento per h

È suriettiva: la scelta $x=\sqrt y$ appartiene anche al dominio $[0,+\infty)$.

È iniettiva. Supponiamo $h(x_1)=h(x_2)$ con $x_1,x_2\ge0$. Allora:

$$
\begin{aligned}
x_1^2&=x_2^2,\\
x_1^2-x_2^2&=0,\\
(x_1-x_2)(x_1+x_2)&=0.
\end{aligned}
$$

Se $x_1+x_2>0$, il secondo fattore non è nullo e deve essere $x_1-x_2=0$.

Se $x_1+x_2=0$, dalla non negatività segue $x_1=x_2=0$.

In entrambi i casi $x_1=x_2$. Quindi $h$ è biiettiva.

| Funzione | Iniettiva | Suriettiva | Biiettiva |
|---|---|---|---|
| $f$ | no | no | no |
| $g$ | no | sì | no |
| $h$ | sì | sì | sì |

Cambiare dominio o codominio cambia la funzione specificata, anche quando la formula rimane uguale.

Prerequisiti: [[07 Iniettività]], [[08 Suriettività]], [[09 Biiettività]].

## 3 Trasformare coppie annidate in terne

### Problema

Siano $A=\{1,2\}$, $B=\{a\}$ e $C=\{0,1\}$. Descrivere la biiezione naturale da $(A\times B)\times C$ ad $A\times B\times C$.

### Svolgimento

Le quattro associazioni sono

$$
\begin{aligned}
((1,a),0)&\longmapsto(1,a,0),\\
((1,a),1)&\longmapsto(1,a,1),\\
((2,a),0)&\longmapsto(2,a,0),\\
((2,a),1)&\longmapsto(2,a,1).
\end{aligned}
$$

Ogni elemento del codominio compare una volta e proviene da un unico elemento del dominio. La corrispondenza è biiettiva.

Gli insiemi sono descritti con strutture diverse, coppie annidate e terne, ma questa associazione conserva tutta l'informazione.

Prerequisito: [[10 Prodotti Cartesiani di Più Insiemi]].
