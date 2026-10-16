---
course: Algebra Lineare
type: lecture
lecture: 7
date: 2026-10-08
status: da studiare
mastery: non verificata
source: "[[GAL 2026-2027 - 20261008 - LEZIONE 7.pdf]]"
---

# Lezione 7 dell'8 ottobre 2026

Stato: **da studiare**. Appunti preparati il 16 ottobre 2026, senza verifica della comprensione.

## Tema e fonte

Reversibilità del MEG, matrici elementari, rango tramite pivot, teorema di Binet e proprietà del determinante.

Il [[GAL 2026-2027 - 20261008 - LEZIONE 7.pdf|PDF originale]] ha 11 pagine, stampate da 62 a 72: pagina stampata = pagina PDF + 61.

## Sequenza e note complete

| Pagine PDF | Stampate | Contenuto | Approfondimento |
|---|---|---|---|
| 1 | 62 | Titolo e argomenti | questa panoramica |
| 2 | 63 | Inverse delle tre operazioni di riga | [[24 Operazioni Elementari e Metodo di Gauss]], [[26 Matrici Elementari e Reversibilità del MEG]] |
| 2-3 | 63-64 | Scambio, riscalamento e sostituzione codificati a sinistra | [[26 Matrici Elementari e Reversibilità del MEG]] |
| 4 | 65 | Prodotti $T,Z$ delle operazioni e loro inverse | [[26 Matrici Elementari e Reversibilità del MEG]] |
| 5-6 | 66-67 | Invarianza del rango e conteggio dei pivot | [[27 Calcolo del Rango con Gauss]] |
| 6 | 67 | Esempio di rango 2 | [[06 Gauss Rango Determinante e Inversa]] |
| 7 | 68 | Teorema di Binet e conseguenze | [[28 Teorema di Binet e Proprietà del Determinante]] |
| 7-8 | 68-69 | Conservazione dell'annullamento e calcolo con MEG | [[29 Calcolo del Determinante con Gauss]] |
| 8-10 | 69-71 | Normalizzazione, scambi, multilinearità e sostituzioni | [[28 Teorema di Binet e Proprietà del Determinante]] |
| 11 | 72 | Determinante nullo con due righe o colonne uguali | [[28 Teorema di Binet e Proprietà del Determinante]] |

## Filo logico

Le operazioni di Gauss si possono annullare e sono prodotti a sinistra per matrici invertibili. Questo permette di tornare da $U$ ad $A$ e giustifica l'invarianza del rango.

Contare le righe non nulle di $U$ diventa così un algoritmo per il rango. Per il determinante si usa invece Binet e si registra come ogni operazione ne modifica il valore.

## Dimostrazioni esplicitate dal tutor

- Inverse delle matrici elementari e ordine dei fattori.
- Invarianza del rango, usando decomposizioni colonna-riga in entrambi i versi.
- Rango di una matrice a scala e lemma necessario sulle combinazioni di righe.
- Binet mediante multilinearità nelle colonne.
- Effetti di scambio, riscalamento e sostituzione sul determinante.
- Criterio fra rango massimo, determinante non nullo e invertibilità.

## Precisazioni matematiche sui passaggi del PDF

Due punti vengono chiariti nelle note, senza riprodurre passaggi non giustificati:

1. Da $(ZT)A=A$ per una singola matrice $A$ non si può cancellare $A$. Le identità $ZT=TZ=I$ si dimostrano costruendo le inverse delle singole operazioni.
2. Da $2\det A=0$ si può concludere $\det A=0$ dividendo per 2 solo in caratteristica diversa da 2. La proprietà delle righe uguali resta vera anche in $\mathbb F_2$ e viene dimostrata senza questa divisione.

Le precisazioni sono integrazioni del tutor, con rimando ai passaggi originali.

## Esempi svolti e collegamenti

- [[06 Gauss Rango Determinante e Inversa]]: rango 2 del PDF, confronto fra Gauss e Laplace, inversa con identità affiancata e caso $\mathbb F_2$.
- Prerequisiti: [[20 Matrici Invertibili]], [[21 Rango e Prodotti Colonna per Riga]], [[22 Determinante e Sviluppo di Laplace]], [[24 Operazioni Elementari e Metodo di Gauss]].

Stato di tutto il materiale: **da studiare**. Nessuna verifica o promozione della padronanza.
