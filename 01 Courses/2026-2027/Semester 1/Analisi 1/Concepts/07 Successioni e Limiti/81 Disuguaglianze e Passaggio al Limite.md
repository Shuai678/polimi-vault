---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 07, PDF pp. 14-15
  - Libro, §3.3.1, Corollario 3.29, p. 88
---

# Disuguaglianze e passaggio al limite

## I due corollari

Siano $a_n\to a\in\mathbb R$ e $b_n\to b\in\mathbb R$.

1. Se $a>b$, allora $a_n>b_n$ definitivamente. Se $a<b$, allora $a_n<b_n$ definitivamente.
2. Se $a_n\geq b_n$ definitivamente, allora $a\geq b$. Se $a_n\leq b_n$ definitivamente, allora $a\leq b$.

Le due direzioni hanno una differenza essenziale: una separazione **stretta fra i limiti** produce una separazione stretta fra i termini avanzati; passando dai termini ai limiti, invece, può comparire uguaglianza.

## Perché sono utili

Permettono di confrontare successioni usando i limiti, oppure di dedurre vincoli sul limite da disuguaglianze valide sulla coda. In entrambe le direzioni si suppone già che i due limiti esistano: il secondo corollario non ne prova l'esistenza.

## Strategia e dimostrazione

Trasformiamo il confronto fra due successioni in un confronto con zero ponendo

$$
c_n=a_n-b_n.
$$

Per [[80 Algebra dei Limiti di Successioni|algebra dei limiti]], $c_n\to a-b$.

Se $a>b$, il limite $a-b$ è strettamente positivo. Per [[79 Teorema di Permanenza del Segno|permanenza del segno]], $c_n>0$ definitivamente, cioè $a_n>b_n$ definitivamente.

Se invece $a_n\geq b_n$ definitivamente, allora $c_n\geq0$ definitivamente. Siccome il limite di $c_n$ esiste, la seconda parte della permanenza del segno dà

$$
a-b\geq0\quad\Longleftrightarrow\quad a\geq b.
$$

Gli enunciati con il verso opposto si ottengono scambiando le successioni.

### Da dire all'orale

> Se due successioni hanno limiti finiti distinti, per indici abbastanza grandi rispettano l'ordine stretto dei limiti. Viceversa, una disuguaglianza definitiva fra due successioni convergenti passa ai limiti nel senso non stretto. La prova si applica alla differenza delle successioni.

## Esempi e controesempi

Per $n\geq1$, $a_n=1/n$ e $b_n=0$ soddisfano $a_n>b_n$ per ogni indice, ma entrambi tendono a zero. Quindi

$$
a_n>b_n\text{ definitivamente}\quad\not\Rightarrow\quad a>b.
$$

Se i limiti coincidono, non possiamo neppure dedurre un ordine definitivo dei termini: $a_n=(-1)^n/n$ e $b_n=0$ hanno lo stesso limite, ma il loro ordine si inverte infinite volte.

Per un esempio con limiti distinti, poniamo

$$
a_n=2-\frac5n,\qquad b_n=1+\frac1n.
$$

Poiché $a=2>b=1$, il primo corollario assicura $a_n>b_n$ definitivamente. La soglia precisa si trova dalla differenza:

$$
a_n-b_n=1-\frac6n>0\Longleftrightarrow n>6.
$$

La disuguaglianza è quindi stretta da $n=7$ in poi; per $n=6$ c'è uguaglianza.

## Errori comuni e prospettiva d'esame

- Conservare il simbolo $>$ passando al limite senza ulteriori ipotesi.
- Concludere un ordine definitivo quando $a=b$.
- Usare le disuguaglianze soltanto per alcuni indici, invece che per tutti quelli oltre una soglia.
- Confondere questo risultato con il [[82 Teorema dei Due Carabinieri|teorema dei due carabinieri]], che permette invece di provare l'esistenza del limite della successione intermedia.

Potenziale rilevanza d'esame: conoscere entrambe le direzioni, la prova con $c_n=a_n-b_n$ e il controesempio che mostra la perdita della stretta disuguaglianza.
