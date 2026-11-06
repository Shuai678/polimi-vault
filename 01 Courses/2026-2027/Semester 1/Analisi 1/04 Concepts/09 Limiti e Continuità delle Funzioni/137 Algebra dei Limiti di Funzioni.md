---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 23-24
---

# Algebra dei limiti di funzioni

## Teorema richiamato dal docente

Siano $f,g:I\subseteq\mathbb R\to\mathbb R$, con $x_0\in\overline{\mathbb R}$ punto di accumulazione per $I$, e supponiamo

$$
\lim_{x\to x_0}f(x)=\ell_1,
\qquad
\lim_{x\to x_0}g(x)=\ell_2,
\qquad\ell_1,\ell_2\in\overline{\mathbb R}.
$$

Il professore riprende, nell'ordine seguente, le regole già viste per le successioni. Le formule danno una conclusione quando l'operazione sui limiti è definita e non presenta una delle forme escluse sotto.

### 1. Somma e differenza

$$
\lim_{x\to x_0}(f(x)\pm g(x))=\ell_1\pm\ell_2.
$$

Per limiti finiti la regola si applica sempre. Con limiti infiniti occorre escludere le combinazioni del tipo $+\infty-\infty$.

### 2. Prodotto

$$
\lim_{x\to x_0}f(x)g(x)=\ell_1\ell_2.
$$

Il caso $0\cdot\infty$ non è deciso da questa formula. Un fattore infinitesimo per un fattore **limitato** è invece già trattato dai [[135 Proprietà Definitive e Teoremi di Confronto per Funzioni|corollari di confronto]].

### 3. Quoziente

$$
\lim_{x\to x_0}\frac{f(x)}{g(x)}=\frac{\ell_1}{\ell_2},
$$

quando il rapporto sui limiti è determinato. La funzione quoziente deve essere definita: serve $g(x)\neq0$ definitivamente, come specifica il docente. Per $\ell_2$ reale non nullo ciò segue dalla permanenza del segno. Il solo fatto che $g$ non sia mai nulla non risolve i casi $0/0$, $\infty/\infty$ o quelli con denominatore tendente a zero senza segno fissato.

### 4. Potenza con esponente variabile

$$
\lim_{x\to x_0}(f(x))^{g(x)}=\ell_1^{\ell_2},
$$

nei casi determinati dell'aritmetizzazione richiamata. Il PDF richiede **$f(x)>0$** in un intorno del punto, escluso al più il centro, così l'esponente reale variabile è ammesso. Se $\ell_1>0$ è finito e $\ell_2$ è finito, il risultato è quello usuale. Le forme $1^{\pm\infty}$, $\infty^0$, $0^0$ richiedono altro studio.

### 5. Potenza con esponente reale fissato

Per $\alpha\in\mathbb R$ fissato,

$$
\lim_{x\to x_0}(f(x))^\alpha=\ell_1^\alpha,
$$

quando l'espressione del limite è definita nel caso considerato. Il docente richiede che $(f(x))^\alpha$ sia definita in un intorno del punto, escluso al più il centro. Per esponenti negativi si esclude la base nulla; per radici di indice pari si controlla il segno. Per $\alpha=0$ e base non nulla la funzione potenza vale direttamente $1$.

## Forme escluse dalla regola diretta — ordine del PDF

$$
[\infty-\infty],\quad[0\cdot\infty],\quad
\left[\frac00\right],\quad\left[\frac\infty\infty\right],
\quad[1^{\pm\infty}],\quad[\infty^0],\quad[0^0].
$$

Il professore richiama anche il caso

$$
\left[\frac{\ell_1}{0}\right],\qquad
\ell_1\in\mathbb R\setminus\{0\},
$$

quando il denominatore tende a zero **senza segno specificato**. Il limite del rapporto non è determinato dai soli valori dei due limiti: bisogna studiare il segno e, quando necessario, i limiti laterali.

## Commenti: perché il segno del denominatore conta

Per $x\to0$, sia $1/x$ sia $1/x^2$ hanno numeratore tendente a $1$ e denominatore tendente a zero. Eppure $1/x$ non ha limite bilatero, mentre $1/x^2\to+\infty$. Per $1/x$, i limiti laterali sono $+\infty$ e $-\infty$; il dato “zero” del denominatore non conteneva l'informazione sul lato.

Una forma indeterminata non è il risultato del limite, e non prova che il limite non esista. Segnala che le regole algebriche dirette non bastano. Si possono usare trasformazioni algebriche, confronti o metodi già introdotti per le successioni, verificando il loro impiego nel contesto delle funzioni.

## Collegamenti e confine della lezione

Riferimenti già disponibili: [[80 Algebra dei Limiti di Successioni]], [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate]], [[89 Limiti di Potenze con Base ed Esponente Variabili]]. Il PDF L14 termina dopo questo richiamo: non sono qui anticipati nuovi teoremi sulla composizione o nuovi sviluppi di calcolo differenziale.

### Da dire all'orale

> Le regole algebriche dei limiti di funzione riprendono quelle delle successioni. Oltre all'esistenza dei limiti, devo controllare che le operazioni siano definite vicino al punto e che l'operazione sui limiti sia determinata. Nei quozienti verifico il denominatore, nelle potenze il dominio reale e nelle forme indeterminate cambio metodo.
