---
course: Algebra Lineare
type: exercise
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 11, PDF pp. 2-12, stampate 97-107"
  - "Esempi numerici e svolgimenti del tutor"
---

# Spazi vettoriali, sottospazi e geometria

Stato: **da studiare**. Soluzioni preparate dal tutor, non svolgimenti attribuiti allo studente.

Gli esempi numerici seguenti sono del tutor, costruiti sui concetti della lezione. Non sono esercizi assegnati dal professore né risultati personali dello studente.

## 1 Una retta: dalle equazioni ai parametri e ritorno

$$
\begin{cases}x+y+z=2,\\x-y+z=0.\end{cases}
$$

Sottraendo le equazioni otteniamo $2y=2$, quindi $y=1$ e $x+z=1$.

Ponendo $z=t$:

$$
(x,y,z)=(1-t,1,t)=(1,1,0)+t(-1,0,1).
$$

Le due righe dei coefficienti non sono proporzionali, quindi il rango è 2: la descrizione ha un parametro effettivo.

Per tornare alle cartesiane basta $y=1$, $x+z=1$. Queste due condizioni ricostruiscono entrambe le equazioni originali.

L'origine non appartiene alla retta, perché la prima equazione darebbe $0=2$. Quindi non è un sottospazio vettoriale.

## 2 Un piano: eliminare i parametri

$$
(x,y,z)=(0,0,1)+s(1,0,1)+t(0,1,-1).
$$

Le coordinate sono $x=s$, $y=t$, $z=1+s-t$. Eliminando $s,t$:

$$
-x+y+z=1.
$$

Viceversa, dato un punto che soddisfa questa equazione, si scelgono $s=x$ e $t=y$ e si ottiene $z=1+x-y$: la parametrizzazione lo riproduce.

I due vettori direzione sono indipendenti perché $\alpha(1,0,1)+\beta(0,1,-1)=0$ impone $\alpha=0$ dalla prima coordinata e $\beta=0$ dalla seconda. Ci sono davvero due parametri non ridondanti.

Il piano omogeneo associato è $-x+y+z=0$, con parametrizzazione $s(1,0,1)+t(0,1,-1)$.

## 3 Due parametri scritti, una sola direzione

$$
S=\{(1,0,0)+s(1,2,3)+t(2,4,6):s,t\in\mathbb R\}.
$$

Poiché $(2,4,6)=2(1,2,3)$:

$$
S=\{(1,0,0)+(s+2t)(1,2,3)\}.
$$

Ponendo $u=s+2t$, ogni reale $u$ è ottenibile, per esempio scegliendo $s=u$, $t=0$. Dunque $S$ è una retta, non un piano.

Non si conta il numero di simboli dei parametri senza verificare la ridondanza.

## 4 Riconoscere un sottospazio con un'equazione omogenea

$$
H=\{(x,y,z):x-2y+z=0\}.
$$

Contiene lo zero. Per $u,v\in H$ e $\alpha,\beta\in\mathbb R$:

$$
(\alpha u_1+\beta v_1)-2(\alpha u_2+\beta v_2)
+(\alpha u_3+\beta v_3)
=\alpha(u_1-2u_2+u_3)+\beta(v_1-2v_2+v_3)=0.
$$

Quindi è chiuso per combinazioni lineari e perciò è un sottospazio.

Ponendo $y=s$, $z=t$, $x=2s-t$:

$$
H=\{s(2,1,0)+t(-1,0,1):s,t\in\mathbb R\}.
$$

Se il termine noto fosse 1 invece di 0, l'origine non apparterrebbe all'insieme e non sarebbe un sottospazio con le operazioni ereditate.

## 5 Contiene lo zero ma non è un sottospazio

$$
U=\{(x,y):xy=0\}.
$$

I vettori $(1,0)$ e $(0,1)$ appartengono a $U$, ma la somma $(1,1)$ no. Un solo controesempio alla chiusura basta a escludere un sottospazio.

Anche il semiasse $S=\{(x,0):x\ge0\}$ contiene lo zero ed è chiuso per somma, ma non per tutti gli scalari: $(-1)(1,0)=(-1,0)\notin S$.

## 6 Un sottospazio di matrici

$$
H=\left\{\begin{pmatrix}a&b\\c&d\end{pmatrix}:a+d=0\right\}
\subseteq M_{\mathbb R}(2,2).
$$

La matrice nulla appartiene a $H$. Se $A,B\in H$, la somma degli elementi diagonali di $\alpha A+\beta B$ è

$$
\alpha(a_{11}+a_{22})+\beta(b_{11}+b_{22})=0.
$$

Quindi $H$ è un sottospazio. Ogni suo elemento ha la forma

$$
\begin{pmatrix}a&b\\c&-a\end{pmatrix}
=a\begin{pmatrix}1&0\\0&-1\end{pmatrix}
+b\begin{pmatrix}0&1\\0&0\end{pmatrix}
+c\begin{pmatrix}0&0\\1&0\end{pmatrix}.
$$

Non serve il prodotto fra matrici per questa verifica.

## 7 Polinomi di grado limitato e di grado fissato

L'insieme $\mathbb R[t]_{\le2}$ contiene lo zero. La somma di due polinomi con potenze al massimo 2 e il multiplo scalare di uno di essi hanno ancora potenze al massimo 2. Quindi è un sottospazio.

L'insieme dei polinomi di grado **esattamente** 2 non lo è: $p(t)=t^2$ e $q(t)=-t^2$ vi appartengono, ma $p+q=0$ no.

Il polinomio nullo è incluso in $\mathbb R[t]_{\le2}$ mediante la rappresentazione $0+0t+0t^2$, indipendentemente dalla convenzione sul suo grado.

## 8 Un sottospazio di funzioni e una sua traslazione

In $V=\mathcal F(\mathbb R,\mathbb R)$, consideriamo

$$
H=\{f:f(0)=0\}.
$$

La funzione nulla vi appartiene e

$$
(\alpha f+\beta g)(0)=\alpha f(0)+\beta g(0)=0.
$$

È quindi un sottospazio.

L'insieme $T=\{f:f(0)=1\}$ non contiene la funzione nulla. Inoltre, se $f,g\in T$, $(f+g)(0)=2\ne1$. Non è un sottospazio; è la traslazione di $H$ per la funzione costante 1.

## 9 Risolvere un'equazione nello spazio dei polinomi

In $\mathbb R[t]$ risolvere $2p-3(1+t^2)=0$.

Aggiungendo $3(1+t^2)$ a entrambi i membri e moltiplicando per $1/2$:

$$
2p=3(1+t^2)\implies p=\frac32+\frac32t^2.
$$

La sostituzione dà $2p-3(1+t^2)=0$. L'unicità segue perché $2\ne0$ nel campo $\mathbb R$.

## Teoria e fonte

- [[36 Spazi Affini ed Equazioni Cartesiane e Parametriche]], [[37 Rette e Piani tra Parametri e Vincoli]].
- [[38 Spazi Vettoriali e Assiomi]], [[39 Esempi di Spazi Vettoriali]], [[40 Proprietà Elementari degli Spazi Vettoriali]], [[41 Sottospazi Vettoriali e Criterio di Chiusura]].
- [[GAL 2026-2027 - 20261015 - LEZIONE 11.pdf#page=2|Lezione 11, pp. 2-12, stampate 97-107]].
