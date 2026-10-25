---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 07, PDF pp. 11-13
  - Libro, §3.3, pp. 84-86
---

# Algebra dei limiti di successioni

## Teorema e condizioni

Siano $a_n\to a\in\mathbb R$ e $b_n\to b\in\mathbb R$. Allora

$$
\lim_{n\to+\infty}(a_n\pm b_n)=a\pm b,
\qquad
\lim_{n\to+\infty}a_nb_n=ab.
$$

Inoltre,

$$
\lim_{n\to+\infty}\frac{a_n}{b_n}=\frac ab\qquad\text{se }b\neq0,
$$

$$
\lim_{n\to+\infty}a_n^{b_n}=a^b\qquad\text{se }a>0.
$$

Per il quoziente, [[79 Teorema di Permanenza del Segno|permanenza del segno]] garantisce $b_n\neq0$ definitivamente. Per la potenza con esponente reale variabile, garantisce $a_n>0$ definitivamente. Le espressioni si considerano quindi almeno da un indice sufficientemente grande.

Questo enunciato riguarda limiti **finiti**. Le tabelle del libro includono anche limiti infiniti, ma qui si segue la forma trattata nella Lezione 07.

## Prosecuzione nella Lezione 08

Le estensioni ai limiti infiniti sono in [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate]]; il metodo logaritmico e le forme indeterminate delle potenze sono in [[89 Limiti di Potenze con Base ed Esponente Variabili]]. L'enunciato precedente conserva le sue ipotesi di limiti finiti.

## In parole semplici

Quando le ipotesi sono rispettate, possiamo calcolare il limite dopo aver sommato, moltiplicato, diviso o elevato a potenza i limiti dei singoli fattori. La verifica delle condizioni precede la sostituzione.

Per ogni costante $c\in\mathbb R$, $ca_n\to ca$: è un caso del prodotto con la successione costante $c$. Applicando ripetutamente somme e prodotti si ottengono anche i limiti dei polinomi in successioni convergenti.

## Dimostrazione della somma e della differenza

La [[30 Disuguaglianza Triangolare|disuguaglianza triangolare]] dà

$$
|(a_n+b_n)-(a+b)|
=|(a_n-a)+(b_n-b)|
\leq|a_n-a|+|b_n-b|.
$$

Fissiamo $\varepsilon>0$. Dalle due convergenze esistono $N_1,N_2$ tali che

$$
|a_n-a|<\frac\varepsilon2\quad(n\geq N_1),
\qquad
|b_n-b|<\frac\varepsilon2\quad(n\geq N_2).
$$

Per $n\geq N=\max\{N_1,N_2\}$,

$$
|(a_n+b_n)-(a+b)|<\frac\varepsilon2+\frac\varepsilon2=\varepsilon.
$$

Questa è la definizione di limite $a+b$. Per la differenza si usa

$$
|(a_n-b_n)-(a-b)|
=|(a_n-a)-(b_n-b)|
\leq|a_n-a|+|b_n-b|,
$$

con la stessa scelta delle soglie.

## Dimostrazione del prodotto

### Strategia

Vogliamo stimare $|a_nb_n-ab|$ attraverso gli errori $|a_n-a|$ e $|b_n-b|$. Aggiungiamo e sottraiamo $a_nb$ per ottenere i fattori desiderati:

$$
a_nb_n-ab=a_nb_n-a_nb+a_nb-ab
=a_n(b_n-b)+b(a_n-a).
$$

Per disuguaglianza triangolare,

$$
|a_nb_n-ab|\leq|a_n|\,|b_n-b|+|b|\,|a_n-a|.
$$

Il coefficiente $|a_n|$ varia con $n$: va controllato prima di scegliere le precisioni.

### Controllo del fattore e scelta della precisione

Poiché $a_n$ converge, dal [[77 Limitatezza delle Successioni Convergenti|teorema di limitatezza]] esiste $M>0$ tale che $|a_n|\leq M$ per ogni indice. Quindi

$$
|a_nb_n-ab|\leq M|b_n-b|+|b|\,|a_n-a|.
$$

Dato $\varepsilon>0$, poniamo

$$
\delta=\frac{\varepsilon}{M+|b|}>0.
$$

Esistono $N_1,N_2$ tali che $|a_n-a|<\delta$ per $n\geq N_1$ e $|b_n-b|<\delta$ per $n\geq N_2$. Per $n\geq\max\{N_1,N_2\}$ si ottiene

$$
|a_nb_n-ab|<(M+|b|)\delta=\varepsilon.
$$

La stima stretta resta valida anche se $b=0$, perché $M>0$ moltiplica un errore strettamente minore di $\delta$. Abbiamo provato $a_nb_n\to ab$.

> [!note] Precisione del passaggio finale
> Nel PDF si ottiene una stima del tipo $(M+|b|)\varepsilon$. Anche questa prova la convergenza, perché il coefficiente è fisso; scegliere subito $\delta=\varepsilon/(M+|b|)$ rende esplicito il rispetto della precisione finale richiesta.

## Quoziente e potenza

Il docente enuncia le due regole senza dimostrazione nel PDF. Le condizioni da ricordare sono $b\neq0$ per il quoziente e $a>0$ per la potenza con esponente reale variabile. L'ipotesi $a>0$ è sufficiente per la formula generale; non esclude singoli casi con base nulla o negativa ed esponente intero fisso, che richiedono un'analisi specifica.

### Da dire all'orale

> Per due successioni convergenti a limiti reali, il limite della somma e del prodotto è la somma e il prodotto dei limiti. Per il quoziente il limite del denominatore deve essere non nullo; per una potenza con esponente reale variabile, il limite della base deve essere positivo.

## Esercizio svolto: quoziente di polinomi

### Testo

Calcolare $\displaystyle\lim_{n\to+\infty}\frac{3n^2-n+4}{2n^2+5}$.

### Idea

La formula del quoziente non si applica direttamente ai limiti di numeratore e denominatore, che sono infiniti. Prima trasformiamo la stessa espressione usando limiti finiti.

### Svolgimento passo per passo

Per $n\geq1$ dividiamo numeratore e denominatore per $n^2$:

$$
\frac{3n^2-n+4}{2n^2+5}
=\frac{3-1/n+4/n^2}{2+5/n^2}.
$$

Da [[78 Limiti di Potenze e Progressioni Geometriche]] sappiamo che $1/n\to0$ e $1/n^2\to0$. Per somme e prodotti, il numeratore tende a $3$ e il denominatore a $2\neq0$. Ora possiamo applicare il quoziente:

$$
\lim_{n\to+\infty}\frac{3n^2-n+4}{2n^2+5}=\frac32.
$$

### Cosa imparare

Una trasformazione algebrica esatta può rendere applicabile una regola le cui ipotesi inizialmente non erano soddisfatte.

## Esempio di potenza

Per $n\geq1$,

$$
\left(2+\frac1n\right)^{3-1/n}\to2^3=8,
$$

perché la base tende a $2>0$ e l'esponente al numero reale $3$.

## Errori comuni e prospettiva d'esame

- Applicare il quoziente con $b=0$: i dati $a_n\to0$ e $b_n\to0$ da soli non determinano il risultato. Per esempio $(1/n^2)/(1/n)=1/n\to0$, mentre $(1/n)/(1/n)=1$.
- Applicare la regola della potenza senza controllare la base o con esponente che non ha limite finito.
- Scrivere il limite del prodotto senza sapere se entrambi i fattori convergono: il [[84 Confronto in Modulo e Prodotto con un Infinitesimo|prodotto di un fattore limitato e uno infinitesimo]] richiederà un risultato diverso.
- Nella dimostrazione dimenticare la limitatezza di $a_n$ o il massimo delle soglie.

Potenziale rilevanza d'esame: enunciati con tutte le condizioni e dimostrazioni di somma e prodotto secondo la sequenza effettiva del PDF.
