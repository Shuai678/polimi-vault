---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 11, PDF pp. 16-17
  - Lezione 12, PDF pp. 6-8, applicazioni
  - Libro, §4.2.2, pp. 122-124; teorema 4.20 ed esempio 4.22
---

# Criterio della radice per serie

## Quando si usa e intuizione

La radice $n$-esima evidenzia la crescita o la decrescita esponenziale dei termini. È particolarmente comoda quando il termine contiene una potenza con esponente $n$. Se $\sqrt[n]{a_n}$ resta sotto $q<1$, allora $a_n\leq q^n$ e la serie è confrontabile con una geometrica convergente.

## Teorema e ipotesi

Sia $a_n\geq0$ definitivamente e supponiamo che esista

$$
\ell=\lim_{n\to+\infty}\sqrt[n]{a_n}\in[0,+\infty].
$$

Allora

$$
\boxed{
\begin{aligned}
0\leq\ell<1&\Longrightarrow\sum a_n\text{ converge e }a_n\to0,\\
\ell>1&\Longrightarrow\sum a_n=+\infty\text{ e }a_n\to+\infty.
\end{aligned}}
$$

Il secondo caso include $\ell=+\infty$; per **$\ell=1$ il criterio non è conclusivo**. “Positivi” è usato nel senso non negativo precisato dal docente: la radice reale è definita anche per termine nullo. A differenza del rapporto, qui non si divide per $a_n$.

## Dimostrazione di supporto

> [!info] Approfondimento dal libro
> Il PDF enuncia il criterio della radice. La prova del teorema 4.20, pp. 122-123, usa il confronto diretto con una geometrica; si esplicitano anche i limiti dei termini presenti nell'enunciato del docente.

### Caso $\ell<1$

Scegliamo $q$ con $\ell<q<1$. Definitivamente

$$
0\leq\sqrt[n]{a_n}\leq q.
$$

Elevando a $n$, operazione crescente su quantità non negative,

$$
0\leq a_n\leq q^n.
$$

La geometrica $\sum q^n$ converge; per il [[107 Criterio del Confronto per Serie]] converge anche $\sum a_n$. Inoltre $q^n\to0$, quindi $a_n\to0$.

### Caso $\ell>1$

Scegliamo $r$ con $1<r<\ell$ per $\ell$ finito, oppure un qualunque $r>1$ se $\ell=+\infty$. Definitivamente $\sqrt[n]{a_n}\geq r$, dunque

$$
a_n\geq r^n\to+\infty.
$$

La condizione necessaria di convergenza fallisce. La serie, definitivamente non negativa, diverge a $+\infty$.

## Esempio del PDF: perché il valore uno è inconclusivo

Per $a_n=n^{-\alpha}$, con $\alpha\in\mathbb R$ fissato,

$$
\sqrt[n]{a_n}=e^{-\alpha\log n/n}\to1.
$$

La giustificazione completa e il rapporto consecutivo sono in [[108 Serie Armoniche Generalizzate e di Bertrand]]. Poiché la serie converge per $\alpha>1$ e diverge per $\alpha\leq1$, il valore $1$ non decide. Non basta nemmeno sapere che ogni radice è minore di $1$: occorre un limite strettamente minore di $1$ per applicare il primo caso.

## Esempio di supporto — Un fattore polinomiale su una geometrica

> [!info] Approfondimento dal libro
> L'esempio 4.22, pp. 123-124, studia $\sum n/3^n$ con il criterio della radice. Il calcolo impiega il limite $n^{1/n}\to1$ già presente nel vault.

Per $a_n=n/3^n>0$,

$$
\sqrt[n]{a_n}=\frac{n^{1/n}}3
=\frac{e^{\log n/n}}3\to\frac13<1.
$$

La [[85 Gerarchia degli Infiniti|gerarchia]] dà $\log n/n\to0$ e il limite dell'esponenziale dà $n^{1/n}\to1$. Pertanto

$$
\boxed{\sum_{n=1}^{+\infty}\frac n{3^n}\text{ converge}.}
$$

Il fattore $n$ non cambia il limite della radice, mentre il denominatore geometrico produce il valore $1/3$.

## Confronto pratico con il criterio del rapporto

Con fattoriali e prodotti successivi spesso si semplifica meglio il rapporto; con espressioni elevate alla $n$ spesso si semplifica meglio la radice. Entrambi confrontano il limite ottenuto con $1$, ma richiedono calcoli diversi e non bisogna scambiare le due espressioni.

Se il limite della radice non esiste, questo teorema nella forma enunciata non fornisce una conclusione. Se vale $1$, si usa un'altra famiglia campione o un confronto disponibile.

### Da dire all'orale

> Per una serie a termini definitivamente non negativi, se la radice ennesima del termine tende a un valore minore di uno, la serie converge; se tende a un valore maggiore di uno, incluso più infinito, la serie diverge positivamente e i termini tendono a più infinito. Per limite uguale a uno non si può concludere. La prova eleva a n una disuguaglianza e confronta con una geometrica.

Potenziale rilevanza d'esame: scelta del criterio, trattamento degli esponenti e distinzione fra limite uguale a uno e limite strettamente minore di uno.

## Applicazioni della Lezione 12 — Da studiare

In [[113 Serie con Fattori Esponenziali Potenze e Logaritmi]] la radice decide la convergenza di $\sum a^n/n^n$ per ogni $a\geq0$ e di $\sum n^a b^n$ per $b\neq1$; per $b=1$ si torna alle armoniche generalizzate. La nota raccoglie i calcoli senza duplicarli qui.
