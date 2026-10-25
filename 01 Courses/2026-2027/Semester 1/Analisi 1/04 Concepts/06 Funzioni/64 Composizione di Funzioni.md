---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 05, PDF pp. 9-12
  - Libro, §2.2, pp. 36-37
---

# Composizione di funzioni

## Idea centrale

Comporre due funzioni significa usare l'uscita della prima come ingresso della seconda.

Se

$$
f:A\to B
\qquad\text{e}\qquad
g:B\to C,
$$

la composizione di $g$ dopo $f$ è la funzione

$$
g\circ f:A\to C,
$$

definita da

$$
(g\circ f)(x)=g(f(x)).
$$

L'ordine di lettura è da destra verso sinistra: prima si applica $f$, poi $g$.

### Da dire all'orale

> La composizione $g\circ f$ associa a $x$ il valore $g(f(x))$: l'immagine prodotta da $f$ deve appartenere al dominio di $g$.

## Dominio effettivo della composizione

Nel caso più generale, se

$$
f:A\to B,
\qquad
g:D\to C,
\qquad D\subseteq B,
$$

non tutti gli elementi di $A$ sono necessariamente ammessi. Il dominio corretto è

$$
D(g\circ f)
=\{x\in A:f(x)\in D\}.
$$

Questa condizione deve essere determinata **prima** di usare o semplificare la formula composta.

## Esempi della lezione

### Una composizione sempre definita

Poniamo

$$
f(x)=x^2+1,
\qquad
g(t)=\log t.
$$

Poiché $x^2+1>0$ per ogni $x\in\mathbb R$,

$$
(g\circ f)(x)=\log(x^2+1)
$$

è definita su tutto $\mathbb R$.

### Una composizione impossibile nel campo reale

Se

$$
f(x)=-x^2,
\qquad
g(t)=\log t,
$$

allora $f(x)\leq0$ per ogni $x$, mentre il logaritmo richiede un argomento positivo. Pertanto $g\circ f$ non è definita in alcun punto reale.

### Dominio ristretto dalla funzione esterna

Con

$$
f(x)=1-x^2,
\qquad
g(t)=\log t,
$$

si deve imporre

$$
f(x)>0
\quad\Longleftrightarrow\quad
1-x^2>0,
$$

quindi

$$
D(g\circ f)=(-1,1).
$$

### La semplificazione non cancella il dominio

Siano

$$
f(x)=\sqrt{x},
\qquad
g(t)=t^2.
$$

Allora

$$
(g\circ f)(x)=(\sqrt{x})^2=x,
$$

ma soltanto per

$$
x\in[0,+\infty).
$$

La composizione non è la funzione identità su tutto $\mathbb R$, perché il dominio ereditato da $\sqrt{x}$ resta $[0,+\infty)$.

## Proprietà algebriche

La composizione è associativa:

$$
(h\circ g)\circ f=h\circ(g\circ f),
$$

quando tutte le composizioni sono definite. Per questo si può scrivere senza ambiguità

$$
h\circ g\circ f.
$$

In generale non è commutativa:

$$
f\circ g\neq g\circ f.
$$

Per esempio, se $f(x)=x+1$ e $g(x)=x^2$,

$$
(g\circ f)(x)=(x+1)^2,
\qquad
(f\circ g)(x)=x^2+1.
$$

## Procedura operativa

1. Identificare la funzione interna, applicata per prima.
2. Determinarne dominio e valori possibili.
3. Imporre che tali valori appartengano al dominio della funzione esterna.
4. Sostituire l'espressione interna nella variabile della funzione esterna.
5. Semplificare conservando il dominio ottenuto.

## Errori comuni

- Leggere $g\circ f$ come “prima $g$, poi $f$”.
- Scambiare $g(f(x))$ con $f(g(x))$.
- Sostituire le formule senza determinare il dominio della composizione.
- Perdere restrizioni dopo una semplificazione, come in $(\sqrt{x})^2=x$.
- Credere che $f(A)\subseteq D(g)$ sia automatico.
- Considerare la composizione commutativa.

## Connessioni

- Richiede [[55 Funzioni Dominio Codominio e Immagine|dominio, codominio e immagine]].
- Usa sistematicamente il [[60 Dominio Naturale di una Funzione|dominio naturale]].
- Le identità della [[66 Funzione Inversa|funzione inversa]] sono composizioni con la funzione identità.

## Prospettiva d'esame

Nei problemi di composizione la parte decisiva è spesso il dominio. Una formula algebricamente semplice non autorizza ad allargare l'insieme sul quale la composizione è stata definita.
