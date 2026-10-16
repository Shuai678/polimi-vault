---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 3, PDF pp. 11-12, pagine stampate 31-32"
---

# Prodotto di una matrice per uno scalare

Stato: **da studiare**.

## Definizione

Siano $\lambda\in\mathbb K$ e $A=(a_{ij})\in M_{\mathbb K}(m,n)$. Il prodotto di $A$ per lo scalare $\lambda$ è la matrice

$$
\lambda A=(\lambda a_{ij})_{ij}.
$$

Formalmente:

$$
\mathbb K\times M_{\mathbb K}(m,n)\longrightarrow M_{\mathbb K}(m,n),
\qquad
(\lambda,A)\longmapsto\lambda A.
$$

Lo scalare moltiplica ogni entrata. Il risultato conserva $m$ righe e $n$ colonne.

## Esempio del professore

$$
A=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}.
$$

Con $\lambda=2$:

$$
\begin{aligned}
2A
&=\begin{pmatrix}
2\cdot1&2\cdot2&2\cdot3\\
2\cdot4&2\cdot5&2\cdot6
\end{pmatrix}\\
&=\begin{pmatrix}2&4&6\\8&10&12\end{pmatrix}.
\end{aligned}
$$

La matrice iniziale e quella finale sono entrambe $2\times3$.

## Proprietà

Siano $A,B\in M_{\mathbb K}(m,n)$ e $\lambda,\mu\in\mathbb K$.

### Distributività rispetto alla somma di matrici

$$
\lambda(A+B)=\lambda A+\lambda B.
$$

Per ogni posizione:

$$
\begin{aligned}
(\lambda(A+B))_{ij}
&=\lambda(a_{ij}+b_{ij})\\
&=\lambda a_{ij}+\lambda b_{ij}\\
&=(\lambda A+\lambda B)_{ij}.
\end{aligned}
$$

La seconda uguaglianza usa la distributività nel campo.

### Distributività rispetto alla somma di scalari

$$
(\lambda+\mu)A=\lambda A+\mu A.
$$

Infatti:

$$
((\lambda+\mu)A)_{ij}
=(\lambda+\mu)a_{ij}
=\lambda a_{ij}+\mu a_{ij}
=(\lambda A+\mu A)_{ij}.
$$

### Compatibilità con il prodotto degli scalari

$$
(\lambda\mu)A=\lambda(\mu A).
$$

Per ogni entrata:

$$
((\lambda\mu)A)_{ij}
=(\lambda\mu)a_{ij}
=\lambda(\mu a_{ij})
=(\lambda(\mu A))_{ij}.
$$

Il prodotto nel campo è anche commutativo, quindi vale $\lambda(\mu A)=\mu(\lambda A)$, come indicato nel PDF.

### Unità

$$
1A=A,
$$

poiché $(1A)_{ij}=1a_{ij}=a_{ij}$.

## Conseguenze

Per le regole del campo, entrata per entrata:

$$
0A=0_{m,n},\qquad
\lambda0_{m,n}=0_{m,n},\qquad
(-1)A=-A.
$$

Qui lo zero davanti ad $A$ è uno scalare; $0_{m,n}$ è una matrice.

Per $A$ e $B$ dello stesso tipo:

$$
\lambda A+\mu B
$$

è una combinazione dei due prodotti per scalari. La sua entrata $(i,j)$ vale $\lambda a_{ij}+\mu b_{ij}$.

## Distinzione fra prodotti

In questa lezione il prodotto definito operativamente è quello fra uno scalare e una matrice. Il consueto prodotto tra due matrici richiede una definizione diversa.

A p. 12 il professore osserva che si potrebbe anche definire un prodotto posizione per posizione. Questa osservazione non definisce il prodotto matriciale riga per colonna.

## Errori da evitare

- Moltiplicare soltanto una riga o una colonna.
- Alterare le dimensioni durante il prodotto per uno scalare.
- Trattare lo scalare come se fosse una matrice di dimensioni arbitrarie.
- Applicare la somma $\lambda A+\mu B$ a matrici di forme diverse.

## Da dire all'orale

> Il prodotto di una matrice per uno scalare si ottiene moltiplicando tutte le sue entrate per lo scalare. Le distributività e la compatibilità con il prodotto degli scalari seguono dalle corrispondenti proprietà del campo.

## Collegamenti e fonte

- [[11 Matrici come Funzioni e Indici]], [[12 Campi Numerici e Campo F2]].
- [[13 Uguaglianza e Somma di Matrici]] e [[15 Proprietà e Costo dei Calcoli Matriciali]].
- Fonte: [[GAL 2026-2027 - 20260930 - LEZIONE 3.pdf#page=11|Lezione 3, pp. 11-12, stampate 31-32]]. I passaggi delle dimostrazioni sono esplicitati dal tutor.

## Proseguimento

Il prodotto fra due matrici, introdotto nella Lezione 4, è sviluppato in [[16 Prodotto Matriciale Righe per Colonne]].
