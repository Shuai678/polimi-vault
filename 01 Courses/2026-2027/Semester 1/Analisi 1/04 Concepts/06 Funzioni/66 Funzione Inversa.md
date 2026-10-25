---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 05, PDF pp. 13-16
  - Lezione 06, PDF pp. 2-3
  - Libro, §2.2, pp. 36-37 e §2.3.6, pp. 52-53
---

# Funzione inversa

## Quando esiste

Sia

$$
f:A\to B.
$$

Se $f$ è iniettiva, ogni $y\in\operatorname{Im}f$ proviene da un unico $x\in A$. Si può quindi definire la funzione inversa

$$
f^{-1}:\operatorname{Im}f\to A,
$$

ponendo

$$
f^{-1}(y)=x
\quad\Longleftrightarrow\quad
f(x)=y.
$$

In questo senso ogni funzione iniettiva è **invertibile sulla propria immagine**. Se $f$ è biiettiva, allora $\operatorname{Im}f=B$ e l'inversa è definita su tutto il codominio:

$$
f^{-1}:B\to A.
$$

## Dominio e immagine si scambiano

Per definizione,

$$
D(f^{-1})=\operatorname{Im}f,
\qquad
\operatorname{Im}(f^{-1})=D(f)=A.
$$

Le composizioni restituiscono l'elemento di partenza:

$$
f^{-1}(f(x))=x
\qquad\text{per ogni }x\in A,
$$

$$
f(f^{-1}(y))=y
\qquad\text{per ogni }y\in\operatorname{Im}f.
$$

### Da dire all'orale

> L'inversa scambia input e output: a ogni valore dell'immagine associa l'unico punto del dominio che lo produce. Per questo l'iniettività è indispensabile.

## Come si calcola

Per trovare $f^{-1}$:

1. scrivere $y=f(x)$;
2. risolvere l'equazione rispetto a $x$;
3. usare il dominio di $f$ per scegliere l'eventuale ramo corretto;
4. scambiare i nomi delle variabili;
5. dichiarare dominio e codominio dell'inversa;
6. verificare le due composizioni identità.

## Esempio della Lezione 06: esponenziale composta

Consideriamo

$$
f:\mathbb R\to(0,+\infty),
\qquad
f(x)=e^{x^3+2}.
$$

La funzione è strettamente crescente, quindi è iniettiva, e la sua immagine è $(0,+\infty)$. Per calcolare l'inversa si risolve

$$
y=e^{x^3+2}.
$$

Poiché $y>0$, si può applicare il logaritmo:

$$
\log y=x^3+2,
\qquad
x^3=\log y-2,
$$

da cui

$$
f^{-1}(y)=\sqrt[3]{\log y-2},
\qquad y>0.
$$

Il dominio dell'inversa non è tutto $\mathbb R$, ma coincide con l'immagine di $f$.

## Esempio: due restrizioni di $x^2$

La funzione $x\mapsto x^2$ su tutto $\mathbb R$ non è iniettiva. Restringendo il dominio a $[0,+\infty)$ si ottiene

$$
h:[0,+\infty)\to[0,+\infty),
\qquad h(x)=x^2.
$$

Da $y=x^2$ e $x\geq0$ segue $x=\sqrt y$, quindi

$$
h^{-1}(y)=\sqrt y.
$$

Restringendo invece il dominio a $(-\infty,0]$,

$$
g:(-\infty,0]\to[0,+\infty),
\qquad g(x)=x^2,
$$

la condizione $x\leq0$ impone il ramo negativo:

$$
g^{-1}(y)=-\sqrt y.
$$

La formula dell'inversa dipende quindi dalla restrizione scelta per il dominio.

## Simmetria del grafico

Se $(a,b)$ appartiene al grafico di $f$, allora $b=f(a)$ e quindi $a=f^{-1}(b)$. Pertanto

$$
(a,b)\in G(f)
\quad\Longleftrightarrow\quad
(b,a)\in G(f^{-1}).
$$

Scambiare le coordinate equivale a riflettere il grafico rispetto alla retta

$$
y=x.
$$

![[66 Funzione Inversa - Simmetria.svg]]

## Attenzione alla notazione

La scrittura $f^{-1}$ indica la funzione inversa, non il reciproco dei valori:

$$
f^{-1}(x)\neq\frac1{f(x)}
$$

in generale. Il reciproco ha senso quando $f(x)\neq0$; l'inversa richiede invece iniettività e scambia input e output.

## Errori comuni

- Cercare l'inversa senza verificare l'iniettività.
- Usare automaticamente il segno positivo nel risolvere $y=x^2$.
- Dimenticare che il dominio dell'inversa è l'immagine della funzione originale.
- Confondere $f^{-1}$ con $1/f$.
- Scambiare le variabili senza risolvere l'equazione.
- Verificare una sola delle due composizioni o farlo su domini errati.

## Connessioni

- Richiede [[65 Funzioni Iniettive e Biiettive|iniettività o biiettività]].
- Le identità dell'inversa sono casi di [[64 Composizione di Funzioni|composizione]].
- Il grafico usa la nozione di [[57 Grafico di una Funzione|riflessione rispetto a $y=x$]].
- La [[67 Monotonia e Funzione Inversa|stretta monotonia]] fornisce un criterio pratico di invertibilità.

## Prospettiva d'esame

Una risposta completa sull'inversa deve specificare la restrizione di dominio, la formula, il dominio dell'inversa e almeno una verifica tramite composizione.
