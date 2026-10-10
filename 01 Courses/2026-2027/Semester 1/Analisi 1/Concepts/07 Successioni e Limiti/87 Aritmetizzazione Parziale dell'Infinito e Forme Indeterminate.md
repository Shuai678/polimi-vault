---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 08, PDF pp. 5-7
  - Libro, §3.3, pp. 84-86
---

# Aritmetizzazione parziale dell'infinito e forme indeterminate

## Intuizione

[[80 Algebra dei Limiti di Successioni]] riguarda limiti finiti. Alcune regole si estendono ai limiti infiniti, ma non tutte: due informazioni come $a_n\to0$ e $b_n\to+\infty$ non bastano a determinare il prodotto.

I simboli $+\infty$ e $-\infty$ descrivono comportamenti di successioni; **non sono numeri reali**. Scritture come $3\cdot(+\infty)=+\infty$ sono abbreviazioni di un teorema sui limiti.

## Somme determinate

Se $a_n\to a\in\mathbb R$ e $b_n\to+\infty$, allora $a_n+b_n\to+\infty$. Se $b_n\to-\infty$, il limite della somma è $-\infty$.

Inoltre, la somma di due successioni che tendono entrambe a $+\infty$ tende a $+\infty$; analogamente, due limiti $-\infty$ danno una somma con limite $-\infty$.

Una somma con infiniti di segno opposto presenta invece la forma indeterminata $+\infty-\infty$.

## Prodotti e segni

Se un fattore tende a un numero reale **non nullo** e l'altro a un infinito, il prodotto diverge con il segno dato dal prodotto dei segni. La stessa regola vale se entrambi i fattori hanno limite infinito.

| Primo limite | Secondo limite | Limite del prodotto |
|---|---|---|
| positivo non nullo, oppure $+\infty$ | $+\infty$ | $+\infty$ |
| positivo non nullo, oppure $+\infty$ | $-\infty$ | $-\infty$ |
| negativo non nullo, oppure $-\infty$ | $+\infty$ | $-\infty$ |
| negativo non nullo, oppure $-\infty$ | $-\infty$ | $+\infty$ |

Se uno dei limiti è zero e l'altro infinito, la regola non decide il risultato.

## Quozienti e significato di $0^+$ e $0^-$

La notazione

$$
b_n\to0^+\quad\Longleftrightarrow\quad b_n\to0\text{ e }b_n>0\text{ definitivamente}
$$

non indica un nuovo numero: aggiunge il segno con cui ci si avvicina a zero. Analogamente $0^-$ richiede $b_n<0$ definitivamente.

Se $a_n\to a\in\mathbb R\setminus\{0\}$,

| Segno di $a$ | Limite del denominatore | Limite di $a_n/b_n$ |
|---|---|---|
| $a>0$ | $0^+$ | $+\infty$ |
| $a>0$ | $0^-$ | $-\infty$ |
| $a<0$ | $0^+$ | $-\infty$ |
| $a<0$ | $0^-$ | $+\infty$ |

Questi casi restano validi se il numeratore tende rispettivamente a $+\infty$ o $-\infty$. Il denominatore deve essere definitivamente non nullo.

Se invece $a_n\to a\in\mathbb R$ e $b_n\to\pm\infty$, allora

$$
\frac{a_n}{b_n}\to0.
$$

Il semplice dato $b_n\to0$, senza il segno definitivo, non determina un infinito con segno. Per esempio $1/[(-1)^n/n]=(-1)^n n$ non ha limite.

## Perché le regole sono plausibili

Un fattore con limite $a>0$ resta definitivamente almeno $a/2$; moltiplicandolo per un fattore positivo che supera ogni soglia si ottiene ancora una successione che supera ogni soglia. Il caso $a<0$ si riconduce a questo cambiando segno. Il risultato di confronto è [[83 Teorema del Confronto per Limiti Infiniti]].

Per un denominatore infinito, $1/b_n\to0$: il numeratore convergente è limitato e si applica [[84 Confronto in Modulo e Prodotto con un Infinitesimo]]. Nel PDF le regole sono enunciate; questa spiegazione collega le conclusioni agli strumenti già disponibili.

## Forme indeterminate aritmetiche

$$
\boxed{\infty-\infty,\qquad0\cdot\infty,\qquad\frac\infty\infty,\qquad\frac00.}
$$

“Indeterminata” significa che **i limiti dei singoli pezzi non bastano**. Non significa che il limite dell'espressione sia impossibile da calcolare o che non esista. Occorre studiare l'espressione concreta.

## Esempio del PDF: quattro esiti per $0\cdot\infty$

Fissiamo $b_n=\sqrt7\,n\to+\infty$. Nei quattro casi seguenti $a_n\to0$:

| $a_n$ | Calcolo esatto di $a_nb_n$ | Esito |
|---|---|---|
| $1/n$ | $\sqrt7$ | limite $\sqrt7$ |
| $1/n^2$ | $\sqrt7/n$ | limite $0$ |
| $1/\sqrt n$ | $\sqrt7\sqrt n$ | limite $+\infty$ |
| $(-1)^n/n$ | $\sqrt7(-1)^n$ | nessun limite |

Nel quarto caso il fattore infinitesimo tende a zero perché il suo modulo è $1/n$, ma il prodotto alterna due valori distinti. Le stesse informazioni sui limiti dei fattori consentono quindi esiti diversi.

## Altri esempi brevi

$$
\frac{-3+1/n}{-1/n}=3n-1\to+\infty,
\qquad
\frac{2+1/n}{-n^2}\to0.
$$

Nel primo caso il numeratore tende a un numero negativo e il denominatore a $0^-$; nel secondo il numeratore ha limite finito e il denominatore tende a $-\infty$.

### Da dire all'orale

> L'aritmetizzazione dell'infinito è parziale: alcune combinazioni di limiti finiti e infiniti hanno un esito determinato, mentre le forme indeterminate richiedono un'analisi ulteriore della successione. Nei quozienti con denominatore infinitesimo va controllato anche il segno definitivo del denominatore.

## Uso negli esercizi ed errori comuni

- Prima si riconosce la forma, poi si sceglie una trasformazione: raccolta del termine dominante, razionalizzazione o passaggio a esponenziale e logaritmo.
- $0\cdot\infty$ non vale automaticamente zero; il teorema sul prodotto limitato per infinitesimo richiede un fattore **limitato**.
- $\infty-\infty$ non vale automaticamente zero.
- Non confondere $b_n\to0^-$ con $b_n\to-\infty$.

Le forme indeterminate delle potenze sono trattate in [[89 Limiti di Potenze con Base ed Esponente Variabili]]. Potenziale rilevanza d'esame: distinguere regole applicabili, condizioni sui segni e forme indeterminate.
