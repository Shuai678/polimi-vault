---
course: Analisi 1
type: concept
status: Da studiare
updated: 2026-11-09
source:
  - Lezione 16, PDF pp. 14-18
  - Libro, §6.3, p. 200, continuità delle inverse elementari; §5.9.3, p. 160, confronto con la trattazione del libro
---

# Continuità delle funzioni elementari

## Corollario del docente e idea di utilizzo

Le funzioni elementari sono **continue sui loro domini**. Il professore le esamina usando l'algebra delle funzioni continue, la composizione e la continuità dell'inversa su un intervallo. Per seno e coseno sviluppa la verifica, prima in zero e poi in un punto generico.

La frase riguarda punti nei quali la funzione è definita: prima di usare la sostituzione diretta in un limite, occorre controllare il dominio.

## Prime funzioni nell'ordine del docente

### 1. Identità

$f(x)=x$ è continua su $\mathbb R$, perché $\lim_{x\to x_0}x=x_0$.

### 2. Costanti

$f(x)=\lambda$, con $\lambda\in\mathbb R$, è continua su $\mathbb R$, perché il limite della costante è la costante.

### 3. Potenze naturali

$f(x)=x^m$ è continua per $m\in\mathbb N$, perché ottenuta come prodotto di funzioni continue. Per $m=0$ si considera la funzione costante $1$; per $m\geq1$ si moltiplicano $m$ copie dell'identità.

### 4. Polinomi

Un polinomio è continuo su $\mathbb R$ perché somma di prodotti di funzioni continue. Si applica [[138 Algebra delle Funzioni Continue]].

### 5. Reciproci di potenze naturali

$f(x)=1/x^m$ è continua dove il denominatore è non nullo, come reciproco di una funzione continua. Per $m\geq1$ il dominio è $\mathbb R\setminus\{0\}$; il caso $m=0$ è la funzione costante $1$.

### 6. Radici

$f(x)=x^{1/m}=\sqrt[m]{x}$, con $m\in\mathbb N$, $m\geq1$, è continua come inversa di una funzione continua su un intervallo. Per $m$ dispari il dominio è $\mathbb R$; per $m$ pari è $[0,+\infty)$, usando la restrizione non negativa della potenza. I rami sono quelli di [[68 Funzioni Potenza e Radice come Inversa]].

### 7. Potenze razionali

$f(x)=x^{n/m}$, con $n,m\in\mathbb Z$, $m\neq0$, è continua sul proprio dominio reale, perché ottenuta componendo potenze, radici ed eventualmente reciproci continui. Restano le convenzioni e le restrizioni di [[34 Potenze con Esponente Razionale]]: in particolare, le potenze negative escludono lo zero e le radici reali di indice pari non ammettono radicandi negativi.

### 8. Esponenziale naturale

$f(x)=e^x$ è continua su $\mathbb R$. Il docente rinvia alle lezioni precedenti: la sua dimostrazione è già in [[130 Continuità di una Funzione#Dimostrazione del professore|Concept 130]] e nel Formulario.

### 9. Logaritmo naturale

$f(x)=\log x$ è continua su $(0,+\infty)$ come inversa dell'esponenziale continua su un intervallo, per [[67 Monotonia e Funzione Inversa#Lezione 16 - Continuità e invertibilità su un intervallo - Da studiare|il teorema sull'inversa]].

### 10. Esponenziale in base qualsiasi ammessa

Per $a>0$, $a\neq1$,

$$
f(x)=a^x=e^{\log(a^x)}=e^{(\log a)x}
$$

è continua su $\mathbb R$ come composizione di funzioni continue.

### 11. Logaritmo in base qualsiasi ammessa

Per $a>0$, $a\neq1$, $f(x)=\log_a x$ è continua su $(0,+\infty)$ come inversa di una funzione continua su un intervallo. La base può rendere la funzione crescente o decrescente, senza impedirne la continuità.

### 12. Potenza con esponente reale

Per $\alpha\in\mathbb R$, sul dominio positivo,

$$
f(x)=x^\alpha=e^{\log(x^\alpha)}=e^{\alpha\log x},\qquad x>0,
$$

è continua per composizione di funzioni continue. Le estensioni ammesse per esponenti naturali o razionali sono già coperte dai casi precedenti e dai loro domini. Qui la riscrittura con il logaritmo richiede $x>0$.

## 13. Seno e coseno: dimostrazione del professore

### Seno in zero

Nella circonferenza goniometrica il docente considera $A=(1,0)$ e il punto $P$ corrispondente a un angolo $x\geq0$. Sia $H$ la proiezione di $P$ sull'asse orizzontale. Il segmento $PH$ ha lunghezza $\sin x$ e l'arco fra $A$ e $P$ ha lunghezza $x$. Si ha

$$
0\leq\sin x\leq x\qquad\forall x\in\left[0,\frac\pi2\right).
$$

Quindi

$$
0\leq|\sin x|\leq|x|\qquad
\forall x\in\left(-\frac\pi2,\frac\pi2\right).
$$

Per confronto, con i due carabinieri,

$$
\lim_{x\to0}\sin x=0=\sin0.
$$

Il seno è continuo in zero.

### Coseno in zero

Il docente usa

$$
\cos x=1-2\left(\sin\frac x2\right)^2.
$$

Per algebra dei limiti,

$$
\lim_{x\to0}\cos x=1=\cos0.
$$

Il coseno è continuo in zero.

### Seno in un punto generico

Per ogni $x_0\in\mathbb R$ e $h\in\mathbb R$,

$$
\sin(x_0+h)=\sin x_0\cos h+\cos x_0\sin h.
$$

Passando al limite per $h\to0$,

$$
\lim_{h\to0}\sin(x_0+h)
=\lim_{h\to0}\bigl(\sin x_0\cos h+\cos x_0\sin h\bigr)
=\sin x_0.
$$

Quindi $\sin x$ è continua in ogni $x_0\in\mathbb R$.

### Coseno in un punto generico

Analogamente,

$$
\cos(x_0+h)=\cos x_0\cos h-\sin x_0\sin h,
$$

$$
\lim_{h\to0}\cos(x_0+h)
=\lim_{h\to0}\bigl(\cos x_0\cos h-\sin x_0\sin h\bigr)
=\cos x_0.
$$

Quindi $\cos x$ è continua in ogni $x_0\in\mathbb R$. $\square$

## Ultime funzioni nell'ordine del docente

### 14. Arcoseno e arcocoseno

$f(x)=\arcsin x$ e $f(x)=\arccos x$ sono continue sui loro domini $[-1,1]$, perché inverse di funzioni continue ristrette a intervalli nei quali sono strettamente monotone. Le restrizioni sono quelle di [[69 Funzioni Goniometriche Inverse]].

### 15. Tangente

$$
f(x)=\tan x=\frac{\sin x}{\cos x}
$$

è continua come quoziente di funzioni continue dove $\cos x\neq0$, cioè su

$$
\mathbb R\setminus\left\{\frac\pi2+k\pi:k\in\mathbb Z\right\}.
$$

### 16. Arcotangente

$f(x)=\arctan x$ è continua su $\mathbb R$ come inversa della tangente continua e strettamente crescente sull'intervallo $(-\pi/2,\pi/2)$.

## Commenti alla prova di seno e coseno

La successione dei passaggi è quella del PDF, pp. 16-17: stima geometrica del seno, continuità del seno in zero, identità per il coseno e sua continuità in zero, formule di addizione per il punto generico. La prova parte da una disuguaglianza geometrica, senza usare il limite notevole $\sin x/x$ come risultato già dimostrato qui.

Per il lato negativo nella stima iniziale si usa $\sin(-x)=-\sin x$, quindi $|\sin x|=\sin|x|$ per $|x|<\pi/2$. Da $|\sin x|\leq|x|\to0$ segue il limite nullo della funzione: per esempio $-|x|\leq\sin x\leq|x|$.

Nel coseno, $x/2\to0$ implica $\sin(x/2)\to0$, perciò $1-2(\sin(x/2))^2\to1$. Nelle formule di addizione, i calcoli finali usano rispettivamente

$$
\sin x_0\cdot1+\cos x_0\cdot0=\sin x_0,
\qquad
\cos x_0\cdot1-\sin x_0\cdot0=\cos x_0.
$$

Ponendo $h=x-x_0$, $h\to0$ equivale a $x\to x_0$. Le formule scritte in termini di $h$ provano così la continuità nel punto richiesto. Questi dettagli esplicitano i passaggi del docente senza sostituirne l'argomento.

![[145 Continuità del Seno e Circonferenza Goniometrica.svg|1000]]

## Esempio svolto: dominio e sostituzione diretta

Consideriamo

$$
F(x)=\frac{\log(1+x^2)}{\sqrt{4-x^2}}.
$$

Il logaritmo richiede $1+x^2>0$, sempre vero. Poiché la radice è al denominatore, serve $4-x^2>0$, quindi $D(F)=(-2,2)$. In questo intervallo le componenti sono continue e il denominatore è non nullo; composizione e quoziente rendono $F$ continua. In particolare,

$$
\lim_{x\to1}F(x)=F(1)=\frac{\log2}{\sqrt3}.
$$

Per $G(x)=\sin\sqrt x$, invece, il dominio è $[0,+\infty)$. La funzione è continua anche in zero nel senso del proprio dominio e $\lim_{x\to0^+}G(x)=G(0)=0$. Non occorre un limite da sinistra esterno al dominio.

## Errori comuni e connessioni

Controllare sempre il dominio della singola formula e della composizione. La continuità di $\log x$ riguarda $x>0$ e non attribuisce un valore al logaritmo in zero. La radice principale di indice pari è continua anche nel suo estremo di dominio, dove si considera l'avvicinamento ammesso.

Le identità e le restrizioni usano [[138 Algebra delle Funzioni Continue]], [[139 Cambio di Variabile nei Limiti e Continuità della Composta]] e la nuova parte del Concept [[67 Monotonia e Funzione Inversa]]. Non tutte le proprietà, come la monotonia, si trasmettono per semplice somma di funzioni continue: la conclusione qui riguarda la continuità.

### Da dire all'orale

> Le funzioni elementari sono continue nei punti del loro dominio. Somme, prodotti, quozienti con denominatore non nullo e composizioni permettono di costruire nuove funzioni continue. Radici, logaritmi e inverse goniometriche usano anche la continuità dell'inversa su un intervallo. Per seno e coseno il docente prova prima la continuità in zero e poi usa le formule di addizione per un punto generico.
