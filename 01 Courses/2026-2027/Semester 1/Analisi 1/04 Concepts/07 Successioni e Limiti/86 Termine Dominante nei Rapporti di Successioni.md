---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 08, PDF pp. 2-4 e 7-9
  - Libro, §3.5.4, pp. 98-99
---

# Termine dominante nei rapporti di successioni

## Quando si usa

Il metodo serve per rapporti tra somme di potenze, logaritmi, esponenziali, fattoriali e quantità limitate. Se numeratore e denominatore sono infiniti, la forma $\infty/\infty$ non determina il risultato: occorre confrontare la crescita delle due somme.

Il **termine dominante** è quello rispetto al quale tutti gli altri addendi, divisi per esso, tendono a zero. Non basta scegliere il termine che sembra più grande per pochi indici. Il riferimento è [[85 Gerarchia degli Infiniti]].

## Procedura e giustificazione

Supponiamo di poter scrivere, per $n$ sufficientemente grande,

$$
P_n=n^p(A+r_n),\qquad Q_n=n^q(B+s_n),
$$

con $A\neq0$, $B\neq0$, $r_n\to0$ e $s_n\to0$. Allora

$$
\frac{P_n}{Q_n}=n^{p-q}\frac{A+r_n}{B+s_n}.
$$

Il rapporto tra parentesi tende ad $A/B$, per [[80 Algebra dei Limiti di Successioni]]. Inoltre $B+s_n$ è definitivamente non nullo, per [[79 Teorema di Permanenza del Segno]]: il rapporto originario è ben definito nella coda.

| Esponenti dominanti | Limite del rapporto |
|---|---|
| $p<q$ | $0$ |
| $p=q$ | $A/B$ |
| $p>q$ e $A/B>0$ | $+\infty$ |
| $p>q$ e $A/B<0$ | $-\infty$ |

Il caso $p>q$ usa [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate]]. Il procedimento resta valido con altre quantità dominanti: si raccoglie quella del numeratore, quella del denominatore e si studia il loro rapporto.

### Da dire all'orale

> Raccolgo in ciascuna somma il termine dominante e verifico che i resti normalizzati tendano a zero. Il limite dipende dal rapporto dei termini dominanti; per potenze dell'indice conta la differenza degli esponenti e, se questa è positiva, il segno del rapporto dei coefficienti.

## Esempio 1: potenza minore al numeratore

### Testo

$$
u_n=\frac{3n^5-4n^3+\log n-8\arctan(n^2+1)-3}
{2n^{16/3}+147\log(n^{52})-\sin n}.
$$

### Idea e svolgimento passo per passo

Qui e negli esempi seguenti $\log$ indica il logaritmo naturale. La proprietà del logaritmo dà $\log(n^{52})=52\log n$ per $n>0$. Raccogliamo $n^5$ e $n^{16/3}$:

$$
u_n=\frac1{n^{1/3}}
\frac{3-\frac4{n^2}+\frac{\log n}{n^5}-8\frac{\arctan(n^2+1)}{n^5}-\frac3{n^5}}
{2+147\cdot52\frac{\log n}{n^{16/3}}-\frac{\sin n}{n^{16/3}}}.
$$

I rapporti con $\log n$ tendono a zero per la gerarchia. Poiché $|\sin n|\leq1$ e $|\arctan(n^2+1)|<\pi/2$, i rapporti che li contengono tendono a zero per [[84 Confronto in Modulo e Prodotto con un Infinitesimo]]. Anche le potenze negative di $n$ tendono a zero.

Il rapporto grande tende dunque a $3/2$ e il fattore esterno tende a zero:

$$
\boxed{u_n\to0.}
$$

**Errore comune:** $\log(n^{52})=52\log n$, mentre $(\log n)^{52}$ è una potenza del logaritmo e non si semplifica così.

## Esempio 2: stessa potenza dominante

### Testo

$$
v_n=\frac{2n^5-47n^4+\log\log n+\cos n}
{5n^5+\arctan\sqrt n+(\log n)^{42}-1}.
$$

### Svolgimento

L'espressione $\log\log n$ è definita per $n\geq2$. Dividendo entrambi i membri della frazione per $n^5$,

$$
v_n=\frac{2-47/n+\frac{\log\log n}{n^5}+\frac{\cos n}{n^5}}
{5+\frac{\arctan\sqrt n}{n^5}+\frac{(\log n)^{42}}{n^5}-\frac1{n^5}}.
$$

Per $n$ grande, $0\leq\log\log n\leq\log n$: il rapporto corrispondente tende a zero per confronto. Seno, coseno e arcotangente sono limitati. Il termine che richiede attenzione è

$$
\frac{(\log n)^{42}}{n^5}
=\left(\frac{\log n}{n^{5/42}}\right)^{42}\to0,
$$

perché $5/42>0$. Il limite di numeratore e denominatore normalizzati è rispettivamente $2$ e $5$:

$$
\boxed{v_n\to\frac25.}
$$

**Cosa imparare:** anche una potenza molto alta del logaritmo è trascurabile rispetto a una potenza positiva fissata di $n$.

## Esempio 3: potenza maggiore al numeratore e segno negativo

### Testo

$$
w_n=\frac{18n^3-n^{3/2}+\sin n+\log\log n}
{-2n^2+n^{3/4}-(\log n)^{18}+7}.
$$

### Svolgimento

Raccogliamo $n^3$ e $n^2$:

$$
w_n=n\,
\frac{18-\frac1{n^{3/2}}+\frac{\sin n}{n^3}+\frac{\log\log n}{n^3}}
{-2+\frac1{n^{5/4}}-\frac{(\log n)^{18}}{n^2}+\frac7{n^2}}.
$$

Infatti $n^{3/4}/n^2=n^{-5/4}$: dopo la raccolta compare **$1/n^{5/4}$**. Tutti i resti tendono a zero; per il logaritmo elevato a potenza si usa

$$
\frac{(\log n)^{18}}{n^2}
=\left(\frac{\log n}{n^{1/9}}\right)^{18}\to0.
$$

Il rapporto tra parentesi tende a $18/(-2)=-9$. Poiché $n\to+\infty$,

$$
\boxed{w_n\to-\infty.}
$$

**Cosa imparare:** la differenza degli esponenti stabilisce la divergenza; i coefficienti ne stabiliscono il segno.

## Esempio 4: esponenziale contro fattoriale

### Testo

$$
z_n=\frac{7\cdot2^n+\log\log n-\arctan n+n^7}
{14n!-n^{42}+\sin n}.
$$

### Idea e svolgimento

Al numeratore domina $2^n$; al denominatore domina $n!$. Quindi

$$
z_n=\frac{2^n}{n!}
\frac{7+\frac{\log\log n}{2^n}-\frac{\arctan n}{2^n}+\frac{n^7}{2^n}}
{14-\frac{n^{42}}{n!}+\frac{\sin n}{n!}}.
$$

La gerarchia dà $n^7/2^n\to0$ e $2^n/n!\to0$. Inoltre

$$
\frac{n^{42}}{n!}=\frac{n^{42}}{2^n}\frac{2^n}{n!}\to0,
\qquad
\frac{\log n}{2^n}=\frac{\log n}{n}\frac{n}{2^n}\to0.
$$

Il secondo rapporto controlla anche $\log\log n/2^n$ per confronto definitivo. Gli addendi limitati divisi per $2^n$ o $n!$ tendono a zero. Il rapporto interno tende a $7/14=1/2$, quello esterno a zero:

$$
\boxed{z_n\to0.}
$$

## Errori comuni e prospettiva d'esame

- Cancellare addendi senza prima dimostrarne la trascurabilità relativa.
- Trattare $\infty/\infty$ come se valesse $1$.
- Dimenticare coefficienti e segni, o dividere un solo addendo anziché tutta la somma.
- Ignorare il dominio di radici e logaritmi o la non nullità definitiva del denominatore.

Potenziale rilevanza d'esame: riconoscere la scala dominante e trasformare il rapporto con un'uguaglianza esatta. La formulazione con resti sarà ripresa in [[93 Notazione o-Piccolo]] e [[94 Equivalenza Asintotica]].
