---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 10, PDF pp. 15-16
  - Libro, §4.1, p. 116; proposizione 4.8
---

# Linearità e algebra delle serie

## Intuizione

Le proprietà delle somme finite passano alle serie mediante il limite delle somme parziali. Il passaggio richiede che i limiti coinvolti esistano e che l'operazione finale sia ammessa dall'[[80 Algebra dei Limiti di Successioni|algebra dei limiti]]: non si può manipolare qualsiasi somma infinita come un numero reale.

## Teorema per serie convergenti

Se $\sum_{n=0}^{+\infty}a_n=A\in\mathbb R$ e $\sum_{n=0}^{+\infty}b_n=B\in\mathbb R$, per ogni $\alpha,\beta\in\mathbb R$ la serie delle combinazioni lineari converge e

$$
\boxed{\sum_{n=0}^{+\infty}(\alpha a_n+\beta b_n)
=\alpha A+\beta B.}
$$

Le ipotesi riguardano la convergenza delle **due serie**, non soltanto quella delle successioni $(a_n)$ e $(b_n)$.

## Dimostrazione passo per passo

Poniamo $A_N=\sum_{n=0}^{N}a_n$ e $B_N=\sum_{n=0}^{N}b_n$. Per la distributività nelle somme finite,

$$
C_N=\sum_{n=0}^{N}(\alpha a_n+\beta b_n)
=\alpha A_N+\beta B_N.
$$

Per ipotesi $A_N\to A$ e $B_N\to B$, entrambi finiti. Quindi

$$
\lim_{N\to+\infty}C_N
=\alpha\lim_{N\to+\infty}A_N+\beta\lim_{N\to+\infty}B_N
=\alpha A+\beta B.
$$

Il limite di $C_N$ è la somma della nuova serie per [[99 Serie Numeriche e Somme Parziali]].

## Estensione alle serie regolari nel PDF

Se le due serie sono regolari, con somme eventualmente infinite, la stessa formula vale **quando l'espressione a destra ha significato e non è una forma indeterminata**. Prima si moltiplicano le somme per i coefficienti, tenendo conto dei segni, poi si controlla l'addizione finale.

Per esempio, una somma finita più $+\infty$ dà $+\infty$; $+\infty+(+\infty)$ dà $+\infty$. Invece $+\infty+(-\infty)$ non è determinata dai due limiti separati. Si usano le regole di [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate]].

Se un coefficiente è zero, eliminiamo prima quel contributo nelle somme finite. La successione nulla ha limite zero: non occorre attribuire un valore numerico alla scrittura $0\cdot\infty$.

### Esempio svolto — Due geometriche convergenti

$$
\begin{aligned}
\sum_{n=0}^{+\infty}\left(\frac3{2^n}-\frac2{3^n}\right)
&=3\sum_{n=0}^{+\infty}\left(\frac12\right)^n
-2\sum_{n=0}^{+\infty}\left(\frac13\right)^n\\
&=3\cdot2-2\cdot\frac32=3.
\end{aligned}
$$

La separazione è giustificata perché entrambe le serie geometriche convergono. Prima si verificano le ipotesi, poi si applica la formula.

## Perché non si possono sottrarre somme infinite indeterminate

Consideriamo $a_n=1$ e $b_n=-1$ per ogni $n$. Le rispettive serie divergono a $+\infty$ e $-\infty$. Però $a_n+b_n=0$ e la serie della somma dei termini vale $0$.

Non abbiamo calcolato $+\infty-\infty=0$: abbiamo sommato i termini **prima del limite**, ottenendo somme parziali nulle. Se invece scegliessimo $a_n=2$ e $b_n=-1$, le due serie separate avrebbero ancora limiti $+\infty$ e $-\infty$, ma la serie della somma dei termini divergerebbe a $+\infty$. I due limiti separati non bastano a decidere.

## Uso negli esercizi ed errori comuni

La linearità consente di combinare serie già note, per esempio geometriche e telescopiche. Conviene prima accertarne il carattere. Se una scomposizione genera una forma indeterminata, si torna alle somme parziali oppure si semplifica il termine generale prima di separare.

- Non separare una serie convergente in una differenza di due serie divergenti e poi sottrarre gli infiniti.
- Non ricavare dalla convergenza della somma la convergenza dei due addendi: l'esempio $1+(-1)$ lo smentisce.
- Non applicare un teorema per serie regolari a serie irregolari senza uno studio diretto delle somme parziali.

### Da dire all'orale

> La combinazione lineare di due serie convergenti converge alla corrispondente combinazione delle somme. La dimostrazione applica l'algebra dei limiti alle combinazioni delle somme parziali. Per serie regolari con somme infinite devo anche verificare che l'operazione nei reali estesi sia definita e non indeterminata.

Potenziale rilevanza d'esame: ipotesi della linearità e riconoscimento delle separazioni che producono forme indeterminate.
