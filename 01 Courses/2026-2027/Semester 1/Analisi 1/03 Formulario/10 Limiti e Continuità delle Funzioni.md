---
course: Analisi 1
type: formula-sheet
status: Da studiare
updated: 2026-11-09
cssclasses:
  - formulario
source:
  - Lezioni 13, 14, 15 e 16, PDF integrali
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

## Lezione 15 - Continuità e cambio di variabile

Nuova parte **Da studiare**, nell'ordine del PDF L15. [[Lecture 15|Indice della lezione]].

[[138 Algebra delle Funzioni Continue|Algebra della continuità]]: somma/differenza, prodotto, quoziente con denominatore non nullo nel punto, potenza fissa ben definita vicino al punto e nel punto.

[[139 Cambio di Variabile nei Limiti e Continuità della Composta|Cambio di variabile]]:

$$
g(x)\to t_0,\quad f(t)\to\ell\ (t\to t_0),\quad
 g(x)\neq t_0\text{ definitivamente}
\ \Longrightarrow\ f(g(x))\to\ell.
$$

La composta deve essere definita nella zona del limite. L'ultima condizione è superflua se $t_0=\pm\infty$ o se $f$ è continua in $t_0$. Se entrambe le funzioni sono continue nei rispettivi punti, la composta è continua.

## Lezione 15 - Confronti e otto limiti notevoli

[[94 Equivalenza Asintotica#Lezione 15 - Equivalenza asintotica per funzioni - Da studiare|Equivalenza]]: $f\sim g\iff f/g\to1\iff f=g+o(g)$. [[93 Notazione o-Piccolo#Lezione 15 - o-piccolo e infinitesimi per funzioni - Da studiare|o-piccolo]]: $f=o(g)\iff f/g\to0$. Il denominatore è definitivamente non nullo. Le equivalenze si moltiplicano, si dividono e si elevano a potenze fisse definite; non si sommano o compongono arbitrariamente con logaritmi ed esponenziali.

[[95 Equivalenti e Sviluppi Asintotici Notevoli#Lezione 15 - Limiti notevoli di funzioni - Da studiare|Limiti notevoli]], angoli in radianti, logaritmo naturale, nell'ordine del docente:

| # | Limite |
|---|---|
| 1 | $\displaystyle\lim_{x\to0}\frac{\sin x}x=1$ |
| 2 | $\displaystyle\lim_{x\to0}\frac{1-\cos x}{x^2}=1/2$ |
| 3 | $\displaystyle\lim_{x\to\pm\infty}(1+1/x)^x=e$ |
| 4 | $\displaystyle\lim_{x\to0}\frac{\log(1+x)}x=1$ |
| 5 | $\displaystyle\lim_{x\to0}\frac{e^x-1}x=1$ |
| 6 | $\displaystyle\lim_{x\to0}\frac{(1+x)^\alpha-1}x=\alpha$, $\alpha\in\mathbb R$ fissato |
| 7 | $\displaystyle\lim_{x\to0}\frac{\tan x}x=1$ |
| 8 | $\displaystyle\lim_{x\to0}\frac{\arctan x}x=1$ |

Negli sviluppi si può sostituire a $x$ un argomento infinitesimo definitivamente non nullo, controllando i domini. Per il coseno la scala è il quadrato dell'argomento; nella potenza l'equivalenza con $\alpha x$ richiede $\alpha\neq0$. Le prove sono rinviate nel PDF.

[[85 Gerarchia degli Infiniti#Lezione 15 - Gerarchia per funzioni - Da studiare|Gerarchia]], per $a>1$, $\alpha,\beta>0$ fissati:

$$
(\log_a x)^\alpha=o(x^\beta),\quad x^\beta=o(a^x)\quad(x\to+\infty),
$$

$$
t^\beta|\log_a t|^\alpha\to0\quad(t\to0^+).
$$

[[140 Grafici Locali e Grafici Probabili|Grafici probabili]]: il termine dominante dipende dalla zona. $f\sim g$ non garantisce uguaglianza di forma o assenza di oscillazioni.

## Lezione 15 - Zeri e Weierstrass

[[141 Teorema degli Zeri e Metodo di Bisezione|Zeri - D15]]: $f\in C^0([a,b])$, $a<b$ reali, $f(a)f(b)<0$ ⇒ $\exists x_0\in(a,b)$ con $f(x_0)=0$. Se $f$ è strettamente monotona, lo zero è unico. Prova del professore in [[D15 Teorema di Esistenza degli Zeri]].

$$
b_n-a_n=\frac{b-a}{2^n},\qquad
c_n=\frac{a_n+b_n}{2},\qquad
|c_n-x_0|\leq\frac{b-a}{2^{n+1}}.
$$

[[142 Teorema di Weierstrass|Weierstrass - D17]]: $f\in C^0([a,b])$, $a<b$ reali ⇒ $\exists x_m,x_M\in[a,b]$ con

$$
f(x_m)\leq f(x)\leq f(x_M)\quad\forall x\in[a,b].
$$

Massimo e minimo sono raggiunti; la funzione è limitata. [[D17 Teorema di Weierstrass|D17]] contiene ora anche la prova del docente, aggiunta dalla Lezione 16; nel PDF L15 era presente solo l'enunciato. Le voci D15 e D17 appartengono alla seconda parte, oltre il primo parziale.

## Lezione 16 - Weierstrass e valori intermedi

Nuova parte **Da studiare**. Percorso completo: [[Lecture 16]].

[[142 Teorema di Weierstrass|Weierstrass - D17]]: la prova del docente è ora nella [[D17 Teorema di Weierstrass|D17]]. Bisezione che conserva $\Lambda=\sup f$; poi esclusione di $\Lambda=+\infty$ e scelta $\Lambda-1/n<f(x_n)\leq\Lambda$ per mostrare che $f(x_M)=\Lambda$.

[[143 Teorema dei Valori Intermedi e Immagine di un Intervallo|Valori intermedi - D16]]: per $f$ continua su un intervallo $I$, da $y_1,y_2\in\operatorname{Im}f$ segue $[y_1,y_2]\subseteq\operatorname{Im}f$ quando $y_1\leq y_2$. L'immagine è un intervallo. Prova del docente: applicare gli zeri a $g=f-\lambda$ fra due controimmagini; [[D16 Teorema dei Valori Intermedi]].

Su un intervallo generale gli estremi dell'immagine possono essere assunti oppure no. Se il dominio è $[a,b]$ con estremi reali, la continuità dà

$$
\operatorname{Im}f=[m,M],\qquad m=\min_{[a,b]}f,\quad M=\max_{[a,b]}f.
$$

## Lezione 16 - Monotonia, continuità e inversa

[[144 Limiti delle Funzioni Monotone su un Intervallo|Limiti delle funzioni monotone]]: per una funzione crescente su $(a,b)$ e $x_0$ interno,

$$
\lim_{x\to x_0^-}f(x)=\sup_{(a,x_0)}f\leq f(x_0)
\leq\inf_{(x_0,b)}f=\lim_{x\to x_0^+}f(x),
$$

con entrambi i limiti finiti. Agli estremi:

$$
\lim_{x\to a^+}f(x)=\inf_{(a,b)}f,\qquad
\lim_{x\to b^-}f(x)=\sup_{(a,b)}f,
$$

eventualmente infiniti. Per la decrescente si scambiano superiore/inferiore e si invertono le disuguaglianze. Le eventuali discontinuità interne sono soltanto a salto. Estremo reale con limite finito: possibile prolungamento continuo; limite infinito: asintoto verticale.

[[67 Monotonia e Funzione Inversa#Lezione 16 - Continuità e invertibilità su un intervallo - Da studiare|Continuità e invertibilità]]: se $f$ è continua su un intervallo, stretta monotonia e invertibilità sulla propria immagine sono equivalenti. In questo caso l'immagine è un intervallo e l'inversa è continua sul proprio dominio, con lo stesso verso di monotonia.

[[145 Continuità delle Funzioni Elementari|Funzioni elementari]]: continue nei rispettivi domini, con le restrizioni per reciproci, radici, logaritmi e potenze. Per seno e coseno: prima zero tramite $\lvert\sin x\rvert\leq\lvert x\rvert$ e $\cos x=1-2\sin^2(x/2)$, poi il punto generico tramite addizione. [[Continuità di Seno e Coseno - Dimostrazione|Prova completa]].

## Lezione 16 - Prove dei limiti notevoli

[[Limiti Notevoli di Logaritmo Esponenziale e Potenza - Dimostrazioni|Prove incorporate dal Concept 95]], nell'ordine:

1. Richiamo del limite di tipo Nepero per argomenti reali, non dimostrato in queste pagine.
2. Logaritmo: continuità di log e cambio reciproco $x=1/t$, considerando entrambi i lati di zero.
3. Esponenziale: $t=e^x-1$, $x=\log(1+t)$, reciproco del rapporto logaritmico.
4. Potenza: prima $\alpha=0$; poi $t=\alpha\log(1+x)$ e prodotto dei due rapporti notevoli.

$$
\frac{(1+x)^\alpha-1}{x}
=\frac{e^{\alpha\log(1+x)}-1}{\alpha\log(1+x)}
\alpha\frac{\log(1+x)}x\longrightarrow\alpha\qquad(\alpha\neq0).
$$

Vicino a zero $1+x>0$ e, fuori dal centro, $\alpha\log(1+x)\neq0$ per $\alpha\neq0$. Commenti e precisazione delle frecce di limite sono nella nota completa.
