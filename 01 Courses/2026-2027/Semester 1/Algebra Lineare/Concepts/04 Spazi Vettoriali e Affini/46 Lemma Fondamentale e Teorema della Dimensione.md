---
course: Algebra Lineare
type: concept
status: da studiare
mastery: non verificata
created: 2026-11-03
source:
  - "Lezione 13, PDF p. 11, stampata 118"
  - "Lezione 15, PDF pp. 2-5, stampate 120-123"
---

# Lemma fondamentale e teorema della dimensione

Stato: **da studiare**.

## Perché serve un teorema sulla dimensione

Le coordinate di un vettore sono uniche **rispetto a una base fissata**. Resta da dimostrare che due basi dello stesso spazio abbiano lo stesso numero di elementi.

Il ponte è il confronto fra quanti vettori servono per generare e quanti possono essere indipendenti.

## Teorema 15.1: lemma fondamentale

Sia $V$ uno spazio vettoriale su $\mathbb K$. Se $T=(v_1,\ldots,v_m)$ genera $V$ e $S=(w_1,\ldots,w_n)$ contiene $n>m$ vettori di $V$, allora $S$ è linearmente dipendente.

Forma equivalente, particolarmente utile:

$$
\boxed{
S\text{ indipendente},\quad T\text{ generatrice}
\implies \#S\le\#T.
}
$$

Non è necessario che i generatori di $T$ siano indipendenti.

## Dimostrazione del lemma

Poiché $T$ genera $V$, ogni $w_j$ si scrive come combinazione dei $v_i$:

$$
w_j=\sum_{i=1}^{m}c_{ij}v_i.
$$

Raccogliamo i coefficienti nella matrice $C=(c_{ij})\in M_{\mathbb K}(m,n)$. Per scalari $\lambda_j$:

$$
\sum_{j=1}^{n}\lambda_jw_j
=\sum_{j=1}^{n}\lambda_j\sum_{i=1}^{m}c_{ij}v_i
=\sum_{i=1}^{m}\left(\sum_{j=1}^{n}c_{ij}\lambda_j\right)v_i.
$$

È sufficiente trovare $\lambda\ne0$ tale che tutti i coefficienti tra parentesi si annullino, cioè

$$
C\lambda=0.
$$

Questo sistema omogeneo ha $n$ incognite e rango

$$
r(C)\le m<n.
$$

Ha quindi almeno $n-r(C)>0$ parametri liberi. Ponendone uno uguale a 1 e gli altri a 0, si ottiene una soluzione non nulla. Per essa $\sum_j\lambda_jw_j=0$: $S$ è dipendente.

**Precisazioni al passaggio del PDF:**

- Il sistema $C\lambda=0$ è una condizione **sufficiente** per la relazione fra i $w_j$. Non è necessariamente equivalente, perché i $v_i$ potrebbero essere dipendenti.
- Non serve affermare che le soluzioni siano infinite: basta una soluzione non nulla. Il ragionamento vale anche sui campi finiti.

## Teorema 15.2: tutte le basi finite hanno la stessa lunghezza

Siano $\mathcal B=(v_1,\ldots,v_m)$ e $\mathcal C=(w_1,\ldots,w_n)$ due basi di $V$.

$\mathcal B$ genera e $\mathcal C$ è indipendente: il lemma dà $n\le m$.

Scambiando i ruoli, $\mathcal C$ genera e $\mathcal B$ è indipendente: $m\le n$.

Pertanto

$$
\boxed{m=n.}
$$

Questo rende ben posta la Definizione 13.6:

$$
\boxed{\dim_{\mathbb K}V=\text{numero di vettori di una base}.}
$$

Il campo fa parte dell'informazione. Il numero non dipende dalla base scelta, ma non è il numero di elementi dello spazio.

## Significato della dimensione

Se $\dim V=d<\infty$:

- ogni famiglia indipendente ha al massimo $d$ vettori;
- ogni famiglia generatrice ha almeno $d$ vettori;
- una base realizza entrambi gli estremi.

Quindi $d$ è il numero **massimo di vettori indipendenti** e il numero **minimo di generatori**.

Inoltre, per una famiglia con esattamente $d$ vettori:

$$
\boxed{\text{indipendente}\iff\text{generatrice}\iff\text{base}.}
$$

### Perché $d$ indipendenti generano

Se $d$ vettori indipendenti non generassero $V$, esisterebbe $u$ fuori dal loro span. Aggiungerlo conserverebbe l'indipendenza: in una relazione $\sum_i\lambda_iv_i+\mu u=0$, $\mu\ne0$ esprimerebbe $u$ nello span, impossibile; dunque $\mu=0$ e poi tutti i $\lambda_i=0$.

Avremmo $d+1$ indipendenti, contro il lemma applicato a una base di $d$ elementi.

### Perché $d$ generatori sono indipendenti

Se fossero dipendenti, una relazione non banale permetterebbe di rimuovere un vettore conservando lo span. Resterebbero $d-1$ generatori, impossibile per il limite minimo.

Questi passaggi esplicitano le implicazioni indicate nella Lezione 15.

## Esempi e limiti delle conclusioni

In $\mathbb R^3$:

- quattro vettori sono sempre dipendenti, ma possono generare tutto lo spazio;
- due vettori possono essere indipendenti, ma non possono generare tutto lo spazio;
- tre vettori sono una base se si verifica l'indipendenza **oppure** la generazione.

Il numero dei vettori da solo non prova una base: tre vettori collineari non sono una base di $\mathbb R^3$.

La dimensione zero corrisponde allo spazio $\{0\}$, con base vuota. Il vettore nullo non costituisce una base di un solo elemento, perché non è indipendente.

## Collegamento con rango e nucleo

Integrazione del tutor ai risultati precedenti: per $A:m\times n$, le direzioni prodotte da Gauss per $Ax=0$ generano il nucleo e sono indipendenti, perché nelle coordinate libere contengono rispettivamente i vettori canonici.

Pertanto

$$
\boxed{\dim\ker(A)=n-r(A).}
$$

Analogamente, [[48 Estrazione di una Base con Gauss]] mostra che lo span delle colonne e quello delle righe hanno entrambi dimensione $r(A)$.

## Da dire all'orale

> Il lemma fondamentale afferma che una famiglia indipendente non può avere più elementi di una famiglia generatrice dello stesso spazio. Applicandolo in entrambi i versi a due basi si ottiene che hanno la stessa lunghezza, cioè la dimensione dello spazio.

## Fonti e collegamenti

- [[45 Basi e Unicità delle Coordinate]], [[47 Basi Canoniche e Spazi Finitamente Generati]], [[49 Completamento di Vettori Indipendenti a una Base]].
- [[GAL 2026-2027 - 20261019 - LEZIONE 13.pdf#page=11|Lezione 13, p. 11, stampata 118]].
- [[GAL 2026-2027 - 20261028 - LEZIONE 15.pdf#page=2|Lezione 15, pp. 2-5, stampate 120-123]].
