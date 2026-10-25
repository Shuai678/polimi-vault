---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 09, PDF pp. 8-14
  - Libro, §3.8, pp. 103-105; esempio 3.54
---

# Calcolo dei limiti con equivalenti asintotici

## Quando si usa e idea del metodo

Gli [[95 Equivalenti e Sviluppi Asintotici Notevoli|equivalenti notevoli]] semplificano prodotti e quozienti con argomenti che tendono a zero. Per le somme con un termine dominante si usa la [[85 Gerarchia degli Infiniti|gerarchia]]; per le differenze con cancellazione si conservano i [[93 Notazione o-Piccolo|resti]].

L'obiettivo è arrivare a un'espressione semplice **asintoticamente equivalente** a tutta la successione, oppure a una somma con resto il cui limite sia controllato. [[94 Equivalenza Asintotica]] assicura che successioni equivalenti hanno lo stesso carattere e lo stesso limite, quando esiste.

## Procedura

1. Controllare il dominio e la non nullità dei denominatori nella coda.
2. Identificare gli argomenti infinitesimi; raccogliere prima i fattori grandi se necessario.
3. Usare gli equivalenti nei prodotti e quozienti, mantenendo coefficienti e segni.
4. Se ci sono sottrazioni di termini equivalenti, scrivere lo sviluppo con resto prima di sottrarre.
5. Trasformare anche i resti moltiplicati per potenze di $n$; verificarne la scala finale.
6. Calcolare il limite dell'espressione risultante.

## Esempio 1 — Rapporto con molti addendi

### Testo — PDF p. 8

Per $n\geq1$, dove il denominatore è non nullo, consideriamo

$$
a_n=\frac{3n^7+5n^{42/95}+\log n-\cos n+5}
{2n^6-18n^3+\arctan n+(\log n)^2-2}.
$$

### Idea

Prima di passare al rapporto, giustifichiamo separatamente il termine dominante di numeratore e denominatore, come in [[86 Termine Dominante nei Rapporti di Successioni]].

### Svolgimento passo per passo

Per il numeratore $N_n$:

$$
\frac{N_n}{3n^7}
=1+\frac{5}{3n^{7-42/95}}
+\frac{\log n}{3n^7}
+\frac{-\cos n+5}{3n^7}\to1.
$$

Il primo resto tende a zero perché $7-42/95=623/95>0$, il secondo per la gerarchia logaritmo-potenza, l'ultimo perché $|-\cos n+5|\leq6$. Dunque $N_n=3n^7+o(n^7)\sim3n^7$.

Per il denominatore $D_n$:

$$
\frac{D_n}{2n^6}
=1-\frac9{n^3}+\frac{\arctan n}{2n^6}
+\frac{(\log n)^2}{2n^6}-\frac1{n^6}\to1.
$$

L'arcotangente è limitata da $\pi/2$ in valore assoluto; inoltre $(\log n)^2/n^6=(\log n/n^3)^2\to0$. Ne segue $D_n=2n^6+o(n^6)\sim2n^6$. Il rapporto con $2n^6$ tende a $1>0$, quindi $D_n>0$ definitivamente: l'espressione è definita nella coda.

Usando la proprietà dei quozienti,

$$
a_n\sim\frac{3n^7}{2n^6}=\frac32n\to+\infty.
$$

### Risultato e cosa imparare

$$
\boxed{\lim_{n\to+\infty}a_n=+\infty.}
$$

Gli addendi si scartano **dopo** aver confrontato ciascuno con la scala dominante; la presenza di termini goniometrici non impone uno studio oscillatorio se sono trascurabili rispetto a tale scala.

## Esempio 2 — Seno, esponenziale e una potenza esterna

### Testo — PDF pp. 9-10

$$
a_n=\frac{\sin(1/n^2)}{e^{7/n}-1}\,n,\qquad n\geq1.
$$

### Idea e svolgimento passo per passo

Gli argomenti $1/n^2$ e $7/n$ tendono entrambi a zero. Il denominatore è positivo perché $7/n>0$. Per il Concept 95,

$$
\sin(1/n^2)\sim\frac1{n^2},\qquad
e^{7/n}-1\sim\frac7n.
$$

Si sostituiscono entrambi dentro un quoziente e poi si moltiplica:

$$
a_n\sim\frac{1/n^2}{7/n}\,n
=\frac1{n^2}\cdot\frac n7\cdot n=\frac17.
$$

### Risultato e errore comune

$$
\boxed{\lim_{n\to+\infty}a_n=\frac17.}
$$

Dimenticare il $7$ nell'argomento dell'esponenziale cambia il risultato. La potenza $n$ esterna va inclusa nel confronto dell'intera successione.

## Esempio 3 — Differenza di radici cubiche in un prodotto

### Testo — PDF pp. 10-12

$$
a_n=\frac{\sqrt[3]{n+1}-n^{1/3}}{1-e^{2/n}}
\,\arctan\!\left(\frac1{n^2}\right)n^{5/3},\qquad n\geq1.
$$

### Idea

Non possiamo sostituire separatamente entrambe le radici con $n^{1/3}$ e sottrarle. Dobbiamo trovare l'equivalente della **differenza intera**. Il denominatore è negativo e non nullo.

### Svolgimento passo per passo

Raccogliamo la potenza di $n$:

$$
\sqrt[3]{n+1}=n^{1/3}\left(1+\frac1n\right)^{1/3}.
$$

L'incremento è ora $1/n\to0$ e l'esponente $1/3$ è fissato. Scriviamo

$$
\left(1+\frac1n\right)^{1/3}
=1+\frac1{3n}+r_n,\qquad r_n=o(1/n).
$$

Moltiplicando e poi sottraendo,

$$
\begin{aligned}
\sqrt[3]{n+1}-n^{1/3}
&=\frac1{3n^{2/3}}+n^{1/3}r_n\\
&=\frac1{3n^{2/3}}+o(n^{-2/3})
\sim\frac1{3n^{2/3}}.
\end{aligned}
$$

Infatti $n^{1/3}r_n/n^{-2/3}=nr_n\to0$. Per gli altri fattori,

$$
1-e^{2/n}\sim-\frac2n,\qquad
\arctan(1/n^2)\sim\frac1{n^2}.
$$

Dunque

$$
a_n\sim
\frac{1/(3n^{2/3})}{-2/n}\frac1{n^2}n^{5/3}
=-\frac16n^{1-2/3-2+5/3}=-\frac16.
$$

### Risultato

$$
\boxed{\lim_{n\to+\infty}a_n=-\frac16.}
$$

### Controllo con un'identità esatta

Il PDF suggerisce anche la differenza di cubi, già usata in [[88 Razionalizzazione e Differenze di Radicali]]. Ponendo $A_n=\sqrt[3]{n+1}$ e $B_n=\sqrt[3]n$,

$$
A_n-B_n=\frac1{A_n^2+A_nB_n+B_n^2}.
$$

Poiché $A_n/B_n=(1+1/n)^{1/3}\to1$, il denominatore diviso per $n^{2/3}$ tende a $3$. Ritroviamo $A_n-B_n\sim1/(3n^{2/3})$.

### Cosa imparare ed errore comune

Raccogliere trasforma un argomento grande in un incremento piccolo. Sarebbe invalido usare $(1+n)^{1/3}=1+n/3+o(n)$ come applicazione dello sviluppo notevole: l'incremento $n$ non tende a zero. Anche $\sqrt[3]{n+1}\sim n^{1/3}$, pur corretto, non basta per calcolare la differenza.

## Esempio 4 — Due radicali divergenti con differenza finita

### Testo — PDF pp. 12-14

$$
a_n=(n^3+n^2)^{1/3}-(n^3-n)^{1/3},\qquad n\geq1.
$$

### Idea

Entrambi i termini sono equivalenti a $n$, ma ciò non determina la loro differenza. Dopo aver raccolto $n$, conserviamo la prima correzione e i resti.

### Svolgimento passo per passo

$$
\begin{aligned}
(n^3+n^2)^{1/3}
&=n\left(1+\frac1n\right)^{1/3}
=n\left(1+\frac1{3n}+r_n\right)
=n+\frac13+nr_n,\\
(n^3-n)^{1/3}
&=n\left(1-\frac1{n^2}\right)^{1/3}
=n\left(1-\frac1{3n^2}+s_n\right)
=n-\frac1{3n}+ns_n,
\end{aligned}
$$

con $r_n=o(1/n)$ e $s_n=o(1/n^2)$. La seconda base è positiva per $n\geq2$, sufficiente per il limite. I resti soddisfano

$$
nr_n=o(1)\to0,\qquad
ns_n=o(1/n)\to0.
$$

Per il secondo limite, $ns_n=(n^2s_n)/n$, con $n^2s_n\to0$. Sottraendo le **uguaglianze con i resti identificati**,

$$
a_n=\frac13+\frac1{3n}+nr_n-ns_n\to\frac13.
$$

### Risultato e cosa imparare

$$
\boxed{\lim_{n\to+\infty}a_n=\frac13.}
$$

> [!info] Approfondimento dal libro
> Lo stesso esercizio è l'esempio 3.54 in §3.8, p. 105. Il testo sottolinea che i due radicali sono equivalenti tra loro, benché la loro differenza non tenda a zero. Qui si rendono espliciti anche i controlli dei due resti dopo la moltiplicazione per $n$.

La scala a cui si deve controllare il resto dipende da ciò che resta dopo la cancellazione. Questo principio è approfondito in [[97 Cancellazioni e Precisione del Resto Asintotico]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: prodotti e rapporti di infinitesimi notevoli, radicali da normalizzare e differenze con termini dominanti uguali. L'errore decisivo è sostituire equivalenti dentro una sottrazione senza controllare il resto.

### Da dire all'orale

> Nei prodotti e nei quozienti posso sostituire successioni equivalenti, verificando che i denominatori siano definitivamente non nulli. Nelle differenze, se i termini principali si cancellano, devo conservare una correzione e un resto abbastanza piccolo rispetto alla scala del risultato, oppure usare un'identità algebrica esatta.
