---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 4, PDF pp. 5-8, stampate 39-42"
---

# PageRank e matrici di transizione

Stato: **da studiare**.

## Il modello didattico

Il PDF introduce un modello di navigazione casuale fra un insieme finito $S$ di pagine web. La rilevanza di una pagina è collegata alla frequenza con cui viene visitata nel modello.

Questa è la costruzione matematica illustrata nella lezione, non una descrizione verificata dell'intero funzionamento attuale di un motore di ricerca.

## Righe di arrivo e colonne di partenza

La convenzione del professore è

$$
a_{ij}=\Pr(\text{arrivo nella pagina }i
\mid\text{partenza dalla pagina }j).
$$

Ogni colonna contiene quindi le probabilità delle possibili destinazioni da una pagina fissata. Si richiedono

$$
a_{ij}\ge0,\qquad \sum_i a_{ij}=1\quad\text{per ogni }j.
$$

La matrice è stocastica per colonne. Non si devono scambiare le somme di riga con quelle di colonna.

## I due comportamenti del PDF

### Navigazione tramite collegamenti

Con tre pagine:

- dalla pagina 1 si passa alla 2 o alla 3 con probabilità $1/2$ ciascuna;
- dalla pagina 2 si passa alla 1 con probabilità 1;
- dalla pagina 3 si passa alla 2 con probabilità 1.

Quindi

$$
T=\begin{pmatrix}
0&1&0\\
\frac12&0&1\\
\frac12&0&0
\end{pmatrix}.
$$

![[18 Navigazione e Matrice di Transizione.svg|960]]

Lo schema del tutor riproduce queste probabilità: ogni freccia va dalla pagina di partenza a quella di arrivo. La disposizione dei nodi è schematica, senza scala geometrica.

### Scelta diretta dell'indirizzo

Il navigatore può scegliere uniformemente una qualunque pagina, anche la stessa da cui parte:

$$
K=\begin{pmatrix}
\frac13&\frac13&\frac13\\
\frac13&\frac13&\frac13\\
\frac13&\frac13&\frac13
\end{pmatrix}.
$$

L'esempio tramite collegamenti è già privo di pagine senza uscite; il PDF non specifica qui una regola generale per gestire pagine senza collegamenti.

## La matrice di Google nel modello

Per $p\in(0,1)$:

$$
G=pT+(1-p)K.
$$

Con probabilità $p$ si usa il collegamento casuale; con probabilità $1-p$ si sceglie direttamente una pagina. Il parametro è spesso chiamato parametro di smorzamento.

Per esempio, scegliendo $p=1/2$ come integrazione del tutor:

$$
G=\begin{pmatrix}
\frac16&\frac23&\frac16\\
\frac5{12}&\frac16&\frac23\\
\frac5{12}&\frac16&\frac16
\end{pmatrix}.
$$

Ogni entrata è non negativa e ogni colonna somma a 1, perché

$$
\sum_i g_{ij}
=p\sum_i t_{ij}+(1-p)\sum_i k_{ij}
=p+(1-p)=1.
$$

## Più passi e distribuzioni

L'entrata

$$
(G^2)_{ij}=\sum_k g_{ik}g_{kj}
$$

somma le probabilità dei percorsi $j\to k\to i$. Il termine $g_{kj}$ riguarda il primo passo, $g_{ik}$ il secondo.

Nel modello con transizioni fissate, $G^q$ descrive $q$ passi.

Se $x^{(0)}$ è una colonna di probabilità iniziali, allora

$$
x^{(q+1)}=Gx^{(q)},\qquad x^{(q)}=G^qx^{(0)}.
$$

La massa totale resta 1:

$$
\sum_i(Gx)_i
=\sum_jx_j\sum_i g_{ij}
=\sum_jx_j=1.
$$

Questa formulazione mediante distribuzioni è esplicitata dal tutor a partire dall'interpretazione delle potenze.

## Che cosa mostrano i grafici

A p. 8 il PDF mostra l'evoluzione di un esempio a cinque nodi alle iterazioni 0, 3 e 10. Non è lo stesso grafo a tre nodi della matrice $T$.

Il professore lascia aperte due domande: se il processo si stabilizzi sempre e quanto contino le probabilità iniziali. Il solo confronto dei tre grafici non dimostra un risultato generale di convergenza.

## Da dire all'orale

> Una matrice di transizione per colonne ha entrate non negative e colonne di somma uno. Il prodotto compone i passi di navigazione; nel modello di PageRank una combinazione di navigazione tramite link e scelta uniforme produce la matrice G.

## Collegamenti e fonte

- [[16 Prodotto Matriciale Righe per Colonne]], [[17 Prodotto Matriciale e Composizione]].
- [[14 Prodotto di una Matrice per uno Scalare]] e [[13 Uguaglianza e Somma di Matrici]].
- Fonte: [[GAL 2026-2027 - 20261001 - LEZIONE 4.pdf#page=5|Lezione 4, pp. 5-8, stampate 39-42]].
