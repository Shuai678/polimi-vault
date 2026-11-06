---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 15, PDF pp. 4-5 e 11, stampate 122-123 e 129"
---

# Completamento di vettori indipendenti a una base

Stato: **da studiare**.

## Il problema complementare all'estrazione

Nell'estrazione si parte da troppi generatori e si eliminano ridondanze. Nel **completamento** si parte da una famiglia indipendente e si aggiungono direzioni mancanti, mantenendo tutti i vettori iniziali.

Sia $\dim V=d<\infty$. Ogni famiglia indipendente $v_1,\ldots,v_k$, con $k\le d$, si può completare a una base di $V$.

Se $k=d$ è già una base. Se $k<d$, occorrono esattamente $d-k$ vettori aggiuntivi.

## Perché si può aggiungere un vettore

Se $\operatorname{Span}(v_1,\ldots,v_k)\ne V$, scegliamo

$$
u\in V\setminus\operatorname{Span}(v_1,\ldots,v_k).
$$

La famiglia allargata è indipendente. Infatti, da

$$
\sum_i\lambda_iv_i+\mu u=0
$$

se $\mu\ne0$ si ricaverebbe $u=-\sum_i(\lambda_i/\mu)v_i$, contro la scelta. Quindi $\mu=0$ e, per indipendenza iniziale, tutti i $\lambda_i=0$.

Ripetendo si aggiungono direzioni, senza superare $d$ indipendenti per il [[46 Lemma Fondamentale e Teorema della Dimensione|lemma fondamentale]]. A $d$ vettori la famiglia è una base.

## Algoritmo con una base o generatori già noti

Per $\mathbb K^n$ si usano i vettori canonici:

$$
A=[v_1\mid\cdots\mid v_k\mid e_1\mid\cdots\mid e_n].
$$

La famiglia completa genera $\mathbb K^n$, perché contiene tutti gli $e_j$.

Si applica Gauss senza scambiare colonne e si estraggono le colonne pivot **originali**. Le prime $k$ colonne sono indipendenti: ciascuna aumenta il rango rispetto a quelle precedenti, quindi viene selezionata. I pivot successivi individuano quali vettori canonici aggiungere.

In uno spazio di dimensione finita diverso da $\mathbb K^n$, si affiancano ai vettori iniziali una base nota o una famiglia generatrice, dopo aver scritto tutti gli oggetti in coordinate compatibili.

## Esempio della Lezione 15

Il PDF completa in $\mathbb R^3$

$$
v_1=\begin{pmatrix}1\\0\\1\end{pmatrix},\qquad
v_2=\begin{pmatrix}0\\1\\1\end{pmatrix}.
$$

Sono indipendenti: le prime due coordinate di $\alpha v_1+\beta v_2=0$ impongono $\alpha=\beta=0$.

Affianchiamo i canonici:

$$
A=
\begin{pmatrix}
1&0&1&0&0\\
0&1&0&1&0\\
1&1&0&0&1
\end{pmatrix}.
$$

Con $R_3\leftarrow R_3-R_1$:

$$
\begin{pmatrix}
1&0&1&0&0\\
0&1&0&1&0\\
0&1&-1&0&1
\end{pmatrix}.
$$

Poi $R_3\leftarrow R_3-R_2$:

$$
U=\begin{pmatrix}
1&0&1&0&0\\
0&1&0&1&0\\
0&0&-1&-1&1
\end{pmatrix}.
$$

I pivot sono nelle colonne 1, 2 e 3. Le corrispondenti colonne **di $A$** sono

$$
\boxed{\mathcal B=(v_1,v_2,e_1).}
$$

Non si sostituisce $e_1$ con la terza colonna trasformata $(1,0,-1)^{\mathsf T}$.

![[49 Completamento dal Piano allo Spazio.svg|1040]]

**Figura del tutor:** $v_1$ e $v_2$ generano il piano $z=x+y$. La direzione $e_1=(1,0,0)$ non vi appartiene perché $0\ne1+0$; aggiungerla permette di raggiungere ogni punto dello spazio. La proiezione obliqua è schematica: non conserva lunghezze e angoli.

### Verifica diretta del risultato

Per qualunque $(x,y,z)$ cerchiamo $\alpha v_1+\beta v_2+\gamma e_1$:

$$
\begin{cases}
\alpha+\gamma=x,\\
\beta=y,\\
\alpha+\beta=z.
\end{cases}
$$

Si ottiene univocamente

$$
\beta=y,\qquad \alpha=z-y,\qquad \gamma=x-z+y.
$$

La famiglia è quindi generatrice e indipendente.

## Quando il procedimento non è applicabile

Se i vettori iniziali sono dipendenti, non è possibile costruire una base che li conservi **tutti**: la stessa relazione non banale rimarrebbe valida in ogni famiglia allargata.

Per esempio, $(1,0,0)$ e $(2,0,0)$ non si completano insieme a una base. Bisogna prima estrarne una sottofamiglia indipendente, cambiando la richiesta.

Non basta inoltre aggiungere un vettore «diverso» dagli altri: deve stare fuori dallo span attuale.

## Da dire all'orale

> Una famiglia indipendente in uno spazio finitamente dimensionale si completa aggiungendo vettori fuori dal suo span. Operativamente si affianca una base nota e si selezionano le colonne pivot originali, conservando quelle indipendenti iniziali.

## Fonti e collegamenti

- [[45 Basi e Unicità delle Coordinate]], [[46 Lemma Fondamentale e Teorema della Dimensione]], [[48 Estrazione di una Base con Gauss]].
- [[11 Dimensione Estrazione e Completamento di Basi]].
- [[GAL 2026-2027 - 20261028 - LEZIONE 15.pdf#page=4|Lezione 15, pp. 4-5, stampate 122-123]].
- [[GAL 2026-2027 - 20261028 - LEZIONE 15.pdf#page=11|Lezione 15, p. 11, stampata 129]].
