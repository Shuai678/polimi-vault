---
course: Analisi 1
type: concept
status: Da studiare
source:
  - Lezione 14, PDF pp. 6-7
  - Libro, §5.1, pp. 132-133
---

# Limiti finiti al finito

## Quarto caso metrico del docente

Siano $f:I\subseteq\mathbb R\to\mathbb R$, $x_0\in\mathbb R$ punto di accumulazione per $I$ e $\ell\in\mathbb R$. Si ha

$$
\boxed{\lim_{x\to x_0}f(x)=\ell}
$$

se e solo se

$$
\forall\varepsilon>0\ \exists\delta>0\ \forall x\in I:
\quad0<|x-x_0|<\delta\Longrightarrow|f(x)-\ell|<\varepsilon.
$$

Nel PDF le stesse condizioni sono espresse con gli intervalli:

$$
x\in(x_0-\delta,x_0+\delta),\quad x\neq x_0
\Longrightarrow f(x)\in(\ell-\varepsilon,\ell+\varepsilon).
$$

## Osservazioni del docente

Non importa che $f$ sia definita oppure no in $x_0$; se è definita, non importa il valore $f(x_0)$. Il limite usa soltanto i punti del dominio **diversi** da $x_0$.

Si possono combinare limiti da destra o da sinistra con limiti per eccesso o difetto. L'esempio di notazione presentato dal docente è

$$
\lim_{x\to x_0^-}f(x)=\ell^+.
$$

Con la sua convenzione significa

$$
\forall\varepsilon>0\ \exists\delta>0:\quad
x\in I,\ x_0-\delta<x<x_0
\Longrightarrow\ell\leq f(x)<\ell+\varepsilon.
$$

Le ascisse arrivano da sinistra, mentre i valori arrivano per eccesso. Sono due informazioni indipendenti.

## Commenti: come scegliere $\delta$

Il valore di $\varepsilon$ è fissato da chi richiede la precisione; dobbiamo costruire $\delta$ affinché la richiesta valga per **tutti** i punti ammessi. Non si sceglie $\delta$ in funzione del singolo $x$ che poi verrà controllato.

### Esempio di supporto svolto: $x^2\to4$ per $x\to2$

Vogliamo rendere $|x^2-4|$ minore di $\varepsilon$. Scomponiamo:

$$
|x^2-4|=|x-2|\,|x+2|.
$$

Imponendo prima $|x-2|<1$ otteniamo $1<x<3$, quindi $|x+2|<5$. Perciò

$$
|x^2-4|<5|x-2|.
$$

Dato $\varepsilon>0$, scegliamo

$$
\delta=\min\left\{1,\frac\varepsilon5\right\}>0.
$$

Se $0<|x-2|<\delta$, valgono insieme la stima $|x+2|<5$ e $5|x-2|<\varepsilon$. Quindi $|x^2-4|<\varepsilon$, come richiesto. Il minimo serve a soddisfare contemporaneamente due condizioni, non a trovare una distanza ottimale.

L'esempio è un'integrazione didattica; il PDF presenta la definizione e il suo schema geometrico.

![[129 Limite Finito al Finito.svg|900]]

Nel grafico la funzione coincide con $x^2$ fuori da $2$, ma nel solo punto è assegnato $f(2)=7$: il limite rimane $4$. È uno schema di supporto per mostrare che il valore al centro non determina il limite.

## Errori comuni e collegamenti

Non eliminare $0<|x-x_0|$: questa condizione esclude il centro dal limite. Nella [[130 Continuità di una Funzione|continuità]] il centro sarà invece compreso. Non confondere “esiste qualche punto vicino con valore vicino” con la richiesta uniforme su tutti i punti dell'intorno privato del centro.

### Da dire all'orale

> Il limite è elle se, fissata qualsiasi precisione positiva sui valori, esiste una distanza positiva dal punto tale che tutti i punti del dominio a distanza non nulla minore di quella distanza hanno immagine a distanza da elle minore della precisione. Il valore della funzione nel punto non interviene.
