---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 11, PDF p. 7, stampata 102"
---

# Spazi vettoriali e assiomi

Stato: **da studiare**.

## Il salto concettuale

Matrici, vettori geometrici, successioni, funzioni e polinomi sono oggetti diversi. Possono però essere sommati e moltiplicati per scalari rispettando le stesse regole.

Uno spazio vettoriale isola queste regole comuni. La parola **vettore** non significa quindi necessariamente una freccia nel piano.

## Definizione 11.2

Uno spazio vettoriale su un campo $\mathbb K$ è un insieme $V$ dotato di due operazioni

$$
+:V\times V\longrightarrow V,
\qquad
\cdot:\mathbb K\times V\longrightarrow V,
$$

che soddisfano gli otto assiomi seguenti.

La somma è interna a $V$: due vettori danno un vettore. Il prodotto per scalare è esterno: uno scalare e un vettore danno un vettore. La notazione $\lambda v$ non introduce un prodotto tra due vettori.

Le operazioni devono essere definite per tutti gli elementi dei domini dichiarati e i risultati devono restare in $V$.

## Gli otto assiomi della lezione

Per ogni $u,v,w\in V$ e $\lambda,\mu\in\mathbb K$:

### V1 Associatività della somma

$$
(u+v)+w=u+(v+w).
$$

Consente di omettere le parentesi in una somma di più vettori.

### V2 Commutatività della somma

$$
u+v=v+u.
$$

### V3 Elemento neutro della somma

Esiste $0_V\in V$ tale che

$$
v+0_V=0_V+v=v.
$$

Questo assioma implica che $V$ non è vuoto.

### V4 Opposto additivo

Per ogni $v\in V$ esiste un vettore $v'\in V$ tale che

$$
v+v'=v'+v=0_V.
$$

Si indica poi con $-v$; l'unicità è dimostrata in [[40 Proprietà Elementari degli Spazi Vettoriali]].

### V5 Distributività rispetto alla somma di vettori

$$
\lambda(u+v)=\lambda u+\lambda v.
$$

### V6 Distributività rispetto alla somma di scalari

$$
(\lambda+\mu)v=\lambda v+\mu v.
$$

La somma a sinistra avviene nel campo; quella a destra in $V$.

### V7 Compatibilità dei prodotti per scalari

$$
(\lambda\mu)v=\lambda(\mu v).
$$

Poiché il campo è commutativo, vale anche $\lambda(\mu v)=\mu(\lambda v)$. Non si tratta di un prodotto di vettori.

### V8 Unità del campo

$$
1_{\mathbb K}v=v.
$$

L'1 del campo è distinto dal vettore nullo e dall'eventuale matrice identità in altri contesti.

## Verifica esemplificativa su matrici

Le matrici di dimensioni fissate $M_{\mathbb K}(m,n)$, con somma e prodotto per scalare già definiti, formano uno spazio vettoriale.

Per esempio V5 segue entrata per entrata:

$$
[\lambda(A+B)]_{ij}
=\lambda(a_{ij}+b_{ij})
=\lambda a_{ij}+\lambda b_{ij}
=[\lambda A+\lambda B]_{ij}.
$$

Si usa la distributività del campo. Lo stesso metodo trasferisce gli altri assiomi dalle entrate alle matrici.

Il vettore nullo è la matrice con tutte le entrate nulle; l'opposta è $(-a_{ij})$. La dimensione delle matrici deve rimanere fissata.

## Perché campo e operazioni fanno parte della definizione

Non basta nominare l'insieme. Bisogna specificare quali scalari e quali operazioni si usano.

Esempio del tutor: $\mathbb Z$ con le operazioni usuali non è uno spazio vettoriale su $\mathbb R$, perché $\frac12\cdot1\notin\mathbb Z$. Inoltre $\mathbb Z$ non è un campo.

L'insieme $\{0_V\}$ è invece uno spazio vettoriale: tutte le operazioni danno $0_V$ e gli assiomi sono soddisfatti.

## Non aggiungere strutture non date

Gli assiomi non forniscono automaticamente lunghezza, angolo, distanza, prodotto scalare o un ordine tra vettori. Tali concetti richiedono strutture ulteriori.

Le immagini aiutano per $\mathbb R^2$ e $\mathbb R^3$, ma la dimostrazione di una proprietà generale deve usare gli assiomi e non soltanto un disegno.

## Da dire all'orale

> Uno spazio vettoriale su un campo è un insieme con somma interna e prodotto esterno per scalari, con gli assiomi di gruppo abeliano per la somma e le quattro compatibilità con il campo. I vettori possono essere anche matrici, funzioni o polinomi.

## Fonte e collegamenti

- [[12 Campi Numerici e Campo F2]], [[13 Uguaglianza e Somma di Matrici]], [[14 Prodotto di una Matrice per uno Scalare]].
- [[39 Esempi di Spazi Vettoriali]], [[40 Proprietà Elementari degli Spazi Vettoriali]], [[41 Sottospazi Vettoriali e Criterio di Chiusura]].
- [[GAL 2026-2027 - 20261015 - LEZIONE 11.pdf#page=7|Lezione 11, p. 7, stampata 102]].
