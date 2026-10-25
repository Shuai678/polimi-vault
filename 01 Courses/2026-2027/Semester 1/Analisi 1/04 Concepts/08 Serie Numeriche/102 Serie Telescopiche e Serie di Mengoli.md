---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 10, PDF pp. 16-18
  - Libro, §4.1, pp. 113-114; esempi 4.1-4.2
---

# Serie telescopiche e serie di Mengoli

## Quando si usa e intuizione

Una serie è **telescopica** quando il termine generale è una differenza di due termini consecutivi di una successione ausiliaria. Nelle somme parziali gli addendi intermedi si cancellano e restano soltanto i bordi.

Nella notazione del professore,

$$
a_n=b_n-b_{n+1}.
$$

Non occorre sommare separatamente le due serie degli $b_n$: potrebbero non convergere. La cancellazione si compie sempre nella **somma finita**.

## Formula delle somme parziali e dimostrazione

Partendo da $n=0$,

$$
\begin{aligned}
S_N&=\sum_{n=0}^{N}(b_n-b_{n+1})\\
&=(b_0-b_1)+(b_1-b_2)+\cdots+(b_N-b_{N+1})\\
&=b_0-b_{N+1}.
\end{aligned}
$$

Ogni $b_k$ con $1\leq k\leq N$ compare una volta con segno positivo e una con segno negativo. L'ultimo termine rimasto è $b_{N+1}$, non $b_N$.

Per un indice iniziale generale $m$ la stessa prova dà

$$
\boxed{\sum_{n=m}^{N}(b_n-b_{n+1})=b_m-b_{N+1}.}
$$

## Teorema sul carattere e sulla somma

La serie $\sum_{n=m}^{+\infty}(b_n-b_{n+1})$ è regolare se e solo se $(b_n)$ ha limite $b^*\in\overline{\mathbb R}$. In tal caso

$$
\boxed{\sum_{n=m}^{+\infty}(b_n-b_{n+1})=b_m-b^*.}
$$

Più precisamente:

- se $b^*\in\mathbb R$, la serie converge alla somma finita $b_m-b^*$;
- se $b_n\to+\infty$, la serie diverge a $-\infty$;
- se $b_n\to-\infty$, la serie diverge a $+\infty$;
- se $(b_n)$ è irregolare, anche la serie è irregolare.

**Dimostrazione.** La formula esatta $S_N=b_m-b_{N+1}$ trasferisce il limite di $b_{N+1}$ a $S_N$. Viceversa $b_{N+1}=b_m-S_N$: se $S_N$ avesse limite, lo avrebbe anche la successione ausiliaria. Uno scarto finito nell'indice non cambia il limite. Per i casi infiniti i segni si invertono sottraendo da $b_m$ finito.

> [!info] Approfondimento dal libro
> L'esempio 4.2 a p. 114 usa l'orientamento opposto, $a_k=A_{k+1}-A_k$, e ottiene $S_N=A_{N+1}-A_1$. È lo stesso meccanismo con segni invertiti. Negli appunti resta la convenzione del docente $b_n-b_{n+1}$.

## Esercizio  — Serie di Mengoli

### Testo

Studiare il carattere e calcolare la somma di

$$
\sum_{n=1}^{+\infty}\frac1{n(n+1)}.
$$

### Idea

Scomponiamo il termine generale nella differenza di due frazioni consecutive.

### Svolgimento passo per passo

Per $n\geq1$,

$$
\frac1n-\frac1{n+1}
=\frac{n+1-n}{n(n+1)}=\frac1{n(n+1)}.
$$

Poniamo $b_n=1/n$. La somma inizia da $1$, perché $b_0$ non è definito. Allora

$$
\begin{aligned}
S_N&=\sum_{n=1}^{N}\left(\frac1n-\frac1{n+1}\right)\\
&=\left(1-\frac12\right)+\left(\frac12-\frac13\right)
+\cdots+\left(\frac1N-\frac1{N+1}\right)\\
&=1-\frac1{N+1}\to1.
\end{aligned}
$$

### Risultato e precisione dell'approssimazione

$$
\boxed{\sum_{n=1}^{+\infty}\frac1{n(n+1)}=1.}
$$

Il calcolo dà anche il resto esatto $1-S_N=1/(N+1)$. Questo permette di approssimare la somma controllando l'errore, senza introdurre ulteriori criteri.

### Cosa imparare ed errore comune

Il termine è riconoscibile perché il denominatore contiene fattori consecutivi. La dimostrazione della somma richiede la scomposizione esatta e poi il limite della somma finita. Separare $\sum1/n-\sum1/(n+1)$ produrrebbe una differenza di infiniti: la [[104 Serie Armonica]] dimostra che entrambe divergono.

## Procedura generale ed errori comuni

1. Cercare una differenza $b_n-b_{n+1}$ mediante frazioni, logaritmi o altre identità esatte.
2. Scrivere alcuni termini della somma finita per identificare i bordi.
3. Mantenere l'indice iniziale corretto e il bordo finale $N+1$.
4. Studiare il limite di $b_n$ e dedurre carattere ed eventuale somma.

Non basta che due addendi “si assomiglino”: la cancellazione deve essere esatta. Inoltre una serie telescopica non converge sempre: dipende dal limite della successione ausiliaria.

### Da dire all'orale

> Una serie telescopica con termine b con indice n meno b con indice n più uno ha somma parziale uguale al primo termine ausiliario meno quello con indice N più uno. Converge se e solo se la successione ausiliaria ha limite finito; la somma è il primo termine meno quel limite. Se il limite ausiliario è infinito, la serie diverge con segno opposto.

Potenziale rilevanza d'esame: riconoscimento della scomposizione, controllo degli indici e somma della serie di Mengoli.
