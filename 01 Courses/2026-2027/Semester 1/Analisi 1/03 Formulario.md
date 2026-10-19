---
course: Analisi 1
type: formula-sheet
updated: 2026-10-18
---

# Formulario di Analisi 1

[[01 Courses/2026-2027/Semester 1/Analisi 1/00 Course Map|Corso]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/02 Exam Book|Exam Book]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/Concepts/00 Indice dei Concetti/00 Indice dei Concetti|Tutti i concetti]]

Formule, definizioni ed enunciati essenziali delle note attuali. I titoli aprono le pagine complete, con spiegazioni, esempi e dimostrazioni. Sono inclusi anche contenuti preparati e ancora da studiare.

> [!info] Teoria del primo parziale
> **D1–D14**: dimostrazioni richieste per il parziale, secondo il perimetro indicato per lo studio; i numeri seguono il [[AM1-regolamento26-27.pdf|regolamento ufficiale]]. L'etichetta segnala la **dimostrazione** da sapere: anche gli altri risultati possono essere richiesti come definizione, enunciato o applicazione. La nota completa della **D14** è ancora da integrare.

## Indice rapido

[[#Linguaggio e dimostrazioni|Linguaggio]] · [[#Numeri reali e ordine|Reali e ordine]] · [[#Numeri complessi|Complessi]] · [[#Funzioni|Funzioni]] · [[#Successioni e limiti|Successioni e limiti]] · [[#Equivalenti e limiti notevoli|Equivalenti]] · [[#Serie numeriche|Serie]]

## Linguaggio e dimostrazioni

| Voce | Essenziale |
| --- | --- |
| [[08 Differenza tra Insiemi\|Differenza]] · [[09 Sottoinsiemi e Inclusione\|inclusione]] | $A\setminus B=\{x\in A:x\notin B\}$. $A\subseteq B\iff\forall x\,(x\in A\Rightarrow x\in B)$. |
| [[12 Congiunzione Logica\|Congiunzione]] · [[13 Disgiunzione Logica\|disgiunzione]] | $P\land Q$: entrambe vere; $P\lor Q$: almeno una vera, anche entrambe. |
| [[15 Implicazione Logica\|Implicazione]] · [[16 Condizioni Necessarie e Sufficienti\|condizioni]] | $P\Rightarrow Q$ è falsa solo con $P$ vera e $Q$ falsa. $P$ è sufficiente per $Q$; $Q$ è necessaria per $P$. $P\Leftrightarrow Q$: entrambe le implicazioni. |
| [[11 Predicati e Variabili Libere\|Quantificatori]] · [[14 Negazione Logica\|negazioni]] | $\neg(\forall x\,P)=\exists x\,\neg P$; $\neg(\exists x\,P)=\forall x\,\neg P$. $\neg(P\land Q)=\neg P\lor\neg Q$; $\neg(P\lor Q)=\neg P\land\neg Q$. |
| [[17 Dimostrazione Diretta\|Diretta]] · [[18 Dimostrazione per Contrapposizione\|contrapposizione]] | Diretta: dalle ipotesi alla tesi. Contrapposizione: $P\Rightarrow Q\iff\neg Q\Rightarrow\neg P$. |
| [[19 Controesempio\|Controesempio]] · [[20 Dimostrazione per Assurdo\|assurdo]] | Per confutare $P\Rightarrow Q$: un caso con $P$ vera e $Q$ falsa. Per assurdo: ipotesi e negazione della tesi devono portare a contraddizione. |
| [[21 Dimostrazione per Induzione\|Induzione]] | Verificare $P(n_0)$ e, per ogni $n\geq n_0$, provare $P(n)\Rightarrow P(n+1)$. Allora $P(n)$ vale per ogni $n\geq n_0$. |

## Numeri reali e ordine

| Voce | Essenziale |
| --- | --- |
| [[03 Numeri Razionali\|Insiemi numerici]] · [[06 Numeri Reali e Irrazionali\|reali]] | $\mathbb N\subset\mathbb Z\subset\mathbb Q\subset\mathbb R\subset\mathbb C$; $\mathbb Q=\{p/q:p,q\in\mathbb Z,\ q\neq0\}$; irrazionali $=\mathbb R\setminus\mathbb Q$. |
| [[20 Dimostrazione per Assurdo\|Irrazionalità di √2]] **D1** | $\sqrt2\notin\mathbb Q$. Dimostrazione per assurdo con frazione ridotta ai minimi termini e parità di numeratore e denominatore. |
| [[21 Dimostrazione per Induzione\|Disuguaglianza di Bernoulli]] **D2** | $(1+x)^n\geq1+nx$ per $x>-1$ e $n\in\mathbb N$, incluso $n=0$. |
| [[22 Campi\|Campo]] · [[23 Campi Ordinati\|campo ordinato]] | Campo: somma e prodotto commutativi e associativi, neutri $0\neq1$, opposti, inversi per elementi non nulli, distributività. Ordine totale compatibile con somma e prodotto di elementi non negativi. |
| [[24 Maggioranti Minoranti e Insiemi Limitati\|Maggioranti e minoranti]] | $M$ maggiorante di $E\iff\forall x\in E,\ x\leq M$; $m$ minorante $\iff\forall x\in E,\ m\leq x$. $E$ limitato se ha entrambi. |
| [[25 Massimo e Minimo\|Massimo e minimo]] · [[26 Estremo Superiore e Inferiore\|estremi]] | $\max E$: maggiorante appartenente a $E$; analogo per $\min E$. $\sup E$: minimo dei maggioranti; $\inf E$: massimo dei minoranti. Se $\sup E\in E$, è il massimo. |
| [[27 Completezza dei Numeri Reali\|Completezza]] | Ogni $E\subseteq\mathbb R$ non vuoto e limitato superiormente possiede $\sup E\in\mathbb R$; analogo per l'infimo. |
| [[28 Caratterizzazione degli Estremi\|Caratterizzazione degli estremi]] | $s=\sup E\iff s$ è maggiorante e $\forall\varepsilon>0\ \exists x\in E:\ s-\varepsilon<x\leq s$. Per l'infimo: $m$ minorante e $m\leq x<m+\varepsilon$. |
| [[29 Valore Assoluto\|Valore assoluto]] · [[30 Disuguaglianza Triangolare\|triangolare]] | $\lvert x\rvert=\max\{x,-x\}$; $\lvert x\rvert\leq r\iff-r\leq x\leq r$ per $r\geq0$. $\lvert x+y\rvert\leq\lvert x\rvert+\lvert y\rvert$; $\bigl\lvert\lvert x\rvert-\lvert y\rvert\bigr\rvert\leq\lvert x-y\rvert$. |
| [[31 Retta Reale e Intervalli\|Intervalli]] · [[32 Densità dei Razionali nei Reali\|densità]] | Parentesi quadre: estremo incluso; tonde: escluso, sempre accanto a $\pm\infty$. Se $x<y$ sono reali, $\exists q\in\mathbb Q$ con $x<q<y$. |
| [[33 Radice Ennesima Reale\|Radici]] · [[34 Potenze con Esponente Razionale\|potenze razionali]] | $\sqrt[n]{y}$: unica radice non negativa per $y\geq0$, $n\geq1$; $\sqrt{x^2}=\lvert x\rvert$. Per $a>0$, $a^{m/n}=\sqrt[n]{a^m}$, $n>0$. |
| [[35 Potenze con Esponente Reale\|Potenze reali]] | Per $a>0$: $a^{u+v}=a^ua^v$, $(a^u)^v=a^{uv}$, $a^{-u}=1/a^u$. Per $a>1$: $a^x=\sup\{a^r:r\in\mathbb Q,\ r<x\}$. |
| [[36 Logaritmi\|Logaritmi]] | $\log_a y=x\iff a^x=y$, con $a>0$, $a\neq1$, $y>0$. Per $u,v>0$: $\log_a(uv)=\log_a u+\log_a v$; $\log_a(u/v)=\log_a u-\log_a v$; $\log_a(u^t)=t\log_a u$. |
| [[36 Logaritmi\|Cambiamento di base]] | $\log_b y=\log_a y/\log_a b$ per $a,b>0$, $a,b\neq1$, $y>0$. In questa pagina $\log=\ln$. |

[[#Indice rapido|↑ Indice]]

## Numeri complessi

| Voce | Essenziale |
| --- | --- |
| [[37 Unità Immaginaria e Forma Algebrica\|Forma algebrica]] · [[38 Operazioni con i Numeri Complessi\|operazioni]] | $z=x+iy$, $i^2=-1$, $\operatorname{Re}z=x$, $\operatorname{Im}z=y$. $(x+iy)(u+iv)=(xu-yv)+i(xv+yu)$. |
| [[41 Coniugato e Modulo dei Numeri Complessi\|Coniugato e modulo]] · [[44 Proprietà del Coniugato\|proprietà]] | $\bar z=x-iy$; $\lvert z\rvert=\sqrt{x^2+y^2}$; $z\bar z=\lvert z\rvert^2$; $\overline{z+w}=\bar z+\bar w$; $\overline{zw}=\bar z\bar w$. |
| [[39 Campo Complesso e Inverso Moltiplicativo\|Inverso]] · [[45 Divisione tra Numeri Complessi\|divisione]] | $z^{-1}=\bar z/\lvert z\rvert^2$ per $z\neq0$; $z/w=z\bar w/\lvert w\rvert^2$ per $w\neq0$. |
| [[01 Courses/2026-2027/Semester 1/Analisi 1/Concepts/05 Numeri Complessi/42 Distanza nel Piano Complesso\|Distanza]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/Concepts/05 Numeri Complessi/43 Luoghi Geometrici nel Piano Complesso\|luoghi geometrici]] | $d(z,w)=\lvert z-w\rvert$. $\lvert z-z_0\rvert=r$: circonferenza per $r>0$; $\operatorname{Re}z=c$: retta verticale; $\operatorname{Im}z=c$: orizzontale. |
| [[01 Courses/2026-2027/Semester 1/Analisi 1/Concepts/05 Numeri Complessi/47 Modulo e Argomento dei Numeri Complessi\|Argomento]] · [[49 Determinazione dell'Argomento per Quadranti\|quadranti]] | Per $z\neq0$, $\cos\theta=x/\lvert z\rvert$, $\sin\theta=y/\lvert z\rvert$; $\theta$ definito modulo $2\pi$. $\arctan(y/x)$ da sola non distingue i quadranti. Zero non ha argomento. |
| [[48 Forma Trigonometrica dei Numeri Complessi\|Forma trigonometrica]] · [[50 Forma Esponenziale e Identità di Eulero\|esponenziale]] | $z=r(\cos\theta+i\sin\theta)=re^{i\theta}$, $r=\lvert z\rvert>0$; $e^{i\theta}=\cos\theta+i\sin\theta$. |
| [[51 Formule di De Moivre - Prodotto e Quoziente\|De Moivre: prodotto e quoziente]] **D3** | $re^{i\theta}Re^{i\varphi}=rRe^{i(\theta+\varphi)}$; $(re^{i\theta})/(Re^{i\varphi})=(r/R)e^{i(\theta-\varphi)}$, con moduli positivi. D3 richiede il prodotto e le potenze. |
| [[52 Formula di De Moivre per le Potenze Complesse\|De Moivre: potenze]] **D3** | $(re^{i\theta})^n=r^ne^{in\theta}$ per $r>0$, $n\in\mathbb N$, $n\geq1$. |
| [[53 Radici Ennesime Complesse\|Radici n-esime]] **D4** | Se $w=Re^{i\varphi}\neq0$, $z^n=w\iff z=z_k=R^{1/n}e^{i(\varphi+2k\pi)/n}$, $k=0,\ldots,n-1$, $n\geq1$. Per $w=0$, unica soluzione $z=0$. |
| [[54 Equazioni Polinomiali Complesse e Teorema Fondamentale dell'Algebra\|Teorema fondamentale dell'algebra]] | Un polinomio complesso non costante di grado $n$ ha esattamente $n$ radici complesse contate con molteplicità. |

[[#Indice rapido|↑ Indice]]

## Funzioni

| Voce | Essenziale |
| --- | --- |
| [[55 Funzioni Dominio Codominio e Immagine\|Funzione e immagine]] · [[57 Grafico di una Funzione\|grafico]] | $f:A\to B$: a ogni $x\in A$ associa un solo $f(x)\in B$. $\operatorname{Im}f=\{f(x):x\in A\}$; $G(f)=\{(x,f(x)):x\in A\}$. |
| [[60 Dominio Naturale di una Funzione\|Dominio naturale]] | Denominatori $\neq0$; radicandi di indice pari $\geq0$; argomenti dei logaritmi $>0$. Conservare i vincoli anche dopo le semplificazioni. |
| [[65 Funzioni Iniettive e Biiettive\|Iniettività]] · [[56 Suriettività\|suriettività]] | Iniettiva: $f(x_1)=f(x_2)\Rightarrow x_1=x_2$. Suriettiva: $\forall y\in B\ \exists x\in A:\ f(x)=y$. Biiettiva: entrambe. |
| [[59 Funzioni Limitate ed Estremi di Funzione\|Limitatezza ed estremi]] | Limitata: $\exists K>0\ \forall x\in A:\ \lvert f(x)\rvert\leq K$. $\sup_A f=\sup\operatorname{Im}f$; è un massimo solo se il valore è assunto. |
| [[01 Courses/2026-2027/Semester 1/Analisi 1/Concepts/06 Funzioni/61 Funzioni Pari e Dispari\|Parità]] · [[01 Courses/2026-2027/Semester 1/Analisi 1/Concepts/06 Funzioni/63 Funzioni Periodiche\|periodicità]] | Dominio simmetrico: pari se $f(-x)=f(x)$, dispari se $f(-x)=-f(x)$. Periodo $T>0$: dominio invariato dalla traslazione e $f(x+T)=f(x)$. |
| [[01 Courses/2026-2027/Semester 1/Analisi 1/Concepts/06 Funzioni/62 Funzioni Monotone\|Monotonia]] | Per ogni $x_1<x_2$ nel dominio: crescente se $f(x_1)\leq f(x_2)$; strettamente crescente se $<$; versi opposti per decrescente. |
| [[64 Composizione di Funzioni\|Composizione]] | $(g\circ f)(x)=g(f(x))$; $D(g\circ f)=\{x\in D(f):f(x)\in D(g)\}$. |
| [[66 Funzione Inversa\|Inversa]] · [[67 Monotonia e Funzione Inversa\|monotonia dell'inversa]] | Se $f$ è iniettiva, $f^{-1}:\operatorname{Im}f\to A$, $f^{-1}(f(x))=x$. Stretta monotonia $\Rightarrow$ iniettività; l'inversa conserva il verso. |
| [[68 Funzioni Potenza e Radice come Inversa\|Potenze e radici inverse]] | $x^m$ con $m$ dispari: invertibile su $\mathbb R$; con $m$ pari: restringere, per esempio a $[0,+\infty)$, per ottenere la radice principale. |
| [[01 Courses/2026-2027/Semester 1/Analisi 1/Concepts/06 Funzioni/69 Funzioni Goniometriche Inverse\|Inverse goniometriche]] | $\arcsin:[-1,1]\to[-\pi/2,\pi/2]$; $\arccos:[-1,1]\to[0,\pi]$; $\arctan:\mathbb R\to(-\pi/2,\pi/2)$. |

[[#Indice rapido|↑ Indice]]

## Successioni e limiti

| Voce | Essenziale |
| --- | --- |
| [[58 Successioni di Numeri Reali\|Successione]] · [[71 Proprietà Definitivamente Vere\|definitivamente]] | Successione reale: funzione $n\mapsto a_n\in\mathbb R$, per interi $n\geq n_0$. $P(n)$ vale definitivamente se $\exists N\ \forall n\geq N:\ P(n)$. |
| [[72 Limite Finito di una Successione\|Limite finito]] | $a_n\to\ell\in\mathbb R\iff\forall\varepsilon>0\ \exists N\ \forall n\geq N:\ \lvert a_n-\ell\rvert<\varepsilon$. L'ordine dei quantificatori è essenziale. |
| [[74 Limiti Infiniti e Regolarità delle Successioni\|Limiti infiniti e regolarità]] | $a_n\to+\infty\iff\forall M>0\ \exists N\ \forall n\geq N:\ a_n>M$; per $-\infty$: $a_n<-M$. Regolare: ammette limite finito o infinito. |
| [[73 Unicità del Limite di Successione\|Unicità del limite]] **D5** | Se esiste, il limite è unico. La nota dimostra il caso finito; l'estensione ai limiti infiniti è in [[74 Limiti Infiniti e Regolarità delle Successioni\|limiti infiniti]]. |
| [[77 Limitatezza delle Successioni Convergenti\|Convergenza e limitatezza]] **D6** | $a_n\to\ell\in\mathbb R\Rightarrow(a_n)$ limitata. Il viceversa è falso: $(-1)^n$. |
| [[79 Teorema di Permanenza del Segno\|Permanenza del segno]] **D7** | Se $a_n\to\ell>0$, anche $\ell=+\infty$, allora $a_n>0$ definitivamente; analogo negativo. Se $a_n\geq0$ definitivamente e il limite esiste, $\ell\geq0$. |
| [[82 Teorema dei Due Carabinieri\|Due carabinieri]] **D8** | Se $a_n\leq b_n\leq c_n$ definitivamente e $a_n,c_n\to\ell\in\mathbb R$, allora $b_n\to\ell$. |
| [[75 Successioni Monotone\|Monotonia]] · [[76 Teorema del Limite delle Successioni Monotone\|limite monotono]] **D9** | Crescente: $a_{n+1}\geq a_n$, limite $\sup\{a_n\}$, finito se limitata superiormente, altrimenti $+\infty$. Decrescente: limite $\inf\{a_n\}$, eventualmente $-\infty$. |
| [[80 Algebra dei Limiti di Successioni\|Algebra dei limiti]] | Se $a_n\to a$, $b_n\to b$ finiti: $a_n+b_n\to a+b$, $a_nb_n\to ab$; $a_n/b_n\to a/b$ se $b\neq0$. Per $a>0$ e basi definitivamente positive: $a_n^{b_n}\to a^b$. |
| [[81 Disuguaglianze e Passaggio al Limite\|Disuguaglianze]] · [[83 Teorema del Confronto per Limiti Infiniti\|confronto infinito]] | $a_n\leq b_n$ definitivamente e limiti esistenti $\Rightarrow\lim a_n\leq\lim b_n$. Se $a_n\to+\infty$, anche $b_n\to+\infty$; analogo con maggiorante a $-\infty$. |
| [[84 Confronto in Modulo e Prodotto con un Infinitesimo\|Limitata × infinitesima]] | $\lvert a_n\rvert\leq M$ definitivamente e $b_n\to0\Rightarrow a_nb_n\to0$, anche se $a_n$ non ha limite. |
| [[78 Limiti di Potenze e Progressioni Geometriche\|Progressione geometrica]] | $q^n\to0$ per $\lvert q\rvert<1$; vale $1$ per $q=1$; tende a $+\infty$ per $q>1$; è irregolare per $q\leq-1$. |
| [[91 Criterio del Rapporto per Successioni\|Rapporto per successioni]] | $a_n>0$ definitivamente, $a_{n+1}/a_n\to L\in[0,+\infty]$: $L<1\Rightarrow a_n\to0$; $L>1\Rightarrow a_n\to+\infty$; $L=1$ non decide. |
| [[87 Aritmetizzazione Parziale dell'Infinito e Forme Indeterminate\|Forme indeterminate]] · [[89 Limiti di Potenze con Base ed Esponente Variabili\|potenze variabili]] | $0/0$, $\infty/\infty$, $0\cdot\infty$, $\infty-\infty$, $1^{\pm\infty}$, $0^0$, $\infty^0$ richiedono studio. Con $a_n>0$: $a_n^{b_n}=e^{b_n\log a_n}$. |

[[#Indice rapido|↑ Indice]]

## Equivalenti e limiti notevoli

Per i rapporti si richiede denominatore non nullo definitivamente; gli angoli sono in radianti. In questa sezione $t=t_n\to0$, $t_n\neq0$ definitivamente.

| Voce | Essenziale |
| --- | --- |
| [[93 Notazione o-Piccolo\|o-piccolo]] · [[94 Equivalenza Asintotica\|equivalenza]] | $a_n=o(b_n)\iff a_n/b_n\to0$. $a_n\sim b_n\iff a_n/b_n\to1\iff a_n=b_n+o(b_n)$. Equivalenza significa errore relativo nullo. |
| [[90 Numero di Nepero e Limiti di Tipo Esponenziale\|Numero di Nepero]] | $e=\lim_{n\to\infty}(1+1/n)^n$; $(1+a/n)^n\to e^a$ per $a\in\mathbb R$ fissato. Più in generale $(1+1/c_n)^{c_n}\to e$ se $c_n\to\pm\infty$. |
| [[95 Equivalenti e Sviluppi Asintotici Notevoli\|Seno e arcotangente]] | $\sin t\sim t$; $\arctan t\sim t$. Quindi $\sin t/t\to1$ e $\arctan t/t\to1$. |
| [[95 Equivalenti e Sviluppi Asintotici Notevoli\|Coseno]] | $1-\cos t\sim t^2/2$; $\cos t=1-t^2/2+o(t^2)$. |
| [[95 Equivalenti e Sviluppi Asintotici Notevoli\|Esponenziale e logaritmo]] | $e^t-1\sim t$; $\log(1+t)\sim t$. Equivalentemente $e^t=1+t+o(t)$ e $\log(1+t)=t+o(t)$. |
| [[95 Equivalenti e Sviluppi Asintotici Notevoli\|Potenza con incremento piccolo]] | $(1+t)^\alpha-1\sim\alpha t$ per $\alpha\neq0$ fissato; $(1+t)^\alpha=1+\alpha t+o(t)$. La base è positiva definitivamente. |
| [[85 Gerarchia degli Infiniti\|Gerarchia degli infiniti]] | $(\log_a n)^\beta=o(n^\alpha)$, $n^\alpha=o(a^n)$, $a^n=o(n!)$, $n!=o(n^n)$; $a>1$, $\alpha,\beta>0$ fissati. |
| [[86 Termine Dominante nei Rapporti di Successioni\|Termini dominanti]] | Se $P_n\sim An^p$, $Q_n\sim Bn^q$, $A,B\neq0$, allora $P_n/Q_n\sim(A/B)n^{p-q}$. |
| [[88 Razionalizzazione e Differenze di Radicali\|Razionalizzazione]] · [[97 Cancellazioni e Precisione del Resto Asintotico\|cancellazioni]] | $\sqrt A-\sqrt B=(A-B)/(\sqrt A+\sqrt B)$ per $A,B\geq0$, non entrambi nulli. Nelle differenze gli equivalenti dei singoli termini possono non bastare: conservare i resti alla scala necessaria. |
| [[96 Calcolo dei Limiti con Equivalenti Asintotici\|Calcolo con equivalenti]] · [[98 Equivalenti Asintotici nelle Funzioni Composte\|composizioni]] | Sostituire in prodotti e quozienti verificando i domini; nelle composizioni controllare ogni argomento. Somme, differenze e potenze variabili richiedono un controllo ulteriore. |

[[#Indice rapido|↑ Indice]]

## Serie numeriche

| Voce | Essenziale |
| --- | --- |
| [[99 Serie Numeriche e Somme Parziali\|Serie e somme parziali]] | $S_N=\sum_{n=n_0}^{N}a_n$. $\sum a_n$ converge se $S_N\to S\in\mathbb R$; diverge se $S_N\to\pm\infty$; è irregolare se il limite non esiste nei reali estesi. |
| [[103 Condizione Necessaria di Convergenza di una Serie\|Condizione necessaria]] **D10** | $\sum a_n$ convergente $\Rightarrow a_n\to0$; usare $a_N=S_N-S_{N-1}$. Il viceversa è falso: la serie armonica diverge. |
| [[100 Serie Geometrica e Rappresentazioni Decimali\|Serie geometrica]] | $\sum_{n=0}^{N}q^n=(1-q^{N+1})/(1-q)$ per $q\neq1$. $\sum_{n=0}^{\infty}q^n$ converge esattamente per $\lvert q\rvert<1$, con somma $1/(1-q)$; da $n=1$ la somma è $q/(1-q)$. |
| [[102 Serie Telescopiche e Serie di Mengoli\|Telescopiche e Mengoli]] | Se $a_n=b_n-b_{n+1}$, $\sum_{n=m}^{N}a_n=b_m-b_{N+1}$. Se $b_n\to b\in\mathbb R$, la somma è $b_m-b$. $\sum_{n=1}^{\infty}1/[n(n+1)]=1$. |
| [[101 Linearità e Algebra delle Serie\|Linearità]] · [[105 Code e Resto di una Serie\|resto]] | Per serie convergenti: $\sum(\alpha a_n+\beta b_n)=\alpha\sum a_n+\beta\sum b_n$. $R_N=\sum_{n=N+1}^{\infty}a_n=S-S_N\to0$. Cambiare finiti termini conserva il carattere, non necessariamente la somma. |
| [[106 Serie a Termini Positivi\|Termini non negativi]] | Se $a_n\geq0$ definitivamente, la serie converge o diverge a $+\infty$. Converge se e solo se le somme parziali sono limitate superiormente. |
| [[107 Criterio del Confronto per Serie\|Confronto]] **D11** | $0\leq a_n\leq b_n$ definitivamente: $\sum b_n$ convergente $\Rightarrow\sum a_n$ convergente; $\sum a_n=+\infty\Rightarrow\sum b_n=+\infty$. |
| [[109 Criterio del Confronto Asintotico per Serie\|Confronto asintotico]] **D12** | $a_n,b_n>0$ definitivamente e $a_n/b_n\to1\Rightarrow$ stesso carattere delle due serie. |
| [[110 Criterio del Rapporto per Serie\|Rapporto per serie]] **D13** | $a_n>0$ definitivamente, $L=\lim a_{n+1}/a_n\in[0,+\infty]$: $L<1$ converge; $L>1$ diverge a $+\infty$; $L=1$ non decide. |
| [[111 Criterio della Radice per Serie\|Radice per serie]] | $a_n\geq0$ definitivamente, $L=\lim\sqrt[n]{a_n}\in[0,+\infty]$: $L<1$ converge; $L>1$ diverge a $+\infty$; $L=1$ non decide. |
| [[104 Serie Armonica\|Armonica]] · [[108 Serie Armoniche Generalizzate e di Bertrand\|armoniche generalizzate]] | $\sum_{n=1}^{\infty}1/n=+\infty$. $\sum_{n=1}^{\infty}1/n^\alpha$ converge se e solo se $\alpha>1$. |
| [[108 Serie Armoniche Generalizzate e di Bertrand\|Serie di Bertrand]] | $\sum_{n=2}^{\infty}1/[n^\alpha(\log n)^\beta]$ converge se $\alpha>1$ oppure $\alpha=1$, $\beta>1$; diverge negli altri casi. |
| [[112 Formula di Stirling e Serie con Fattoriali\|Stirling]] | $n!\sim\sqrt{2\pi n}(n/e)^n$; quindi $n!/n^n\sim\sqrt{2\pi n}/e^n$. |
| **Convergenza assoluta ⇒ semplice · D14** | Assoluta: $\sum\lvert a_n\rvert<+\infty$. La convergenza assoluta implica la convergenza di $\sum a_n$. **Da integrare: nota completa e dimostrazione**; al momento non presenti negli appunti. |

[[#Indice rapido|↑ Indice]]

> [!tip]- Aggiungere una voce
> Inserisci una riga nella sezione dell'argomento: **nome collegato alla nota completa** e **formula/enunciato con le ipotesi**. Aggiungi **D + numero** solo quando la dimostrazione è nell'elenco del regolamento; per i numeri oltre 14 specifica **oltre il primo parziale**. Mantieni esempi e spiegazioni estese nelle note dei concetti.
