---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-10-16
source:
  - "Lezione 6, PDF pp. 12-17, stampate 56-61"
  - "Lezione 7, PDF p. 2, stampata 63"
---

# Operazioni elementari e metodo di Gauss

Stato: **da studiare**.

## Obiettivo

Il metodo di eliminazione di Gauss, abbreviato **MEG** nel PDF, trasforma una matrice $A\in M_{\mathbb K}(m,n)$ in una matrice [[25 Pivot e Matrici a Scala|a scala]] $U$ dello stesso tipo.

La riduzione concentra le entrate non nulle verso l'alto e a destra, mediante operazioni reversibili sulle righe. Se la matrice è quadrata, l'uscita è triangolare superiore.

## Le tre operazioni consentite

| Operazione | Notazione | Condizioni | Operazione inversa |
|---|---|---|---|
| Scambio | $R_i\leftrightarrow R_j$ | $i\ne j$ | stesso scambio |
| Riscalamento | $R_i\leftarrow\lambda R_i$ | $\lambda\ne0$ | moltiplicazione per $\lambda^{-1}$ |
| Sostituzione | $R_i\leftarrow R_i+\lambda R_k$ | $i\ne k$ | $R_i\leftarrow R_i-\lambda R_k$ |

Ogni operazione agisce sull'intera riga, incluse le entrate a destra del pivot. Moltiplicare una riga per zero non è consentito: non sarebbe reversibile.

La sostituzione lascia invariata la riga $R_k$ usata per costruire il multiplo.

## Esempi iniziali del PDF

- Scambiando le righe di $\begin{pmatrix}0&0&1\\2&3&7\end{pmatrix}$ si ottiene $\begin{pmatrix}2&3&7\\0&0&1\end{pmatrix}$.
- Moltiplicando per $10^4$ la riga $(10^{-8},4,7)$ si ottiene $(10^{-4},4\cdot10^4,7\cdot10^4)$.
- Applicando $R_2\leftarrow R_2-4R_1$ a $\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}$ si ottiene $\begin{pmatrix}1&2&3\\0&-3&-6\end{pmatrix}$.

I calcoli numerici qui sono su $\mathbb R$.

## L'algoritmo del professore

### Casi di arresto

La matrice nulla è già a scala. Anche una matrice con una sola riga è a scala.

### Passo 1 Individuare la prima colonna utile

Nella matrice ancora da trattare si cerca, da sinistra, la prima colonna che contiene un elemento non nullo. Se non esiste, tutte le righe rimaste sono nulle.

### Passo 2 Scegliere una riga

In quella colonna si sceglie una riga con entrata non nulla. Questa entrata diventa il pivot.

### Passo 3 Portare il pivot nella prima riga attiva

Se necessario si scambia la riga scelta con la prima riga della parte ancora da trattare.

### Passo 4 Annullare sotto il pivot

Se il pivot nella riga attiva è $p\ne0$ e nella stessa colonna una riga inferiore ha entrata $a$, si applica

$$
R_{\mathrm{inferiore}}
\leftarrow
R_{\mathrm{inferiore}}-\frac apR_{\mathrm{pivot}}.
$$

L'entrata da eliminare diventa

$$
a-\frac ap\,p=a-a=0.
$$

La divisione è lecita perché si lavora in un campo e $p\ne0$. L'operazione modifica anche le altre entrate della riga.

### Passo 5 Ripetere sulle righe inferiori

Si lascia fissa la riga del pivot e si ripete il procedimento sulle righe rimaste. Nel PDF la ricorsione mantiene tutte le colonne; quelle già trattate sono nulle nelle righe inferiori e i nuovi pivot si trovano quindi più a destra.

## Termine e scelte

Ogni passaggio fissa una nuova riga con pivot o conclude che le righe rimaste sono nulle. Il numero di passaggi è finito.

La scelta della riga pivot non è unica. L'uscita a scala può cambiare, ma il [[27 Calcolo del Rango con Gauss|numero dei pivot]] rimane lo stesso.

Non è obbligatorio trasformare ogni pivot in 1. Un eventuale riscalamento deve essere registrato, specialmente nel [[29 Calcolo del Determinante con Gauss|calcolo del determinante]].

## Esempio completo della lezione

La riduzione della matrice reale

$$
A=\begin{pmatrix}
0&0&2&0\\
1&0&1&-1\\
2&0&1&4
\end{pmatrix}
$$

è riportata passo per passo in [[05 Rango Laplace e Matrici Triangolari]]. Vi si ottiene

$$
U=\begin{pmatrix}
1&0&1&-1\\
0&0&-1&6\\
0&0&0&12
\end{pmatrix}.
$$

## Precauzioni operative

- Non scegliere un pivot nullo.
- Non cambiare una sola entrata invece dell'intera riga.
- Non confondere operazioni di riga e di colonna.
- Non trattare l'ultima colonna come termini noti se il testo ha fornito soltanto una matrice.
- Non supporre che il determinante rimanga invariato sotto tutti e tre i tipi di operazione.

## Da dire all'orale

> Il metodo di Gauss usa scambi, riscalamenti non nulli e somme di multipli di altre righe per ottenere una matrice a scala. Ogni pivot viene usato per annullare le entrate sottostanti, poi si procede sulle righe inferiori.

## Collegamenti e fonti

- [[25 Pivot e Matrici a Scala]], [[26 Matrici Elementari e Reversibilità del MEG]].
- [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf#page=12|Lezione 6, pp. 12-17, stampate 56-61]].
- [[GAL 2026-2027 - 20261008 - LEZIONE 7.pdf#page=2|Lezione 7, p. 2, stampata 63]].
