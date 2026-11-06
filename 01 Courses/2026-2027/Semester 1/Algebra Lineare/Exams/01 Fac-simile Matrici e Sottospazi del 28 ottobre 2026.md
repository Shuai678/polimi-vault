---
course: Algebra Lineare
type: exam-practice
status: da studiare
mastery: non verificata
created: 2026-11-03
source: "[[GAL 2026-2027 - 20261028 - LEZIONE 15.pdf#page=12]]"
---

# Fac-simile su matrici e sottospazi

Stato: **da studiare**. Il documento include già lo svolgimento del professore; i passaggi sono trascritti e verificati dal tutor. Non risulta una simulazione effettuata dallo studente.

## Fonte e paginazione

Il fac-simile è contenuto nelle **pagine PDF 12-15 della Lezione 15**. Ha una numerazione propria da 1 a 4: la p. 12 del PDF corrisponde alla p. 1 del fac-simile.

L'intestazione riporta «Giovedì 28 Ottobre 2026 - Fac-simile». Si conserva l'identificazione del documento senza dedurne la data di una prova effettivamente svolta o le regole amministrative dell'esame.

- PDF p. 12, fac-simile p. 1: testo.
- PDF p. 13, fac-simile p. 2: verifica di sottospazio e sistema delle entrate.
- PDF p. 14, fac-simile p. 3: basi di $V,W$ e impostazione della decomposizione.
- PDF p. 15, fac-simile p. 4: completamento dei calcoli.

## Testo

In $M_{\mathbb R}(2,2)$, con base canonica $(E_{11},E_{12},E_{21},E_{22})$, sia

$$
B=\begin{pmatrix}1&2\\3&6\end{pmatrix}.
$$

1. Dimostrare che $V=\{A\in M_{\mathbb R}(2,2):BA=0\}$ è un sottospazio.
2. Determinare dimensione e basi di $V$ e di
   $W=\operatorname{Span}(BE_{11},BE_{12},BE_{21},BE_{22})$.
3. Stabilire se esistono $A_1\in V$ e $A_2\in W$ tali che $A_1+A_2=I_2$; in caso affermativo esibirle.

## Prerequisiti e metodo

Usare distributività del prodotto matriciale, criterio di sottospazio, confronto delle entrate, sistemi omogenei, basi e dimensione. $A$ è la matrice incognita; $B$ è fissata e il prodotto è **$BA$**, non $AB$.

Prima si descrivono i sottospazi mediante parametri; poi si impone l'uguaglianza con l'identità confrontando quattro entrate.

> [!example]- Soluzione I - Dimostrare che V è un sottospazio
> La matrice nulla appartiene a $V$ perché $B0=0$.
>
> Se $A,C\in V$ e $\alpha,\beta\in\mathbb R$:
>
> $$
> B(\alpha A+\beta C)=\alpha BA+\beta BC=0.
> $$
>
> Quindi $\alpha A+\beta C\in V$. Per il criterio di chiusura, $V$ è un sottospazio.
>
> Nello svolgimento del PDF si verificano separatamente somma e scalare; qui si include esplicitamente anche la non-vuotezza tramite la matrice nulla.

> [!example]- Soluzione II - Base e dimensione di V
> Scriviamo $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$. Allora
>
> $$
> BA=
> \begin{pmatrix}a+2c&b+2d\\3a+6c&3b+6d\end{pmatrix}.
> $$
>
> Le quattro equazioni equivalgono a due:
>
> $$
> a+2c=0,\qquad b+2d=0,
> $$
>
> perché le altre sono i loro tripli. Poniamo $c=s$, $d=t$:
>
> $$
> A=\begin{pmatrix}-2s&-2t\\s&t\end{pmatrix}
> =sV_1+tV_2,
> $$
>
> $$
> V_1=\begin{pmatrix}-2&0\\1&0\end{pmatrix},
> \qquad
> V_2=\begin{pmatrix}0&-2\\0&1\end{pmatrix}.
> $$
>
> I due vettori generano $V$. Sono indipendenti: l'entrata $(2,1)$ della combinazione nulla impone $s=0$, quella $(2,2)$ impone $t=0$.
>
> Quindi $\mathcal B_V=(V_1,V_2)$ è una base e $\dim V=2$.

> [!example]- Soluzione III - Base e dimensione di W
> Calcoliamo i quattro generatori nello stesso ordine della base canonica:
>
> $$
> BE_{11}=\begin{pmatrix}1&0\\3&0\end{pmatrix}=W_1,\qquad
> BE_{12}=\begin{pmatrix}0&1\\0&3\end{pmatrix}=W_2,
> $$
>
> $$
> BE_{21}=\begin{pmatrix}2&0\\6&0\end{pmatrix}=2W_1,\qquad
> BE_{22}=\begin{pmatrix}0&2\\0&6\end{pmatrix}=2W_2.
> $$
>
> I due ultimi generatori sono ridondanti. I primi due sono indipendenti perché nelle entrate $(1,1)$ e $(1,2)$ della combinazione $\mu_1W_1+\mu_2W_2=0$ si leggono rispettivamente $\mu_1=0$ e $\mu_2=0$.
>
> Dunque $\mathcal B_W=(W_1,W_2)$ è una base e $\dim W=2$. In particolare,
>
> $$
> W=\left\{\begin{pmatrix}u&v\\3u&3v\end{pmatrix}:u,v\in\mathbb R\right\}.
> $$

> [!example]- Soluzione IV - Decomporre l'identità
> Cerchiamo
>
> $$
> A_1=\lambda_1V_1+\lambda_2V_2,\qquad
> A_2=\mu_1W_1+\mu_2W_2.
> $$
>
> Confrontando le entrate di $A_1+A_2=I_2$:
>
> $$
> \begin{cases}
> -2\lambda_1+\mu_1=1,\\
> -2\lambda_2+\mu_2=0,\\
> \lambda_1+3\mu_1=0,\\
> \lambda_2+3\mu_2=1.
> \end{cases}
> $$
>
> Le prime e terze equazioni coinvolgono solo $\lambda_1,\mu_1$. Dalla prima $\mu_1=1+2\lambda_1$:
>
> $$
> \lambda_1+3(1+2\lambda_1)=0
> \implies7\lambda_1=-3.
> $$
>
> Quindi $\lambda_1=-3/7$ e $\mu_1=1/7$.
>
> Dalla seconda $\mu_2=2\lambda_2$; sostituendo nella quarta:
>
> $$
> \lambda_2+6\lambda_2=1
> \implies\lambda_2=\frac17,\qquad\mu_2=\frac27.
> $$
>
> Otteniamo
>
> $$
> \boxed{
> A_1=\begin{pmatrix}6/7&-2/7\\-3/7&1/7\end{pmatrix},
> \qquad
> A_2=\begin{pmatrix}1/7&2/7\\3/7&6/7\end{pmatrix}.
> }
> $$
>
> Verifiche indipendenti:
>
> $$
> BA_1=\begin{pmatrix}0&0\\0&0\end{pmatrix},\qquad
> A_2=\frac17W_1+\frac27W_2\in W,
> $$
>
> $$
> A_1+A_2=
> \begin{pmatrix}(6+1)/7&(-2+2)/7\\(-3+3)/7&(1+6)/7\end{pmatrix}=I_2.
> $$
>
> La decomposizione richiesta esiste.

## Osservazione aggiuntiva del tutor sull'unicità

Se una matrice appartiene sia a $V$ sia a $W$, deve avere colonne del tipo $s(-2,1)^{\mathsf T}$ e contemporaneamente $u(1,3)^{\mathsf T}$. Per una colonna:

$$
-2s=u,\qquad s=3u
\implies7s=0\implies s=u=0.
$$

La stessa cosa vale per la seconda colonna. Quindi $V\cap W=\{0\}$.

Se $I_2=A_1+A_2=A_1'+A_2'$, la differenza $A_1-A_1'=A_2'-A_2$ appartiene all'intersezione, dunque è nulla: la decomposizione è unica. Questo approfondimento non è necessario per il solo quesito di esistenza.

## Avvertenze operative

- Non confondere $BE_{ij}$ con $E_{ij}B$.
- Quattro entrate di una matrice diventano quattro incognite scalari, nell'ordine fissato.
- Per chiamare una famiglia «base» servono generazione e indipendenza.
- $\dim V+\dim W=4$ da sola non dimostra l'esistenza della decomposizione: il sistema o l'intersezione vanno controllati.
- Il fac-simile documenta questo esercizio, non eventuali modalità o scadenze aggiornate dell'esame.

## Collegamenti e fonte

- [[16 Prodotto Matriciale Righe per Colonne]], [[41 Sottospazi Vettoriali e Criterio di Chiusura]], [[45 Basi e Unicità delle Coordinate]], [[47 Basi Canoniche e Spazi Finitamente Generati]].
- [[GAL 2026-2027 - 20261028 - LEZIONE 15.pdf#page=12|Testo: PDF p. 12, fac-simile p. 1]].
- [[GAL 2026-2027 - 20261028 - LEZIONE 15.pdf#page=13|Svolgimento: PDF pp. 13-15, fac-simile pp. 2-4]].
