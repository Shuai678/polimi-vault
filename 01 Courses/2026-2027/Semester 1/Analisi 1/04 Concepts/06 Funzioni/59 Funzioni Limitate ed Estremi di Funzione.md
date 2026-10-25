---
course: Analisi 1
type: concept
status: da-studiare
source:
  - Lezione 05, PDF pp. 2-4
  - Libro, §2.3.2, pp. 39-44
---

# Funzioni limitate ed estremi di funzione

## Idea centrale

Le nozioni di maggiorante, minorante, massimo, minimo, estremo superiore ed estremo inferiore si applicano a una funzione guardando il suo insieme dei valori, cioè la sua immagine.

Sia

$$
f:A\to\mathbb R,
\qquad A\neq\varnothing.
$$

Studiare quanto è grande o piccola $f$ significa quindi studiare

$$
\operatorname{Im}f=\{f(x):x\in A\}.
$$

## Limitatezza

La funzione $f$ è **limitata superiormente** se esiste $M\in\mathbb R$ tale che

$$
f(x)\leq M
\qquad\text{per ogni }x\in A.
$$

È **limitata inferiormente** se esiste $m\in\mathbb R$ tale che

$$
m\leq f(x)
\qquad\text{per ogni }x\in A.
$$

È **limitata** se è limitata sia superiormente sia inferiormente. Equivalentemente, esiste $K>0$ tale che

$$
|f(x)|\leq K
\qquad\text{per ogni }x\in A.
$$

### Da dire all'orale

> Una funzione è limitata superiormente, inferiormente o in entrambi i versi quando lo è la sua immagine. Le disuguaglianze devono valere per ogni punto del dominio.

## Estremi della funzione

Si definiscono

$$
\sup_A f:=\sup\operatorname{Im}f,
\qquad
\inf_A f:=\inf\operatorname{Im}f.
$$

Se l'estremo è raggiunto da almeno un punto del dominio, si parla di massimo o minimo:

$$
\max_A f=f(x_M)
\quad\Longleftrightarrow\quad
f(x)\leq f(x_M)\ \text{per ogni }x\in A,
$$

$$
\min_A f=f(x_m)
\quad\Longleftrightarrow\quad
f(x_m)\leq f(x)\ \text{per ogni }x\in A.
$$

La differenza decisiva è l'appartenenza all'immagine:

- se $\sup_A f\in\operatorname{Im}f$, allora $\sup_A f=\max_A f$;
- se $\inf_A f\in\operatorname{Im}f$, allora $\inf_A f=\min_A f$.

## Esempio della lezione

Consideriamo

$$
f(x)=\frac{1}{1+x^2},
\qquad x\in\mathbb R.
$$

Poiché $x^2\geq0$,

$$
1+x^2\geq1
\quad\Longrightarrow\quad
0<f(x)\leq1.
$$

Inoltre $f(0)=1$, mentre $f(x)$ può avvicinarsi quanto si vuole a $0$ facendo crescere $|x|$, senza mai assumere il valore $0$. Ne segue che

$$
\operatorname{Im}f=(0,1],
$$

$$
\sup_{\mathbb R}f=\max_{\mathbb R}f=1,
\qquad
\inf_{\mathbb R}f=0,
$$

ma il minimo non esiste.

![[59 Funzioni Limitate - Estremi.svg]]

## Procedura operativa

Per determinare gli estremi di una funzione:

1. stabilire il dominio;
2. ricavare disuguaglianze valide per ogni $x$ del dominio;
3. individuare i migliori maggioranti e minoranti, cioè superiore e inferiore;
4. controllare separatamente se tali valori sono effettivamente assunti;
5. soltanto in caso affermativo chiamarli massimo o minimo.

## Errori comuni

- Confondere un maggiorante qualsiasi con l'estremo superiore.
- Concludere che esiste un massimo solo perché la funzione è limitata superiormente.
- Dimenticare di verificare se superiore o inferiore appartengono all'immagine.
- Cercare gli estremi nel dominio anziché nell'insieme dei valori della funzione.
- Scrivere $\min f=0$ per $f(x)=1/(1+x^2)$: $0$ non è mai assunto.

## Connessioni

- Traduce alle funzioni [[24 Maggioranti Minoranti e Insiemi Limitati|maggioranti, minoranti e limitatezza]].
- Usa [[25 Massimo e Minimo|massimo e minimo]] e [[26 Estremo Superiore e Inferiore|estremo superiore e inferiore]].
- Richiede la distinzione tra [[55 Funzioni Dominio Codominio e Immagine|immagine e codominio]].

## Prospettiva d'esame

Potenziale rilevanza d'esame: determinare $\sup f$, $\inf f$, massimo e minimo, motivando sia la barriera sia l'eventuale raggiungimento del valore.
