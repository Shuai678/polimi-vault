---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 12, PDF pp. 28-30
---

# Equivalenti con esponente variabile nelle serie

## Perché serve una cautela nuova

L'equivalente $(1+x)^\beta-1\sim\beta x$ dei [[95 Equivalenti e Sviluppi Asintotici Notevoli|limiti notevoli]] è formulato per esponente $\beta$ **fissato**. Se l'esponente dipende da $n$, bisogna controllare anche il prodotto fra l'esponente e l'incremento della base.

Il metodo corretto usa la riscrittura [[89 Limiti di Potenze con Base ed Esponente Variabili|esponenziale-logaritmo]], prima di applicare gli equivalenti.

## Regola con esponente variabile

Supponiamo che $\varepsilon_n\to0$, $1+\varepsilon_n>0$ definitivamente e

$$
c_n\varepsilon_n\longrightarrow0.
$$

Se $\varepsilon_n$ e $c_n$ sono non nulli definitivamente, allora

$$
\boxed{(1+\varepsilon_n)^{c_n}-1\sim c_n\varepsilon_n.}
$$

Le condizioni di non nullità servono a definire il rapporto dell'equivalenza. In presenza di termini nulli si può usare la corrispondente identità con resto, trattando separatamente quegli indici.

### Dimostrazione

Poniamo

$$
t_n=c_n\log(1+\varepsilon_n).
$$

Poiché $\log(1+\varepsilon_n)/\varepsilon_n\to1$,

$$
t_n=c_n\varepsilon_n\,
\frac{\log(1+\varepsilon_n)}{\varepsilon_n}\longrightarrow0.
$$

Usando ora $e^{t_n}-1\sim t_n$,

$$
\frac{(1+\varepsilon_n)^{c_n}-1}{c_n\varepsilon_n}
=\frac{e^{t_n}-1}{t_n}
 \frac{\log(1+\varepsilon_n)}{\varepsilon_n}
\longrightarrow1\cdot1=1.
$$

Abbiamo controllato che l'argomento del secondo equivalente tende davvero a zero: è il passaggio che non si può omettere.

## Esercizio conclusivo del docente

### Testo

Discutere, al variare di $\alpha\in\mathbb R$,

$$
\sum_{n=2}^{+\infty}
\frac{\left[(1+\sin(1/n))^{\log n}-1\right]^\alpha}
{(1+\log\log n+\log n)\,\log\bigl((2n+1)^2\bigr)}.
$$

> [!note] Leggere correttamente la formula
> Nel denominatore compare $\log\bigl((2n+1)^2\bigr)=2\log(2n+1)$, **non** $[\log(2n+1)]^2$. Il quadrato è dentro l'argomento del logaritmo. Inoltre $\log\log n$ significa $\log(\log n)$.

### Idea

Il termine è positivo. Si cerca un equivalente positivo della forma $C/[n^p(\log n)^\beta]$, poi si usa la classificazione delle [[108 Serie Armoniche Generalizzate e di Bertrand|serie di Bertrand]] tramite [[109 Criterio del Confronto Asintotico per Serie|confronto asintotico]].

### 1. Dominio e segno

Per $n\geq2$, $\sin(1/n)>0$ e $\log n>0$, quindi

$$
h_n=(1+\sin(1/n))^{\log n}-1>0.
$$

La potenza $h_n^\alpha$ è definita e positiva per ogni parametro reale, anche negativo. Il denominatore è positivo definitivamente; anche i primi termini da $2$ sono definiti e positivi. Per verificarlo senza approssimazioni, dalla stima $e\leq4$ segue $\log2\geq1/2$; per $n\geq2$,

$$
\log\log n\geq\log(1/2)=-\log2,
\quad\log n\geq\log2,
\quad1+\log\log n+\log n\geq1.
$$

L'altro fattore, $\log((2n+1)^2)$, è positivo perché $(2n+1)^2>1$.

### 2. L'incremento della potenza variabile

Poniamo $\varepsilon_n=\sin(1/n)$ e $c_n=\log n$. Vale

$$
\varepsilon_n\sim\frac1n,\qquad
c_n\varepsilon_n\sim\frac{\log n}{n}\longrightarrow0.
$$

La regola appena dimostrata è dunque applicabile e fornisce

$$
h_n\sim(\log n)\sin(1/n)\sim\frac{\log n}{n}.
$$

Equivalentemente, il PDF passa attraverso

$$
t_n=(\log n)\log(1+\sin(1/n))
\sim\frac{\log n}{n}\to0,
\qquad h_n=e^{t_n}-1\sim t_n.
$$

Per $\alpha$ fissato, le quantità sono positive e

$$
\frac{h_n^\alpha}{(\log n/n)^\alpha}
=\left(\frac{h_n}{\log n/n}\right)^\alpha\longrightarrow1.
$$

Quindi $h_n^\alpha\sim(\log n)^\alpha/n^\alpha$. Questo vale anche per $\alpha=0$, caso in cui entrambi i membri valgono esattamente $1$.

### 3. Equivalente del denominatore

Poiché $\log\log n/\log n\to0$ per la gerarchia, applicata alla variabile $\log n\to+\infty$,

$$
\frac{1+\log\log n+\log n}{\log n}
=\frac1{\log n}+\frac{\log\log n}{\log n}+1\to1.
$$

Per il secondo fattore,

$$
\log\bigl((2n+1)^2\bigr)
=2\log(2n+1)
=2\log n+2\log\left(2+\frac1n\right)
\sim2\log n.
$$

Il termine $\log(2+1/n)$ ha limite finito, mentre $\log n\to+\infty$. Pertanto il denominatore complessivo è equivalente a $2(\log n)^2$.

### 4. Confronto con Bertrand

Chiamando $u_n$ il termine generale,

$$
u_n\sim
\frac{(\log n)^\alpha/n^\alpha}{2(\log n)^2}
=\frac1{2n^\alpha(\log n)^{2-\alpha}}.
$$

Il fattore $1/2>0$ non cambia il carattere. Nella serie di Bertrand i parametri sono

$$
p=\alpha,\qquad\beta=2-\alpha.
$$

- Se $\alpha>1$, $p>1$: la serie converge per qualunque valore del fattore logaritmico.
- Se $\alpha<1$, $p<1$: la serie diverge a $+\infty$.
- Se $\alpha=1$, $\beta=1$: resta il caso limite $\sum1/(n\log n)$, che diverge. La costante $1/2$ non cambia la conclusione.

### Risultato

$$
\boxed{\text{La serie converge se e solo se }\alpha>1;
\text{ per }\alpha\leq1\text{ diverge a }+\infty.}
$$

## Cosa imparare ed errori comuni

La condizione decisiva nella potenza variabile è $c_n\varepsilon_n\to0$, non il solo fatto che la base tenda a $1$. Ad esempio, $(1+1/n)^n-1\to e-1$, mentre $n(1/n)=1$: il rapporto non tende a $1$, quindi la stessa equivalenza non vale se il prodotto non tende a zero.

Nelle espressioni con una sottrazione di $1$, prima si espone la piccola quantità tramite esponenziale e logaritmo; non si sostituisce soltanto l'intera potenza con $1$, perché si perderebbe proprio il termine che decide il carattere. È lo stesso problema di precisione discusso in [[97 Cancellazioni e Precisione del Resto Asintotico]].

Dopo il confronto con Bertrand occorre sempre sostituire il valore di frontiera $\alpha=1$: il criterio distingue $\beta>1$ da $\beta=1$. Non basta concludere sulla base dei due intervalli aperti.

### Da dire all'orale

> Per una potenza con esponente variabile scrivo la base alla c enne come esponenziale di c enne per il logaritmo della base. Posso usare l'equivalente dell'esponenziale meno uno solo dopo aver mostrato che questo nuovo esponente tende a zero. Nell'esercizio ottengo una serie di Bertrand con esponenti alfa e due meno alfa; il caso alfa uguale a uno dà uno su enne logaritmo di enne e diverge.
