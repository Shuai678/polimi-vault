---
course: Analisi 1
type: formula-sheet
status: Da studiare
updated: 2026-11-03
cssclasses:
  - formulario
source:
  - Lezioni 13 e 14, PDF integrali
---

# Limiti e continuità delle funzioni

[[00 Indice Formulario|Indice del formulario]] · [[Lecture 13|Lezione 13]] · [[Lecture 14|Lezione 14]]

> [!note] Seconda parte - Da studiare
> Formule e condizioni nell'ordine dei PDF. Le note collegate contengono le spiegazioni complete e distinguono prove del professore e commenti aggiunti.

## Intorni, accumulazione e limite

[[119 Intorni Finiti e Infiniti|Intorni]]:

$$
\mathcal U(x_0)=(x_0-\varepsilon,x_0+\varepsilon),\quad\varepsilon>0;
\qquad\mathcal U(+\infty)=(M,+\infty),\quad\mathcal U(-\infty)=(-\infty,M).
$$

[[120 Punti di Accumulazione|Accumulo]]: per ogni intorno, $(\mathcal U(x_0)\cap I)\setminus\{x_0\}\neq\varnothing$. $x_0$ può non appartenere a $I$.

[[121 Limite di Funzione e Definizione Successionale|Limite successionale]]: ogni $x_n\in I$, $x_n\neq x_0$, $x_n\to x_0$ deve soddisfare $f(x_n)\to\ell$. Due successioni ammissibili con limiti delle immagini diversi escludono il limite.

[[122 Unicità del Limite di Funzione|Unicità]]: il limite, quando esiste, è unico anche nella retta estesa. Prova del docente: ricondurre per assurdo la stessa successione di immagini a due limiti diversi.

[[123 Definizione Topologica di Limite e Teorema Ponte|Definizione topologica]]:

$$
\forall\mathcal U(\ell)\ \exists\mathcal U(x_0):
\quad x\in(\mathcal U(x_0)\cap I)\setminus\{x_0\}
\Rightarrow f(x)\in\mathcal U(\ell).
$$

Teorema ponte: equivalenza con la definizione successionale; senza dimostrazione nel PDF.

## Casi metrici e asintoti - Lezione 13

In tutte le formule: $x\in I$ e il punto/direzione di avvicinamento è di accumulazione per il dominio.

| Caso | Quantificatori e condizione |
|---|---|
| [[124 Limiti Finiti all'Infinito e Asintoti Orizzontali\|Finito a più infinito]] | $\forall\varepsilon>0\ \exists M>0:\ x>M\Rightarrow\lvert f(x)-\ell\rvert<\varepsilon$ |
| Finito a meno infinito | $\forall\varepsilon>0\ \exists M>0:\ x<-M\Rightarrow\lvert f(x)-\ell\rvert<\varepsilon$ |

**Orizzontale:** limite finito $\ell$ a una delle due direzioni infinite ⇒ asintoto $y=\ell$.

**Eccesso/difetto:** $\ell^+$ o $\ell^-$ significa limite $\ell$ con $f(x)\geq\ell$ o $f(x)\leq\ell$ definitivamente, secondo il docente. I segni sul valore non indicano il lato delle ascisse.

[[125 Limiti Infiniti all'Infinito|Limiti infiniti all'infinito]]: per ogni $M>0$ esiste $K>0$ tale che, per $x\in I$,

- a $+\infty$: $x>K\Rightarrow f(x)>M$ per il limite $+\infty$, oppure $f(x)<-M$ per il limite $-\infty$;
- a $-\infty$: si sostituisce la condizione sull'ascissa con $x<-K$.

[[126 Asintoti Obliqui|Obliquo]]:

$$
m=\lim_{x\to\pm\infty}\frac{f(x)}x\in\mathbb R\setminus\{0\},
\qquad q=\lim_{x\to\pm\infty}(f(x)-mx)\in\mathbb R.
$$

Servono entrambi; l'asintoto è $y=mx+q$ e $f(x)-(mx+q)\to0$.

## Limiti al finito e laterali - Lezione 14

[[127 Limiti Infiniti al Finito|Limite infinito al finito]]:

$$
\forall M>0\ \exists\delta>0:\quad
0<|x-x_0|<\delta\Rightarrow f(x)>M
\quad\text{oppure}\quad f(x)<-M.
$$

[[128 Limiti Laterali e Asintoti Verticali|Laterali]]: da destra $x_0<x<x_0+\delta$; da sinistra $x_0-\delta<x<x_0$. Se il dominio accumula da entrambi i lati, il bilatero vale $\ell$ se e solo se i due laterali valgono lo stesso $\ell\in\overline{\mathbb R}$.

**Verticale:** almeno un limite laterale infinito ⇒ asintoto $x=x_0$.

[[129 Limiti Finiti al Finito|Limite finito al finito]]:

$$
\forall\varepsilon>0\ \exists\delta>0:\quad
0<|x-x_0|<\delta\Rightarrow|f(x)-\ell|<\varepsilon.
$$

## Continuità e classificazione delle discontinuità

[[130 Continuità di una Funzione|Continuità]]: $x_0\in I$ e, nella definizione del docente, punto di accumulazione per $I$.

$$
\lim_{x\to x_0}f(x)=f(x_0);
\qquad
\forall\varepsilon>0\ \exists\delta>0:\ |x-x_0|<\delta
\Rightarrow |f(x)-f(x_0)|<\varepsilon.
$$

Qui il centro è compreso. Per ogni successione $x_n\in I$ tendente a $x_0$, $f(x_n)\to f(x_0)$. Notazione: $f\in C^0(I)$.

[[131 Funzione di Dirichlet e Discontinuità Ovunque|Dirichlet]]: valore $1$ sui razionali e $0$ sugli irrazionali; non ha limite in alcun punto della retta reale estesa; la prova usa successioni razionali e irrazionali.

| Tipo secondo il docente | Condizioni, con $x_0\in I$ |
|---|---|
| [[132 Discontinuità Eliminabili ed Estensione per Continuità\|Eliminabile]] | Limite $\ell\in\mathbb R$ esistente ma diverso da $f(x_0)$; porre $f(x_0)=\ell$ elimina la discontinuità |
| [[133 Discontinuità a Salto\|Prima specie / salto]] | Due limiti laterali finiti e diversi; $s(x_0)=\ell_\mathrm{destro}-\ell_\mathrm{sinistro}$ |
| [[134 Discontinuità di Seconda Specie\|Seconda specie]] | Almeno un limite laterale infinito oppure non esistente nella retta estesa; include l'oscillazione |

Se $x_0$ era escluso dal dominio ma il limite è finito, si parla di **estensione per continuità**, aggiungendo il punto e il valore limite. Se il limite è infinito o non esiste, nessun valore reale al solo centro rende la funzione continua.

## Proprietà definitive, confronti, segno e algebra

[[135 Proprietà Definitive e Teoremi di Confronto per Funzioni|Proprietà definitiva]]: vale per tutti i punti del dominio di un intorno opportuno, escluso il centro.

- Due carabinieri: $f\leq g\leq h$ definitivamente e limiti di $f,h$ uguali a $\ell$ ⇒ $g\to\ell$.
- Confronti infiniti: $f\leq g$, $f\to+\infty$ ⇒ $g\to+\infty$; $g\to-\infty$ ⇒ $f\to-\infty$.
- $|f|\leq g$, $g\to0$ ⇒ $f\to0$.
- $g\to0$, $h$ definitivamente limitata ⇒ $gh\to0$.

[[136 Permanenza del Segno per Funzioni|Permanenza del segno]]: limite $\ell>0$ ⇒ positività definitiva; $\ell<0$ ⇒ negatività definitiva. Viceversa, segno non negativo/non positivo e limite esistente ⇒ limite non negativo/non positivo. La positività dei valori può dare limite zero.

[[137 Algebra dei Limiti di Funzioni|Algebra]]: somma/differenza, prodotto, quoziente, potenza variabile, potenza fissa. Controllare dominio e forme escluse; nelle potenze reali variabili il PDF richiede base positiva. Il denominatore tendente a zero senza segno fissato richiede uno studio ulteriore.

## Dimostrazioni della seconda parte

[[01 Dimostrazioni Seconda Parte|Indice delle prove della seconda parte]]: unicità del limite di funzione e continuità dell'esponenziale, entrambe svolte dal docente. Le note incorporano la prova dal Concept corrispondente per mantenerla allineata.
