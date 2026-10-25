---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 12, PDF pp. 16-19
  - Libro, §4.3, p. 124, teorema 4.23
---

# Serie alternate e criterio di Leibniz

## Intuizione e definizione

Una **serie a segni alterni** ha la forma

$$
\sum_{n=0}^{+\infty}(-1)^n a_n,
\qquad a_n\geq0\text{ definitivamente}.
$$

Qui $a_n$ è l'**ampiezza**; il termine completo della serie è $(-1)^n a_n$. I segni alternano, salvo eventuali termini nulli. Se le ampiezze diminuiscono verso zero, le somme parziali correggono alternativamente un eccesso e un difetto, con correzioni sempre più piccole.

La partenza da $0$ serve a fissare la notazione del docente. Spostare l'indice iniziale o cambiare il segno di tutta la serie non cambia la convergenza; per identificare somme parziali superiori e inferiori va sempre controllato il segno effettivo dell'ultimo termine.

## Teorema di Leibniz

Supponiamo che, almeno da un certo indice in poi,

1. $a_n\geq0$;
2. $a_{n+1}\leq a_n$;
3. $a_n\to0$.

Allora $\sum(-1)^n a_n$ **converge semplicemente** a una somma $S$. Per le somme parziali $S_N=\sum_{n=0}^{N}(-1)^n a_n$, definitivamente

$$
S_{2k+1}\leq S\leq S_{2k},\qquad
S_{2k}\downarrow S,\quad S_{2k+1}\uparrow S.
$$

Il [[105 Code e Resto di una Serie|resto]] $R_N=S-S_N$ soddisfa

$$
\boxed{|R_N|\leq a_{N+1}.}
$$

Il resto ha il segno del primo termine escluso, quando non è nullo: $(-1)^{N+1}R_N\geq0$.

> [!note] Indici della stima
> Se le ipotesi sono vere solo definitivamente, anche monotonia delle due sottosuccessioni e stima del resto valgono per indici sufficientemente grandi. Se valgono dall'inizio, la stima vale per ogni $N$. Questa precisazione rende esplicita la condizione “definitivamente” dell'enunciato del docente.

## Perché è utile

Leibniz può provare convergenza anche quando la [[114 Convergenza Assoluta e Semplice delle Serie|serie dei moduli]] diverge. Inoltre controlla l'errore di approssimazione: per assicurare $|S-S_N|\leq\varepsilon$ basta scegliere un indice nella coda monotona con $a_{N+1}\leq\varepsilon$. Non serve conoscere il valore di $S$.

![[115 Somme Parziali nel Criterio di Leibniz.svg|900]]

Il grafico usa $a_n=2^{-n}$. La somma è $S=2/3$ per la [[100 Serie Geometrica e Rappresentazioni Decimali|geometrica]] di ragione $-1/2$. Le somme parziali pari arrivano dall'alto e quelle dispari dal basso.

## Dimostrazione di supporto

> [!info] Integrazione didattica — Da studiare
> Il docente scrive «NO DIM.»; anche il libro, teorema 4.23, enuncia il risultato senza dimostrarlo. La prova qui sotto è aggiunta per spiegare il meccanismo usando il [[76 Teorema del Limite delle Successioni Monotone|teorema sulle successioni monotone]] già disponibile. Non è una dimostrazione svolta nel PDF né una voce dell'elenco ufficiale delle dimostrazioni per questo tratto del corso.

### 1. Separare somme parziali pari e dispari

Per $k$ sufficientemente grande, i termini necessari sono nella coda non negativa e non crescente. Pertanto

$$
S_{2k+2}-S_{2k}=-a_{2k+1}+a_{2k+2}\leq0,
$$

$$
S_{2k+3}-S_{2k+1}=a_{2k+2}-a_{2k+3}\geq0.
$$

La sottosuccessione pari è non crescente, la dispari non decrescente. Inoltre

$$
S_{2k}-S_{2k+1}=a_{2k+1}\geq0.
$$

### 2. Ottenere due limiti finiti e mostrarli uguali

Fissato un indice $K$ abbastanza grande, per $k\geq K$,

$$
S_{2K+1}\leq S_{2k+1}\leq S_{2k}\leq S_{2K}.
$$

Le due sottosuccessioni sono monotone e limitate, quindi hanno limiti finiti, diciamo $L_\mathrm{dispari}$ e $L_\mathrm{pari}$. Ma la loro differenza vale $a_{2k+1}\to0$: i due limiti coincidono in un numero $S$.

Ogni indice è pari oppure dispari. Poiché entrambe le sottosuccessioni sono definitivamente vicine allo stesso $S$, lo sono tutte le somme parziali: $S_N\to S$. Questo prova la convergenza semplice.

### 3. Stimare il resto

Se $N$ è pari e sufficientemente grande,

$$
S_{N+1}\leq S\leq S_N.
$$

Quindi $-a_{N+1}=S_{N+1}-S_N\leq R_N\leq0$. Se $N$ è dispari,

$$
S_N\leq S\leq S_{N+1},
$$

quindi $0\leq R_N\leq S_{N+1}-S_N=a_{N+1}$. Nei due casi $|R_N|\leq a_{N+1}$, con il segno del primo termine escluso.

## Esempio del docente — Armoniche generalizzate alternate

### Testo

Discutere, per $\alpha\in\mathbb R$,

$$
\sum_{n=1}^{+\infty}\frac{(-1)^n}{n^\alpha}.
$$

### Svolgimento e classificazione

Per $\alpha>0$, l'ampiezza $a_n=1/n^\alpha$ è positiva, non crescente e tende a zero. Leibniz prova la convergenza semplice. La serie dei moduli $\sum1/n^\alpha$ converge solo per $\alpha>1$.

| Valore di $\alpha$ | Risultato |
|---|---|
| $\alpha>1$ | Convergenza assoluta, quindi semplice |
| $0<\alpha\leq1$ | Convergenza solo semplice |
| $\alpha\leq0$ | Serie irregolare |

Per l'ultima riga non basta dire “Leibniz non si applica”: occorre studiare le somme parziali. Se $\alpha=0$, esse alternano fra $0$ e $-1$. Se $\alpha<0$, poniamo $p=-\alpha>0$. Le ampiezze $n^p$ crescono e non tendono a zero. Inoltre

$$
S_{2k}=\sum_{j=1}^{k}\bigl[(2j)^p-(2j-1)^p\bigr]\geq0,
$$

$$
S_{2k+1}=-1+\sum_{j=1}^{k}\bigl[(2j)^p-(2j+1)^p\bigr]\leq-1.
$$

La condizione necessaria esclude un limite finito; le somme parziali dispari impediscono un limite $+\infty$, quelle pari impediscono un limite $-\infty$. La serie è dunque irregolare, come indicato dal docente.

### Stima concreta del resto

Per l'armonica alternata $\sum_{n=1}^{+\infty}(-1)^n/n$, la somma parziale fino a $N$ approssima la somma con errore al più $1/(N+1)$. Per un errore al più $10^{-3}$ è sufficiente $N\geq999$. Questo numero è una garanzia sufficiente, non una stima dell'errore esatto.

## Errori comuni e connessioni

- Verificare solo alternanza e limite zero: serve anche la monotonia delle ampiezze nella coda.
- Applicare la monotonia al termine completo $(-1)^n a_n$: la condizione riguarda $a_n$.
- Concludere “solo semplice” da Leibniz senza studiare prima o dopo la serie dei moduli.
- Identificare $R_N$ con $a_{N+1}$: è una disuguaglianza sui moduli, non un'uguaglianza.

La necessità della monotonia e i limiti del confronto asintotico sono sviluppati in [[116 Monotonia e Confronti nelle Serie Alternate]].

### Da dire all'orale

> Una serie a segni alterni converge se le ampiezze sono definitivamente non negative, non crescenti e tendono a zero. Il resto è in modulo al più il primo termine escluso, a partire dalla coda in cui valgono le ipotesi. Per distinguere convergenza assoluta e solo semplice devo studiare separatamente la serie dei moduli.
