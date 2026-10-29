---
course: Analisi 1
type: formula-sheet
updated: 2026-10-29
cssclasses:
  - formulario
---

# Formulario unico dei limiti

[[00 Indice Formulario|Indice del formulario]] · [[05 Successioni e Limiti|Teoria delle successioni]] · [[06 Equivalenti e Limiti Notevoli|Equivalenti e limiti notevoli]]

Tabella di ripasso dei principali limiti di successioni, compresi quelli delle funzioni goniometriche inverse. In tutta la nota si suppone:

$$
\boxed{n\to+\infty}
$$

Il simbolo $\log$ indica il **logaritmo naturale** e gli angoli sono in **radianti**. Si considerano interi $n\geq1$, aumentando l'indice iniziale quando il dominio lo richiede: per esempio $n\geq2$ per $\arcsin(2/n)$, $\arccos(2/n)$ e $n/\log n$.

## Tabella dei limiti

**Categorie:** [[#Trigonometriche inverse|Trigonometriche inverse]] · [[#Trigonometriche|Trigonometriche]] · [[#Logaritmi|Logaritmi]] · [[#Esponenziali|Esponenziali]] · [[#Limiti notevoli|Limiti notevoli]] · [[#Potenze e radici|Potenze e radici]] · [[#Successioni oscillanti|Successioni oscillanti]] · [[#Arcotangente avanzata|Arcotangente avanzata]]

### Trigonometriche inverse

| Successione | Limite |
| --- | :---: |
| $\arctan n$ | $\dfrac{\pi}{2}$ |
| $\arctan(-n)$ | $-\dfrac{\pi}{2}$ |
| $\arctan\dfrac1n$ | $0$ |
| $\arcsin\dfrac1n$ | $0$ |
| $\arcsin\dfrac2n$ | $0$ |
| $\arccos\dfrac1n$ | $\dfrac{\pi}{2}$ |
| $\arccos\dfrac2n$ | $\dfrac{\pi}{2}$ |

### Trigonometriche

| Successione | Limite |
| --- | :---: |
| $\sin n$ | Non esiste |
| $\cos n$ | Non esiste |
| $\tan n$ | Non esiste |
| $\sin\dfrac1n$ | $0$ |
| $\cos\dfrac1n$ | $1$ |
| $\tan\dfrac1n$ | $0$ |
| $\dfrac{\sin n}{n}$ | $0$ |
| $\dfrac{\cos n}{n}$ | $0$ |

### Logaritmi

| Successione | Limite |
| --- | :---: |
| $\log n$ | $+\infty$ |
| $\log\dfrac1n$ | $-\infty$ |
| $\log\!\left(1+\dfrac1n\right)$ | $0$ |
| $\log(n+1)-\log n$ | $0$ |
| $\dfrac{\log n}{n}$ | $0$ |
| $\dfrac{\log n}{\sqrt n}$ | $0$ |
| $\dfrac{n}{\log n}$ | $+\infty$ |

### Esponenziali

| Successione | Limite |
| --- | :---: |
| $e^n$ | $+\infty$ |
| $e^{-n}$ | $0$ |
| $ne^{-n}$ | $0$ |
| $\dfrac{n^2}{e^n}$ | $0$ |
| $e^{1/n}$ | $1$ |

### Limiti notevoli

| Successione | Limite |
| --- | :---: |
| $n\sin\dfrac1n$ | $1$ |
| $n\tan\dfrac1n$ | $1$ |
| $n\arctan\dfrac1n$ | $1$ |
| $n\arcsin\dfrac1n$ | $1$ |
| $n\log\!\left(1+\dfrac1n\right)$ | $1$ |
| $n\left(e^{1/n}-1\right)$ | $1$ |
| $n^2\left(1-\cos\dfrac1n\right)$ | $\dfrac12$ |
| $\left(1+\dfrac1n\right)^n$ | $e$ |
| $\left(1+\dfrac an\right)^n$, $a\in\mathbb R$ fissato | $e^a$ |

### Potenze e radici

| Successione | Limite |
| --- | :---: |
| $n^{1/n}$ | $1$ |
| $a^{1/n}$, $a>0$ fissato | $1$ |
| $\dfrac{n+1}{n}$ | $1$ |
| $\sqrt{n^2+1}-n$ | $0$ |
| $\sqrt{n^2+2n}-n$ | $1$ |
| $\dfrac{n!}{n^n}$ | $0$ |
| $\dfrac{2^n}{n!}$ | $0$ |

### Successioni oscillanti

| Successione | Limite |
| --- | :---: |
| $(-1)^n$ | Non esiste |
| $(-2)^n$ | Non esiste |
| $\dfrac{(-1)^n}{n}$ | $0$ |

### Arcotangente avanzata

| Successione | Limite |
| --- | :---: |
| $\dfrac\pi2-\arctan n$ | $0$ |
| $n\left(\dfrac\pi2-\arctan n\right)$ | $1$ |

Le costanti indicate sono indipendenti da $n$. Per $\left(1+a/n\right)^n$ la base è positiva definitivamente anche quando $a<0$.

> [!note] Oscillazioni e limite
> **Non esiste** significa che la successione non ha limite neppure nei reali estesi. In particolare $(-2)^{2k}\to+\infty$ e $(-2)^{2k+1}\to-\infty$: l'alternanza del segno impedisce un unico limite. Invece un fattore limitato moltiplicato per $1/n$ tende a zero, come in $\sin n/n$, $\cos n/n$ e $(-1)^n/n$; vedi [[84 Confronto in Modulo e Prodotto con un Infinitesimo]].

## Come usare gli asintotici insieme alla tabella

Prima di scegliere una formula, controllare **dove tende l'argomento della funzione**. Le equivalenze raccolte in [[95 Equivalenti e Sviluppi Asintotici Notevoli]] valgono per un argomento che tende a zero.

### Caso 1 — L'argomento tende a zero

Per esempio:

$$
\arctan\frac2n.
$$

Poiché $2/n\to0$, si applica $\arctan t\sim t$ per $t\to0$:

$$
\arctan\frac2n\sim\frac2n\to0.
$$

Lo stesso ragionamento, applicato a $1/n$, permette di ricavare $n\arctan(1/n)\to1$. È decisivo verificare l'argomento, indipendentemente dal numero assegnato alla formula nel proprio foglio degli asintotici.

### Caso 2 — L'argomento tende all'infinito

Per $\arctan n$, l'argomento tende a $+\infty$, quindi l'equivalenza $\arctan t\sim t$ per $t\to0$ non si applica. Si usa invece:

$$
\boxed{\lim_{n\to+\infty}\arctan n=\frac\pi2}.
$$

Per le definizioni e gli intervalli delle inverse, vedi [[69 Funzioni Goniometriche Inverse]].

### Arcotangente avanzata: ridurre l'argomento a zero

Per $n>0$ vale l'identità:

$$
\frac\pi2-\arctan n=\arctan\frac1n.
$$

Il membro destro ha argomento infinitesimo, quindi:

$$
\frac\pi2-\arctan n\sim\frac1n.
$$

Da questa equivalenza si ricavano entrambi i limiti dell'ultima categoria della tabella:

$$
\frac\pi2-\arctan n\to0,
\qquad
n\left(\frac\pi2-\arctan n\right)\to1.
$$

## Gerarchia degli infiniti da memorizzare

Per $n\to+\infty$, $\alpha>0$ e $a>1$ **fissati**:

$$
\boxed{\log n\ll n^\alpha\ll a^n\ll n!\ll n^n}.
$$

Qui $f_n\ll g_n$ significa $f_n/g_n\to0$, cioè $f_n=o(g_n)$. La gerarchia è utile nelle forme indeterminate $\infty/\infty$: il termine che cresce più lentamente, diviso per quello che cresce più rapidamente, tende a zero.

Per esempio:

$$
\frac{\log n}{\sqrt n}\to0,
\qquad
\frac{n^2}{e^n}\to0,
\qquad
\frac{2^n}{n!}\to0,
\qquad
\frac{n!}{n^n}\to0.
$$

La versione generale, che include le potenze positive del logaritmo, è in [[85 Gerarchia degli Infiniti]].

## Ripasso per il parziale

Per il parziale del **2 novembre** indicato nel materiale fornito, concentrare inizialmente il ripasso su **funzioni trigonometriche inverse**, **limiti notevoli** e **gerarchia degli infiniti**. Non occorre imparare tutta la tabella a memoria: molti risultati si ricavano con continuità, limiti notevoli ed equivalenti asintotici.

---

[[07 Serie Numeriche|← Serie Numeriche]] · [[00 Indice Formulario#Indice rapido|↑ Indice]]
