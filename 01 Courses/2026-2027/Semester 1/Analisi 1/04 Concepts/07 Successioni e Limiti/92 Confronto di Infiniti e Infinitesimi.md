---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 08, PDF pp. 18-20
  - Libro, §3.8, pp. 101-102
---

# Confronto di infiniti e infinitesimi

## Intuizione e condizioni

Due successioni possono tendere entrambe a infinito o entrambe a zero, ma con velocità diverse. Il confronto si effettua calcolando il rapporto $a_n/b_n$, con $b_n\neq0$ definitivamente.

Una successione è **infinita** se tende a $+\infty$ o a $-\infty$; è **infinitesima** se tende a zero. La semplice illimitatezza non basta a chiamarla infinita: si veda [[74 Limiti Infiniti e Regolarità delle Successioni]].

## Definizione: confronto di infiniti

Siano $a_n$ e $b_n$ due successioni infinite. Se il rapporto ammette limite,

| Limite di $a_n/b_n$ | Nome del confronto |
|---|---|
| $0$ | $a_n$ è un infinito di **ordine inferiore** a $b_n$ |
| $\ell\in\mathbb R\setminus\{0\}$ | $a_n$ e $b_n$ sono infiniti dello **stesso ordine** |
| $+\infty$ o $-\infty$ | $a_n$ è un infinito di **ordine superiore** a $b_n$ |

Se il rapporto non ha limite, le successioni sono **non confrontabili secondo questa definizione**. “Stesso ordine” consente un rapporto negativo: per esempio $-3n$ e $n$ hanno rapporto $-3$.

### Esempi dalla gerarchia

A p. 18, con $a>1$, $\alpha>0$ e $\beta>0$ fissati:

- $(\log_a n)^\beta$ è un infinito di ordine inferiore rispetto a $n^\alpha$, $a^n$, $n!$ e $n^n$;
- $n!$ è un infinito di ordine superiore rispetto a $n^\alpha$, $a^n$ e $(\log_a n)^\beta$.

I confronti fra termini adiacenti sono in [[85 Gerarchia degli Infiniti]]. Per quelli non adiacenti si concatenano i rapporti. Per esempio,

$$
\frac{n^\alpha}{n!}
=\frac{n^\alpha}{a^n}\frac{a^n}{n!}\to0,
$$

quindi $n^\alpha$ ha ordine inferiore a $n!$, equivalentemente $n!$ ha ordine superiore a $n^\alpha$. Analogamente,

$$
\frac{(\log_a n)^\beta}{n^n}
=\frac{(\log_a n)^\beta}{n^\alpha}
\frac{n^\alpha}{a^n}\frac{a^n}{n!}\frac{n!}{n^n}\to0.
$$

Ogni fattore tende a zero e si applica la regola del prodotto per limiti finiti.

### Esempio : stesso ordine

Per $n\geq2$,

$$
\frac{\log n}{\log(n^2)}=\frac{\log n}{2\log n}=\frac12.
$$

Quindi $\log n$ e $\log(n^2)$ sono infiniti dello stesso ordine. Il rapporto non è $1$: non sono equivalenti asintoticamente nel senso di [[94 Equivalenza Asintotica]].

### Esempio del PDF: non confrontabilità

Consideriamo $a_n=(2+\sin n)n$ e $b_n=n$. Poiché $a_n\geq n$, entrambi tendono a $+\infty$. Ma

$$
\frac{a_n}{b_n}=2+\sin n
$$

non ha limite. Le due successioni non sono confrontabili secondo la definizione, pur avendo $n\leq a_n\leq3n$.

Per giustificare la non convergenza di $\sin n$ senza risultati ulteriori, supponiamo per assurdo $\sin n\to L$. Dall'identità

$$
\sin(n+2)+\sin n=2\cos1\,\sin(n+1)
$$

seguirebbe $2L=2\cos1\,L$, quindi $L=0$ perché $\cos1\neq1$. Dall'altra identità

$$
\sin(n+1)=\sin n\cos1+\cos n\sin1
$$

si ricaverebbe anche $\cos n\to0$, dato che $\sin1\neq0$. Ma allora $\sin^2n+\cos^2n\to0$, in contraddizione con $\sin^2n+\cos^2n=1$. Inoltre il rapporto $2+\sin n$ è limitato, quindi non può avere un limite infinito.

## Definizione: confronto di infinitesimi

Siano ora $a_n\to0$ e $b_n\to0$, con $b_n\neq0$ definitivamente.

| Limite di $a_n/b_n$ | Nome del confronto |
|---|---|
| $0$ | $a_n$ è un infinitesimo di **ordine superiore** a $b_n$ |
| $\ell\in\mathbb R\setminus\{0\}$ | $a_n$ e $b_n$ sono infinitesimi dello **stesso ordine** |
| $+\infty$ o $-\infty$ | $a_n$ è un infinitesimo di **ordine inferiore** a $b_n$ |

Se il rapporto non ha limite, sono non confrontabili. Il verso dei nomi si inverte: un infinitesimo di ordine superiore si annulla più rapidamente, mentre un infinito di ordine superiore cresce più rapidamente in modulo.

![[92 Ordine di Infiniti e Infinitesimi.svg|760]]

### Esempio svolto: potenze inverse

Con $a_n=1/n^2$ e $b_n=1/n$,

$$
\frac{a_n}{b_n}=\frac1n\to0.
$$

Dunque $1/n^2$ è un infinitesimo di ordine **superiore** a $1/n$. Il confronto inverso dà $b_n/a_n=n\to+\infty$, perciò $1/n$ è di ordine **inferiore** a $1/n^2$.

### Esempio: reciproci della gerarchia

Per $a>1$, $\alpha>0$ e $\beta>0$ fissati, $1/n^n$ è un infinitesimo di ordine superiore a ciascuno dei seguenti:

$$
\frac1{(\log_a n)^\beta},\qquad\frac1{n^\alpha},\qquad
\frac1{a^n},\qquad\frac1{n!}.
$$

Per esempio

$$
\frac{1/n^n}{1/n!}=\frac{n!}{n^n}\to0.
$$

Gli altri rapporti sono rispettivamente $(\log_a n)^\beta/n^n$, $n^\alpha/n^n$ e $a^n/n^n$. Si scompongono in prodotti dei rapporti adiacenti della [[85 Gerarchia degli Infiniti|gerarchia]], tutti tendenti a zero.

### Da dire all'orale

> Confronto due infiniti o due infinitesimi tramite il limite del loro rapporto. Un rapporto nullo indica ordine inferiore per gli infiniti e ordine superiore per gli infinitesimi; un limite finito non nullo indica lo stesso ordine. Se il rapporto non ammette limite, le successioni non sono confrontabili secondo questa definizione.

## Errori comuni e prospettiva d'esame

- Invertire il nome dell'ordine nel passaggio dagli infiniti agli infinitesimi.
- Dimenticare quale successione sta al numeratore del rapporto.
- Confondere stesso ordine con rapporto uguale a $1$.
- Dichiarare non confrontabili successioni senza controllare se il rapporto abbia un limite infinito.
- Confondere non confrontabilità tramite limite con impossibilità di qualunque disuguaglianza tra i termini.

Potenziale rilevanza d'esame: definizioni con la non nullità del denominatore, confronto concreto e spiegazione del verso degli ordini. Il rapporto nullo si esprimerà con [[93 Notazione o-Piccolo]].
