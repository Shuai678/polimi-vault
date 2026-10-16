---
course: Algebra Lineare
type: lecture
lecture: 6
date: 2026-10-07
status: da studiare
mastery: non verificata
source: "[[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf]]"
---

# Lezione 6 del 7 ottobre 2026

Stato: **da studiare**. Appunti preparati il 16 ottobre 2026, senza verifica della comprensione.

## Tema e fonte

Inverse, rango tramite prodotti colonna-riga, determinante, matrici triangolari, algoritmo di Gauss e forma a scala.

Il [[GAL 2026-2027 - 20261007 - LEZIONE 6.pdf|PDF originale]] ha 17 pagine, stampate da 45 a 61: pagina stampata = pagina PDF + 44.

La numerazione originale è mantenuta; non si ricostruisce una Lezione 5 non fornita.

## Sequenza e note complete

| Pagine PDF | Stampate | Contenuto | Approfondimento |
|---|---|---|---|
| 1 | 45 | Titolo e argomenti | questa panoramica |
| 2 | 46 | Definizione 6.1 di inverse destra, sinistra e bilatera | [[20 Matrici Invertibili]] |
| 3 | 47 | Proposizione 6.2, coincidenza e unicità | [[20 Matrici Invertibili]] |
| 4 | 48 | Non commutatività, colonna-riga, definizione 6.3 di rango | [[16 Prodotto Matriciale Righe per Colonne]], [[21 Rango e Prodotti Colonna per Riga]] |
| 5-6 | 49-50 | Decomposizioni, limiti del rango e probabilità congiunte | [[21 Rango e Prodotti Colonna per Riga]] |
| 6 | 50 | Esempio proposto sui due dadi | [[05 Rango Laplace e Matrici Triangolari]] |
| 7-9 | 51-53 | Definizione 6.4, Laplace ed esempio di determinante 20 | [[22 Determinante e Sviluppo di Laplace]] |
| 10 | 54 | Riga nulla e definizione 6.5 di triangolare | [[22 Determinante e Sviluppo di Laplace]], [[23 Matrici Diagonali e Triangolari]] |
| 11 | 55 | Determinante della triangolare e obiettivi del corso | [[23 Matrici Diagonali e Triangolari]] |
| 12-14 | 56-58 | Tre operazioni elementari e algoritmo MEG | [[24 Operazioni Elementari e Metodo di Gauss]] |
| 15-16 | 59-60 | Esempio completo $3\times4$ | [[05 Rango Laplace e Matrici Triangolari]] |
| 16-17 | 60-61 | Definizione 6.6, pivot e matrice a scala | [[25 Pivot e Matrici a Scala]] |

## Filo logico

L'identità rende possibile chiedere l'esistenza di un'inversa per il prodotto. La rappresentazione mediante prodotti colonna-riga introduce il rango come minimo numero di addendi.

Il determinante viene definito ricorsivamente con Laplace. La sua formula particolarmente semplice sulle triangolari motiva la ricerca di una procedura che trasformi le matrici in forma a scala: il MEG.

## Dimostrazioni e calcoli

- Coincidenza dell'inversa destra e sinistra, con dimensioni e associatività esplicite.
- Unicità dell'inversa.
- Limite $r(A)\le\min(m,n)$ tramite decomposizioni per righe e colonne.
- Fattorizzazione della tabella di probabilità della moneta e del dado.
- Soluzione completa del problema sulla parità dei due dadi, assumendoli equi e indipendenti.
- Determinante 20 della matrice del professore, sviluppato su due scelte diverse.
- Determinante triangolare mediante ricorsione sulla prima colonna o riga.
- Tutte le operazioni intermedie nell'esempio reale con pivot 1, $-1$ e 12.

Il rango è presentato secondo la definizione del docente, senza sostituirla subito con il solo conteggio dei pivot: il collegamento viene dimostrato nella [[27 Calcolo del Rango con Gauss|nota della Lezione 7]].

## Esempi svolti e collegamenti

- [[05 Rango Laplace e Matrici Triangolari]].
- Per un successivo calcolo dell'inversa: [[06 Gauss Rango Determinante e Inversa]].
- Prerequisiti: [[16 Prodotto Matriciale Righe per Colonne]], [[19 Proprietà del Prodotto e Matrice Identità]].
- Segue: [[01 Courses/2026-2027/Semester 1/Algebra Lineare/Lectures/Lecture 07|Lezione 7]].

Tutti gli argomenti ed esempi restano **da studiare**. I calcoli preparati dal tutor non sono attribuiti allo studente.
