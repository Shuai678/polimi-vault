---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 13, PDF pp. 8-10, stampate 115-117"
  - "Lezione 15, PDF pp. 8-11, stampate 126-129"
---

# Estrazione di una base con Gauss

Stato: **da studiare**.

## Che cosa significa estrarre

Data una famiglia finita che genera $V$, **estrarre una base** significa scegliere una sottofamiglia dei vettori **originali** che continui a generare $V$ e sia indipendente.

È diverso da costruire una base qualsiasi, i cui vettori possono essere combinazioni nuove.

## Esistenza per eliminazione delle ridondanze

Se i generatori sono dipendenti, esiste una relazione non banale. Un vettore con coefficiente non nullo si esprime tramite gli altri e può essere rimosso senza cambiare lo span.

Si ripete finché la famiglia rimasta è indipendente. Il procedimento termina perché la famiglia iniziale è finita. Essa genera ancora $V$, quindi è una base. Per $V=\{0\}$ si può arrivare alla famiglia vuota.

Gauss rende il procedimento sistematico.

## Metodo 1: vettori disposti per righe

Si costruisce $A$ mettendo i vettori come righe. Le operazioni elementari non cambiano lo span delle righe:

$$
\operatorname{Span}(R_1(A),\ldots,R_m(A))
=\operatorname{Span}(R_1(U),\ldots,R_m(U)).
$$

Ogni nuova riga è combinazione delle vecchie e, per reversibilità, vale anche l'inclusione opposta.

Le righe **non nulle** della matrice a scala $U$ sono indipendenti: in una relazione fra esse, la colonna del primo pivot forza a zero il coefficiente della prima riga; i pivot successivi fanno lo stesso con gli altri.

Quindi le righe non nulle di $U$ danno una base dello span. Ma sono generalmente **vettori nuovi**: questo metodo costruisce una base, senza garantire di estrarla dalla famiglia iniziale.

**Precisazione al PDF, p. 9:** una riga nulla non è indipendente. L'affermazione sulle righe di una matrice a scala va intesa per le sole righe non nulle.

## Metodo 2: vettori disposti per colonne

Per estrarre vettori originali si affiancano come colonne:

$$
A=[v_1\mid\cdots\mid v_s].
$$

Si applicano solo operazioni elementari **di riga**, ottenendo $U=TA$, con $T$ invertibile.

1. Individuare le colonne di $U$ che contengono i pivot.
2. Registrarne gli **indici** $j_1,\ldots,j_r$.
3. Scegliere $v_{j_1},\ldots,v_{j_r}$ dalla matrice **iniziale $A$**.

$$
\boxed{\text{Base estratta}=(C_{j_1}(A),\ldots,C_{j_r}(A)).}
$$

Non si prendono come risposta le colonne trasformate di $U$.

## Perché il metodo delle colonne funziona

Per ogni lista $\lambda$:

$$
A\lambda=0\iff TA\lambda=0\iff U\lambda=0.
$$

Quindi $\ker(A)=\ker(U)$: le relazioni fra le colonne, con gli stessi coefficienti e gli stessi indici, sono conservate.

Le colonne pivot di $U$ sono indipendenti: restringendosi alle righe dei pivot formano una matrice triangolare con diagonale non nulla. Inoltre generano tutte le colonne di $U$: nelle prime $r$ righe il sistema con queste colonne è quadrato triangolare invertibile, mentre le righe successive sono nulle.

Ogni relazione che esprime una colonna di $U$ tramite quelle pivot è una relazione omogenea, quindi vale con gli stessi coefficienti per le corrispondenti colonne di $A$. Indipendenza e generazione si trasferiscono alla famiglia originale selezionata.

Invece, in generale:

$$
\operatorname{Span}(C_1(A),\ldots,C_s(A))
\ne \operatorname{Span}(C_1(U),\ldots,C_s(U)).
$$

Le dimensioni sono uguali, ma i sottospazi possono essere diversi.

## Esempio del professore

$$
w_1=\begin{pmatrix}0\\2\\1\end{pmatrix},\quad
w_2=\begin{pmatrix}4\\1\\2\end{pmatrix},\quad
w_3=\begin{pmatrix}4\\-3\\0\end{pmatrix}.
$$

Affiancando:

$$
A=\begin{pmatrix}0&4&4\\2&1&-3\\1&2&0\end{pmatrix}
\longrightarrow
U=\begin{pmatrix}1&2&0\\0&1&1\\0&0&0\end{pmatrix}.
$$

Il calcolo completo è in [[11 Dimensione Estrazione e Completamento di Basi]]. I pivot sono nelle colonne 1 e 2:

$$
\boxed{(w_1,w_2)\text{ è una base dello span iniziale}.}
$$

Dall'omogeneo di $U$ si ottiene $\lambda=t(2,-1,1)$, quindi

$$
2w_1-w_2+w_3=0,\qquad w_3=w_2-2w_1.
$$

La stessa relazione vale per le colonne di $U$, ma i vettori non coincidono.

Controesempio concreto alla conservazione dello span delle colonne: tutte le colonne di $U$ hanno terza coordinata zero, mentre $w_1$ ha terza coordinata 1. Lo span originale non è quel piano coordinato.

## Confronto fra i due metodi

| Obiettivo | Procedimento | Vettori della risposta |
|---|---|---|
| Una base qualsiasi dello span | vettori per righe, poi Gauss | righe non nulle finali |
| Una base estratta dai dati | vettori per colonne, poi Gauss di riga | colonne originali con indici pivot |

Per entrambe le costruzioni il numero di vettori della base è il numero dei pivot:

$$
\dim\operatorname{Span}(\text{righe di }A)
=\dim\operatorname{Span}(\text{colonne di }A)=r(A).
$$

Questa uguaglianza collega il rango definito nelle lezioni precedenti alla dimensione degli spazi generati.

## Da dire all'orale

> Per estrarre una base si mettono i vettori per colonne, si riduce per righe e si conservano le colonne della matrice originale corrispondenti ai pivot. Le operazioni conservano le relazioni fra le colonne, non necessariamente il loro span geometrico.

## Fonti e collegamenti

- [[24 Operazioni Elementari e Metodo di Gauss]], [[27 Calcolo del Rango con Gauss]], [[44 Dipendenza e Indipendenza Lineare]], [[49 Completamento di Vettori Indipendenti a una Base]].
- [[GAL 2026-2027 - 20261019 - LEZIONE 13.pdf#page=8|Lezione 13, pp. 8-10, stampate 115-117]].
- [[GAL 2026-2027 - 20261028 - LEZIONE 15.pdf#page=8|Lezione 15, pp. 8-11, stampate 126-129]].
