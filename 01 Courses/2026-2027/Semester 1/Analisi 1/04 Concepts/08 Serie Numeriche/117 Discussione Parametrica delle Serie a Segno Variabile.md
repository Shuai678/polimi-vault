---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 12, PDF pp. 24-27
---

# Discussione parametrica delle serie a segno variabile

## Quando si usa e idea

Se una base dipende da un parametro reale, il suo segno può cambiare: la stessa formula può descrivere serie positive, alternate o nulle. Prima di scegliere un criterio conviene isolare una base geometrica e individuare i valori di frontiera.

L'esercizio del docente combina [[111 Criterio della Radice per Serie|radice]], [[114 Convergenza Assoluta e Semplice delle Serie|convergenza assoluta]], [[115 Serie Alternate e Criterio di Leibniz|Leibniz]] e [[103 Condizione Necessaria di Convergenza di una Serie|condizione necessaria]].

## Esercizio — Testo

Discutere al variare di $\alpha\in\mathbb R$ il carattere della serie

$$
\sum_{n=1}^{+\infty}\frac{(\alpha-1)^n}{n\,2^n}.
$$

## Riduzione del parametro

Poniamo

$$
q=\frac{\alpha-1}{2}.
$$

La serie diventa $\sum q^n/n$. I valori di frontiera $q=-1,0,1$ corrispondono rispettivamente ad $\alpha=-1,1,3$. Per $q<0$ i segni alternano, per $q>0$ i termini sono positivi, per $q=0$ sono tutti nulli.

## Svolgimento passo per passo

### 1. $|q|<1$: convergenza assoluta

Per $q\neq0$, la serie dei moduli è $\sum|q|^n/n$ e

$$
\sqrt[n]{\frac{|q|^n}{n}}
=|q|\exp\left(-\frac{\log n}{n}\right)\longrightarrow|q|<1.
$$

Per il criterio della radice converge la serie dei moduli, quindi quella originaria converge assolutamente. Se $q=0$, la serie è nulla e converge assolutamente direttamente. Traducendo $-1<q<1$,

$$
-1<\frac{\alpha-1}{2}<1
\iff -2<\alpha-1<2
\iff -1<\alpha<3.
$$

### 2. $q=1$, ossia $\alpha=3$

La serie è $\sum1/n$: diverge a $+\infty$.

### 3. $q=-1$, ossia $\alpha=-1$

La serie è $\sum(-1)^n/n$: converge per Leibniz. La serie dei moduli è armonica, quindi la convergenza è **solo semplice**.

### 4. $q>1$, ossia $\alpha>3$

La [[85 Gerarchia degli Infiniti|crescita esponenziale prevale su quella polinomiale]], perciò $q^n/n\to+\infty$. Il termine non tende a zero e la serie non converge. Essendo a termini positivi, diverge a $+\infty$.

### 5. $q<-1$, ossia $\alpha<-1$

Scriviamo $q=-r$, con $r>1$. Il termine è $(-1)^n c_n$, dove $c_n=r^n/n\to+\infty$. La condizione necessaria esclude la convergenza finita.

Per distinguere divergenza e irregolarità, esaminiamo le somme parziali. Siccome

$$
\frac{c_{n+1}}{c_n}=r\frac n{n+1}\longrightarrow r>1,
$$

le ampiezze sono definitivamente crescenti. Quindi, da un certo indice in poi,

$$
S_{2k}-S_{2k-2}=c_{2k}-c_{2k-1}\geq0,
$$

$$
S_{2k+1}-S_{2k-1}=c_{2k}-c_{2k+1}\leq0.
$$

Le somme parziali pari sono definitivamente limitate inferiormente dal loro valore iniziale nella coda: l'intera successione non può tendere a $-\infty$. Quelle dispari sono definitivamente limitate superiormente: l'intera successione non può tendere a $+\infty$. Poiché è già escluso un limite finito, la serie è **irregolare**.

## Risultato

| Valore di $\alpha$ | Carattere |
|---|---|
| $\alpha<-1$ | Irregolare |
| $\alpha=-1$ | Convergente solo semplicemente |
| $-1<\alpha<3$ | Assolutamente convergente; per $\alpha=1$ è la serie nulla |
| $\alpha\geq3$ | Divergente a $+\infty$ |

![[117 Classificazione Parametrica della Serie.svg|900]]

L'estremo $\alpha=-1$ appartiene all'insieme di convergenza semplice ma non a quello di convergenza assoluta. L'estremo $\alpha=3$ non appartiene a nessuno dei due.

## Procedura generalizzabile

1. Raccogliere la dipendenza esponenziale in una base $q(\alpha)$.
2. Individuare separatamente $q<-1$, $q=-1$, $-1<q<0$, $q=0$, $0<q<1$, $q=1$, $q>1$; unire poi i casi con la stessa conclusione.
3. Studiare la serie dei moduli negli intervalli interni.
4. Sostituire esattamente i parametri di frontiera nella formula originaria.
5. Fuori dalla regione di convergenza, distinguere divergenza positiva e irregolarità usando segni e somme parziali.

## Errori comuni

Il criterio della radice si applica ai **moduli** quando la base è negativa. Un limite della radice dei moduli maggiore di $1$ esclude la convergenza della serie originaria, ma non ne prova la divergenza positiva: con i segni alterni può esserci irregolarità. Il valore $\alpha=1$ non va perso dividendo per un termine nullo.

Non occorre calcolare la somma della serie per determinarne il carattere. Qui i criteri disponibili risolvono la classificazione senza introdurre formule per la somma non ancora trattate.

### Da dire all'orale

> Riducendo la base a q uguale ad alfa meno uno diviso due, ottengo convergenza assoluta per modulo di q minore di uno. Alla frontiera q uguale a meno uno resta l'armonica alternata, solo semplicemente convergente; a q uguale a uno resta l'armonica divergente. Per q maggiore di uno la divergenza è positiva, mentre per q minore di meno uno la serie è irregolare.
